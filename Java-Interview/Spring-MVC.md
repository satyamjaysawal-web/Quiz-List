


Here’s a comprehensive list of interview questions related to **Spring MVC** (Model-View-Controller). These questions cover various concepts, components, and best practices associated with Spring MVC, and can help candidates prepare for interviews focused on this framework.

### Spring MVC Interview Questions

#### Basic Concepts
1. **What is Spring MVC?**
2. **Explain the MVC design pattern.**
3. **What are the advantages of using Spring MVC?**
4. **What are the main components of Spring MVC?**
5. **How does Spring MVC differ from traditional servlet-based applications?**

#### Configuration and Setup
6. **How do you configure a Spring MVC application?**
7. **What is the role of `DispatcherServlet` in Spring MVC?**
8. **What are the different ways to configure Spring MVC?**
9. **How do you define a Spring MVC controller?**
10. **What is the purpose of the `@Controller` annotation?**
11. **How do you configure view resolution in Spring MVC?**

#### Request Handling
12. **What is the purpose of the `@RequestMapping` annotation?**
13. **How can you handle different HTTP methods (GET, POST, etc.) in Spring MVC?**
14. **What is the role of `@GetMapping` and `@PostMapping` annotations?**
15. **How do you access request parameters in a Spring MVC controller?**
16. **How can you pass data from the controller to the view?**
17. **What is the difference between `@ModelAttribute` and `@RequestParam`?**

#### View Layer
18. **What are the different view technologies supported by Spring MVC?**
19. **How do you configure a view resolver in Spring MVC?**
20. **What is the purpose of `InternalResourceViewResolver`?**
21. **How do you return a JSON response from a Spring MVC controller?**
22. **Explain how to use JSP as a view in Spring MVC.**

#### Form Handling
23. **How do you handle form submissions in Spring MVC?**
24. **What is the purpose of the `@Valid` annotation in form validation?**
25. **How can you perform validation on user input in Spring MVC?**
26. **What are `BindingResult` and its role in form handling?**
27. **How can you use Spring's `@InitBinder` annotation?**

#### Exception Handling
28. **How do you handle exceptions in Spring MVC?**
29. **What is the purpose of `@ControllerAdvice`?**
30. **How can you define custom error pages in Spring MVC?**
31. **Explain how to use `@ExceptionHandler` annotation.**

#### Interceptors and Filters
32. **What is the role of interceptors in Spring MVC?**
33. **How do you configure an interceptor in a Spring MVC application?**
34. **What is the difference between a filter and an interceptor in Spring MVC?**

#### Testing
35. **How do you test Spring MVC controllers?**
36. **What tools do you use for testing Spring MVC applications?**
37. **How can you mock requests and responses in unit tests?**

#### Best Practices
38. **What are some best practices for building Spring MVC applications?**
39. **How do you manage application properties in Spring MVC?**
40. **What is the significance of separating concerns in Spring MVC applications?**

#### Miscellaneous
41. **How do you implement internationalization (i18n) in Spring MVC?**
42. **What is the use of Spring Security with Spring MVC?**
43. **How do you implement file uploads in Spring MVC?**
44. **How can you implement pagination and sorting in Spring MVC?**
45. **What are RESTful services, and how does Spring MVC support them?**
46. **How do you handle CORS in Spring MVC applications?**

---

---


Here’s a comprehensive list of terms and concepts related to **Spring MVC**, organized in a clear table format:

