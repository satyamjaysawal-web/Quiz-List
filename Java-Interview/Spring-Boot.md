Here’s a comprehensive list of **Spring Boot** interview questions. These questions cover the core concepts, configuration, features, and practical usage of Spring Boot, and can help candidates prepare for interviews focused on Spring Boot.

### Spring Boot Interview Questions

#### Basic Concepts
1. **What is Spring Boot?**
2. **How does Spring Boot differ from Spring Framework?**
3. **What are the main advantages of using Spring Boot?**
4. **What are the key features of Spring Boot?**
5. **Explain the concept of "Convention over Configuration" in Spring Boot.**
6. **What is Auto-Configuration in Spring Boot?**
7. **How does Spring Boot simplify application development?**
8. **What is the role of the `@SpringBootApplication` annotation?**
9. **What are Spring Boot Starters?**
10. **Explain the Spring Boot "fat JAR" and "thin JAR" concepts.**
11. **What is Spring Boot Initializr?**
12. **What is the purpose of the `application.properties` or `application.yml` file in Spring Boot?**

#### Auto-Configuration and Annotations
13. **How does Spring Boot Auto-Configuration work?**
14. **How can you exclude specific Auto-Configurations in Spring Boot?**
15. **What are some common Spring Boot annotations?**
16. **Explain the `@EnableAutoConfiguration` annotation.**
17. **What is the difference between `@SpringBootApplication` and `@EnableAutoConfiguration`?**
18. **What is the use of `@RestController` in Spring Boot?**
19. **How do you configure component scanning in Spring Boot?**
20. **How does `@ConfigurationProperties` work in Spring Boot?**

#### Spring Boot Configuration
21. **How do you configure an external application property in Spring Boot?**
22. **How do you define a custom property in Spring Boot?**
23. **What is the purpose of `@Value` annotation in Spring Boot?**
24. **What are profiles in Spring Boot, and how do you use them?**
25. **How do you configure different profiles in Spring Boot?**
26. **How do you switch between profiles in Spring Boot?**
27. **What is the use of `spring.profiles.active` property?**
28. **What is the difference between `application.properties` and `application.yml`?**

#### Embedded Server and Deployment
29. **What is the default embedded server in Spring Boot?**
30. **How do you change the default port in Spring Boot?**
31. **How do you configure an embedded servlet container in Spring Boot?**
32. **How can you deploy a Spring Boot application as a WAR file?**
33. **What is the purpose of the `SpringApplication` class in Spring Boot?**

#### RESTful Web Services
34. **How do you create a RESTful web service in Spring Boot?**
35. **What is the difference between `@Controller` and `@RestController` in Spring Boot?**
36. **How do you handle exceptions in Spring Boot REST API?**
37. **What is the role of `@ResponseEntity` in Spring Boot REST?**
38. **How do you configure CORS in Spring Boot REST?**
39. **How do you document a RESTful API using Spring Boot?**

#### Spring Boot Actuator
40. **What is Spring Boot Actuator?**
41. **How do you enable Spring Boot Actuator endpoints?**
42. **What are some commonly used Spring Boot Actuator endpoints?**
43. **How can you create custom Actuator endpoints in Spring Boot?**
44. **How do you secure Spring Boot Actuator endpoints?**
45. **What is the `/health` endpoint in Spring Boot Actuator?**
46. **How do you monitor and manage a Spring Boot application using Actuator?**

#### Spring Boot Testing
47. **What is Spring Boot Test?**
48. **How do you write unit tests for Spring Boot applications?**
49. **What is the role of `@SpringBootTest`?**
50. **How do you mock beans and components in Spring Boot tests?**
51. **What is the role of `@MockBean` and `@SpyBean` in Spring Boot tests?**
52. **How do you perform integration testing in Spring Boot?**

#### Spring Boot Security
53. **How do you implement security in Spring Boot?**
54. **What is the role of Spring Security in Spring Boot?**
55. **How do you secure a Spring Boot application with JWT (JSON Web Tokens)?**
56. **What is the purpose of `@EnableWebSecurity` annotation in Spring Boot?**
57. **How do you customize authentication and authorization in Spring Boot?**
58. **How do you configure password encoding in Spring Boot?**

#### Spring Boot with Databases
59. **How do you configure a database in Spring Boot?**
60. **What is Spring Data JPA, and how does it integrate with Spring Boot?**
61. **How do you configure H2 as an in-memory database in Spring Boot?**
62. **What is the role of `spring.datasource.url` in Spring Boot?**
63. **How do you use Spring Boot with Hibernate?**
64. **What is the role of `@Entity` in Spring Boot JPA?**
65. **How do you implement pagination and sorting in Spring Boot?**
66. **How do you configure and use Flyway or Liquibase with Spring Boot?**

#### Spring Boot Caching
67. **How do you implement caching in Spring Boot?**
68. **What is the role of `@Cacheable` and `@CacheEvict` annotations?**
69. **How do you configure EhCache or Redis with Spring Boot?**

#### Spring Boot Logging
70. **What is the default logging framework in Spring Boot?**
71. **How do you configure custom logging in Spring Boot?**
72. **What is the role of `logback-spring.xml` or `log4j2-spring.xml` in Spring Boot?**
73. **How do you log in different environments using Spring Boot profiles?**

#### Spring Boot DevTools
74. **What is Spring Boot DevTools, and how does it help in development?**
75. **How do you enable automatic restart with Spring Boot DevTools?**
76. **How does live reload work with Spring Boot DevTools?**

#### Microservices with Spring Boot
77. **How do you build microservices using Spring Boot?**
78. **What is Spring Cloud, and how does it integrate with Spring Boot?**
79. **How do you handle service discovery with Spring Boot and Eureka?**
80. **What is Spring Cloud Config, and how does it work with Spring Boot?**
81. **How do you implement circuit breaker patterns in Spring Boot using Resilience4j or Hystrix?**
82. **How do you use Feign clients in Spring Boot for inter-service communication?**

#### Miscellaneous
83. **What is the difference between Spring Boot and Spring Cloud?**
84. **How do you manage transactions in Spring Boot?**
85. **What is `@EnableAutoConfiguration` and how does it work in Spring Boot?**
86. **What are some common performance tuning tips for Spring Boot applications?**
87. **How do you deploy a Spring Boot application to a cloud platform like AWS, Azure, or Google Cloud?**
88. **How do you implement asynchronous processing in Spring Boot?**
89. **What is the use of `@Async` annotation in Spring Boot?**
90. **How do you configure and use message brokers like RabbitMQ or Kafka with Spring Boot?**


---
---

Here is a table listing various terms related to Spring Boot, organized in a clear format:

