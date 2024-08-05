# Project: Transaction Audit Platform

**Description:** Develop a platform that manages financial transactions and includes auditing functionalities to track and record operations. Use custom annotations, AOP for auditing aspects, and reflection for dynamic processing.

**Key Features:**

**Transaction Management:**

- Create, update, and view financial transactions.
- Perform debit and credit operations.

**Transaction Audit:**

- Track all financial transaction operations.
- Record details such as user, timestamp, and type of operation.

**Audit Reports:**

- Generate detailed reports of audited operations.

**Study/Practice Topics:**

- **Custom Annotations:** Create and use custom annotations.
- **AOP (Aspect-Oriented Programming):** Implement aspects for auditing.
- **Reflection:** Use reflection for dynamic processing of classes and methods.
- **Spring Boot:** Basic project structure.
- **Spring AOP:** Implement AOP with Spring.
- **JPA/Hibernate:** Data persistence.
- **REST APIs:** Expose functionalities through RESTful APIs.
- **Testing:** JUnit and Mockito for testing.

**Project Structure:**

1. **Project Setup:**

   Create a new Spring Boot project with dependencies for Spring AOP, Spring Data JPA, and H2 Database for quick development.

2. **Creating Custom Annotations:**

   Create a custom annotation `@Auditable` to mark methods that need to be audited.

   ```java
   @Retention(RetentionPolicy.RUNTIME)
   @Target(ElementType.METHOD)
   public @interface Auditable {
       String value() default "";
   }
