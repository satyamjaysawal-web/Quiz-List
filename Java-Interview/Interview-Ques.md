

## List of **Core Java interview questions** 

### 1. **Basic Java Concepts**
- What are the key features of Java?
- Explain the concept of platform independence in Java.
- What is the difference between JDK, JRE, and JVM?
- Explain the use of the `main()` method in Java.
- What is the difference between `==` and `.equals()` in Java?
- What is the default value of local variables in Java?
- What are wrapper classes in Java?
- What is the difference between static and non-static methods?
- What is the significance of the `final` keyword in Java?
- How does Java handle memory management?

### 2. **Object-Oriented Programming (OOP)**
- What is Object-Oriented Programming? How does Java support OOP?
- What are the main principles of OOP (Inheritance, Polymorphism, Abstraction, Encapsulation)?
- What is the difference between an interface and an abstract class?
- Can you provide an example of multiple inheritance in Java?
- How does method overloading differ from method overriding?
- What is the use of the `super` and `this` keyword in Java?
- What is the difference between a constructor and a method?
- Can a constructor be overloaded?
- Explain the use of the `instanceof` operator.
- What is the difference between IS-A and HAS-A relationships in OOP?

### 3. **String Handling**
- What is the difference between `String`, `StringBuilder`, and `StringBuffer`?
- Why are strings immutable in Java?
- How does the `intern()` method work in Java's String class?
- What is the difference between `concat()` and the `+` operator for string concatenation?
- Explain the `substring()` method and its performance considerations.

### 4. **Exception Handling**
- What is exception handling in Java?
- What is the difference between `checked` and `unchecked` exceptions?
- How does the `try-catch` block work? Can you have multiple `catch` blocks?
- What is the purpose of the `finally` block?
- Explain the concept of `throw` and `throws` in exception handling.
- What is the `Exception` class hierarchy in Java?
- How do you create custom exceptions in Java?
- What is the difference between `Error` and `Exception` in Java?

### 5. **Multithreading and Concurrency**
- What is a thread in Java, and how is it different from a process?
- How do you create a thread in Java? Explain `Runnable` and `Thread` class.
- What are the different states of a thread?
- What is the difference between `start()` and `run()` methods?
- What is thread synchronization? Explain `synchronized` keyword.
- What are deadlocks, and how do you avoid them in Java?
- Explain the concept of `wait()` and `notify()` in Java.
- What is the difference between a `Thread` and an `ExecutorService`?
- What are thread pools, and why are they used?
- What is a `volatile` variable in Java, and how does it differ from `synchronized`?

### 6. **Collections Framework**
- What is the Java Collections Framework?
- Explain the differences between `ArrayList` and `LinkedList`.
- What is the difference between `HashMap` and `Hashtable`?
- How does `HashMap` work internally?
- What is the difference between `Set` and `List`?
- What is the difference between `TreeSet`, `HashSet`, and `LinkedHashSet`?
- How does a `HashSet` handle duplicates?
- Explain the use of `Comparator` and `Comparable`.
- What is a `Queue`, and how does it differ from a `Stack`?
- What is the difference between `Iterator` and `ListIterator`?

### 7. **Inner Classes**
- What are inner classes in Java? Explain its types (static, local, anonymous).
- What is the purpose of anonymous inner classes?
- What is the difference between a nested static class and a regular inner class?
- Can an inner class access the outer class’s variables?

### 8. **Java I/O**
- What are the main classes involved in Java I/O?
- Explain the difference between `InputStream` and `Reader`.
- What is the difference between `FileInputStream` and `BufferedInputStream`?
- How does `Serializable` work in Java?
- What is the purpose of the `transient` keyword in Java?
- What is the difference between `FileReader` and `BufferedReader`?

### 9. **JVM Internals**
- What are the main components of JVM architecture?
- What is the role of ClassLoader in Java?
- How does the garbage collection mechanism work in Java?
- What is the difference between heap and stack memory?
- Explain the difference between Minor GC and Major GC.
- What is the purpose of the `Permanent Generation` (PermGen) space?
- What are memory leaks in Java, and how can they be avoided?

### 10. **Java 8 Features (and beyond)**
- What are the key features introduced in Java 8?
- Explain the concept of Lambda expressions and provide an example.
- What are functional interfaces in Java?
- Explain the `Stream` API and its advantages.
- What is the purpose of the `Optional` class in Java?
- What is the difference between `map()` and `flatMap()` in Streams?
- What are `default` and `static` methods in interfaces?
- How do `forEach()`, `filter()`, and `collect()` methods work in streams?
- What is a method reference in Java?

### 11. **Java Memory Model and Performance**
- What is the Java Memory Model (JMM)?
- How does Java manage memory allocation and deallocation?
- What is a memory leak, and how can you detect and avoid it in Java?
- What are soft references, weak references, and phantom references?
- What is the `finalize()` method in Java?
- Explain the purpose of garbage collection tuning and common GC algorithms like G1, CMS.
- How would you optimize performance in a Java application?

### 12. **Serialization**
- What is serialization in Java?
- How do you make an object serializable in Java?
- What is the purpose of the `serialVersionUID`?
- What is the transient keyword and how is it used in serialization?

