# Spring Boot Persistence Exercise

A Java 21 and Spring Boot learning project using Spring Web, Spring Data JPA, and PostgreSQL. It implements software-engineer record creation and lookup through controller, service, and repository layers.

## API

| Method | Route | Operation |
| --- | --- | --- |
| GET | `/api/v1/software-engineers` | List records |
| GET | `/api/v1/software-engineers/{id}` | Read one record |
| POST | `/api/v1/software-engineers` | Create a record |

See [the controller](src/main/java/com/amigoscode/springboot/SoftwareEngineerController.java) and [service](src/main/java/com/amigoscode/springboot/SoftwareEngineerService.java).

## Development prerequisites

Use JDK 21, the included Maven wrapper, and an isolated PostgreSQL database. Review `docker-compose.yml` and `src/main/resources/application.properties`: the application expects database `amigos` on localhost port 5332, which must be prepared before startup.

The configuration uses `spring.jpa.hibernate.ddl-auto=create-drop`, which recreates application tables and drops them at shutdown. Use disposable data only. Run `./mvnw spring-boot:run` on macOS/Linux or `.\mvnw.cmd spring-boot:run` in PowerShell.

This is a focused persistence exercise. The package namespace is `com.amigoscode`; preserve attribution to any learning material used. Authentication, update/delete endpoints, migrations, and substantive API tests are outside the implementation. A generated context-loading test is included.
