# Java Spring Boot + JPA Copilot Instructions

## General Java Development Practices
- Always follow SOLID, DRY, KISS, and YAGNI principles.
- Adhere to OWASP security best practices.
- Break tasks into the smallest units and solve step by step.

## Spring Boot Project Structure
- Use Java Spring Boot 3 (Maven, Java 17, Spring Web, Spring Data JPA, Thymeleaf, Lombok, Oracle driver).
- RestControllers handle all request/response logic.
- DataDal classes handle all database operation logic using Repository methods.
- RestControllers must not autowire Repositories directly unless absolutely necessary.
- DataDal classes must not query the database directly (use Repositories).
- Use Domain Model classes for data transfer between RestControllers and DataDal classes.
- Entity classes are only for carrying data from database queries.
- Entities and repositories are separate fro the Redis and Oracle implementations. Both must be managed to support the same functionality regardless of backend implementations.

## Entity Class Conventions
- Annotate with @Entity and @Data (Lombok).
- Use lombok for all getters, setters, and constructors.
- Use @Table(name="table_name") for table names.
- Use @Column(name="column_name") for column names.
- Use @Id and @GeneratedValue(strategy=GenerationType.IDENTITY) for IDs.
- Use FetchType.LAZY for relationships.
- Annotate properties with validation annotations (e.g., @Size, @NotEmpty, @Email).

## DTO Conventions
- Use Java records for DTOs unless otherwise specified.
- Include a compact canonical constructor for parameter validation (not null, blank, etc.).
- Mapping from entity to DTO and reverse is done with Mapstruct mappers.

## Repository Class Conventions
- Annotate with @Repository.
- Use interfaces extending JpaRepository<Entity, ID>.
- Use JPQL for @Query methods.
- Use @EntityGraph(attributePaths={...}) to avoid N+1 problems in relationship queries.
- Use DTOs for multi-join queries with @Query.
- Only create repository methods for complex queries; use Spring Data JPA for simple CRUD operations.

## Service Class Conventions
- Service classes are interfaces; implementations are ServiceImpl classes annotated with @Service.
- Autowire dependencies in ServiceImpl without constructors unless specified.
- ServiceImpl methods return DTOs (not entities) unless necessary.
- Use repository methods with .orElseThrow for existence checks.
- Use @Transactional or transactionTemplate for multiple sequential DB operations.

## RestController Conventions
- Annotate with @RestController and specify class-level @RequestMapping.
- Use best-practice HTTP method annotations (e.g., @PostMapping, @GetMapping).
- Autowire dependencies in class methods without constructors unless specified.
- Implement all logic in try-catch blocks; handle errors with GlobalExceptionHandler.
- This project uses generated API model objects and Resource classes using the openapi.yml file.
- The "target/generated-sources/openapi" folder contains the generated API model objects and Resource classes.
- If the generated sources for openapi.yml are not present, run the Maven command "mvn clean compile" to generate them.
- All RestControllers must override the default methods in the generated API model objects.

## ApiResponse & GlobalExceptionHandler
- ApiResponse and GlobalExceptionHandler classes must be present and follow best practices for structure and error handling.

## Code Quality
- Use Java 17 features where applicable.
- Before coding, write pseudocode for the intended functionality.
- Use TDD (Test Driven Development) for all changes.
- Unit test coverage must be at least 80%.
- Write unit tests for all classes and methods except generated code via Lombok or Swagger.
- Use Mockito for mocking dependencies in unit tests.
- Use JUnit 5 for unit tests.

## Project Specific Instructions
- The ServiceAdapter class handles the mapping of all domain objects to API model objects via the usage of "DomainToProvider" classes.
- The DomainToProvider classes match the name of the domain object they are mapping.