| **Spring MVC Term**            | **Description**                                                      |
|--------------------------------|---------------------------------------------------------------------|
| **Spring MVC**                 | A module of the Spring Framework that provides model-view-controller architecture for web applications. |
| **DispatcherServlet**          | The front controller in Spring MVC that routes requests to appropriate handler methods. |
| **Controller**                 | A component that handles user requests and returns the appropriate response. |
| **@Controller**                | Annotation used to indicate that a class serves as a controller in Spring MVC. |
| **@RequestMapping**            | Annotation used to map HTTP requests to handler methods of MVC and REST controllers. |
| **@GetMapping**                | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.GET)`. |
| **@PostMapping**               | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.POST)`. |
| **@PutMapping**                | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.PUT)`. |
| **@DeleteMapping**             | A composed annotation that acts as a shortcut for `@RequestMapping(method = RequestMethod.DELETE)`. |
| **Model**                      | An interface that defines a holder for model attributes, used to pass data to the view. |
| **ModelAndView**               | A holder for both Model and View, used to return data and specify the view to be rendered. |
| **View Resolver**              | A component that resolves logical view names to actual view implementations. |
| **@ResponseBody**              | Annotation used to indicate that the return value of a method should be bound to the web response body. |
| **View**                       | Represents the visual representation of the model (e.g., JSP, Thymeleaf, etc.). |
| **@RequestParam**              | Annotation used to extract query parameters from the URL.           |
| **@PathVariable**              | Annotation used to extract values from the URI path.                |
| **@SessionAttributes**         | Annotation used to indicate that certain model attributes should be stored in the session. |
| **@InitBinder**                | Annotation used to customize the data binding process, often for form validation. |
| **BindingResult**              | An object that holds the results of binding and validation for a particular model attribute. |
| **@ModelAttribute**            | Annotation used to bind request parameters to a model attribute or populate it. |
| **Form Validation**            | The process of validating user input in web forms, typically using JSR-303/JSR-380 (Bean Validation). |
| **@Valid**                     | Annotation to trigger validation on a model attribute.              |
| **@ExceptionHandler**          | Annotation to define a method that handles exceptions thrown by controller methods. |
| **Controller Advice**          | A mechanism for handling global exceptions, binding, and model attributes across all controllers. |
| **@ControllerAdvice**          | Annotation that allows you to define global behavior for controllers. |
| **RESTful Web Services**       | Services that conform to REST architecture, often built using Spring MVC. |
| **ResponseEntity**             | A class that represents the entire HTTP response, including status code, headers, and body. |
| **Content Negotiation**        | Mechanism that allows different representations of resources to be served based on the request (e.g., JSON, XML). |
| **Error Handling**             | Mechanism to handle and display error messages in the application.  |
| **Static Resources**           | Files like CSS, JavaScript, and images that can be served directly to the client. |
| **Interceptors**               | Components that can intercept requests and responses for preprocessing and postprocessing. |
| **@RequestBody**               | Annotation used to bind the HTTP request body to a method parameter, typically for POST requests. |
| **HandlerMapping**             | A component that maps incoming requests to the appropriate handler (controller) methods. |
| **HandlerAdapter**             | An interface that defines the method for handling requests.         |
| **Session Management**         | Mechanism to manage user sessions, typically using cookies or URL rewriting. |
| **@CrossOrigin**               | Annotation to enable Cross-Origin Resource Sharing (CORS) for a specific controller or method. |
| **Thymeleaf**                  | A modern server-side Java template engine for rendering views in Spring MVC applications. |
| **JSP (JavaServer Pages)**     | A technology for building web pages with Java, often used as a view in Spring MVC. |
| **ModelView**                  | An object that encapsulates both the model and the view, allowing a controller to return data and the view to render it. |
| **Redirect Attributes**        | Used to pass flash attributes (temporary data) during redirect scenarios. |
| **Flash Scope**                | A mechanism to store attributes temporarily, available for the next request. |
| **WebApplicationInitializer**   | Interface for configuring the servlet context programmatically, typically used for Java-based configuration. |
| **Error Pages**                | Custom error pages that can be configured for different HTTP error status codes. |
| **Resource Handler**           | A component that handles requests for static resources.            |
| **MVC Configuration**          | Configuration settings for setting up and customizing Spring MVC behavior. |
| **@EnableWebMvc**             | Annotation that enables Spring MVC configuration in a Spring application. |
| **Conversion Service**         | A service that handles the conversion between different types, often used in form binding. |
| **LocaleResolver**             | Interface used to resolve the locale (language and region) for a web request. |
| **LocaleChangeInterceptor**    | An interceptor that allows changing the locale based on a request parameter. |
| **Content Negotiation Strategy** | Strategy for determining the format of the response based on the request. |
| **HATEOAS (Hypermedia as the Engine of Application State)** | A constraint of the REST application architecture that provides information about available actions in responses. |
| **Spring Security Integration** | Integrating Spring Security with Spring MVC to secure web applications. |
| **@SessionScope**              | Annotation that indicates that a bean is scoped to an HTTP session. |

This table provides a comprehensive overview of important terms, annotations, and concepts related to Spring MVC, helping you understand the framework better. If you need further clarification or details on specific topics, feel free to ask!
---

---

Certainly! Below are answers to the Spring MVC interview questions, including code examples and outputs where applicable, written in Hinglish. 

### Spring MVC Interview Questions and Answers

#### 1. What is Spring MVC?
**Spring MVC ek framework hai jo Model-View-Controller design pattern pe based hai. Iska use web applications develop karne ke liye hota hai, jahan business logic ko presentation se alag rakha jata hai.**

#### 2. Explain the MVC design pattern.
**MVC pattern teen parts mein application ko divide karta hai:**

- **Model**: Data aur business logic ko represent karta hai.
- **View**: User interface ko represent karta hai.
- **Controller**: User input ko handle karta hai aur Model aur View ke beech interaction karta hai.

#### 3. What are the advantages of using Spring MVC?
- **Loose Coupling**: Components ek dusre se loosely coupled hote hain.
- **Flexibility**: Multiple view technologies support karta hai.
- **Ease of Testing**: Unit testing asan hota hai.
- **Built-in Validation**: Form validation ke liye support.

#### 4. What are the main components of Spring MVC?
- **DispatcherServlet**: Front controller hota hai jo requests ko process karta hai.
- **Controller**: User input ko handle karta hai.
- **View Resolver**: Response ko render karta hai.
- **Model**: Data ko represent karta hai.

#### 5. How does Spring MVC differ from traditional servlet-based applications?
**Spring MVC mein aapko code ko organize karne ke liye Controller aur View layer ka use karna hota hai, jabki traditional servlet-based application mein ye sab kuch ek servlet mein hota hai, jo complexity ko badha deta hai.**

---

#### 6. How do you configure a Spring MVC application?
**Spring MVC application ko configure karne ke liye `web.xml` aur Spring configuration file ka use hota hai.**

**Example: `web.xml`**

```xml
<web-app>
    <servlet>
        <servlet-name>dispatcher</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
        <load-on-startup>1</load-on-startup>
    </servlet>
    <servlet-mapping>
        <servlet-name>dispatcher</servlet-name>
        <url-pattern>/</url-pattern>
    </servlet-mapping>