### 13. **Java Design Patterns**
- What are design patterns?
- Explain the Singleton design pattern. How do you implement it?
- What is the Factory design pattern in Java?
- What is the difference between Factory and Abstract Factory design patterns?
- Explain the Observer design pattern.
- What is the Builder pattern and when would you use it?
- What is the Adapter design pattern?

---
---

Here’s the list of 30 tricky Core Java interview questions translated into Hinglish, along with their definitions and examples with comments.

### Tricky Core Java Interview Questions in Hinglish

---

1. **What is the Diamond Problem in Java?**
   - **Definition:** Diamond Problem tab hota hai jab ek class do classes se inherit karti hai jinke methods same signature ke hote hain. 
   - **Example:**
     ```java
     interface A {
         void display();
     }

     interface B {
         void display();
     }

     class C implements A, B {
         // Yahan display() method ko override karna padega
         public void display() {
             System.out.println("Display from Class C");
         }
     }
     ```

2. **Can you override a private or static method in Java?**
   - **Definition:** Nahi, aap private method ko override nahi kar sakte kyunki wo subclass ko visible nahi hote. Static methods ko hide kiya ja sakta hai lekin unhe override nahi kiya ja sakta.
   - **Example:**
     ```java
     class Parent {
         private void show() {
             System.out.println("Parent's show");
         }
     }

     class Child extends Parent {
         // Ye method override nahi ho sakta
         void show() {
             System.out.println("Child's show");
         }
     }
     ```

3. **What will happen if you try to call a method on a null object reference?**
   - **Definition:** Agar aap null object reference par method call karne ki koshish karte hain, toh `NullPointerException` aayega.
   - **Example:**
     ```java
     String str = null;
     // Ye line exception throw karegi
     System.out.println(str.length()); // NullPointerException
     ```

4. **What is the output of the following code snippet?**
   ```java
   String s1 = new String("abc");
   String s2 = new String("abc");
   System.out.println(s1 == s2);
   ```
   - **Definition:** `==` operator reference equality check karta hai.
   - **Output:** 
     ```
     false // kyunki s1 aur s2 alag objects hain
     ```

5. **What is the difference between String, StringBuilder, and StringBuffer?**
   - **Definition:** `String` immutable hota hai, jabki `StringBuilder` aur `StringBuffer` mutable hote hain. `StringBuffer` synchronized hai (thread-safe), jabki `StringBuilder` nahi hai.
   - **Example:**
     ```java
     String str = "Hello"; // Immutable
     StringBuilder sb = new StringBuilder("Hello"); // Mutable
     StringBuffer sbf = new StringBuffer("Hello"); // Thread-safe
     ```

6. **Can you use this keyword in a static context?**
   - **Definition:** Nahi, aap static methods mein `this` keyword ka use nahi kar sakte kyunki `this` current object ko refer karta hai.
   - **Example:**
     ```java
     class MyClass {
         static void myMethod() {
             // Ye line error throw karegi
             System.out.println(this); // Cannot use 'this' in a static context
         }
     }
     ```

7. **What is the purpose of the transient keyword?**
   - **Definition:** `transient` keyword ka use yeh batane ke liye hota hai ki variable ko serialization ke dauran ignore karna hai.
   - **Example:**
     ```java
     class MyClass implements Serializable {
         int a;
         transient int b; // Ye variable serialize nahi hoga
     }
     ```

8. **What is the difference between == and .equals() when comparing two String objects?**
   - **Definition:** `==` reference equality check karta hai, jabki `.equals()` value equality check karta hai.
   - **Example:**
     ```java
     String s1 = new String("Java");
     String s2 = new String("Java");
     System.out.println(s1 == s2); // false
     System.out.println(s1.equals(s2)); // true
     ```

9. **What is method overloading, and how is it different from method overriding?**
   - **Definition:** Method overloading mein same method ka naam different parameters ke saath define kiya jaata hai, jabki method overriding mein subclass parent class ka method redefine karta hai.
   - **Example:**
     ```java
     class MyClass {
         void display(int a) { // Method Overloading
             System.out.println("Integer: " + a);
         }

         void display(String b) { // Method Overloading
             System.out.println("String: " + b);
         }
     }
     ```

10. **What will happen if you call the finalize() method in Java?**
    - **Definition:** `finalize()` method garbage collector dwara call hota hai jab object ko reclaim kiya ja raha hota hai, lekin yeh guaranteed nahi hai ki yeh hamesha call hoga.
    - **Example:**
      ```java
      class MyClass {
          protected void finalize() {
              System.out.println("Finalize method called");
          }
      }
      ```

11. **What are the main advantages of using interfaces over abstract classes?**
    - **Definition:** Interfaces multiple inheritance allow karte hain, default aur static methods rakh sakte hain, aur loose coupling achieve karne mein madad karte hain.
    - **Example:**
      ```java
      interface Animal {
          void eat(); // abstract method
      }

      class Dog implements Animal {
          public void eat() {
              System.out.println("Dog is eating");
          }
      }
      ```

