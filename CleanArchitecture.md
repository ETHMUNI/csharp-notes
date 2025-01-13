# Clean Architecture with ASP.NET Core 3.0 Notes
Link: https://www.youtube.com/watch?v=dK4Yb6-LxAk&ab_channel=GOTOConferences

## Domain Layer

* Entities
* Value Objects
* Enumerations
* Logic
* Exceptions
* Events

### Notes

* Make the setter with private: ```public string Title { get; private set; }```
* If you are going to use a Object from another entity make sure to initialize it: ```public TodoList() { Items = new List<TodoItems>();}```
* A good idea to have a AuditableEntity class. This have CreatedBy, Created LastModifiedBy and LastModified. This is a standard for all entity classes.
  * Here is how it would look: https://github.com/jasontaylordev/CleanArchitecture/blob/main/src/Domain/Common/BaseAuditableEntity.cs

### Key Points

* Avoid using data annotations
* Use value objects where appropriate
* Create custom domain exceptions
* Initiialuse all collections & use private setters
* Automatically track changes (with auditable and C base type)

## Application Layer

* Interfaces
* Models (View Models & DTOs)
* Logic
* Commands / Queries
* Validators
* Custom Exceptions

### CQRS - Command Query Responsibility Segregation

* Separate reads(Queries) from writes (commands)
* Can maximise performance and simplicity
* Easy to add new features, just add a new query or command
* Easy to maintain, changes only affects one command or query

### CQRS + MediatR

* Define commands and queries as requests
* Application layer is jusr a series of requests / response objects
* Ability to attach additional behaviour before, and / or after each request, eg. logging, validation, caching, auth and so on

### Key Points
* Using CQRS + MediatR simplifies your overall design
* Fluent Validation is useful for all validation scenarios
* AutoMapper simplifies mapping and projections
* Independent of infrastructure conecerns

## Infrastructure Layer

* Persistence
* Identity
* File System
* System Clock
* API Clients

### Notes

### Key Points
* Independent of the database
* Use Fluent API configuration over data annotation
* Prefer conventions over configuration
* Automatically apply all entity type configuration
* No layers depends on Infrastructure layer, eg. Presentation Layer

## Presentation Layer

* SPA - Angular, React, Vue
* Web API
* Razor Pages
* MCV
* Web Forms

### Key Points 
* Controllers should not contain any applicacation logic - only resposible for taking a request and conevert it into a reponse and that logic lives in the application layer
* Create and consume welle defined view models
* Open API bridges the gap between the front end and back end
* NSwag automates generation of Open API specification and clients 
