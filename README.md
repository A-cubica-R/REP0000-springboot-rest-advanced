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
   