12. **Why does Java not support multiple inheritance with classes?**
    - **Definition:** Java multiple inheritance ko avoid karta hai taaki ambiguity aur complexity na ho, jo Diamond Problem ka karan ban sakta hai.
    - **Example:** N/A (Conceptual)

13. **What is the significance of the volatile keyword in Java?**
    - **Definition:** `volatile` keyword yeh ensure karta hai ki variable ka value different threads ke liye visible rahega.
    - **Example:**
      ```java
      class MyClass {
          volatile int counter = 0; // Multiple threads is variable ko access kar sakte hain
      }
      ```

14. **Can you create a constructor for an interface in Java?**
    - **Definition:** Nahi, interfaces mein constructors nahi hote kyunki unhe instantiate nahi kiya ja sakta.
    - **Example:** N/A (Conceptual)

15. **What will happen if you try to modify a string object?**
    - **Definition:** `String` immutable hai, isliye koi bhi modification ek naya `String` object create karega.
    - **Example:**
      ```java
      String s = "Hello";
      s = s + " World"; // Naya object create hoga
      ```

16. **What is the difference between shallow copy and deep copy?**
    - **Definition:** Shallow copy sirf reference copy karta hai, jabki deep copy naye objects create karta hai aur original object ke saare fields ko copy karta hai.
    - **Example:**
      ```java
      class MyClass {
          int[] arr = {1, 2, 3};
      }

      MyClass obj1 = new MyClass();
      MyClass obj2 = obj1; // Shallow copy

      MyClass obj3 = new MyClass();
      obj3.arr = obj1.arr.clone(); // Deep copy
      ```

17. **What is the purpose of the super keyword?**
    - **Definition:** `super` keyword parent class ko refer karta hai aur parent class ke methods aur constructors ko access karne ke liye use hota hai.
    - **Example:**
      ```java
      class Parent {
          void display() {
              System.out.println("Parent class");
          }
      }

      class Child extends Parent {
          void display() {
              super.display(); // Parent class ka method call karna
              System.out.println("Child class");
          }
      }
      ```

18. **What will be the output of the following code?**
    ```java
    int x = 0;
    System.out.println(x++);
    System.out.println(++x);
    ```
    - **Definition:** `x++` mein value print hoti hai aur fir increment hota hai, jabki `++x` mein pehle increment hota hai aur fir print hota hai.
    - **Output:**
      ```
      0
      2
      ```

19. **Why are Java arrays covariant?**
    - **Definition:** Java arrays covariant hote hain, yaani aap subclass ka array superclass ke array ko assign kar sakte hain, lekin isse runtime mein `ArrayStoreException` aa sakta hai agar incompatible types store karne ki koshish ki jaaye.
    - **Example:**
      ```java
      Object[] objArray = new String[10]; // Covariant
      objArray[0] = new Object(); // ArrayStoreException
      ```



20. **What is an anonymous inner class, and when would you use it?**
    - **Definition:** Anonymous inner class bina naam ki class hoti hai jo ek statement mein define aur instantiate ki jaati hai. Ye aksar event handling ya interface implementation ke liye use hoti hai.
    - **Example:**
      ```java
      class MyClass {
          void createAnonymousClass() {
              new Runnable() {
                  public void run() {
                      System.out.println("Running in anonymous inner class");
                  }
              }.run(); // Ye call method ko invoke karega
          }
      }
      ```

---

21. **What happens if you remove the `super()` call in a constructor?**
    - **Definition:** Agar aap parent class ke constructor ko call nahi karte hain, toh Java compiler automatically super() ko pehle line mein add kar deta hai. Lekin, agar parent class ka constructor parameterized hai aur aap super() ko call nahi karte, toh compilation error aayega.
    - **Example:**
      ```java
      class Parent {
          Parent(int a) {
              System.out.println("Parent class constructor");
          }
      }

      class Child extends Parent {
          Child() {
              // super(); ye automatically add hota hai
              System.out.println("Child class constructor");
          }
      }
      ```

22. **What is the purpose of the `finalize()` method?**
    - **Definition:** `finalize()` method ko garbage collector call karta hai jab object ko destroy karne wala hota hai, jisse aap resource cleanup kar sakte hain.
    - **Example:**
      ```java
      class MyClass {
          protected void finalize() {
              System.out.println("Finalize method called");
          }
      }
      ```

23. **What is the difference between checked and unchecked exceptions?**
    - **Definition:** Checked exceptions wo hote hain jo compile-time par check hote hain, jabki unchecked exceptions runtime par occur hote hain.
    - **Example:**
      ```java
      // Checked Exception
      try {
          throw new IOException("Checked Exception");
      } catch (IOException e) {
          System.out.println(e.getMessage());
      }

      // Unchecked Exception
      try {
          int a = 5 / 0; // ArithmeticException
      } catch (ArithmeticException e) {
          System.out.println(e.getMessage());
      }
      ```