</web-app>
```

**Example: `dispatcher-servlet.xml`**

```xml
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                           http://www.springframework.org/schema/beans/spring-beans.xsd">

    <context:component-scan base-package="com.example.controller" />
    <mvc:annotation-driven />
    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
        <property name="prefix" value="/WEB-INF/views/" />
        <property name="suffix" value=".jsp" />
    </bean>
</beans>
```

#### 7. What is the role of `DispatcherServlet` in Spring MVC?
**`DispatcherServlet` front controller hota hai jo incoming requests ko handle karta hai. Ye request ko controller tak pahunchata hai aur response ko view layer ko return karta hai.**

#### 8. What are the different ways to configure Spring MVC?
- **XML Configuration**: Jaise `dispatcher-servlet.xml`.
- **Java Configuration**: `@Configuration` aur `@EnableWebMvc` annotations ka use.
- **Annotation-based Configuration**: Annotations ke through controllers aur views ko configure karna.

**Example: Java Configuration**

```java
@Configuration
@EnableWebMvc
@ComponentScan("com.example")
public class WebConfig implements WebMvcConfigurer {
    // Configuration methods
}
```

#### 9. How do you define a Spring MVC controller?
**Controller ko define karne ke liye `@Controller` annotation ka use hota hai.**

**Example:**

```java
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;

@Controller
@RequestMapping("/home")
public class HomeController {