| **Spring Boot Term**           | **Description**                                                      |
|--------------------------------|---------------------------------------------------------------------|
| **Spring Boot**                | A framework to simplify the bootstrapping and development of new Spring applications. |
| **@SpringBootApplication**     | A convenience annotation that combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`. |
| **Auto-Configuration**         | Mechanism to automatically configure Spring applications based on dependencies. |
| **Starter POMs**               | Pre-configured dependency descriptors to easily add dependencies.   |
| **Spring Boot CLI**            | A command-line interface for developing Spring applications.        |
| **Spring Initializr**          | A web-based tool for generating Spring Boot project templates.     |
| **Actuator**                   | Module that provides production-ready features such as monitoring and metrics. |
| **Properties File**            | Configuration file (`application.properties` or `application.yml`) for application settings. |
| **Profiles**                   | Mechanism to define different configurations for different environments (e.g., dev, test, prod). |
| **@ConfigurationProperties**   | Annotation to bind external properties to a Java object.             |
| **Embedded Server**            | A server (like Tomcat or Jetty) that runs within the Spring Boot application. |
| **RESTful Web Services**       | Services built using Spring Boot to handle HTTP requests and responses in REST architecture. |
| **Spring Data JPA**            | A Spring module that makes it easy to implement JPA-based repositories. |
| **@RestController**            | Specialized version of `@Controller` for creating RESTful APIs.    |
| **@Controller**                | Annotation used to define a Spring MVC controller.                  |
| **@RequestMapping**            | Annotation for mapping HTTP requests to handler methods.             |
| **@GetMapping**                | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.GET)`. |
| **@PostMapping**               | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.POST)`. |
| **@PutMapping**                | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.PUT)`. |
| **@DeleteMapping**             | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.DELETE)`. |
| **@PathVariable**              | Annotation to extract values from the URI path.                     |
| **@RequestParam**              | Annotation to extract query parameters from the URL.                 |
| **@Value**                     | Annotation to inject values from properties files.                  |
| **@Component**                 | Generic stereotype for any Spring-managed component.                |
| **@Service**                   | Specialized form of `@Component`, used for service layer beans.    |
| **@Repository**                | Specialized form of `@Component`, used for Data Access Objects (DAOs). |
| **Spring Security**            | A module for securing Spring applications.                           |
| **Caching**                    | Mechanism to store frequently accessed data for performance improvement. |
| **@EnableCaching**             | Annotation to enable caching in a Spring Boot application.          |
| **Error Handling**             | Mechanisms to manage and respond to errors (e.g., `@ControllerAdvice`). |
| **Testing**                    | Spring Boot provides support for testing with JUnit and Mockito.    |
| **Spring Boot DevTools**       | Tools to improve the development experience (e.g., automatic restarts). |
| **Application Context**        | Central interface for providing configuration and management of beans. |
| **Dependency Injection**       | A design pattern used to implement IoC (Inversion of Control).      |
| **Bean**                       | An object that is instantiated, assembled, and managed by the Spring IoC container. |
| **CommandLineRunner**          | A functional interface for code that needs to run on application startup. |
| **ApplicationListener**        | Interface for listening to application events.                       |
| **Spring Boot Actuator**       | Provides built-in endpoints for monitoring and managing Spring Boot applications. |
| **@Scheduled**                 | Annotation to indicate that a method should be run on a scheduled basis. |
| **Custom Filter**              | A filter that processes requests and responses in Spring applications. |
| **Multipart File Upload**      | Handling file uploads in Spring Boot applications.                  |

This table includes essential terms and concepts related to Spring Boot, making it easier to understand and reference for development or study purposes.

Here’s an expanded table with more terms and concepts related to Spring Boot:

| **Spring Boot Term**           | **Description**                                                      |
|--------------------------------|---------------------------------------------------------------------|
| **Spring Boot Starter Web**    | Starter dependency for building web applications, including RESTful applications. |
| **Spring Boot Starter Data JPA** | Starter dependency for Spring Data JPA, simplifying database interactions. |
| **Spring Boot Starter Security** | Starter dependency for Spring Security, providing authentication and authorization features. |
| **Spring Boot Starter Test**   | Starter for testing Spring Boot applications with JUnit and Mockito. |
| **Spring Boot Starter Actuator** | Starter for Spring Boot Actuator, which provides production-ready features. |
| **@EnableAutoConfiguration**   | Enables auto-configuration support in Spring Boot applications. |
| **Health Indicators**          | Components that provide health status of an application for monitoring purposes. |
| **Environment**                | Represents the context in which the application runs, including configuration properties. |
| **Application Runner**         | Interface to run specific code after the application context is loaded. |
| **Conditional Annotations**    | Annotations like `@ConditionalOnProperty`, `@ConditionalOnClass` for conditional bean registration. |
| **@Bean**                      | Annotation to indicate that a method produces a bean to be managed by the Spring container. |
| **Spring Boot DevTools**       | Tools that enhance the development experience with features like automatic restarts. |
| **External Configuration**      | Mechanism for managing application properties via `application.properties`, YAML files, or environment variables. |
| **Spring Cloud**               | A suite of tools for developing cloud-native applications using Spring Boot. |
| **WebFlux**                    | A reactive programming framework for building non-blocking web applications. |
| **WebMvcConfigurer**           | Interface for customizing Spring MVC configurations.               |
| **WebSecurityConfigurerAdapter** | Base class for configuring Spring Security in web applications.  |
| **Session Management**         | Mechanism to manage user sessions in web applications.             |
| **CORS**                       | Cross-Origin Resource Sharing, a security feature that allows restricted resources to be requested from another domain. |
| **File Upload**                | Handling file uploads using Spring Boot, often with `MultipartFile`. |
| **Exception Handling**         | Mechanism to manage exceptions globally using `@ControllerAdvice`. |
| **Async Support**              | Enables asynchronous processing of methods, improving performance.  |
| **Logging**                    | Built-in logging capabilities using SLF4J, Logback, or Log4j.     |
| **Swagger/OpenAPI**            | Tools for API documentation and testing, often integrated with Spring Boot. |
| **Embedded Databases**         | Support for embedded databases like H2, HSQLDB, or Derby for testing. |
| **REST Clients**               | Components for making REST API calls, often using `RestTemplate` or `WebClient`. |
| **Configuration Classes**      | Classes annotated with `@Configuration` to define beans and configurations. |
| **DataSource**                 | Represents a factory for connections to the physical data source.   |
| **JPA Entities**               | Classes that represent database tables in a Java application.      |
| **@Entity**                    | Annotation to mark a class as a JPA entity.                        |
| **@Id**                        | Annotation to specify the primary key of an entity.                |
| **Spring Retry**               | A library for retrying operations in a configurable way, often useful for transient failures. |
| **Async RestTemplate**         | A non-blocking alternative to `RestTemplate` for making REST API calls. |
| **Scheduled Tasks**            | Tasks scheduled to run at fixed intervals or cron expressions using `@Scheduled`. |
| **Spring Data REST**           | Automatically exposes Spring Data repositories as RESTful APIs.    |
| **Custom Error Pages**         | Mechanism to handle and display custom error pages for different HTTP status codes. |
| **Spring HATEOAS**             | A set of libraries for implementing Hypermedia as the Engine of Application State in REST APIs. |
| **PropertySource**             | An annotation to indicate a source of properties for configuration.  |
| **Profiles**                   | Define different sets of configurations for various environments (e.g., `dev`, `prod`). |
| **@ConditionalOnClass**        | Conditional annotation for loading a bean only if a specific class is present. |
| **@EnableScheduling**          | Enables support for scheduled tasks in Spring Boot applications.   |
| **Spring Batch**               | A framework for batch processing of data in Spring applications.   |
| **Spring Integration**         | A framework for building integration solutions in Spring applications. |
| **JobRepository**              | Interface for managing the metadata of jobs in Spring Batch.      |
| **Spring AMQP**                | Provides support for AMQP messaging (e.g., RabbitMQ).             |
| **OAuth2**                     | An authorization framework for securing APIs with access tokens.   |
| **JWT**                        | JSON Web Tokens, a method for securely transmitting information between parties. |
| **@Scheduled(fixedDelay)**     | Schedule a task to run after a fixed delay after the last completion. |
| **@Scheduled(fixedRate)**      | Schedule a task to run at a fixed interval regardless of the completion time. |
| **H2 Database**                | A lightweight in-memory database often used for development and testing in Spring Boot applications. |
| **@Configuration**             | Indicates that the class can be used by the Spring IoC container as a source of bean definitions. |
| **Spring Boot Test**           | Testing support for Spring Boot applications, including annotations like `@SpringBootTest`. |
| **CommandLineRunner**          | A functional interface for executing code upon application startup. |
| **Service Layer**              | Layer in an application architecture that contains business logic and service methods. |
| **Controller Layer**           | Layer that handles incoming HTTP requests and maps them to appropriate service methods. |
| **Model-View-Controller (MVC)**| Architectural pattern used for developing web applications.        |
| **Data Transfer Objects (DTO)**| Objects used to transfer data between processes, especially in APIs. |
| **Spring ORM**                 | Module providing integration with popular Object-Relational Mapping frameworks (like Hibernate). |
| **Thread Pool**                | A pool of threads that can be used for executing asynchronous tasks. |
| **Spring Web**                 | Module for building web applications using Spring Framework features. |
| **Testing Annotations**        | Annotations like `@MockBean`, `@Test`, `@Autowired` used in testing Spring applications. |
| **Integration Tests**          | Tests that verify the interaction between different components of the application. |
| **Unit Tests**                 | Tests that focus on a small part of the application in isolation.  |
| **WebClient**                  | A non-blocking, reactive client for making HTTP requests in Spring applications. |
| **MongoDB**                    | A NoSQL database supported by Spring Data for managing document-based data. |
| **Kafka**                      | A distributed messaging system that can be integrated with Spring Boot applications. |
| **@EnableWebSecurity**         | Annotation to enable Spring Security in web applications.           |
| **Circuit Breaker**            | A design pattern used to detect failures and encapsulate the logic of preventing the application from repeatedly trying to execute an operation that's likely to fail. |
| **Spring Boot 2.x**            | Version of Spring Boot that introduced many enhancements, including reactive programming support. |

This expanded table provides a more comprehensive overview of terms related to Spring Boot, including additional concepts, annotations, and frameworks that are commonly used in conjunction with Spring Boot applications.

---


---



Providing detailed answers for all **Spring Boot interview questions** with code examples and explanations in Hinglish would make this response extremely lengthy. To give you a practical and manageable resource, I'll answer **some of the most important questions**. If you'd like more specific details on certain questions later, just ask!

Here are answers to selected key questions from different sections, written in **Hinglish**.

---

### 1. **What is Spring Boot?**
**Answer:**  
Spring Boot ek extension hai Spring Framework ka jo application development ko simplify karta hai. Isme auto-configuration, embedded servers jaise Tomcat, aur jar deployment ki facility hoti hai, jisse minimal configuration mein applications build ho jaati hain.

---

### 2. **How does Spring Boot differ from Spring Framework?**
**Answer:**
- **Spring Framework:** Bohot saari manual configuration required hoti hai.
- **Spring Boot:** Automatic configuration ke sath aata hai, jisme boilerplate code likhne ki zarurat nahi hoti.

---

### 3. **What is Auto-Configuration in Spring Boot?**
**Answer:**  
Auto-configuration feature Spring Boot ka ek powerful feature hai jo automatically Spring Beans aur dependencies ko configure karta hai. Agar aap apne project mein dependencies add karte ho, to Spring Boot use automatically configure kar dega.

**Example:**
Agar aap JDBC driver add karte ho apne `pom.xml` mein, to Spring Boot automatically `DataSource` ko configure kar deta hai.

```xml
<!-- pom.xml mein dependency -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

#output: DataSource aur JDBC template automatic configure ho jayega, aur aap directly database access kar sakte ho.

---

### 4. **What are Spring Boot Starters?**
**Answer:**  
Spring Boot starters pre-configured dependencies ka collection hota hai jo aapko alag-alag Spring modules use karne ke liye saare required dependencies provide karta hai.

**Example:**  
- **spring-boot-starter-web**: Web applications banane ke liye.
- **spring-boot-starter-data-jpa**: JPA aur Hibernate integration ke liye.

---

### 5. **What is the role of the `@SpringBootApplication` annotation?**
**Answer:**
`@SpringBootApplication` teen annotations ka combination hai:  
1. `@EnableAutoConfiguration`
2. `@ComponentScan`
3. `@Configuration`

Ye annotation Spring Boot application ko start karta hai aur auto-configuration enable karta hai.

**Example:**
```java
@SpringBootApplication
public class MySpringBootApplication {
    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}
```

#output: Application run karne par Spring Boot automatically beans, configuration, aur component scan kar lega.

---

### 6. **How do you configure a Spring Boot application?**
**Answer:**  
Spring Boot application ko configure karne ke liye aap `application.properties` ya `application.yml` file use kar sakte ho.

**Example:**
- **application.properties**
```properties
server.port=8081
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
```

- **application.yml**
```yaml
server:
  port: 8081
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/mydb
```

#output: Server port 8081 pe chalega aur MySQL database use hoga.

---

### 7. **How do you create a RESTful web service in Spring Boot?**
**Answer:**  
RESTful web service banane ke liye aap `@RestController` aur `@GetMapping`, `@PostMapping` jaise annotations use karte ho.

**Example:**
```java
@RestController
@RequestMapping("/api")
public class UserController {

    @GetMapping("/users")
    public List<String> getUsers() {
        return Arrays.asList("John", "Jane", "Alex");
    }
}
```

#output: Agar aap `/api/users` endpoint hit karte ho, to ye list of users return karega as JSON response.

```bash
GET http://localhost:8080/api/users
# Output: ["John", "Jane", "Alex"]
```

---

### 8. **How do you configure different profiles in Spring Boot?**
**Answer:**  
Spring Boot mein profiles ko configure karne ke liye aap `application-{profile}.properties` ya `application.yml` file mein configurations specify kar sakte ho.

**Example:**
- **application-dev.properties**
```properties
server.port=8080
spring.datasource.url=jdbc:mysql://localhost:3306/devdb
```

- **application-prod.properties**
```properties
server.port=8082
spring.datasource.url=jdbc:mysql://localhost:3306/proddb
```

#output: Aap `spring.profiles.active=dev` ya `prod` karoge to respectively dev ya prod settings load hogi.

---

### 9. **What is Spring Boot Actuator?**
**Answer:**  
Spring Boot Actuator ek module hai jo aapki application ki monitoring aur management ke liye endpoints provide karta hai. Jaise `/health`, `/metrics`, `/info` endpoints aapki application ke health, metrics, etc. ka status check karne ke liye use hote hain.

**Example:**  
```xml
<!-- pom.xml mein dependency -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

Actuator ko enable karne ke liye:
```properties
management.endpoints.web.exposure.include=*
```

#output: Aap `/actuator/health` endpoint se application ki health check kar sakte ho.

```bash
GET http://localhost:8080/actuator/health
# Output: {"status": "UP"}
```

---

### 10. **How do you secure Spring Boot applications with Spring Security?**
**Answer:**  
Spring Boot application ko secure karne ke liye aap `spring-boot-starter-security` dependency use karte ho. By default, ye form-based authentication provide karta hai.

**Example:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

**Security Configuration:**
```java
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
            .antMatchers("/api/public").permitAll() // Public endpoint
            .anyRequest().authenticated()           // Secure all other endpoints
            .and()
            .httpBasic(); // Basic Authentication
    }
}
```

#output: `/api/public` endpoint publicly accessible hoga, baaki endpoints authentication maangenge.

---

### 11. **How do you test Spring Boot applications?**
**Answer:**  
Spring Boot applications ko test karne ke liye `@SpringBootTest` use kar sakte ho jo context load karta hai. Saath mein aap JUnit aur Mockito use kar sakte ho unit testing ke liye.

**Example:**
```java
@SpringBootTest
public class UserServiceTest {

    @Autowired
    private UserService userService;

    @Test
    public void testGetUsers() {
        List<String> users = userService.getUsers();
        assertEquals(3, users.size());
    }
}
```

#output: JUnit test run hote time Spring context load hoga aur service method ka test hoga.

---

### 12. **How do you implement pagination and sorting in Spring Boot?**
**Answer:**  
Spring Data JPA ke sath `Pageable` aur `Sort` objects use kar ke aap pagination aur sorting implement kar sakte ho.

**Example:**
```java
public interface UserRepository extends JpaRepository<User, Long> {
    Page<User> findAll(Pageable pageable);
}
```

Controller mein pagination aur sorting handle karne ke liye:
```java
@GetMapping("/users")
public Page<User> getUsers(Pageable pageable) {
    return userRepository.findAll(pageable);
}
```

#output: Ye API pageable aur sortable response dega, jo paginated aur sorted data return karega.

```bash
GET http://localhost:8080/users?page=0&size=10&sort=name,asc
# Output: First 10 users sorted by name
```

---

If you want answers to other questions or more examples in code, feel free to ask!




Sure! Let's continue answering the rest of the **Spring Boot interview questions** with examples and explanations in **Hinglish**.

---

### 13. **How does Spring Boot Auto-Configuration work?**
**Answer:**  
Spring Boot Auto-Configuration automatically configure karta hai Spring application ke beans ko based on dependencies jo aapke classpath mein available hoti hain. Ye internally `@Conditional` annotations ka use karta hai to check whether a bean or configuration should be applied or not.

**Example:**  
Agar aapne MySQL dependency add ki hai, to Spring Boot automatically `DataSource` ko configure kar dega agar configuration properties file mein correct settings hon.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=password
```