24. **What is the difference between `StringBuilder` and `StringBuffer`?**
    - **Definition:** `StringBuilder` non-synchronized hai aur fast hai, jabki `StringBuffer` synchronized hai aur thread-safe hai.
    - **Example:**
      ```java
      StringBuilder sb = new StringBuilder("Hello");
      sb.append(" World");
      System.out.println(sb); // Output: Hello World

      StringBuffer sbb = new StringBuffer("Hello");
      sbb.append(" World");
      System.out.println(sbb); // Output: Hello World
      ```

25. **What is the difference between an interface and an abstract class?**
    - **Definition:** Interface sirf abstract methods aur constants define karte hain, jabki abstract class mein concrete methods bhi ho sakte hain. Ek class sirf ek abstract class ko extend kar sakta hai, lekin multiple interfaces ko implement kar sakta hai.
    - **Example:**
      ```java
      interface Animal {
          void sound(); // abstract method
      }

      abstract class Bird {
          abstract void fly(); // abstract method

          void eat() { // concrete method
              System.out.println("Bird is eating");
          }
      }
      ```

26. **What is method overriding, and how is it different from method hiding?**
    - **Definition:** Method overriding tab hota hai jab subclass parent class ke method ko redefine karta hai. Method hiding tab hota hai jab static methods ko subclass mein same naam se define kiya jata hai.
    - **Example:**
      ```java
      class Parent {
          void display() {
              System.out.println("Parent class display");
          }
      }

      class Child extends Parent {
          @Override
          void display() { // Method Overriding
              System.out.println("Child class display");
          }
      }

      class Test {
          static void show() {
              System.out.println("Static method in Parent");
          }
      }

      class TestChild extends Test {
          static void show() { // Method Hiding
              System.out.println("Static method in Child");
          }
      }
      ```

27. **Can you access static methods and variables using an object reference?**
    - **Definition:** Haan, aap static methods aur variables ko object reference ke through access kar sakte hain, lekin ye best practice nahi hai. Static members ko class name ke through access karna chahiye.
    - **Example:**
      ```java
      class MyClass {
          static int value = 10;

          static void display() {
              System.out.println("Static method");
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass();
              System.out.println(obj.value); // Possible but not recommended
              obj.display(); // Possible but not recommended
          }
      }
      ```

28. **What will happen if you don't override `equals()` method in a class?**
    - **Definition:** Agar aap `equals()` method ko override nahi karte hain, toh default implementation `Object` class se use hoti hai, jo reference equality check karti hai.
    - **Example:**
      ```java
      class MyClass {
          int value;

          MyClass(int value) {
              this.value = value;
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj1 = new MyClass(10);
              MyClass obj2 = new MyClass(10);
              System.out.println(obj1.equals(obj2)); // false, kyunki reference check hoga
          }
      }
      ```

29. **What is the purpose of the `instanceof` operator?**
    - **Definition:** `instanceof` operator yeh check karta hai ki kya ek object kisi specific class ya interface ka instance hai ya nahi.
    - **Example:**
      ```java
      class Animal {}

      class Dog extends Animal {}

      public class Test {
          public static void main(String[] args) {
              Dog dog = new Dog();
              System.out.println(dog instanceof Animal); // true
              System.out.println(dog instanceof Dog); // true
              System.out.println(dog instanceof Object); // true
          }
      }
      ```

30. **What is a `HashMap`, and how does it work?**
    - **Definition:** `HashMap` key-value pairs store karta hai aur internally hash table use karta hai. Ye null keys aur null values allow karta hai, lekin order maintain nahi karta.
    - **Example:**
      ```java
      import java.util.HashMap;

      public class Test {
          public static void main(String[] args) {
              HashMap<String, Integer> map = new HashMap<>();
              map.put("A", 1);
              map.put("B", 2);
              map.put("C", 3);
              System.out.println(map.get("B")); // Output: 2
              System.out.println(map); // Output: {A=1, B=2, C=3} (Order not guaranteed)
          }
      }
      ```

---
Certainly! Here are more tricky Core Java interview questions in Hinglish, along with their definitions and examples.

---

### Additional Tricky Java Interview Questions

31. **What is the diamond problem in Java?**
    - **Definition:** Diamond problem tab hota hai jab ek class do interfaces se same method inherit karte hain, aur compiler nahi jaan pata ki kaunsa method use kare. Java mein ye problem interfaces ke saath hota hai, lekin isko resolve karne ke liye method overriding ka use hota hai.
    - **Example:**
      ```java
      interface A {
          void show();
      }

      interface B extends A {
          default void show() {
              System.out.println("Show from B");
          }
      }

      interface C extends A {
          default void show() {
              System.out.println("Show from C");
          }
      }

      class D implements B, C {
          @Override
          public void show() {
              B.super.show(); // Ya C.super.show() ka use karke ambiguity resolve kar sakte hain
          }
      }
      ```

32. **What will happen if you attempt to access a static variable from a non-static context?**
    - **Definition:** Aap static variable ko non-static context se access kar sakte hain, lekin ye best practice nahi hai, kyunki static variables class-level par belong karte hain.
    - **Example:**
      ```java
      class MyClass {
          static int value = 20;

          void display() {
              System.out.println(value); // Possible, but not recommended
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass();
              obj.display(); // Output: 20
          }
      }
      ```