    @GetMapping
    public String home() {
        return "home"; // returns home.jsp
    }
}
```

#### 10. What is the purpose of the `@Controller` annotation?
**`@Controller` annotation batata hai ki yeh class Spring MVC ke Controller component ke roop mein kaam karegi. Isse Spring is class ke methods ko request handling ke liye identify kar sakta hai.**

#### 11. How do you configure view resolution in Spring MVC?
**View resolution ke liye `InternalResourceViewResolver` ka use kiya jata hai jo JSP pages ko locate karne mein madad karta hai.**

**Example:**

```xml
<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
    <property name="prefix" value="/WEB-INF/views/" />
    <property name="suffix" value=".jsp" />
</bean>
```

#### 12. What is the purpose of the `@RequestMapping` annotation?
**`@RequestMapping` annotation ko HTTP requests ko specific controller methods ke saath map karne ke liye use kiya jata hai.**

**Example:**

```java
@RequestMapping("/welcome")
public String welcome() {
    return "welcome"; // returns welcome.jsp
}
```

#### 13. How can you handle different HTTP methods (GET, POST, etc.) in Spring MVC?
**Aap `@RequestMapping` ke saath HTTP method specify kar sakte hain.**

**Example:**

```java
@RequestMapping(value = "/submit", method = RequestMethod.POST)
public String submitForm(@ModelAttribute("user") User user) {
    // handle form submission
    return "success"; // returns success.jsp
}
```

#### 14. What is the role of `@GetMapping` and `@PostMapping` annotations?
**`@GetMapping` aur `@PostMapping` specific HTTP methods ko handle karne ke liye shorthand annotations hain.**

**Example:**

```java
@GetMapping("/users")
public List<User> getUsers() {
    // return user list
}

@PostMapping("/users")
public String addUser(@ModelAttribute User user) {
    // add user
    return "redirect:/users";
}
```

#### 15. How do you access request parameters in a Spring MVC controller?
**Aap `@RequestParam` annotation ka use karke request parameters ko access kar sakte hain.**

**Example:**

```java
@GetMapping("/greet")
public String greet(@RequestParam("name") String name, Model model) {
    model.addAttribute("message", "Hello " + name);
    return "greet"; // returns greet.jsp
}
```

#### 16. How can you pass data from the controller to the view?
**Data ko model object ke through view tak pass kiya jata hai.**

**Example:**

```java
@GetMapping("/welcome")
public String welcome(Model model) {
    model.addAttribute("message", "Welcome to Spring MVC!");
    return "welcome"; // returns welcome.jsp
}
```

#### 17. What is the difference between `@ModelAttribute` and `@RequestParam`?
- **`@RequestParam`**: Specific request parameters ko bind karta hai.
- **`@ModelAttribute`**: Entire object ko bind karta hai jo form ke fields se aata hai.

**Example:**

```java
// @RequestParam example
@GetMapping("/user")
public String getUser(@RequestParam("id") Long id) {
    // fetch user by id
}

// @ModelAttribute example
@PostMapping("/user")
public String addUser(@ModelAttribute User user) {
    // save user
}
```

---

#### 18. What are the different view technologies supported by Spring MVC?
**Spring MVC kai view technologies support karta hai, jaise:**
- **JSP**
- **Thymeleaf**
- **Freemarker**
- **Velocity**
- **PDF Views**

#### 19. How do you configure a view resolver in Spring MVC?
**View resolver ko `InternalResourceViewResolver` ke through configure kiya jata hai.**

**Example:**

```xml
<bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
    <property name="prefix" value="/WEB-INF/views/" />
    <property name="suffix" value=".jsp" />
</bean>
```

#### 20. What is the purpose of `InternalResourceViewResolver`?
**`InternalResourceViewResolver` JSP files ko locate karne ke liye use hota hai, jisse aap JSP pages ko easily return kar sakte hain.**

#### 21. How do you return a JSON response from a Spring MVC controller?
**Aap `@ResponseBody` annotation ka use karke JSON response return kar sakte hain.**

**Example:**

```java
@GetMapping("/user")
@ResponseBody
public User getUser() {
    return new User("John", "Doe"); // returns JSON
}
```

#### 22. Explain how to use JSP as a view in Spring MVC.
**Aap JSP ko view ke roop mein use karne ke liye view resolver configure karte hain.**

**Example:**

1. **View Resolver Configuration**:
   ```xml
   <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
       <property name="prefix" value="/WEB-INF/views/" />
       <property name="suffix" value=".jsp" />
   </

