# Java basic REST CRUD backend with Spring Boot and Spring Data JPA

This bundle generates a full backend application for CRUD operations.

This project is a fork of **java-rest-springboot-jpa-basic**, adapted to use **Lombok**, improve the **DTOs**, and simplify the structure into a cleaner architecture using more modern technologies.

Original bundle author: https://github.com/l-gu

The generated application is as simple as possible:

- single-module project
- REST controllers based on Spring Boot
- JSON payloads based on improved DTOs
- thin service layer
- DTO ↔ JPA entity mapping
- persistence based on JPA entities with Spring Data JPA repositories

Versions and compatibility:

- The base Spring Boot version is defined in [pom_xml.vm](pom_xml.vm) through `SPRING_BOOT_VERSION`.
- `ModelMapper` and `springdoc-openapi` are also controlled from template properties in [pom_xml.vm](pom_xml.vm).
- Dependencies such as MySQL may not declare a version because it is managed by the Spring Boot parent.

Variables used by this bundle:

- Standard Telosys variables: `SRC`, `RES`, `TEST_SRC`, `TEST_RES`, `ROOT_PKG`, `BEANNAME`.
- Project variables used in `pom_xml.vm`: `MAVEN_GROUP_ID`, `MAVEN_ARTIFACT_ID`, `PROJECT_VERSION`, `PROJECT_NAME`, `SPRING_BOOT_VERSION`, `JAVA_VERSION`, `MODELMAPPER_VERSION`, `SPRINGDOC_VERSION`.
- Project variables used in `main-resources/application_properties.vm`: `REST_SERVER_PORT`, `PROJECT_NAME`, `DB_JDBC_DRIVER_CLASS`, `DB_JDBC_URL`, `DB_USER`, `DB_PASSWORD`, `DB_JPA_DIALECT`, `REST_API_ROOT`, `SECURITY_USER`, `SECURITY_PASSWORD`.
- Project variables used in Java templates: `REST_API_ROOT` (in `main-java/XxxRestController_java.vm`).

Used variables not found in the provided `telosys-tools.cfg`:

- `SPRING_BOOT_VERSION`
- `JAVA_VERSION`
- `MODELMAPPER_VERSION`
- `SPRINGDOC_VERSION`

Suggested entries to add in `telosys-tools.cfg`:

- `ProjectVariable.SPRING_BOOT_VERSION=4.0.5`
- `ProjectVariable.JAVA_VERSION=17`
- `ProjectVariable.MODELMAPPER_VERSION=3.2.6`
- `ProjectVariable.SPRINGDOC_VERSION=3.0.3`
   