33. **What is the difference between `final`, `finally`, and `finalize()`?**
    - **Definition:** 
      - `final` keyword ko variables, methods, aur classes ko modify nahi karne ke liye use kiya jata hai.
      - `finally` block exception handling mein cleanup code ke liye use hota hai, jo hamesha execute hota hai chahe exception aaye ya nahi.
      - `finalize()` method garbage collector dwara call kiya jata hai object ko destroy karne se pehle.
    - **Example:**
      ```java
      class MyClass {
          final int x = 10; // final variable

          void display() {
              System.out.println(x);
          }

          protected void finalize() { // finalize method
              System.out.println("Finalize called");
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass();
              obj.display();
              obj = null; // Nullifying reference
              System.gc(); // Suggesting garbage collection
          }
      }
      ```

34. **Can a class implement multiple interfaces with the same method signature?**
    - **Definition:** Haan, ek class multiple interfaces ko implement kar sakti hai jo same method signature rakhte hain. Lekin class ko us method ko override karna padega.
    - **Example:**
      ```java
      interface X {
          void display();
      }

      interface Y {
          void display();
      }

      class Z implements X, Y {
          @Override
          public void display() {
              System.out.println("Display method from Z");
          }
      }
      ```

35. **What is a transient variable?**
    - **Definition:** Transient variable ko serialization ke dauran ignore kiya jata hai. Agar variable transient hai, toh uska state serialization ke samay save nahi hota.
    - **Example:**
      ```java
      import java.io.*;

      class MyClass implements Serializable {
          int x;
          transient int y; // transient variable

          MyClass(int x, int y) {
              this.x = x;
              this.y = y;
          }
      }

      public class Test {
          public static void main(String[] args) throws IOException, ClassNotFoundException {
              MyClass obj = new MyClass(10, 20);
              FileOutputStream fos = new FileOutputStream("file.txt");
              ObjectOutputStream oos = new ObjectOutputStream(fos);
              oos.writeObject(obj);

              FileInputStream fis = new FileInputStream("file.txt");
              ObjectInputStream ois = new ObjectInputStream(fis);
              MyClass obj2 = (MyClass) ois.readObject();
              System.out.println("x: " + obj2.x + ", y: " + obj2.y); // y will be 0
          }
      }
      ```

36. **What will happen if you try to modify an immutable object?**
    - **Definition:** Agar aap immutable object (jaise `String`) ko modify karne ki koshish karte hain, toh ek naya object create hota hai aur purana object unchanged rehta hai.
    - **Example:**
      ```java
      public class Test {
          public static void main(String[] args) {
              String str = "Hello";
              str.concat(" World"); // Attempt to modify
              System.out.println(str); // Output: Hello (unchanged)
              str = str.concat(" World"); // New object creation
              System.out.println(str); // Output: Hello World
          }
      }
      ```

37. **What is the difference between `ArrayList` and `Vector`?**
    - **Definition:** `ArrayList` non-synchronized hai aur faster hai, jabki `Vector` synchronized hai aur thread-safe hai. `ArrayList` ko dynamically grow karne ke liye array use karta hai, jabki `Vector` apne size ko double karta hai jab capacity exceed hoti hai.
    - **Example:**
      ```java
      import java.util.*;

      public class Test {
          public static void main(String[] args) {
              ArrayList<Integer> arrayList = new ArrayList<>();
              arrayList.add(1);
              arrayList.add(2);

              Vector<Integer> vector = new Vector<>();
              vector.add(1);
              vector.add(2);

              System.out.println("ArrayList: " + arrayList);
              System.out.println("Vector: " + vector);
          }
      }
      ```

38. **What is the difference between a deep copy and a shallow copy?**
    - **Definition:** Shallow copy ek object ke reference ko copy karta hai, jabki deep copy ek naya object create karta hai aur original object ke saath linked objects ko bhi copy karta hai.
    - **Example:**
      ```java
      class Address {
          String city;

          Address(String city) {
              this.city = city;
          }
      }

      class Person {
          String name;
          Address address;

          Person(String name, Address address) {
              this.name = name;
              this.address = address;
          }

          // Shallow copy
          Person shallowCopy() {
              return new Person(name, address);
          }

          // Deep copy
          Person deepCopy() {
              return new Person(name, new Address(address.city));
          }
      }

      public class Test {
          public static void main(String[] args) {
              Address address = new Address("Delhi");
              Person person1 = new Person("John", address);
              Person person2 = person1.shallowCopy(); // Shallow copy

              person2.address.city = "Mumbai"; // Change in address
              System.out.println(person1.address.city); // Output: Mumbai (changed)

              Person person3 = person1.deepCopy(); // Deep copy
              person3.address.city = "Kolkata"; // Change in address
              System.out.println(person1.address.city); // Output: Mumbai (unchanged)
          }
      }
      ```

39. **Can a constructor call another constructor in the same class?**
    - **Definition:** Haan, ek constructor dusre constructor ko call kar sakta hai using `this()` keyword. Ye constructor chaining ka ek example hai.
    - **Example:**
      ```java
      class MyClass {
          MyClass() {
              this(10); // Calling another constructor
              System.out.println("Default Constructor");
          }

          MyClass(int x) {
              System.out.println("Parameterized Constructor: " + x);
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass(); // Output: Parameterized Constructor: 10
                                             // Default Constructor
          }
      }
      ```