#output: `DataSource` bean automatically configure ho jayega bina manually define kare.

---

### 14. **How can you exclude specific Auto-Configurations in Spring Boot?**
**Answer:**  
Agar aapko specific auto-configurations ko exclude karna ho, to aap `@SpringBootApplication` ke saath `exclude` attribute use kar sakte ho.

**Example:**
```java
@SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })
public class MySpringBootApplication {
    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}
```

#output: Ye configuration `DataSourceAutoConfiguration` ko disable karega.

---

### 15. **What is the purpose of `@RestController` in Spring Boot?**
**Answer:**  
`@RestController` annotation ka use tab hota hai jab aapko RESTful web services banani hoti hain. Ye annotation `@Controller` aur `@ResponseBody` ka combination hai, jo JSON ya XML response return karta hai directly bina view ke.

**Example:**
```java
@RestController
public class ProductController {

    @GetMapping("/products")
    public List<String> getProducts() {
        return Arrays.asList("Laptop", "Mobile", "Tablet");
    }
}
```

#output: `/products` endpoint JSON response return karega:

```json
["Laptop", "Mobile", "Tablet"]
```

---

### 16. **How do you configure view resolution in Spring Boot?**
**Answer:**  
Spring Boot mein view resolution ko configure karne ke liye `application.properties` file mein view resolver set karna hota hai. Jaise agar aap JSP views use kar rahe ho, to `InternalResourceViewResolver` ko set karte ho.

**Example:**
```properties
spring.mvc.view.prefix=/WEB-INF/views/
spring.mvc.view.suffix=.jsp
```

#output: Ye configuration ensure karega ki JSP files `/WEB-INF/views/` folder mein stored hain aur `.jsp` extension ke sath hain.

---

### 17. **How do you handle exceptions in Spring Boot REST API?**
**Answer:**  
Spring Boot REST API mein exceptions ko handle karne ke liye `@ControllerAdvice` aur `@ExceptionHandler` annotations ka use karte hain. Ye global exception handling provide karta hai.

**Example:**
```java
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(ResourceNotFoundException.class)
    public ResponseEntity<String> handleResourceNotFound(ResourceNotFoundException ex) {
        return new ResponseEntity<>(ex.getMessage(), HttpStatus.NOT_FOUND);
    }
}
```

#output: Agar `ResourceNotFoundException` throw hota hai, to 404 Not Found response milega with custom error message.

---

### 18. **What is the role of `@ConfigurationProperties` in Spring Boot?**
**Answer:**  
`@ConfigurationProperties` annotation ka use hota hai external configuration properties ko Spring Beans mein bind karne ke liye. Iska fayda ye hota hai ki aap configuration ko type-safe way mein manage kar sakte ho.

**Example:**
```java
@ConfigurationProperties(prefix = "mail")
public class MailProperties {
    private String host;
    private int port;

    // Getters and Setters
}
```

**application.properties:**
```properties
mail.host=smtp.mailtrap.io
mail.port=2525
```

#output: `MailProperties` class mein automatically mail settings bind ho jayengi.

---

### 19. **How do you monitor and manage a Spring Boot application using Actuator?**
**Answer:**  
Spring Boot Actuator monitoring aur management ke endpoints provide karta hai jaise `/actuator/health`, `/actuator/metrics`, etc. Aap inhe enable karne ke liye `application.properties` mein settings kar sakte ho.

**Example:**
```properties
management.endpoints.web.exposure.include=*
```

#output: Aap `http://localhost:8080/actuator/health` pe ja ke application ki health status check kar sakte ho.

---

### 20. **How do you switch between profiles in Spring Boot?**
**Answer:**  
Spring Boot mein profiles ka use hota hai different environments ke liye alag-alag configurations manage karne ke liye. Profiles ko `application-{profile}.properties` ya `application.yml` mein set kar sakte ho. Profiles switch karne ke liye aap `spring.profiles.active` property use karte ho.

**Example:**
```properties
# application-dev.properties
spring.datasource.url=jdbc:mysql://localhost:3306/devdb
```

```properties
# application-prod.properties
spring.datasource.url=jdbc:mysql://localhost:3306/proddb
```

Command-line ya `application.properties` mein:
```properties
spring.profiles.active=dev
```

#output: Dev environment ke liye configurations load hongi.

---

### 21. **How do you write unit tests for Spring Boot applications?**
**Answer:**  
Spring Boot applications ke liye unit tests likhne ke liye `@SpringBootTest`, `@MockBean`, aur `Mockito` ka use hota hai. `@SpringBootTest` context load karta hai, aur `Mockito` mocks ko inject karta hai for unit testing.

**Example:**
```java
@SpringBootTest
public class UserServiceTest {

    @Autowired
    private UserService userService;

    @MockBean
    private UserRepository userRepository;

    @Test
    public void testGetUserById() {
        User user = new User(1L, "John");
        Mockito.when(userRepository.findById(1L)).thenReturn(Optional.of(user));

        User found = userService.getUserById(1L);
        assertEquals("John", found.getName());
    }
}
```

#output: Ye test `UserService` ko test karega bina database access ke.

---

### 22. **What is the default logging framework in Spring Boot?**
**Answer:**  
Spring Boot mein default logging framework **Logback** hota hai, lekin aap `log4j2` ya `SLF4J` bhi use kar sakte ho based on your preference.

By default, logging ko configure karne ke liye aap `application.properties` ya custom configuration files use kar sakte ho.

**Example:**
```properties
logging.level.org.springframework=DEBUG
logging.file.name=spring-boot-application.log
```

#output: Ye logging level `DEBUG` set karega aur logs `spring-boot-application.log` file mein store honge.

---

### 23. **How do you implement caching in Spring Boot?**
**Answer:**  
Spring Boot mein caching ko implement karne ke liye `spring-boot-starter-cache` aur `@EnableCaching` annotation ka use karte hain.

**Example:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
</dependency>
```

**Configuration:**
```java
@EnableCaching
@SpringBootApplication
public class MySpringBootApplication {
    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}
```

**Caching example:**
```java
@Cacheable("users")
public User getUserById(Long id) {
    // DB query
    return userRepository.findById(id).orElse(null);
}
```

#output: First time DB se data fetch hoga, but next time cache se data milega.

---

### 24. **How do you configure H2 as an in-memory database in Spring Boot?**
**Answer:**  
Spring Boot mein H2 in-memory database ko configure karne ke liye aap `spring-boot-starter-data-jpa` aur `h2` dependency use kar sakte ho. Aapko `application.properties` mein configuration set karna hota hai.

**Example:**
```xml
<dependency>
    <groupId>com.h2database</groupId>
    <artifactId>h2</artifactId>
</dependency>
```

**application.properties:**
```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
```

#output: H2 console `http://localhost:8080/h2-console` par available hogi, aur in-memory database se interact kar sakte hain.

---

### 25. **How do you implement file uploads in Spring Boot?**
**Answer:**  
Spring Boot mein file uploads ko implement karne ke liye `MultipartFile` use kar sakte ho.

**Example:**
```java
@RestController
@RequestMapping("/api/files")
public class FileUploadController {

    @PostMapping("/upload")


    public String uploadFile(@RequestParam("file") MultipartFile file) {
        if (!file.isEmpty()) {
            // File save logic
            return "File uploaded successfully!";
        }
        return "File upload failed!";
    }
}
```

#output: API file ko server par upload karegi aur success/failure message return karegi.

```bash
POST http://localhost:8080/api/files/upload
# Output: "File uploaded successfully!"
```

---

Agar aapko aur koi specific questions ya detail chahiye toh aap pooch sakte ho!


Chaltein hain Spring Boot interview questions ke answers ke agle part par. Ab hum aur bhi important questions ko cover karenge, with examples in **Hinglish**.

---

### 26. **How do you connect Spring Boot with a relational database like MySQL or PostgreSQL?**
**Answer:**  
Spring Boot ko relational database (jaise MySQL ya PostgreSQL) ke saath connect karne ke liye aapko `spring-boot-starter-data-jpa` dependency add karni hoti hai, aur `application.properties` file mein database connection settings define karni hoti hain.

**Example (MySQL connection):**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
</dependency>
```

**application.properties:**
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=rootpassword
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

#output: Spring Boot application automatically MySQL database ke sath connect ho jayegi aur JPA ke through aap database operations kar paoge.

**Example (PostgreSQL connection):**
```xml
<dependency>
    <groupId>org.postgresql</groupId>
    <artifactId>postgresql</artifactId>
</dependency>
```

**application.properties:**
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/mydb
spring.datasource.username=postgres
spring.datasource.password=postgrespassword
spring.datasource.driver-class-name=org.postgresql.Driver
spring.jpa.hibernate.ddl-auto=update
```

#output: PostgreSQL ke liye bhi wahi steps honge, aur aap PostgreSQL database ke sath connect ho sakte ho.

---

### 27. **What is `@PathVariable` and how is it used in Spring Boot?**
**Answer:**  
`@PathVariable` ka use tab hota hai jab aapko URL mein se dynamic path parameters ko retrieve karna ho. Jaise agar aapko kisi resource ka ID chahiye jo URL ke part mein ho, to `@PathVariable` use hota hai.

**Example:**
```java
@RestController
@RequestMapping("/api")
public class UserController {

    @GetMapping("/users/{id}")
    public String getUserById(@PathVariable("id") Long id) {
        return "User ID: " + id;
    }
}
```

#output: Jab aap `/api/users/101` ko call karoge, to aapko `101` id ka output milega as response.

```bash
GET http://localhost:8080/api/users/101
# Output: "User ID: 101"
```

---

### 28. **What is the difference between `@RequestParam` and `@PathVariable`?**
**Answer:**  
- **`@RequestParam:`** Query parameters ko retrieve karne ke liye use hota hai jo URL mein `?key=value` format mein pass hote hain.
- **`@PathVariable:`** URL path ke part ko retrieve karne ke liye use hota hai jo `/resource/{id}` jaisa hota hai.

**Example:**

1. **`@RequestParam` Example:**
   ```java
   @GetMapping("/search")
   public String searchUser(@RequestParam("name") String name) {
       return "Searching user: " + name;
   }
   ```

   #output: `GET /search?name=John` request ke response mein "Searching user: John" milega.

   ```bash
   GET http://localhost:8080/search?name=John
   # Output: "Searching user: John"
   ```

2. **`@PathVariable` Example:**
   ```java
   @GetMapping("/users/{id}")
   public String getUser(@PathVariable("id") Long id) {
       return "User ID: " + id;
   }
   ```

   #output: `GET /users/101` request ke response mein "User ID: 101" milega.

---

### 29. **How do you handle validation in Spring Boot?**
**Answer:**  
Spring Boot mein validation handle karne ke liye aap `javax.validation.constraints` annotations aur `@Valid` annotation ka use karte hain. Agar validation rules break hote hain to errors automatically handle hote hain.

**Example:**
```java
public class User {

    @NotNull(message = "Name cannot be null")
    private String name;

    @Email(message = "Email should be valid")
    private String email;

    // Getters and Setters
}
```

