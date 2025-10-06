# 1.Add dependency of postgreSQL driver

## 1.1 Configure dependencies in build.gradle

```java 
dependencies {
// 1. Spring Data JPA dependency(para la ORM, p. ej. Hibernate)
implementation 'org.springframework.boot:spring-boot-starter-data-jpa'

    // 2. PostgreSQL driver dependency(is runtimeOnly because is only needed 
    // in execution time)
    runtimeOnly 'org.postgresql:postgresql'
    
    // Others standard dependencies of Spring Boot
    implementation 'org.springframework.boot:spring-boot-starter-web'
    testImplementation 'org.springframework.boot:spring-boot-starter-test'
}
```

# 2.Configure connection properties

```java
//URL database connection
spring.datasource.url=jdbc:postgresql://localhost:5432/name-db

//Credentials
spring.datasource.username=postgre-user
spring.datasource.password=secret-password

//Driver Class 
spring.datasource.driver-class-name=org.postgresql.Driver

//Optional configuration to JPA/Hibernate
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

```