40. **What is the purpose of the `volatile` keyword in Java?**
    - **Definition:** `volatile` keyword variable ko thread-safe banata hai. Ye ensure karta hai ki variable ka value hamesha main memory se read hota hai, isse caching issues nahi hote.
    - **Example:**
      ```java
      class MyClass {
          volatile int counter = 0;

          void increment() {
              counter++;
          }

          int getCounter() {
              return counter;
          }
      }

      public class Test {
          public static void main(String[] args) throws InterruptedException {
              MyClass obj = new MyClass();

              Thread t1 = new Thread(() -> {
                  for (int i = 0; i < 1000; i++) {
                      obj.increment();
                  }
              });

              Thread t2 = new Thread(() -> {
                  for (int i = 0; i < 1000; i++) {
                      obj.increment();
                  }
              });

              t1.start();
              t2.start();
              t1.join();
              t2.join();

              System.out.println("Counter: " + obj.getCounter()); // Output: Counter: 2000 (consistent)
         

---
Certainly! Here are more tricky Core Java interview questions in Hinglish, along with their definitions and examples:

---

### More Tricky Java Interview Questions

41. **What is method overloading, and how is it different from method overriding?**
    - **Definition:** 
      - Method overloading ek class mein ek hi naam ke multiple methods define karna hai, lekin unke parameter list (number, type, ya order) alag hone chahiye. 
      - Method overriding tab hota hai jab subclass parent class ke method ko redefine karta hai.
    - **Example:**
      ```java
      class MyClass {
          void display(int a) { // Method Overloading
              System.out.println("Integer: " + a);
          }

          void display(String b) { // Method Overloading
              System.out.println("String: " + b);
          }

          void show() { // Method in Parent
              System.out.println("Show from Parent");
          }
      }

      class SubClass extends MyClass {
          @Override
          void show() { // Method Overriding
              System.out.println("Show from SubClass");
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj1 = new MyClass();
              obj1.display(10); // Output: Integer: 10
              obj1.display("Hello"); // Output: String: Hello

              SubClass obj2 = new SubClass();
              obj2.show(); // Output: Show from SubClass
          }
      }
      ```

42. **What is the difference between `StringBuilder` and `StringBuffer`?**
    - **Definition:** 
      - `StringBuffer` synchronized hai, isliye ye thread-safe hai. 
      - `StringBuilder` non-synchronized hai, isliye ye zyada fast hai lekin thread-safe nahi hai.
    - **Example:**
      ```java
      public class Test {
          public static void main(String[] args) {
              StringBuffer sb = new StringBuffer("Hello");
              sb.append(" World!"); // Thread-safe
              System.out.println(sb); // Output: Hello World!

              StringBuilder sb2 = new StringBuilder("Hello");
              sb2.append(" World!"); // Non-synchronized
              System.out.println(sb2); // Output: Hello World!
          }
      }
      ```

43. **What is an abstract class, and how is it different from an interface?**
    - **Definition:** 
      - Abstract class ko directly instantiate nahi kiya ja sakta. Ismein abstract methods (without body) aur concrete methods (with body) dono ho sakte hain.
      - Interface mein sirf abstract methods hote hain (Java 8 se default methods allow hai).
    - **Example:**
      ```java
      abstract class Animal { // Abstract Class
          abstract void sound(); // Abstract Method

          void eat() { // Concrete Method
              System.out.println("Eating...");
          }
      }

      class Dog extends Animal {
          void sound() { // Implementing abstract method
              System.out.println("Bark");
          }
      }

      public class Test {
          public static void main(String[] args) {
              Animal animal = new Dog();
              animal.sound(); // Output: Bark
              animal.eat(); // Output: Eating...
          }
      }
      ```

44. **What is a Singleton class?**
    - **Definition:** 
      - Singleton class ek aisi class hai jiska sirf ek hi instance create hota hai, aur ye instance globally accessible hota hai. Ye pattern generally resource management ke liye use hota hai.
    - **Example:**
      ```java
      class Singleton {
          private static Singleton instance;

          private Singleton() {} // Private constructor

          public static Singleton getInstance() {
              if (instance == null) {
                  instance = new Singleton();
              }
              return instance;
          }
      }

      public class Test {
          public static void main(String[] args) {
              Singleton obj1 = Singleton.getInstance();
              Singleton obj2 = Singleton.getInstance();

              System.out.println(obj1 == obj2); // Output: true (same instance)
          }
      }
      ```

45. **What is the use of the `super` keyword in Java?**
    - **Definition:** 
      - `super` keyword parent class ke reference ko denote karta hai. Iska use parent class ke constructor ya method ko call karne ke liye hota hai.
    - **Example:**
      ```java
      class Animal {
          Animal() {
              System.out.println("Animal constructor");
          }
      }

      class Dog extends Animal {
          Dog() {
              super(); // Calling parent class constructor
              System.out.println("Dog constructor");
          }
      }

      public class Test {
          public static void main(String[] args) {
              Dog dog = new Dog(); // Output: Animal constructor
                                   // Dog constructor
          }
      }
      ```

46. **What is the purpose of the `this` keyword in Java?**
    - **Definition:** 
      - `this` keyword current class ka reference hai. Ye instance variables aur methods ko refer karne ke liye use hota hai.
    - **Example:**
      ```java
      class MyClass {
          int value;

          MyClass(int value) {
              this.value = value; // 'this' is used to differentiate between class variable and parameter
          }

          void display() {
              System.out.println("Value: " + this.value);
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass(10);
              obj.display(); // Output: Value: 10
          }
      }
      ```

47. **What are checked and unchecked exceptions?**
    - **Definition:** 
      - Checked exceptions woh exceptions hain jo compile time par check hoti hain, jaise `IOException`. Inhe handle karna mandatory hota hai.
      - Unchecked exceptions woh exceptions hain jo runtime par occur hoti hain, jaise `NullPointerException`.
    - **Example:**
      ```java
      public class Test {
          public static void main(String[] args) {
              // Checked Exception Example
              try {
                  throw new IOException("Checked Exception");
              } catch (IOException e) {
                  System.out.println(e.getMessage());
              }

              // Unchecked Exception Example
              try {
                  String str = null;
                  System.out.println(str.length()); // This will throw NullPointerException
              } catch (NullPointerException e) {
                  System.out.println("Unchecked Exception: " + e.getMessage());
              }
          }
      }
      ```

48. **What is a `final` class?**
    - **Definition:** 
      - `final` class ko extend nahi kiya ja sakta. Ye inheritance ko rokne ke liye use hota hai.
    - **Example:**
      ```java
      final class FinalClass {
          void display() {
              System.out.println("This is a final class");
          }
      }

      // The following class declaration will cause a compile-time error
      // class SubClass extends FinalClass {} // Error: Cannot inherit from final 'FinalClass'

      public class Test {
          public static void main(String[] args) {
              FinalClass obj = new FinalClass();
              obj.display(); // Output: This is a final class
          }
      }
      ```

49. **What is the `instanceof` operator?**
    - **Definition:** 
      - `instanceof` operator ka use kisi object ke type ko check karne ke liye hota hai. Ye true return karta hai agar object specified class ya interface ka instance hai.
    - **Example:**
      ```java
      class Animal {}
      class Dog extends Animal {}

      public class Test {
          public static void main(String[] args) {
              Dog dog = new Dog();
              System.out.println(dog instanceof Dog); // Output: true
              System.out.println(dog instanceof Animal); // Output: true
              System.out.println(dog instanceof Object); // Output: true
          }
      }
      ```

50. **What are lambda expressions in Java?**
    - **Definition:** 
      - Lambda expressions Java 8 mein introduce hui thi. Ye functional interface ka ek concise representation hoti hai. Ye code ko cleaner aur more readable banata hai.
    - **Example:**
      ```java
      import java.util.*;

      public class Test {
          public static void main(String[] args) {
              List<String> list = Arrays.asList("Java", "Python", "C++");

              // Lambda expression to print each element
              list.forEach(item -> System.out.println(item)); // Output: Java, Python, C++
          }
      }
      ```

51. **What is the difference between method reference and lambda expression?**
    - **Definition:** 
      - Lambda expressions ek function ko define karne ka tarika hain, jabki method references already existing methods ko refer karte hain.
    - **Example:**
      ```java
      import java.util.*;

      class Print {
          static void printItem(String item) {
              System.out.println(item);
          }
      }

      public class Test {
          public static void main(String[] args) {
              List<String> list = Arrays.asList("Java", "Python", "C++");

              // Lambda Expression
              list.forEach(item -> System.out.println(item)); // Output: Java, Python, C++

              // Method Reference
              list.forEach(Print::printItem); // Output: Java, Python, C++
          }
      }
      ```
Certainly! Here’s the continuation of the tricky Core Java interview questions in Hinglish, along with their definitions and examples:

---

### More Tricky Java Interview Questions

52. **What is a functional interface?**
    - **Definition:** 
      - Functional interface woh interface hota hai jisme sirf ek abstract method hota hai. Ye lambda expressions ko support karte hain. Java 8 mein `@FunctionalInterface` annotation ka use karke aap isse clearly define kar sakte hain.
    - **Example:**
      ```java
      @FunctionalInterface
      interface MyFunctionalInterface {
          void display(); // Single abstract method
      }

      public class Test {
          public static void main(String[] args) {
              // Lambda expression implementing functional interface
              MyFunctionalInterface myFunc = () -> System.out.println("Hello from Functional Interface");
              myFunc.display(); // Output: Hello from Functional Interface
          }
      }
      ```

53. **What is the Stream API in Java?**
    - **Definition:** 
      - Stream API Java 8 mein introduce hui thi, jo collections ya data sources se data ko process karne ka ek functional style provide karta hai. Ye lazy evaluation aur functional-style operations ko support karta hai.
    - **Example:**
      ```java
      import java.util.*;
      import java.util.stream.*;

      public class Test {
          public static void main(String[] args) {
              List<String> list = Arrays.asList("Java", "Python", "C++", "JavaScript");

              // Using Stream API to filter and print elements
              list.stream()
                  .filter(s -> s.startsWith("J")) // Filtering strings that start with 'J'
                  .forEach(System.out::println); // Output: Java, JavaScript
          }
      }
      ```

54. **What is the `default` method in interfaces?**
    - **Definition:** 
      - Java 8 se aap interfaces mein `default` methods define kar sakte hain. Ye methods interface mein define hote hain aur isse implement karne wale classes ko override karna optional hota hai.
    - **Example:**
      ```java
      interface MyInterface {
          void display(); // Abstract method

          default void show() { // Default method
              System.out.println("Default Show Method");
          }
      }

      class MyClass implements MyInterface {
          public void display() {
              System.out.println("Display Method");
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass();
              obj.display(); // Output: Display Method
              obj.show();    // Output: Default Show Method
          }
      }
      ```

55. **What is the purpose of the `static` keyword in Java?**
    - **Definition:** 
      - `static` keyword ka use class level par variables aur methods ko define karne ke liye hota hai. Static members ko class ke instance create kiye bina access kiya ja sakta hai.
    - **Example:**
      ```java
      class MyClass {
          static int count = 0; // Static variable

          static void increment() { // Static method
              count++;
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass.increment();
              System.out.println("Count: " + MyClass.count); // Output: Count: 1
          }
      }
      ```

56. **What is the difference between `==` and `equals()` in Java?**
    - **Definition:** 
      - `==` operator reference comparison ke liye use hota hai, jabki `equals()` method content comparison ke liye use hota hai.
    - **Example:**
      ```java
      public class Test {
          public static void main(String[] args) {
              String str1 = new String("Hello");
              String str2 = new String("Hello");

              System.out.println(str1 == str2); // Output: false (reference comparison)
              System.out.println(str1.equals(str2)); // Output: true (content comparison)
          }
      }
      ```

57. **What is the difference between `Hashtable` and `HashMap`?**
    - **Definition:** 
      - `Hashtable` synchronized hai aur thread-safe hai, jabki `HashMap` non-synchronized hai aur not thread-safe hai. `HashMap` null keys aur values ko allow karta hai, jabki `Hashtable` nahi karta.
    - **Example:**
      ```java
      import java.util.*;

      public class Test {
          public static void main(String[] args) {
              // Using HashMap
              HashMap<String, String> hashMap = new HashMap<>();
              hashMap.put(null, "value1");
              hashMap.put("key2", null);
              System.out.println("HashMap: " + hashMap); // Output: HashMap: {null=value1, key2=null}

              // Using Hashtable
              Hashtable<String, String> hashTable = new Hashtable<>();
              // hashTable.put(null, "value1"); // Throws NullPointerException
              // hashTable.put("key2", null); // Throws NullPointerException
              hashTable.put("key1", "value1");
              System.out.println("Hashtable: " + hashTable); // Output: Hashtable: {key1=value1}
          }
      }
      ```

58. **What is an annotation in Java?**
    - **Definition:** 
      - Annotations metadata hoti hain jo code ke elements (classes, methods, variables, etc.) ko describe karti hain. Ye compile-time aur runtime ke liye additional information provide karti hain.
    - **Example:**
      ```java
      import java.lang.annotation.*;

      @Retention(RetentionPolicy.RUNTIME)
      @Target(ElementType.METHOD)
      @interface MyAnnotation {
          String value();
      }

      public class Test {
          @MyAnnotation(value = "My Method Annotation")
          public void myMethod() {
              System.out.println("Method with Annotation");
          }

          public static void main(String[] args) throws Exception {
              Test test = new Test();
              test.myMethod();

              // Accessing annotation
              MyAnnotation annotation = test.getClass().getMethod("myMethod").getAnnotation(MyAnnotation.class);
              System.out.println("Annotation Value: " + annotation.value()); // Output: Annotation Value: My Method Annotation
          }
      }
      ```

59. **What is the `finalize()` method in Java?**
    - **Definition:** 
      - `finalize()` method garbage collection se pehle object ko cleanup karne ke liye use hota hai. Ye method object ke garbage collector dwara call kiya jata hai.
    - **Example:**
      ```java
      class MyClass {
          protected void finalize() { // finalize method
              System.out.println("Finalize method called");
          }
      }

      public class Test {
          public static void main(String[] args) {
              MyClass obj = new MyClass();
              obj = null; // Nullifying reference
              System.gc(); // Suggesting garbage collection
          }
      }
      ```

60. **What is the difference between a process and a thread?**
    - **Definition:** 
      - Process ek program ka execution instance hai, jabki thread ek process ka lightweight unit hota hai. Threads same process ke andar execute hoti hain aur unhe share kiya jata hai resources.
    - **Example:**
      ```java
      class MyThread extends Thread {
          public void run() {
              System.out.println("Thread is running");
          }

          public static void main(String[] args) {
              MyThread thread = new MyThread();
              thread.start(); // Starting the thread
          }
      }
      ```

---
---
---