**Controller:**
```java
@RestController
@RequestMapping("/api")
public class UserController {

    @PostMapping("/users")
    public ResponseEntity<String> createUser(@Valid @RequestBody User user, BindingResult result) {
        if (result.hasErrors()) {
            return new ResponseEntity<>(result.getFieldError().getDefaultMessage(), HttpStatus.BAD_REQUEST);
        }
        return new ResponseEntity<>("User created successfully", HttpStatus.OK);
    }
}
```

#output: Agar user input valid hoga to success message milega, nahi to validation error message return hoga.

```bash
POST /api/users
{
    "name": "",
    "email": "invalid-email"
}
# Output: "Name cannot be null" or "Email should be valid"
```

---

### 30. **How can you run a Spring Boot application on a custom port?**
**Answer:**  
Aap Spring Boot application ko custom port par run karne ke liye `application.properties` file mein `server.port` property define kar sakte ho.

**Example:**
```properties
server.port=9090
```

#output: Application ab port `9090` par run hogi instead of default `8080`.

Aap command-line arguments ke through bhi custom port set kar sakte ho:
```bash
java -jar myapp.jar --server.port=9090
```

---

### 31. **How do you implement internationalization (i18n) in Spring Boot?**
**Answer:**  
Spring Boot mein internationalization (i18n) implement karne ke liye aap `MessageSource` ko configure karte ho aur `messages.properties` files create karte ho for different languages.

**Example:**

1. **Configuration:**
   ```java
   @Bean
   public MessageSource messageSource() {
       ReloadableResourceBundleMessageSource messageSource = new ReloadableResourceBundleMessageSource();
       messageSource.setBasename("classpath:messages");
       messageSource.setDefaultEncoding("UTF-8");
       return messageSource;
   }
   ```

2. **messages_en.properties:**
   ```properties
   greeting=Hello, how are you?
   ```

3. **messages_fr.properties:**
   ```properties
   greeting=Bonjour, comment ça va?
   ```

**Controller:**
```java
@RestController
public class GreetingController {

    @Autowired
    private MessageSource messageSource;

    @GetMapping("/greet")
    public String greet(@RequestHeader(name = "Accept-Language", required = false) Locale locale) {
        return messageSource.getMessage("greeting", null, locale);
    }
}
```

#output: Depending on `Accept-Language` header, response "Hello, how are you?" ya "Bonjour, comment ça va?" milega.

```bash
GET /greet
Accept-Language: fr
# Output: "Bonjour, comment ça va?"
```

---

### 32. **How do you enable HTTPS in Spring Boot?**
**Answer:**  
Spring Boot application mein HTTPS enable karne ke liye aapko SSL ke liye `keystore` configure karna hota hai.

**Steps:**
1. Pehle ek self-signed certificate generate karo using `keytool`:
   ```bash
   keytool -genkey -alias mydomain -keyalg RSA -keystore keystore.p12 -storetype PKCS12 -validity 365 -keysize 2048
   ```

2. **application.properties:**
   ```properties
   server.port=8443
   server.ssl.key-store=classpath:keystore.p12
   server.ssl.key-store-password=changeit
   server.ssl.key-store-type=PKCS12
   server.ssl.key-alias=mydomain
   ```

#output: Application ab HTTPS pe chalegi on port `8443`.

---

### 33. **What is `@Scheduled` annotation in Spring Boot?**
**Answer:**  
`@Scheduled` annotation ka use scheduled tasks ko define karne ke liye hota hai jo kisi specific interval ya cron expression ke hisaab se run hoti hain.

**Example:**
```java
@Component
public class ScheduledTasks {

    @Scheduled(fixedRate = 5000)
    public void performTask() {
        System.out.println("Task performed every 5 seconds");
    }

    @Scheduled(cron = "0 0 12 * * ?")
    public void performTaskAtNoon() {
        System.out.println("Task performed every day at noon");
    }
}
```

#output: Pehla task har 5 seconds mein run hoga, aur doosra task har din 12 baje run hoga.

---

### 34. **How do you handle static resources in Spring Boot?**
**Answer:**  
Spring Boot

 automatically static resources ko handle karta hai agar aap unhe specific folders mein rakhte ho, jaise:
- `src/main/resources/static` (For static files like HTML, CSS, JS)
- `src/main/resources/templates` (For Thymeleaf templates)

**Example:**
1. Agar aap `src/main/resources/static/index.html` create karte ho, to aap directly `/index.html` ko browser mein access kar sakte ho.

2. **application.properties:**
   ```properties
   spring.mvc.static-path-pattern=/static/**
   ```

#output: Static resources jaise CSS, JS, images directly serve ho sakti hain without explicit configuration.

---

### 35. **How do you secure a Spring Boot application using Spring Security?**
**Answer:**  
Spring Boot application ko secure karne ke liye `spring-boot-starter-security` dependency aur custom security configurations ko define karte ho. By default, Spring Security application ko basic authentication se secure kar deta hai.

**Example:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

**Security Configuration:**
```java
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
            .antMatchers("/public/**").permitAll()
            .anyRequest().authenticated()
            .and()
            .httpBasic();
    }
}
```

#output: Application ab basic authentication prompt karegi, aur `/public/**` path ko sab log access kar sakte hain bina login ke.

```bash
GET /api/private
# Output: Basic authentication prompt
```

---

Agar aapko aur detailed examples ya explanations chahiye, ya kisi aur topic ka question hai, toh aap mujhe bata sakte ho!







### 43. **What is Spring Boot's auto-configuration feature, and how does it work?**
**Answer:**  
**Auto-configuration** Spring Boot ka core feature hai jo application ke dependencies aur classpath ko dekh kar automatic configuration provide karta hai. Iska matlab hai ki aapko manually configuration karne ki zarurat nahi hoti; Spring Boot automatically beans aur configurations ko create kar deta hai based on what it finds in your classpath.

**How It Works:**
1. **Spring Boot Starter Dependencies:** Jaise hi aap specific starter dependencies ko apne project mein include karte ho (jaise `spring-boot-starter-data-jpa`), Spring Boot automatically related configuration ko detect karta hai.
2. **Conditional Annotations:** Auto-configuration classes `@ConditionalOnMissingBean`, `@ConditionalOnClass` jaise annotations ka use karti hain jo conditional configuration karti hain. Agar aap manually koi bean define nahi karte, tab Spring Boot us bean ko automatically create karta hai.

**Example:**
Jab aap JPA dependency add karte ho, to Spring Boot automatically Hibernate aur JPA ko configure karta hai agar aapke classpath mein relevant libraries present hain.

**Maven Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

#output: Agar aap `spring-boot-starter-data-jpa` ko add karte ho, Spring Boot aapke database connection, Hibernate configuration ko auto-configure karega bina manually XML ya Java config likhne ke.

---

### 44. **How do you exclude a specific auto-configuration class in Spring Boot?**
**Answer:**  
Kuch cases mein aapko kuch unwanted auto-configuration ko disable ya exclude karna padta hai. Aap `@SpringBootApplication` annotation ke sath `exclude` attribute ka use kar sakte ho ya `application.properties` ke through specific configuration ko exclude kar sakte ho.

**Example using `exclude` attribute:**
```java
@SpringBootApplication(exclude = { DataSourceAutoConfiguration.class })
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

#output: Above configuration mein, `DataSourceAutoConfiguration` class ko exclude kiya gaya hai, to application koi default DataSource configure nahi karega.

**Example in `application.properties`:**
```properties
spring.autoconfigure.exclude=org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration
```

#output: Is approach se bhi `DataSourceAutoConfiguration` ko exclude kiya ja sakta hai.

---

### 45. **How do you create custom exceptions in Spring Boot, and how do you handle them globally?**
**Answer:**  
Spring Boot mein custom exceptions aur global exception handling karne ke liye aap custom exceptions create kar sakte ho aur `@ControllerAdvice` ke sath centralized error handling implement kar sakte ho.

#### 1. **Create Custom Exception:**
```java
public class ResourceNotFoundException extends RuntimeException {
    public ResourceNotFoundException(String message) {
        super(message);
    }
}
```

#### 2. **Global Exception Handler Using `@ControllerAdvice`:**
`@ControllerAdvice` global exception handling ke liye use hota hai. Aap `@ExceptionHandler` annotation ka use karke specific exceptions ko handle kar sakte ho.

```java
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(ResourceNotFoundException.class)
    public ResponseEntity<String> handleResourceNotFound(ResourceNotFoundException ex) {
        return new ResponseEntity<>(ex.getMessage(), HttpStatus.NOT_FOUND);
    }

    @ExceptionHandler(Exception.class)
    public ResponseEntity<String> handleGenericException(Exception ex) {
        return new ResponseEntity<>("Internal Server Error: " + ex.getMessage(), HttpStatus.INTERNAL_SERVER_ERROR);
    }
}
```

#output: Agar koi resource `ResourceNotFoundException` throw karta hai, to global exception handler 404 response code ke sath custom error message return karega.

---

### 46. **How do you enable scheduling in Spring Boot?**
**Answer:**  
Spring Boot mein **scheduling** ko enable karne ke liye aapko `@EnableScheduling` annotation ka use karna hota hai aur methods ko `@Scheduled` annotation ke sath define karte ho. Isse aap periodic tasks ko schedule kar sakte ho.

#### 1. **Enable Scheduling in Main Class:**
```java
@SpringBootApplication
@EnableScheduling
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

#### 2. **Create Scheduled Method:**
```java
@Component
public class ScheduledTasks {

    @Scheduled(fixedRate = 5000)
    public void performTask() {
        System.out.println("Task performed at " + new Date());
    }
}
```

- `@Scheduled(fixedRate = 5000)`: Task har 5 seconds mein repeat hoga.
- `@Scheduled(cron = "0 0 * * * *")`: Aap cron expressions bhi use kar sakte ho for more complex scheduling.

#output: Console mein har 5 seconds ke interval mein message print hoga: "Task performed at [current timestamp]".

---

### 47. **How do you access the database in Spring Boot using Spring Data JPA?**
**Answer:**  
Spring Boot ke sath Spring Data JPA ko integrate karne ke liye aap `JpaRepository` interface ko use karte ho, jo common CRUD operations ko handle karta hai. Aapko manually queries likhne ki zarurat nahi hoti.

#### 1. **Add Spring Data JPA Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
```

#### 2. **Entity Class Define Kare:**
```java
@Entity
public class Product {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    private double price;

    // Getters and Setters
}
```

#### 3. **Repository Interface Define Kare:**
```java
public interface ProductRepository extends JpaRepository<Product, Long> {
}
```

#### 4. **Use Repository in Service or Controller:**
```java
@RestController
@RequestMapping("/products")
public class ProductController {

    @Autowired
    private ProductRepository productRepository;

    @GetMapping
    public List<Product> getAllProducts() {
        return productRepository.findAll();
    }

    @PostMapping
    public Product createProduct(@RequestBody Product product) {
        return productRepository.save(product);
    }
}
```

#output: API `/products` ke through aap products ko retrieve aur create kar sakte ho, JPA automatically database mein CRUD operations perform karega.

---

### 48. **How do you implement caching in Spring Boot?**
**Answer:**  
Spring Boot mein **caching** implement karne ke liye `@EnableCaching` annotation ko use karte ho. Caching ko enable karke aap frequently accessed data ko cache mein store karke performance improve kar sakte ho.

#### 1. **Enable Caching in Main Class:**
```java
@SpringBootApplication
@EnableCaching
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

#### 2. **Add Cacheable Method:**
Aap `@Cacheable` annotation ka use karke caching ko enable kar sakte ho. Pehli baar jab method call hota hai, result ko cache mein store kiya jata hai. Next time, cache se result return hota hai bina method call kiye.

```java
@Service
public class ProductService {

    @Cacheable("products")
    public List<Product> getAllProducts() {
        System.out.println("Fetching from database...");
        return productRepository.findAll();
    }
}
```

