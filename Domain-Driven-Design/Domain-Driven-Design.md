# Estructura de Archivos en un Proyecto con Domain-Driven Design (DDD)

La arquitectura **Domain-Driven Design (DDD)** organiza un proyecto dividiendo responsabilidades en diferentes capas para mantener un diseño limpio, escalable y alineado con el dominio del negocio.

---

## **Principios de DDD**

1. **Separación de Responsabilidades**:
   - Divide el sistema en capas claras: dominio, aplicación, infraestructura e interfaces.

2. **Modelo de Dominio**:
   - El centro del proyecto es un modelo que refleja las reglas y conceptos del negocio.

3. **Contextos Delimitados (Bounded Contexts)**:
   - Divide el sistema en subdominios independientes para evitar conflictos entre conceptos similares.

4. **Lógica en el Dominio**:
   - Toda lógica de negocio compleja debe residir en el núcleo de dominio, no en servicios o controladores.

5. **Interfaces para Dependencias**:
   - Usa abstracciones (interfaces) para definir dependencias, lo que facilita la implementación en capas externas.

6. **Eventos de Dominio**:
   - Usa eventos para comunicar cambios importantes dentro del dominio.

---

## **Estructura de Archivos**

```plaintext
src/
├── Application/                  # Lógica de aplicación (casos de uso, servicios de aplicación)
│   ├── UseCases/                 # Casos de uso
│   │   └── CreateUserUseCase.cs
│   ├── Services/                 # Servicios específicos de aplicación
│   │   └── UserApplicationService.cs
│   └── DTOs/                     # Data Transfer Objects
│       └── UserDto.cs
│
├── Domain/                       # Núcleo de reglas de negocio
│   ├── Models/                   # Entidades y Objetos de Valor
│   │   ├── User.cs
│   │   └── ValueObjects/
│   │       └── Email.cs
│   ├── Repositories/             # Interfaces para repositorios
│   │   └── IUserRepository.cs
│   ├── Services/                 # Servicios de dominio
│   │   └── UserDomainService.cs
│   ├── Events/                   # Eventos de dominio
│   │   └── UserCreatedEvent.cs
│   └── Exceptions/               # Excepciones específicas del dominio
│       └── InvalidEmailException.cs
│
├── Infrastructure/               # Implementaciones técnicas (base de datos, frameworks, etc.)
│   ├── Persistence/              # Persistencia de datos
│   │   ├── EFRepositories/       # Implementación de repositorios (Entity Framework, etc.)
│   │   │   └── UserRepository.cs
│   │   ├── Mappers/              # Mapeadores (Domain <-> DTO/Entity)
│   │   │   └── UserMapper.cs
│   │   └── DbContext/            # Contextos de base de datos
│   │       └── AppDbContext.cs
│   ├── ExternalServices/         # Integraciones con servicios externos (APIs, correo, etc.)
│   │   └── EmailService.cs
│   └── Configuration/            # Configuración (DI, archivos, etc.)
│       └── DependencyInjection.cs
│
├── Interfaces/                   # Interfaces de usuario (API, CLI, etc.)
│   ├── Controllers/              # Controladores (API, MVC, etc.)
│   │   └── UserController.cs
│   ├── GraphQL/                  # Esquemas y resolvers de GraphQL
│   │   └── UserSchema.cs
│   ├── CLI/                      # Comandos para interfaces de línea de comandos
│   │   └── UserCommand.cs
│   └── Views/                    # Vistas (si aplica, como Razor Pages)
│       └── UserView.cshtml
│
└── Shared/                       # Recursos compartidos entre capas
    ├── Utils/                    # Utilidades comunes (helpers, extensiones, etc.)
    │   └── StringHelper.cs
    ├── Exceptions/               # Excepciones globales
    │   └── NotFoundException.cs
    └── Kernel/                   # Abstracciones comunes (base classes, interfaces)
        └── BaseEntity.cs
```

---

## **Explicación de Capas**

### **1. Application**
- Contiene la lógica específica de los casos de uso y orquesta las interacciones entre el dominio y las interfaces.
- Se enfoca en procesos, no en lógica de negocio.

**Ejemplo**: `CreateUserUseCase` maneja la creación de un usuario coordinando validaciones y persistencia.

---

### **2. Domain**
- Es el núcleo del sistema. Representa las reglas de negocio mediante:
  - **Entidades**: Con estado e identidad.
  - **Objetos de Valor**: Valores inmutables.
  - **Eventos**: Para comunicar cambios significativos.
  - **Servicios de Dominio**: Para operaciones complejas que involucran múltiples entidades.

**Ejemplo**: `User` es una entidad con propiedades como `Id`, `Name` y `Email`.

---

### **3. Infrastructure**
- Implementa detalles técnicos como persistencia, mapeadores y acceso a servicios externos.

**Ejemplo**: `UserRepository` implementa las operaciones de datos usando Entity Framework.

---

### **4. Interfaces**
- Define cómo los clientes interactúan con el sistema mediante controladores REST, CLI o interfaces gráficas.

**Ejemplo**: `UserController` recibe solicitudes HTTP para crear y listar usuarios.

---

### **5. Shared**
- Contiene recursos reutilizables como utilidades, excepciones comunes y clases base.

---

## **Ejemplo Práctico**
### **Modelo del Dominio: `User.cs`**
```csharp
namespace MyProject.Domain.Models
{
    public class User
    {
        public Guid Id { get; private set; }
        public string Name { get; private set; }
        public string Email { get; private set; }

        public User(string name, string email)
        {
            Id = Guid.NewGuid();
            Name = name;
            Email = email;
        }

        public void UpdateName(string name)
        {
            Name = name;
        }

        public void UpdateEmail(string email)
        {
            Email = email;
        }
    }
}
```

---

### **Repositorio: `IUserRepository.cs`**
```csharp
namespace MyProject.Domain.Repositories
{
    public interface IUserRepository
    {
        Task<User?> GetByIdAsync(Guid id);
        Task<IEnumerable<User>> GetAllAsync();
        Task AddAsync(User user);
        Task UpdateAsync(User user);
        Task DeleteAsync(Guid id);
    }
}
```

---

### **Mapper: `UserMapper.cs`**
```csharp
namespace MyProject.Infrastructure.Mappers
{
    public static class UserMapper
    {
        public static UserEntity ToEntity(User user)
        {
            return new UserEntity
            {
                Id = user.Id,
                Name = user.Name,
                Email = user.Email
            };
        }

        public static User ToDomain(UserEntity entity)
        {
            return new User(entity.Name, entity.Email)
            {
                Id = entity.Id
            };
        }
    }
}
```