bean>
   ```

2. **Controller**:
   ```java
   @GetMapping("/home")
   public String home() {
       return "home"; // home.jsp will be resolved
   }
   ```

#### 23. How do you handle form submissions in Spring MVC?
**Form submissions ko handle karne ke liye, aap `@ModelAttribute` aur `@PostMapping` ka use karte hain.**

**Example:**

```java
@PostMapping("/submitForm")
public String submitForm(@ModelAttribute User user) {
    // Save user details
    return "result"; // returns result.jsp
}
```

#### 24. What is the purpose of the `@Valid` annotation in form validation?
**`@Valid` annotation ka use form data ki validation ke liye hota hai. Iska use `BindingResult` ke sath hota hai.**

**Example:**

```java
@PostMapping("/register")
public String register(@Valid @ModelAttribute User user, BindingResult result) {
    if (result.hasErrors()) {
        return "register"; // return to the registration page
    }
    // save user
    return "success"; // return success page
}
```

#### 25. How can you perform validation on user input in Spring MVC?
**Spring MVC validation ke liye `@Valid` annotation aur `BindingResult` ka use karta hai. Aapko validation rules define karne ke liye Java Bean Validation (JSR-303) ka use karna hota hai.**

**Example:**

```java
public class User {
    @NotNull
    private String username;

    @Email
    private String email;

    // getters and setters
}
```

#### 26. What are `BindingResult` and its role in form handling?
**`BindingResult` form submission ke dauran errors ko capture karne ke liye use hota hai. Isse aapko pata chalta hai ki user input valid hai ya nahi.**

**Example:**

```java
@PostMapping("/user")
public String submit(@Valid @ModelAttribute User user, BindingResult result) {
    if (result.hasErrors()) {
        return "form"; // return to the form page
    }
    return "success"; // process success
}
```

#### 27. How can you use Spring's `@InitBinder` annotation?
**`@InitBinder` annotation ka use input data ko customize karne ke liye kiya jata hai, jaise ki special formatting ya custom property editors set karne ke liye.**

**Example:**

```java
@InitBinder
public void initBinder(WebDataBinder binder) {
    binder.registerCustomEditor(Date.class, new CustomDateEditor(new SimpleDateFormat("yyyy-MM-dd"), true));
}
```

#### 28. How do you handle exceptions in Spring MVC?
**Spring MVC mein exceptions ko handle karne ke liye `@ExceptionHandler` ya `@ControllerAdvice` ka use hota hai.**

**Example:**

```java
@ExceptionHandler(Exception.class)
public String handleException(Exception e) {
    return "error"; // returns error.jsp
}
```

#### 29. What is the purpose of `@ControllerAdvice`?
**`@ControllerAdvice` application-wide exception handling ke liye use hota hai. Isse aap globally exceptions ko handle kar sakte hain.**

**Example:**

```java
@ControllerAdvice
public class GlobalExceptionHandler {
    @ExceptionHandler(Exception.class)
    public String handleAllExceptions(Exception ex) {
        return "error"; // returns error.jsp
    }
}
```

#### 30. How can you define custom error pages in Spring MVC?
**Aap custom error pages define karne ke liye `web.xml` mein error pages ko specify kar sakte hain.**

**Example:**

```xml
<error-page>
    <error-code>404</error-code>
    <location>/WEB-INF/views/error404.jsp</location>
</error-page>
<error-page>
    <error-code>500</error-code>
    <location>/WEB-INF/views/error500.jsp</location>