#### 3. **Configure Cache in `application.properties`:**
```properties
spring.cache.type=simple
```

#output: Pehli baar jab `getAllProducts` method call hota hai, console mein "Fetching from database..." print hoga. Agli baar ye cache se data return karega bina database hit kare.

---

### 49. **How do you deploy a Spring Boot application to an external server?**
**Answer:**  
Spring Boot applications ko easily deploy kiya ja sakta hai external server pe, jaise **Tomcat**, **Heroku**, **AWS**, etc. by creating WAR or JAR files.

#### 1. **WAR File Creation for External Tomcat:**
Agar aap Spring Boot application ko Tomcat server pe deploy karna chahte ho, to `WAR` file banana hoga instead of JAR.

**Step 1:** Pom file mein packaging type WAR set karna:
```xml
<packaging>war</packaging>
```

**Step 2:** `SpringBootServletInitializer` ko extend karna:
```java
@SpringBootApplication
public class MyApplication extends SpringBootServletInitializer {

    @Override
    protected SpringApplicationBuilder configure(SpringApplicationBuilder application) {
        return application.sources(MyApplication.class);
    }

    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

**Step 3:** WAR file create karna:
```bash
mvn clean package
```

**Step 4:** External Tomcat mein WAR deploy karna.

#output: A

ap WAR file ko Tomcat server ke `webapps` folder mein deploy karoge aur application external server pe run hogi.

---

### 50. **What is Spring Boot's embedded server feature, and how does it work?**
**Answer:**  
Spring Boot applications ke sath **embedded server** ka concept use hota hai. Matlab, aapko separate external server configure karne ki zarurat nahi hoti. Spring Boot **Tomcat**, **Jetty**, ya **Undertow** ko as an embedded server ke sath run karta hai.

**How it Works:**
- Jab aap Spring Boot application ko run karte ho, wo internally ek embedded web server ko start karta hai jo JAR file ke andar bundled hota hai.
- Default server Spring Boot ke sath **Tomcat** hota hai, but aap `application.properties` mein Jetty ya Undertow ko configure kar sakte ho.

#output: Aapka Spring Boot application directly run hoga bina kisi separate server ke.

```bash
mvn spring-boot:run
# Output: Tomcat started on port 8080
```

---

Agar aapko in Spring Boot interview questions mein se kisi bhi answer ka aur detailed explanation ya example chahiye, toh aap bata sakte ho!




### 51. **What are Spring Boot profiles, and how do you use them?**
**Answer:**  
**Spring Boot Profiles** aapko application ke different configurations ko manage karne ki suvidha dete hain. Iska istemal kar ke aap alag-alag environments (jaise development, testing, production) ke liye specific settings define kar sakte hain.

**Usage:**
1. **Define Profiles:** Aap `application-{profile}.properties` files create karte ho.
   - Example:
     - `application-dev.properties` (Development configuration)
     - `application-prod.properties` (Production configuration)

2. **Activate Profiles:**
   - Command Line: 
   ```bash
   java -jar myapp.jar --spring.profiles.active=dev
   ```
   - In `application.properties`:
   ```properties
   spring.profiles.active=dev
   ```

3. **Access Profile-Specific Properties:**
   - Jaise hi profile active hoti hai, Spring Boot corresponding properties file se configurations ko load karta hai.

**Example:**
`application-dev.properties`:
```properties
server.port=8081
spring.datasource.url=jdbc:mysql://localhost/dev_db
```

`application-prod.properties`:
```properties
server.port=8080
spring.datasource.url=jdbc:mysql://localhost/prod_db
```

#output: `dev` profile active hone par application port `8081` pe chalega aur development database ka connection establish karega.

---

### 52. **Explain Spring Boot's Actuator. What are its benefits?**
**Answer:**  
**Spring Boot Actuator** aapko application ke health, metrics, and monitoring ke liye additional features provide karta hai. Isse aap easily application ke internal state ko access aur manage kar sakte ho.

**Benefits:**
1. **Health Checks:** Application ki health status jaanne ke liye endpoints available hain.
2. **Metrics:** Application performance metrics jaise memory usage, garbage collection stats etc. access kar sakte ho.
3. **Monitoring:** External monitoring tools ke sath integration aasaan hota hai.
4. **Environment Info:** Application ke environment information jaise properties, active profiles, etc. jaan sakte ho.

**Example Usage:**
1. **Add Actuator Dependency:**
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-actuator</artifactId>
   </dependency>
   ```

2. **Access Actuator Endpoints:**
   - Default endpoints access karne ke liye:
     - `/actuator/health`: Application ki health check karega.
     - `/actuator/metrics`: Metrics information dega.
     - `/actuator/env`: Environment properties show karega.

#output: Aap apne application ke health aur metrics ko `/actuator/health` aur `/actuator/metrics` endpoints ke through dekh sakte ho.

---

### 53. **How do you handle validation in Spring Boot?**
**Answer:**  
Spring Boot mein validation handle karne ke liye aap `javax.validation` annotations ka use kar sakte ho. Ye validation annotations aapke model classes mein use hote hain aur input data ko validate karne mein help karte hain.

#### Example:
1. **Add Validation Dependency:**
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-validation</artifactId>
   </dependency>
   ```

2. **Create a Model Class with Validation Annotations:**
```java
public class User {

    @NotNull
    @Size(min = 2, max = 30)
    private String name;

    @Email
    private String email;

    @Min(18)
    private int age;

    // Getters and Setters
}
```

3. **Use Validation in Controller:**
```java
@RestController
@RequestMapping("/users")
public class UserController {

    @PostMapping
    public ResponseEntity<String> createUser(@Valid @RequestBody User user) {
        return ResponseEntity.ok("User created successfully");
    }
}
```

#output: Agar `User` object mein validation fail hoti hai (jaise `name` empty hai), to Spring Boot automatic 400 Bad Request response return karega with error details.

---

### 54. **What are the different ways to externalize configuration in Spring Boot?**
**Answer:**  
Spring Boot mein configuration externalize karne ke kai tarike hain, jisse aap environment-specific configurations ko manage kar sakte ho.

1. **application.properties or application.yml:** 
   - Default configuration files hain jahan aap key-value pairs define kar sakte ho.

2. **Environment Variables:** 
   - Operating system ki environment variables ko Spring Boot application mein use kar sakte ho.
   - Example: `SPRING_DATASOURCE_URL` variable ko define karna.

3. **Command Line Arguments:**
   - Aap application ko command line arguments ke through run karte waqt configuration set kar sakte ho.
   ```bash
   java -jar myapp.jar --server.port=8081
   ```

4. **Profile-Specific Properties:**
   - Jaise ki pehle discuss kiya, aap `application-{profile}.properties` files create karke alag-alag environments ke liye configurations define kar sakte ho.

5. **Config Server:**
   - Spring Cloud Config Server ka use kar ke centralized configuration manage kar sakte ho.

#output: In methods se aap easily configuration ko externalize kar sakte ho aur different environments ke liye specific settings apply kar sakte ho.

---

### 55. **Explain Spring Boot's `@ConfigurationProperties` annotation.**
**Answer:**  
`@ConfigurationProperties` annotation ka use aapko application properties ya YAML files se data bind karne ke liye hota hai. Ye aapko configuration ko strongly typed beans mein convert karne ki suvidha deta hai.

#### Usage:
1. **Create a Configuration Class:**
```java
@Configuration
@ConfigurationProperties(prefix = "app")
public class AppProperties {

    private String name;
    private String version;

    // Getters and Setters
}
```

2. **Use in Main Application:**
```java
@SpringBootApplication
@EnableConfigurationProperties(AppProperties.class)
public class MyApplication {

    public static void main(String[] args) {
        ApplicationContext context = SpringApplication.run(MyApplication.class, args);
        AppProperties appProperties = context.getBean(AppProperties.class);
        System.out.println(appProperties.getName());
    }
}
```

3. **application.properties:**
```properties
app.name=My Spring Boot Application
app.version=1.0.0
```

#output: Application start hone par `AppProperties` class mein properties bind hongi aur aap `app.name` aur `app.version` ko access kar sakte ho.

---

### 56. **What is the difference between `@Component`, `@Service`, and `@Repository` annotations?**
**Answer:**  
Ye annotations Spring framework mein bean definitions ke liye use hote hain, lekin inka alag-alag purpose hai.

1. **`@Component`:** 
   - General-purpose annotation hai jo Spring ko indicate karta hai ki ye class ek Spring-managed component hai.
   - Use case: Common components ya utility classes.

2. **`@Service`:** 
   - Ye annotation `@Component` ka specialization hai, jo service layer ki classes ko indicate karta hai.
   - Use case: Business logic ko encapsulate karne ke liye.

3. **`@Repository`:** 
   - Ye bhi `@Component` ka specialization hai, jo data access layer ki classes ko represent karta hai.
   - Ye exception handling ko facilitate karta hai, jisse data access exceptions ko Spring’s DataAccessException hierarchy mein convert kiya ja sake.
   - Use case: Database operations ko perform karne ke liye.

**Example:**
```java
@Component
public class MyComponent {
    // General utility methods
}

@Service
public class MyService {
    // Business logic methods
}

@Repository
public class MyRepository {
    // Data access methods
}
```

#output: `@Component`, `@Service`, aur `@Repository` annotations ka use kar ke aap apne code ko better organize kar sakte ho aur Spring ko specific roles samajh sakte ho.

---

### 57. **How do you handle file uploads in Spring Boot?**
**Answer:**  
Spring Boot mein file uploads handle karne ke liye aap `MultipartFile` class ka use kar sakte ho.

#### Example:
1. **Add Dependency in `pom.xml`:**
   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-web</artifactId>
   </dependency>
   ```

2. **Create Controller to Handle File Upload:**
```java
@RestController
@RequestMapping("/upload")
public class FileUploadController {

    @PostMapping
    public ResponseEntity<String> uploadFile(@RequestParam("file") MultipartFile file) {
        // Process file
        String filename = file.getOriginalFilename();
        return ResponseEntity.ok("File uploaded: " + filename);
    }
}
```

3. **HTML Form for File Upload:**
```html
<form method="POST" action="/upload" enctype="multipart/form-data">
    <input type="file" name="file" />
    <button type="submit">Upload</button>
</form>
```

#output: File upload hone par response message mein file ka naam return hoga.

---

### 58. **How do you implement pagination

 and sorting in Spring Boot?**
**Answer:**  
Spring Boot aur Spring Data JPA ke sath pagination aur sorting ko implement karna bahut aasaan hai. Aap `Pageable` interface ka istemal kar sakte ho.

#### Example:
1. **Repository Interface:**
```java
public interface ProductRepository extends JpaRepository<Product, Long> {
    Page<Product> findAll(Pageable pageable);
}
```

2. **Service Layer:**
```java
@Service
public class ProductService {

    @Autowired
    private ProductRepository productRepository;

    public Page<Product> getProducts(int page, int size) {
        Pageable pageable = PageRequest.of(page, size);
        return productRepository.findAll(pageable);
    }
}
```

3. **Controller Layer:**
```java
@RestController
@RequestMapping("/products")
public class ProductController {

    @Autowired
    private ProductService productService;

    @GetMapping
    public Page<Product> getProducts(@RequestParam int page, @RequestParam int size) {
        return productService.getProducts(page, size);
    }
}
```

#output: `/products?page=0&size=10` request karne par aapko pehli page ke 10 products milenge.

---

### 59. **What is Spring Boot DevTools, and how do you use it?**
**Answer:**  
**Spring Boot DevTools** development ke dauran productivity enhance karne ke liye helpful tools ka ek set provide karta hai. Iska main feature **hot-reloading** hai, jisse aap changes karne par application ko baar baar restart nahi karna padta.

#### Usage:
1. **Add DevTools Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```

2. **Automatic Restart:**
   - Jab bhi aap source code mein changes karte hain, DevTools application ko automatically restart karta hai, jisse latest changes reflect ho jate hain.

3. **LiveReload Support:**
   - DevTools static resources ke changes ko automatically detect karta hai aur browser ko refresh kar deta hai agar aapke application mein LiveReload enabled hai.

#output: DevTools ki madad se aapke application ki productivity badh jayegi aur aapko frequent restarts nahi karne padege.

---

### 60. **How do you integrate Spring Boot with Thymeleaf for web applications?**
**Answer:**  
**Thymeleaf** ek modern server-side Java template engine hai jo Spring Boot ke sath easily integrate hota hai. Ye HTML pages ko generate karne ke liye use hota hai.

#### Steps to Integrate:
1. **Add Thymeleaf Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
```

2. **Create HTML Template:**
   - Template files ko `src/main/resources/templates` folder mein rakhna hota hai.
```html
<!DOCTYPE html>
<html xmlns:th="http://www.w3.org/1999/xhtml">
<head>
    <title>Product List</title>
</head>
<body>
<h1>Product List</h1>
<table>
    <tr>
        <th>Name</th>
        <th>Price</th>
    </tr>
    <tr th:each="product : ${products}">
        <td th:text="${product.name}"></td>
        <td th:text="${product.price}"></td>
    </tr>
</table>
</body>
</html>
```

3. **Create Controller to Serve Template:**
```java
@Controller
public class ProductController {

    @GetMapping("/products")
    public String getProducts(Model model) {
        List<Product> products = // fetch products from service
        model.addAttribute("products", products);
        return "productList"; // Thymeleaf template name
    }
}
```

#output: Jab aap `/products` URL ko hit karte hain, aapko `productList.html` template render hote hue dikhai dega, jisme products ka list hoga.

---

### 61. **How do you implement security in Spring Boot using Spring Security?**
**Answer:**  
**Spring Security** ko use karke aap apne Spring Boot application mein security implement kar sakte ho. Ye authentication aur authorization ko handle karta hai.

#### Steps to Implement Security:
1. **Add Spring Security Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

2. **Create Security Configuration:**
```java
@Configuration
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .antMatchers("/public/**").permitAll()
                .anyRequest().authenticated()
                .and()
            .formLogin();
    }

    @Override
    protected void configure(AuthenticationManagerBuilder auth) throws Exception {
        auth.inMemoryAuthentication()
            .withUser("user").password(passwordEncoder().encode("password")).roles("USER");
    }

    @Bean
    public PasswordEncoder passwordEncoder() {
        return new BCryptPasswordEncoder();
    }
}
```

#output: Is configuration se application ko `/public/**` endpoints ke liye anonymous access milega, aur baaki endpoints ke liye authentication zaruri hoga.

---

### 62. **What are the differences between `@RestController` and `@Controller`?**
**Answer:**  
`@RestController` aur `@Controller` dono Spring framework ke annotations hain, lekin unka purpose alag hai.

1. **`@Controller`:** 
   - Ye traditional MVC controller ko represent karta hai. Ye view ko return karta hai aur JSP, Thymeleaf, ya kisi bhi view technology ka use kar sakta hai.
   - Use case: Web applications jahan view rendering ki zarurat hoti hai.

2. **`@RestController`:** 
   - Ye `@Controller` ka specialization hai jo automatically response ko JSON ya XML format mein convert karta hai.
   - Ye `@ResponseBody` ko internally apply karta hai, isliye aapko har method mein `@ResponseBody` likhne ki zarurat nahi hoti.
   - Use case: RESTful APIs jahan data ko directly return karna hota hai bina view rendering ke.

**Example:**
```java
@Controller
public class MyController {
    @GetMapping("/hello")
    public String sayHello() {
        return "hello"; // returns view name
    }
}

@RestController
public class MyRestController {
    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, World!"; // returns JSON response
    }
}
```

#output: `@Controller` use karke aapko view page milega, jabki `@RestController` use karke aapko JSON response milega.

---

### 63. **How do you implement custom authentication in Spring Security?**
**Answer:**  
Custom authentication implement karne ke liye, aapko `UserDetailsService` ko implement karna hoga jo user details ko load karega, aur aapko `AuthenticationProvider` ka use karke custom logic define karna hoga.

#### Example:
1. **Create UserDetailsService Implementation:**
```java
@Service
public class CustomUserDetailsService implements UserDetailsService {

    @Autowired
    private UserRepository userRepository;

    @Override
    public UserDetails loadUserByUsername(String username) throws UsernameNotFoundException {
        User user = userRepository.findByUsername(username);
        if (user == null) {
            throw new UsernameNotFoundException("User not found");
        }
        return new org.springframework.security.core.userdetails.User(user.getUsername(), user.getPassword(), new ArrayList<>());
    }
}
```

2. **Use CustomUserDetailsService in Security Config:**
```java
@Configuration
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Autowired
    private CustomUserDetailsService customUserDetailsService;

    @Override
    protected void configure(AuthenticationManagerBuilder auth) throws Exception {
        auth.userDetailsService(customUserDetailsService).passwordEncoder(passwordEncoder());
    }

    // Other configurations...
}
```

#output: Custom user authentication process implement hota hai, jisme aapke database se user details load hote hain.

---

### 64. **What are some common REST API best practices in Spring Boot?**
**Answer:**  
REST APIs design karte waqt kuch best practices follow karna chahiye:

1. **Use Proper HTTP Methods:**
   - GET: Data retrieve karne ke liye.
   - POST: Data create karne ke liye.
   - PUT: Data update karne ke liye.
   - DELETE: Data delete karne ke liye.

2. **Resource Naming:**
   - URIs ko nouns ki tarah represent karein, jaise `/products`, `/users`.

3. **Use Plural Nouns:**
   - Resources ko plural form mein naam dena chahiye, jaise `/products` instead of `/product`.

4. **Versioning:**
   - API versioning ko implement karein, jaise `/api/v1/products`.

5. **Error Handling:**
   - Standard error responses define karein. JSON format mein error messages return karein.
   ```json
   {
       "timestamp": "2022-10-01T12:30:

45",
       "status": 404,
       "error": "Not Found",
       "message": "Product not found",
       "path": "/products/1"
   }
   ```

6. **Use HATEOAS:**
   - API responses mein links provide karein jisse clients ko resources navigate karne mein madad mile.

7. **Statelessness:**
   - API ko stateless rakhein, har request ko independently process karein.

#output: In practices se aapka REST API more reliable aur user-friendly banega.

---

### 65. **How do you use Spring Boot with a message broker like RabbitMQ?**
**Answer:**  
Spring Boot ke sath **RabbitMQ** ka use karne ke liye aapko `spring-boot-starter-amqp` dependency add karni hoti hai.

#### Steps:
1. **Add Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-amqp</artifactId>
</dependency>
```

2. **Configure RabbitMQ in `application.properties`:**
```properties
spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
```

3. **Create a Message Sender:**
```java
@Service
public class MessageSender {

    @Autowired
    private RabbitTemplate rabbitTemplate;

    public void sendMessage(String message) {
        rabbitTemplate.convertAndSend("myQueue", message);
    }
}
```

4. **Create a Message Receiver:**
```java
@Component
public class MessageReceiver {

    @RabbitListener(queues = "myQueue")
    public void receiveMessage(String message) {
        System.out.println("Received message: " + message);
    }
}
```

5. **Configure RabbitMQ Queue:**
```java
@Configuration
public class RabbitConfig {

    @Bean
    public Queue myQueue() {
        return new Queue("myQueue", false);
    }
}
```

#output: Aapka message sender aur receiver RabbitMQ ke through communicate karega.

---

### 66. **What are Spring Boot Starter Dependencies?**
**Answer:**  
**Spring Boot Starter Dependencies** aise pre-defined dependency bundles hain jo aapko different functionalities ke liye easily dependencies manage karne ki suvidha dete hain. Ye dependencies ko use karke aap quickly Spring Boot applications setup kar sakte ho.

#### Common Starters:
1. **spring-boot-starter-web:** Web applications ke liye, includes Spring MVC, Tomcat.
2. **spring-boot-starter-data-jpa:** Data access ke liye, includes Spring Data JPA aur Hibernate.
3. **spring-boot-starter-security:** Security features ke liye.
4. **spring-boot-starter-thymeleaf:** Thymeleaf template engine ke liye.
5. **spring-boot-starter-test:** Testing ke liye, includes JUnit, Mockito, etc.

**Example Usage:**
```xml
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
</dependencies>
```

#output: Aap easily different functionalities ko integrate kar sakte ho bina individually dependencies manage kiye.

---

### 67. **How do you customize error handling in Spring Boot?**
**Answer:**  
Spring Boot mein error handling ko customize karne ke liye aap `@ControllerAdvice` aur `@ExceptionHandler` annotations ka istemal kar sakte ho.

#### Example:
1. **Create Global Exception Handler:**
```java
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(ProductNotFoundException.class)
    public ResponseEntity<ErrorResponse> handleProductNotFound(ProductNotFoundException ex) {
        ErrorResponse errorResponse = new ErrorResponse("Product Not Found", ex.getMessage());
        return new ResponseEntity<>(errorResponse, HttpStatus.NOT_FOUND);
    }
}
```

2. **Create Custom Exception:**
```java
public class ProductNotFoundException extends RuntimeException {
    public ProductNotFoundException(String message) {
        super(message);
    }
}
```

3. **Throw Custom Exception in Service:**
```java
public Product getProductById(Long id) {
    return productRepository.findById(id)
        .orElseThrow(() -> new ProductNotFoundException("Product with id " + id + " not found"));
}
```

#output: Agar product nahi milta, to custom error response return hoga jisme error message aur status code hoga.

---

### 68. **What is Spring Boot's `@SpringBootApplication` annotation?**
**Answer:**  
`@SpringBootApplication` ek convenience annotation hai jo Spring Boot application ko configure karne ke liye use hota hai. Ye 3 important annotations ka combination hai:

1. **`@Configuration`:** Ye class ko Spring configuration source banata hai.
2. **`@EnableAutoConfiguration`:** Ye Spring Boot ke auto-configuration features ko enable karta hai.
3. **`@ComponentScan`:** Ye application ke components ko scan karta hai jo same package ya sub-packages mein hain.

**Usage Example:**
```java
@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

#output: Ye annotation aapke application ke liye ek entry point create karta hai aur Spring Boot ke features ko enable karta hai.

---

### 69. **What is the purpose of the `application.properties` file in Spring Boot?**
**Answer:**  
`application.properties` file Spring Boot applications mein configuration settings ko define karne ke liye use hoti hai. Is file mein aap application ke behavior ko customize karne ke liye key-value pairs define kar sakte ho.

#### Common Properties:
1. **Server Configuration:**
   ```properties
   server.port=8080
   ```

2. **Database Configuration:**
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/mydb
   spring.datasource.username=root
   spring.datasource.password=password
   ```

3. **Logging Configuration:**
   ```properties
   logging.level.root=INFO
   ```

4. **Custom Application Properties:**
   ```properties
   app.name=My Spring Boot Application
   app.version=1.0.0
   ```

#output: `application.properties` file se aap easily application ki settings ko manage kar sakte ho.

---

### 70. **How do you use `@Value` annotation in Spring Boot?**
**Answer:**  
`@Value` annotation ka use Spring Boot mein properties ko inject karne ke liye hota hai. Iska istemal aap configuration properties ko directly Spring beans mein inject karne ke liye kar sakte ho.

#### Example:
1. **Define Properties in `application.properties`:**
```properties
app.name=My Spring Boot Application
app.version=1.0.0
```

2. **Inject Properties in a Spring Bean:**
```java
@Component
public class AppConfig {

    @Value("${app.name}")
    private String appName;