</error-page>
```

---

#### 31. What is the role of interceptors in Spring MVC?
**Interceptors ka use request ko process karne se pehle aur baad mein kuch actions perform karne ke liye hota hai, jaise logging ya authentication.**

#### 32. How do you configure an interceptor in a Spring MVC application?
**Interceptor ko configure karne ke liye `WebMvcConfigurer` interface implement karte hain.**

**Example:**

```java
@Configuration
public class WebConfig implements WebMvcConfigurer {
    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        registry.addInterceptor(new MyInterceptor());
    }
}
```

#### 33. What is the difference between a filter and an interceptor in Spring MVC?
- **Filter**: Servlet ke lifecycle mein request ko modify kar sakta hai, par controller ko nahi jaanta.
- **Interceptor**: Spring MVC lifecycle mein request ko modify kar sakta hai aur controller ke specific methods ko intercept kar sakta hai.

#### 34. How do you test Spring MVC controllers?
**Spring MVC controllers ko test karne ke liye `MockMvc` ka use hota hai.**

**Example:**

```java
@RunWith(SpringJUnit4ClassRunner.class)
@WebAppConfiguration
@ContextConfiguration(classes = WebConfig.class)
public class HomeControllerTest {
    @Autowired
    private WebApplicationContext wac;
    
    private MockMvc mockMvc;

    @Before
    public void setup() {
        mockMvc = MockMvcBuilders.webAppContextSetup(wac).build();
    }

    @Test
    public void testHome() throws Exception {
        mockMvc.perform(get("/home"))
               .andExpect(status().isOk())
               .andExpect(view().name("home"));
    }
}
```

#### 35. What tools do you use for testing Spring MVC applications?
- **JUnit**: Unit testing ke liye.
- **Mockito**: Mock objects create karne ke liye.
- **Spring Test**: Spring context ke sath tests likhne ke liye.

---

#### 36. What are some best practices for building Spring MVC applications?
- **Layered Architecture**: Business logic aur presentation ko separate rakhein.
- **Use DTOs**: Data transfer objects ka use karein.
- **Proper Validation**: User input ki validation zaroori hai.
- **Exception Handling**: Global exception handling implement karein.

#### 37. How do you manage application properties in Spring MVC?
**Application properties ko `application.properties` file mein define kiya jata hai aur `@Value` annotation ke through access kiya jata hai.**

**Example:**

```properties
app.title=My Spring MVC Application
```

**Accessing in Controller:**

```java
@Value("${app.title}")
private String appTitle;
```

#### 38. What is the significance of separating concerns in Spring MVC applications?
**Separation of concerns se application ko modular aur maintainable banaya ja sakta hai. Ye testing aur debugging ko asan banata hai.**

#### 39. How do you implement internationalization (i18n) in Spring MVC?
**Internationalization ke liye `MessageSource` aur `LocaleResolver` ka use hota hai.**

**Example:**

```java
@Bean
public MessageSource messageSource() {
    ResourceBundleMessageSource messageSource = new ResourceBundleMessageSource();
    messageSource.setBasename("messages");
    return messageSource;
}
```

#### 40. What is the use of Spring Security with Spring MVC?
**Spring Security ko application ke security needs ke liye use kiya jata hai, jaise authentication aur authorization.**

#### 41. How do you implement file uploads in Spring MVC?
**File uploads ke liye `MultipartFile` ka use hota hai.**

**Example:**

```java
@PostMapping("/upload")
public String handleFileUpload(@RequestParam("file") MultipartFile file) {
    // handle file upload
    return "uploadSuccess"; // returns success page
}
```

#### 42. How can you implement pagination and sorting in Spring MVC?
**Pagination aur sorting ke liye Spring Data JPA ka use hota hai.**

**Example:**

```java
@GetMapping("/users")
public Page<User> listUsers(Pageable pageable) {
    return userService.findAll(pageable);
}
```

#### 43. What are RESTful services, and how does Spring MVC support them?
**RESTful services web services hain jo HTTP protocol ka use karte hain. Spring MVC `@RestController` annotation ke through REST APIs ko support karta hai.**

**Example:**

```java
@RestController
@RequestMapping("/api/users")
public class UserController {
    
    @GetMapping
    public List<User> getAllUsers() {
        return userService.findAll();
    }
}
```

#### 44. How do you handle CORS in Spring MVC applications?
**CORS ko handle karne ke liye `@CrossOrigin` annotation ka use hota hai.**

**Example:**

```java
@CrossOrigin(origins = "http://localhost:3000")
@GetMapping("/users")
public List<User> getUsers() {
    return userService.findAll();
}
```

---




---
---