    @Value("${app.version}")
    private String appVersion;

    public String getAppName() {
        return appName;
    }

    public String getAppVersion() {
        return appVersion;
    }
}
```

#output: Aap `AppConfig` class mein `appName` aur `appVersion` properties ko use kar sakte ho.

---

### 71. **What is Spring Boot's `@Conditional` annotation?**
**Answer:**  
`@Conditional` annotation ka use Spring Boot mein conditional bean definitions ke liye hota hai. Iska istemal aap specific conditions par based beans ko register karne ke liye karte ho.

#### Example:
1. **Create Custom Condition:**
```java
public class MyCondition implements Condition {
    @Override
    public boolean matches(ConditionContext context, AnnotatedTypeMetadata metadata) {
        return "dev".equals(System.getProperty("spring.profiles.active"));
    }
}
```

2. **Use `@Conditional` Annotation:**
```java
@Configuration
public class AppConfig {

    @Bean
    @Conditional(MyCondition.class)
    public MyService myService() {
        return new MyService();
    }
}
```

#output: `myService` bean sirf tab hi register hoga jab active profile `dev` ho.

---

### 72. **How do you schedule tasks in Spring Boot?**
**Answer:**  
Spring Boot mein tasks ko schedule karne ke liye aap `@Scheduled` annotation ka use kar sakte ho. Isse aap periodic tasks ko execute kar sakte ho.

#### Steps to Enable Scheduling:
1. **Enable Scheduling:**
```java
@Configuration
@EnableScheduling
public class SchedulerConfig {
}
```

2. **Create Scheduled Task:**
```java
@Component
public class ScheduledTasks {

    @Scheduled(fixedRate = 5000)
    public void performTask() {
        System.out.println("Task executed at: " + new Date());
    }
}
```

#output: Task har 5 seconds ke interval par execute hoga aur console mein current timestamp print hoga.

---

### 73. **What are Spring Boot's testing features?**
**Answer:**  
Spring Boot testing features aapko unit aur integration testing ke liye helpful tools provide karte hain. Kuch key features hain:

1. **Spring Boot Test Starter:** 
   - `spring-boot-st

arter-test` dependency testing ke liye essential libraries provide karta hai, jaise JUnit, Mockito, etc.

2. **@SpringBootTest Annotation:**
   - Ye annotation aapko integration testing ke liye use hota hai, jisse aap application context ko load kar sakte ho.

3. **MockMvc:** 
   - Ye aapko web layer ke testing ke liye use hota hai, jisse aap controllers ko mock kar sakte ho.

4. **@MockBean:** 
   - Ye aapko dependencies ko mock karne ki suvidha deta hai, jisse aap unit testing kar sakte ho.

#### Example of a Unit Test:
```java
@RunWith(SpringRunner.class)
@SpringBootTest
public class ProductServiceTests {

    @MockBean
    private ProductRepository productRepository;

    @Autowired
    private ProductService productService;

    @Test
    public void testGetProductById() {
        Product product = new Product(1L, "Product A");
        Mockito.when(productRepository.findById(1L)).thenReturn(Optional.of(product));

        Product found = productService.getProductById(1L);
        assertEquals(product.getName(), found.getName());
    }
}
```

#output: Ye test verify karega ki `getProductById` method sahi product return kar raha hai.

---

### 74. **What are profiles in Spring Boot, and how do you use them?**
**Answer:**  
Spring Boot mein **profiles** ka use aapko different configurations ko manage karne ke liye hota hai, jaise development, testing, production, etc. Profiles se aap specific configurations ko load kar sakte ho.

#### Steps to Use Profiles:
1. **Define Properties in `application-{profile}.properties`:**
```properties
# application-dev.properties
app.name=Dev Application
```
```properties
# application-prod.properties
app.name=Prod Application
```

2. **Activate Profile:**
   - Aap profile ko activate kar sakte ho command line se:
   ```
   --spring.profiles.active=dev
   ```

3. **Inject Profile Properties:**
```java
@Value("${app.name}")
private String appName;
```

#output: Application run hone par active profile ke hisab se properties load hongi.

---

### 75. **How do you connect Spring Boot to a database?**
**Answer:**  
Spring Boot ko database se connect karne ke liye aapko kuch simple steps follow karne honge.

#### Steps:
1. **Add Database Dependency:** 
   - Jaise MySQL ke liye:
```xml
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <scope>runtime</scope>
</dependency>
```

2. **Configure Database in `application.properties`:**
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/mydb
spring.datasource.username=root
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update
```

3. **Create Entity Class:**
```java
@Entity
public class Product {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    private String name;
    private Double price;

    // Getters and Setters
}
```

4. **Create Repository Interface:**
```java
public interface ProductRepository extends JpaRepository<Product, Long> {
}
```

#output: Ab aap apne application mein database ke sath interact kar sakte ho.

---

### 76. **How do you create a RESTful API in Spring Boot?**
**Answer:**  
Spring Boot mein RESTful API create karne ke liye aapko controllers, services, aur repositories ka use karna hota hai.

#### Steps:
1. **Create a Controller:**
```java
@RestController
@RequestMapping("/api/products")
public class ProductController {

    @Autowired
    private ProductService productService;

    @GetMapping
    public List<Product> getAllProducts() {
        return productService.getAllProducts();
    }

    @PostMapping
    public Product createProduct(@RequestBody Product product) {
        return productService.createProduct(product);
    }
}
```

2. **Create a Service:**
```java
@Service
public class ProductService {

    @Autowired
    private ProductRepository productRepository;

    public List<Product> getAllProducts() {
        return productRepository.findAll();
    }

    public Product createProduct(Product product) {
        return productRepository.save(product);
    }
}
```

3. **Create a Repository:**
```java
public interface ProductRepository extends JpaRepository<Product, Long> {
}
```

#output: Aap `/api/products` endpoint par products ka list fetch kar sakte ho aur naye products create kar sakte ho.

---

### 77. **How do you handle cross-origin requests in Spring Boot?**
**Answer:**  
Cross-Origin Resource Sharing (CORS) ko handle karne ke liye aap Spring Boot mein `@CrossOrigin` annotation ka use kar sakte ho.

#### Example:
1. **Add `@CrossOrigin` Annotation to Controller:**
```java
@RestController
@RequestMapping("/api/products")
@CrossOrigin(origins = "http://localhost:3000")
public class ProductController {
    // ...
}
```

2. **Global CORS Configuration:**
```java
@Configuration
public class WebConfig implements WebMvcConfigurer {

    @Override
    public void addCorsMappings(CorsRegistry registry) {
        registry.addMapping("/**").allowedOrigins("http://localhost:3000");
    }
}
```

#output: Aapke specified origins se requests ko allow kiya jayega.

---

### 78. **What is the purpose of `@Transactional` in Spring Boot?**
**Answer:**  
`@Transactional` annotation ka use transaction management ke liye hota hai. Iska istemal aapko database operations ko atomic, consistent, isolated, aur durable (ACID) banane ke liye hota hai.

#### Example:
1. **Use `@Transactional` in Service Layer:**
```java
@Service
public class ProductService {

    @Autowired
    private ProductRepository productRepository;

    @Transactional
    public void createProduct(Product product) {
        productRepository.save(product);
        // Other operations
    }
}
```

#output: Agar `createProduct` method mein koi error aata hai, to transaction rollback ho jayega aur koi data change nahi hoga.

---

### 79. **How do you use Actuator in Spring Boot?**
**Answer:**  
**Spring Boot Actuator** aapko application ke health, metrics, and monitoring information provide karta hai. Iska istemal aapko application ko manage aur monitor karne ke liye hota hai.

#### Steps to Enable Actuator:
1. **Add Actuator Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>
```

2. **Configure Actuator in `application.properties`:**
```properties
management.endpoints.web.exposure.include=health,info
```

3. **Access Actuator Endpoints:**
   - Application run hone par, aap endpoints ko access kar sakte ho:
   - `http://localhost:8080/actuator/health`
   - `http://localhost:8080/actuator/info`

#output: Aapko application ki health aur information metrics milengi jo aapko monitoring mein madad karegi.

---

### 80. **How do you enable logging in Spring Boot?**
**Answer:**  
Spring Boot mein logging enable karne ke liye aap `application.properties` file mein logging configurations define kar sakte ho.

#### Common Logging Configurations:
1. **Log Level:**
```properties
logging.level.root=INFO
logging.level.com.example=DEBUG
```

2. **Log File Configuration:**
```properties
logging.file.name=myapp.log
logging.file.path=/var/logs
```

3. **Logging Pattern:**
```properties
logging.pattern.console=%d{yyyy-MM-dd HH:mm:ss} - %msg%n
```

#output: Aapko console ya file mein logs generate karne ki flexibility milegi.

---

### 81. **What is the difference between `@Component`, `@Service`, `@Repository`, and `@Controller`?**
**Answer:**  
Ye sabhi annotations Spring framework ke part hain, lekin unka use case alag hai:

1. **`@Component`:** 
   - Ye general-purpose component ko define karta hai. Aap ise custom beans ke liye use kar sakte ho.

2. **`@Service`:** 
   - Ye service layer ko represent karta hai. Iska istemal business logic ko define karne ke liye hota hai.

3. **`@Repository`:** 
   - Ye data access layer ko represent karta hai. Iska istemal database operations ke liye hota hai, aur ye data access exceptions ko translate karta hai.

4. **`@Controller`:** 
   - Ye presentation layer ko represent karta hai. Iska istemal web layer mein request handling ke liye hota hai.

#output: In annotations ka istemal aapke code ki readability aur maintainability ko enhance karta hai.

---

### 82. **How do you implement file upload in Spring Boot?**
**Answer:**  
Spring Boot mein file upload implement karne ke liye aapko `MultipartFile` ka use karna hota hai.

#### Steps:
1. **Create HTML Form for File Upload:**
```html
<form method="POST" enctype="

multipart/form-data" action="/upload">
    <input type="file" name="file" />
    <button type="submit">Upload</button>
</form>
```

2. **Create Controller for Handling Upload:**
```java
@RestController
public class FileUploadController {

    @PostMapping("/upload")
    public ResponseEntity<String> uploadFile(@RequestParam("file") MultipartFile file) {
        // File processing logic here
        return ResponseEntity.ok("File uploaded successfully: " + file.getOriginalFilename());
    }
}
```

#output: Aapke application ko files upload karne ki capability mil jayegi.

---

### 83. **What is Spring Boot's `@EnableAutoConfiguration` annotation?**
**Answer:**  
`@EnableAutoConfiguration` annotation Spring Boot application ko auto-configuration features enable karne ke liye use hota hai. Isse Spring Boot automatically aapke application ke dependencies ko detect karke configuration kar deta hai.

**Example:**
```java
@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}
```

#output: Aapka application required beans aur configurations ko automatically configure karega.

---

### 84. **How do you implement pagination in Spring Boot?**
**Answer:**  
Spring Boot mein pagination implement karne ke liye aap `Pageable` aur `Page` interfaces ka istemal kar sakte ho.

#### Steps:
1. **Modify Repository:**
```java
public interface ProductRepository extends JpaRepository<Product, Long> {
    Page<Product> findAll(Pageable pageable);
}
```

2. **Modify Service:**
```java
public Page<Product> getProducts(Pageable pageable) {
    return productRepository.findAll(pageable);
}
```

3. **Modify Controller:**
```java
@GetMapping
public Page<Product> getAllProducts(@RequestParam(defaultValue = "0") int page,
                                     @RequestParam(defaultValue = "10") int size) {
    Pageable pageable = PageRequest.of(page, size);
    return productService.getProducts(pageable);
}
```

#output: Aap `/api/products?page=0&size=10` endpoint par pagination ke sath products fetch kar sakte ho.

---

### 85. **What is Spring Boot DevTools?**
**Answer:**  
**Spring Boot DevTools** development time ke liye ek helpful tool hai jo aapke application ko quickly rebuild aur reload karne ki capability deta hai. Iska istemal aapko development process ko enhance karne ke liye hota hai.

#### Features:
1. **Automatic Restart:** 
   - Code changes ke baad application automatically restart hota hai.
   
2. **Live Reload:**
   - Aapke browser ko refresh kiye bina changes dekh sakte ho.

3. **Additional Configuration:**
   - DevTools se aap debugging aur logging ko enhance kar sakte ho.

#### Steps to Enable DevTools:
1. **Add DevTools Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```

#output: Aapke development workflow mein speed aur efficiency badhegi.

---

### 86. **What is Spring Security?**
**Answer:**  
**Spring Security** ek powerful authentication aur authorization framework hai jo aapko applications ko secure karne ki capability deta hai. Iska istemal aapko various security concerns ko handle karne ke liye hota hai, jaise login, role-based access, CSRF protection, etc.

#### Key Features:
1. **Authentication:** 
   - User ko verify karne ke liye.

2. **Authorization:** 
   - User ke access ko control karne ke liye.

3. **CSRF Protection:** 
   - Cross-Site Request Forgery se bachne ke liye.

4. **Session Management:** 
   - User sessions ko manage karne ke liye.

#### Basic Configuration Example:
```java
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
            .antMatchers("/login").permitAll()
            .anyRequest().authenticated()
            .and()
            .formLogin();
    }
}
```

#output: Aapke application ki security ko enhance karne ke liye ye framework helpful hai.

---

### 87. **How do you create a custom error page in Spring Boot?**
**Answer:**  
Custom error pages create karne ke liye aapko specific error codes ke liye HTML pages create karne honge.

#### Steps:
1. **Create Custom Error Page:**
   - Create a file named `error.html` in `src/main/resources/templates/`:
```html
<!DOCTYPE html>
<html>
<head>
    <title>Error</title>
</head>
<body>
    <h1>Oops! Something went wrong.</h1>
    <p>Please try again later.</p>
</body>
</html>
```

2. **Create a Controller to Handle Errors:**
```java
@Controller
public class ErrorController implements org.springframework.boot.web.servlet.error.ErrorController {

    @RequestMapping("/error")
    public String handleError() {
        return "error"; // return error.html
    }
}
```

#output: Aapko custom error page dikhega jab koi error occur hoga.

---

### 88. **What is the purpose of `@ConfigurationProperties` in Spring Boot?**
**Answer:**  
`@ConfigurationProperties` annotation ka use external configuration properties ko bind karne ke liye hota hai. Isse aapko complex properties ko manage karne mein madad milti hai.

#### Example:
1. **Define Properties in `application.properties`:**
```properties
app.name=My App
app.version=1.0.0
```

2. **Create a Configuration Class:**
```java
@Component
@ConfigurationProperties(prefix = "app")
public class AppConfig {
    private String name;
    private String version;

    // Getters and Setters
}
```

#output: Aap `AppConfig` class ke properties ko easily access kar sakte ho.

---

### 89. **How do you implement security in a REST API using Spring Boot?**
**Answer:**  
Spring Boot mein REST API ke liye security implement karne ke liye aap **Spring Security** ka use karte ho.

#### Steps:
1. **Add Spring Security Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

2. **Configure Security:**
```java
@EnableWebSecurity
public class SecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .csrf().disable() // CSRF ko disable karna
            .authorizeRequests()
            .antMatchers("/api/public").permitAll() // Public endpoint
            .anyRequest().authenticated() // Authenticated requests
            .and()
            .httpBasic(); // Basic authentication
    }
}
```

#output: Aapke REST API endpoints par security apply ho jayegi.

---

### 90. **What is the difference between `@PathVariable` and `@RequestParam`?**
**Answer:**  
**`@PathVariable`** aur **`@RequestParam`** dono annotations HTTP request parameters ko handle karne ke liye use hote hain, lekin inka use case alag hai.

1. **`@PathVariable`:** 
   - URL ke path se values extract karne ke liye use hota hai.
   - Example: `/api/products/{id}`
   ```java
   @GetMapping("/products/{id}")
   public Product getProductById(@PathVariable Long id) {
       return productService.getProductById(id);
   }
   ```

2. **`@RequestParam`:** 
   - Query parameters se values extract karne ke liye use hota hai.
   - Example: `/api/products?page=1&size=10`
   ```java
   @GetMapping("/products")
   public Page<Product> getAllProducts(@RequestParam int page, @RequestParam int size) {
       return productService.getProducts(page, size);
   }
   ```

#output: Ye dono annotations alag-alag tarike se request parameters ko handle karte hain.

---

### 91. **How do you implement caching in Spring Boot?**
**Answer:**  
Spring Boot mein caching implement karne ke liye aapko **Spring Cache** abstraction ka use karna hota hai.

#### Steps:
1. **Add Caching Dependency:**
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
</dependency>
```

2. **Enable Caching:**
```java
@Configuration
@EnableCaching
public class CacheConfig {
}
```

3. **Use Caching in Service:**
```java
@Service
public class ProductService {

    @Cacheable("products")
    public Product getProductById(Long id) {
        // Expensive operation
        return productRepository.findById(id).orElse(null);
    }
}
```

#output: Aapko caching mechanism milega jisse frequent calls par performance enhance hoti hai.

---

### 92. **What is Spring Boot's `@PostConstruct` annotation?**
**Answer:**  
`@PostConstruct` annotation ka use

 kisi method ko initialize karne ke liye hota hai jab Spring container us bean ko create kar leta hai. Iska istemal aapko bean initialization tasks perform karne ke liye hota hai.

#### Example:
```java
@Component
public class MyBean {

    @PostConstruct
    public void init() {
        // Initialization logic here
        System.out.println("Bean initialized");
    }
}
```

#output: Aapke bean ke creation ke baad initialization logic automatically execute hoga.

---

### 93. **How do you handle exceptions in Spring Boot?**
**Answer:**  
Spring Boot mein exceptions handle karne ke liye aapko **@ControllerAdvice** aur **@ExceptionHandler** annotations ka use karna hota hai.

#### Steps:
1. **Create Global Exception Handler:**
```java
@ControllerAdvice
public class GlobalExceptionHandler {

    @ExceptionHandler(ProductNotFoundException.class)
    public ResponseEntity<String> handleProductNotFound(ProductNotFoundException ex) {
        return ResponseEntity.status(HttpStatus.NOT_FOUND).body(ex.getMessage());
    }
}
```

2. **Throw Exception in Controller:**
```java
@GetMapping("/products/{id}")
public Product getProductById(@PathVariable Long id) {
    return productService.getProductById(id)
        .orElseThrow(() -> new ProductNotFoundException("Product not found"));
}
```

#output: Aapko centralized exception handling mechanism milega.

---

### 94. **What is Spring Boot's `@Scheduled` annotation?**
**Answer:**  
`@Scheduled` annotation ka use aapko periodic tasks execute karne ke liye hota hai, jisse aap specific intervals par methods ko call kar sakte ho.

#### Example:
1. **Enable Scheduling:**
```java
@Configuration
@EnableScheduling
public class SchedulerConfig {
}
```

2. **Create Scheduled Task:**
```java
@Component
public class ScheduledTasks {

    @Scheduled(fixedRate = 5000)
    public void performTask() {
        System.out.println("Task executed every 5 seconds");
    }
}
```

#output: Aapke specified interval par task execute hoga.

---

### 95. **How do you create a custom filter in Spring Boot?**
**Answer:**  
Spring Boot mein custom filter create karne ke liye aapko **Filter** interface implement karna hota hai.

#### Steps:
1. **Create Custom Filter:**
```java
import javax.servlet.Filter;
import javax.servlet.FilterChain;
import javax.servlet.FilterConfig;
import javax.servlet.ServletException;
import javax.servlet.ServletRequest;
import javax.servlet.ServletResponse;
import java.io.IOException;

@Component
public class CustomFilter implements Filter {

    @Override
    public void doFilter(ServletRequest request, ServletResponse response, FilterChain chain)
            throws IOException, ServletException {
        // Pre-processing logic
        System.out.println("Custom filter executed");
        chain.doFilter(request, response); // Proceed to the next filter or resource
    }

    @Override
    public void init(FilterConfig filterConfig) throws ServletException {
    }

    @Override
    public void destroy() {
    }
}
```

#output: Aapke application mein request processing ke beech custom logic execute hoga.

---

### 96. **What is Spring Boot's `@Value` annotation?**
**Answer:**  
`@Value` annotation ka use external properties ko inject karne ke liye hota hai, jaise `application.properties` file se values ko retrieve karne ke liye.

#### Example:
1. **Define Property in `application.properties`:**
```properties
app.name=My Application
```

2. **Inject Property in Class:**
```java
@Component
public class MyComponent {

    @Value("${app.name}")
    private String appName;

    public void printAppName() {
        System.out.println("Application Name: " + appName);
    }
}
```

#output: Aapko external properties se values inject karne ki capability milegi.

---

### 97. **How do you implement a REST client in Spring Boot?**
**Answer:**  
Spring Boot mein REST client implement karne ke liye aap **RestTemplate** ya **WebClient** ka use kar sakte ho.

#### Using RestTemplate:
1. **Add RestTemplate Bean:**
```java
@Bean
public RestTemplate restTemplate() {
    return new RestTemplate();
}
```

2. **Use RestTemplate in Service:**
```java
@Service
public class MyService {

    @Autowired
    private RestTemplate restTemplate;

    public Product getProduct() {
        ResponseEntity<Product> response = restTemplate.getForEntity("http://localhost:8080/api/products/1", Product.class);
        return response.getBody();
    }
}
```

#output: Aap external REST APIs ke sath interact kar sakte ho.

---

### 98. **What is the difference between `@RestController` and `@Controller`?**
**Answer:**  
**`@RestController`** aur **`@Controller`** annotations mein key difference hai ki:

1. **`@RestController`:** 
   - Ye automatically response ko JSON ya XML format mein convert karta hai. Iska istemal RESTful APIs banane ke liye hota hai.
   - Example:
```java
@RestController
@RequestMapping("/api/products")
public class ProductRestController {
    // Methods returning JSON
}
```

2. **`@Controller`:** 
   - Ye view-based applications ke liye use hota hai. Isme response ko view resolver ke through render kiya jata hai.
   - Example:
```java
@Controller
@RequestMapping("/products")
public class ProductController {
    // Methods returning views
}
```

#output: Aapko response format aur use case ke hisab se correct annotation choose karna hoga.

---

### 99. **How do you enable HTTPS in Spring Boot?**
**Answer:**  
Spring Boot application mein HTTPS enable karne ke liye aapko SSL certificate ki zaroorat hoti hai.

#### Steps:
1. **Generate Self-Signed Certificate:**
```bash
keytool -genkeypair -alias myapp -keyalg RSA -keystore myapp.jks -storepass password
```

2. **Configure SSL in `application.properties`:**
```properties
server.port=8443
server.ssl.key-store=classpath:myapp.jks
server.ssl.key-store-password=password
server.ssl.keyStoreType=JKS
```

#output: Aapka application HTTPS par run hoga.

---

### 100. **What are Spring Boot starters?**
**Answer:**  
**Spring Boot starters** pre-configured dependencies hain jo aapko application development mein madad karte hain. Ye specific functionalities ko add karne ke liye hoti hain.

#### Examples:
1. **`spring-boot-starter-web`:** 
   - Web applications ke liye basic dependencies.

2. **`spring-boot-starter-data-jpa`:** 
   - JPA aur Hibernate ke liye dependencies.

3. **`spring-boot-starter-security`:** 
   - Spring Security ko include karne ke liye.

#output: Aap easily functionalities add kar sakte ho without manual configuration.

---



















---
---




