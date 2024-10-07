


## **Java interview questions with code examples**
---

### 1. **What is the difference between method overloading and method overriding?**

#### Method Overloading Example:
```java
class OverloadingExample {
    void display(int a) {
        System.out.println("Integer: " + a);
    }
    
    void display(double a) {
        System.out.println("Double: " + a);
    }
}

public class Main {
    public static void main(String[] args) {
        OverloadingExample obj = new OverloadingExample();
        obj.display(10);    // Calls the first method
        obj.display(5.5);   // Calls the second method
    }
}
```
**#Output:**
```
Integer: 10
Double: 5.5
```

#### Method Overriding Example:
```java
class Parent {
    void show() {
        System.out.println("Parent class method");
    }
}

class Child extends Parent {
    @Override
    void show() {
        System.out.println("Child class method");
    }
}

public class Main {
    public static void main(String[] args) {
        Parent obj = new Child();  // Upcasting
        obj.show();    // Calls Child class's method due to overriding
    }
}
```
**#Output:**
```
Child class method
```

---

### 2. **What is Inheritance in Java?**

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();  // Inherited method from Animal class
        dog.bark(); // Dog's own method
    }
}
```
**#Output:**
```
This animal eats food.
The dog barks.
```

---

### 3. **What is Polymorphism in Java?**

#### Compile-time Polymorphism (Method Overloading):
```java
class PolyExample {
    void print(int a) {
        System.out.println("Integer: " + a);
    }
    
    void print(String b) {
        System.out.println("String: " + b);
    }
}

public class Main {
    public static void main(String[] args) {
        PolyExample obj = new PolyExample();
        obj.print(5);    // Calls the int version
        obj.print("Java"); // Calls the String version
    }
}
```
**#Output:**
```
Integer: 5
String: Java
```

#### Runtime Polymorphism (Method Overriding):
```java
class Shape {
    void draw() {
        System.out.println("Drawing Shape");
    }
}

class Circle extends Shape {
    @Override
    void draw() {
        System.out.println("Drawing Circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape shape = new Circle();  // Runtime polymorphism
        shape.draw();  // Calls Circle's draw method
    }
}
```
**#Output:**
```
Drawing Circle
```

---

### 4. **What is an Abstract Class?**

```java
abstract class Vehicle {
    abstract void start();
    
    void fuel() {
        System.out.println("Vehicle needs fuel.");
    }
}

class Car extends Vehicle {
    @Override
    void start() {
        System.out.println("Car starts with key.");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle car = new Car();
        car.start();  // Abstract method implementation
        car.fuel();   // Non-abstract method
    }
}
```
**#Output:**
```
Car starts with key.
Vehicle needs fuel.
```

---

### 5. **What is the difference between ArrayList and LinkedList?**

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // ArrayList example
        ArrayList<String> arrayList = new ArrayList<>();
        arrayList.add("Apple");
        arrayList.add("Banana");
        
        // LinkedList example
        LinkedList<String> linkedList = new LinkedList<>();
        linkedList.add("Dog");
        linkedList.add("Cat");
        
        System.out.println("ArrayList: " + arrayList);
        System.out.println("LinkedList: " + linkedList);
    }
}
```
**#Output:**
```
ArrayList: [Apple, Banana]
LinkedList: [Dog, Cat]
```

---

### 6. **What is Exception Handling in Java?**

```java
public class Main {
    public static void main(String[] args) {
        try {
            int divide = 10 / 0;  // This will cause an exception
        } catch (ArithmeticException e) {
            System.out.println("Exception caught: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed.");
        }
    }
}
```
**#Output:**
```
Exception caught: / by zero
Finally block executed.
```

---

### 7. **What is the difference between ‘==’ and ‘equals()’ method?**

```java
public class Main {
    public static void main(String[] args) {
        String s1 = new String("Java");
        String s2 = new String("Java");
        
        // == checks reference
        if (s1 == s2) {
            System.out.println("s1 and s2 references are equal");
        } else {
            System.out.println("s1 and s2 references are not equal");
        }
        
        // equals() checks content
        if (s1.equals(s2)) {
            System.out.println("s1 and s2 content is equal");
        }
    }
}
```
**#Output:**
```
s1 and s2 references are not equal
s1 and s2 content is equal
```

---

### 8. **What is Synchronization in Java?**

```java
class Table {
    synchronized void printTable(int n) {
        for (int i = 1; i <= 5; i++) {
            System.out.println(n * i);
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                System.out.println(e);
            }
        }
    }
}

class MyThread extends Thread {
    Table t;
    
    MyThread(Table t) {
        this.t = t;
    }
    
    public void run() {
        t.printTable(5);
    }
}

public class Main {
    public static void main(String[] args) {
        Table obj = new Table();  // Shared object
        MyThread t1 = new MyThread(obj);
        MyThread t2 = new MyThread(obj);
        
        t1.start();
        t2.start();
    }
}
```
**#Output (Synchronization ensures one thread runs at a time):**
```
5
10
15
20
25
5
10
15
20
25
```

---

### 9. **What is the final keyword in Java?**

```java
class FinalKeywordExample {
    final int CONSTANT = 100;  // Constant variable
    
    final void show() {  // Final method
        System.out.println("This is a final method.");
    }
}

public class Main extends FinalKeywordExample {
    // Cannot override final method
    // void show() {}  // This will cause a compilation error

    public static void main(String[] args) {
        FinalKeywordExample obj = new FinalKeywordExample();
        obj.show();
        System.out.println("Constant value: " + obj.CONSTANT);
    }
}
```
**#Output:**
```
This is a final method.
Constant value: 100
```

---

### 10. **What is a Constructor in Java?**

```java
class Person {
    String name;
    int age;
    
    // Constructor
    Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
    
    void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person("Rahul", 25);  // Constructor called
        p.display();
    }
}
```
**#Output:**
```
Name: Rahul, Age: 25
```


### 11. **What is the use of the `super` keyword in Java?**

```java
class Animal {
    String name = "Animal";

    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    String name = "Dog";

    void sound() {
        System.out.println("Dog barks");
    }

    void display() {
        System.out.println("Name in Dog: " + name);       // Refers to Dog class variable
        System.out.println("Name in Animal: " + super.name); // Refers to Animal class variable
        super.sound();  // Calls parent class method
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.display();
    }
}
```
**#Output:**
```
Name in Dog: Dog
Name in Animal: Animal
Animal makes sound
```

---

### 12. **What is the `this` keyword in Java?**

```java
class Student {
    String name;
    int age;

    // Using 'this' to refer to current object's variables
    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void display() {
        System.out.println("Name: " + this.name + ", Age: " + this.age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student("John", 21);
        s1.display();
    }
}
```
**#Output:**
```
Name: John, Age: 21
```

---

### 13. **What is a Static method in Java?**

```java
class MathUtils {
    // Static method
    static int square(int n) {
        return n * n;
    }
}

public class Main {
    public static void main(String[] args) {
        // Call static method without object creation
        int result = MathUtils.square(5);
        System.out.println("Square of 5: " + result);
    }
}
```
**#Output:**
```
Square of 5: 25
```

---

### 14. **What is Encapsulation in Java?**

```java
class Employee {
    // Private data member
    private String name;
    private int age;

    // Getter method for name
    public String getName() {
        return name;
    }

    // Setter method for name
    public void setName(String name) {
        this.name = name;
    }

    // Getter method for age
    public int getAge() {
        return age;
    }

    // Setter method for age
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        } else {
            System.out.println("Invalid age");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee();
        emp.setName("Alice");
        emp.setAge(30);
        System.out.println("Name: " + emp.getName());
        System.out.println("Age: " + emp.getAge());
    }
}
```
**#Output:**
```
Name: Alice
Age: 30
```

---

### 15. **What is an Interface in Java?**

```java
interface Drawable {
    void draw();
}

class Circle implements Drawable {
    @Override
    public void draw() {
        System.out.println("Drawing a Circle");
    }
}

class Square implements Drawable {
    @Override
    public void draw() {
        System.out.println("Drawing a Square");
    }
}

public class Main {
    public static void main(String[] args) {
        Drawable circle = new Circle();
        Drawable square = new Square();
        circle.draw();
        square.draw();
    }
}
```
**#Output:**
```
Drawing a Circle
Drawing a Square
```

---

### 16. **What is the difference between `final`, `finally`, and `finalize`?**

- `final`: Used to declare constants, prevent inheritance or method overriding.
- `finally`: Block that executes after `try-catch`, ensuring cleanup code.
- `finalize()`: Called by the garbage collector before the object is destroyed.

#### Example of `finally` block:
```java
public class Main {
    public static void main(String[] args) {
        try {
            int divide = 5 / 0;  // Will cause an exception
        } catch (ArithmeticException e) {
            System.out.println("Exception caught: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed");
        }
    }
}
```
**#Output:**
```
Exception caught: / by zero
Finally block executed
```

---

### 17. **What is the difference between HashMap and TreeMap?**

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // HashMap: No ordering
        HashMap<Integer, String> hashMap = new HashMap<>();
        hashMap.put(3, "C");
        hashMap.put(1, "A");
        hashMap.put(2, "B");
        System.out.println("HashMap: " + hashMap);

        // TreeMap: Sorted by keys
        TreeMap<Integer, String> treeMap = new TreeMap<>();
        treeMap.put(3, "C");
        treeMap.put(1, "A");
        treeMap.put(2, "B");
        System.out.println("TreeMap: " + treeMap);
    }
}
```
**#Output:**
```
HashMap: {1=A, 2=B, 3=C}
TreeMap: {1=A, 2=B, 3=C}
```

---

### 18. **What is a Singleton class in Java?**

```java
class Singleton {
    // Static instance of Singleton class
    private static Singleton instance;

    // Private constructor to restrict instantiation
    private Singleton() {
        System.out.println("Singleton instance created");
    }

    // Public method to get the single instance of the class
    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}

public class Main {
    public static void main(String[] args) {
        Singleton s1 = Singleton.getInstance();
        Singleton s2 = Singleton.getInstance();
        
        if (s1 == s2) {
            System.out.println("Both are the same instance");
        }
    }
}
```
**#Output:**
```
Singleton instance created
Both are the same instance
```

---

### 19. **What is the difference between `throw` and `throws`?**

```java
class Test {
    // Throws declaration for the method
    public void checkAge(int age) throws Exception {
        if (age < 18) {
            // Throwing an exception
            throw new Exception("Age is less than 18");
        } else {
            System.out.println("You are eligible to vote.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Test test = new Test();
        try {
            test.checkAge(16);  // This will throw an exception
        } catch (Exception e) {
            System.out.println("Exception caught: " + e.getMessage());
        }
    }
}
```
**#Output:**
```
Exception caught: Age is less than 18
```

---

### 20. **What is a Constructor Overloading in Java?**

```java
class Student {
    String name;
    int age;

    // Default constructor
    Student() {
        name = "Unknown";
        age = 0;
    }

    // Parameterized constructor
    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    void display() {
        System.out.println("Name: " + name + ", Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        Student s1 = new Student();         // Calls default constructor
        Student s2 = new Student("John", 22); // Calls parameterized constructor
        
        s1.display();
        s2.display();
    }
}
```
**#Output:**
```
Name: Unknown, Age: 0
Name: John, Age: 22
```

---

### 21. **What is Garbage Collection in Java?**

```java
public class Main {
    public static void main(String[] args) {
        Main obj = new Main();
        
        // Dereferencing object
        obj = null;
        
        // Suggesting JVM to run garbage collector
        System.gc();
        System.out.println("Garbage Collector called");
    }
    
    // finalize method is called by Garbage Collector before object is destroyed
    @Override
    protected void finalize() {
        System.out.println("finalize method executed");
    }
}
```
**#Output:**
```
Garbage Collector called
finalize method executed
```

---
Sure! Let's continue with more **Core Java interview questions**, along with their **code examples** and **#output**.

---

### 22. **What is an Enum in Java?**

```java
enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
}

public class Main {
    public static void main(String[] args) {
        Day today = Day.FRIDAY;
        
        switch (today) {
            case MONDAY:
                System.out.println("Start of the work week");
                break;
            case FRIDAY:
                System.out.println("End of the work week");
                break;
            case SUNDAY:
                System.out.println("It's a holiday");
                break;
            default:
                System.out.println("Midweek day");
        }
    }
}
```
**#Output:**
```
End of the work week
```

---

### 23. **What is the difference between Interface and Abstract Class?**

- **Abstract Class**: Can have both abstract and non-abstract methods. Supports constructors and static methods.
- **Interface**: Can have abstract methods and default methods (since Java 8), no constructors allowed.

#### Example showing both:
```java
abstract class Animal {
    abstract void sound();

    void eat() {
        System.out.println("Animal eats food.");
    }
}

interface Flyable {
    void fly();
}

class Bird extends Animal implements Flyable {
    @Override
    void sound() {
        System.out.println("Bird chirps");
    }

    @Override
    public void fly() {
        System.out.println("Bird flies");
    }
}

public class Main {
    public static void main(String[] args) {
        Bird bird = new Bird();
        bird.sound();
        bird.eat();
        bird.fly();
    }
}
```
**#Output:**
```
Bird chirps
Animal eats food.
Bird flies
```

---

### 24. **What is a Multithreading in Java?**

```java
class MyThread extends Thread {
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println(i + " from " + Thread.currentThread().getName());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread t1 = new MyThread();
        MyThread t2 = new MyThread();
        
        t1.start();  // Starts the first thread
        t2.start();  // Starts the second thread
    }
}
```
**#Output:**
```
1 from Thread-0
1 from Thread-1
2 from Thread-0
2 from Thread-1
...
```
(Note: The exact order may vary due to thread scheduling.)

---

### 25. **What is the `volatile` keyword in Java?**

```java
class MyThread extends Thread {
    volatile boolean running = true;

    public void run() {
        while (running) {
            System.out.println("Thread is running...");
            try {
                Thread.sleep(500);
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
        }
        System.out.println("Thread has stopped.");
    }

    public void stopRunning() {
        running = false;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        MyThread thread = new MyThread();
        thread.start();
        
        Thread.sleep(2000);  // Allow the thread to run for 2 seconds
        thread.stopRunning();  // Stop the thread
    }
}
```
**#Output:**
```
Thread is running...
Thread is running...
Thread is running...
Thread is running...
Thread has stopped.
```

---

### 26. **What is the use of `transient` keyword in Java?**

```java
import java.io.*;

class Employee implements Serializable {
    String name;
    transient int salary;  // `transient` prevents this from being serialized

    Employee(String name, int salary) {
        this.name = name;
        this.salary = salary;
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("John", 5000);

        try {
            // Serialize the object
            FileOutputStream fos = new FileOutputStream("employee.ser");
            ObjectOutputStream oos = new ObjectOutputStream(fos);
            oos.writeObject(emp);
            oos.close();
            fos.close();

            // Deserialize the object
            FileInputStream fis = new FileInputStream("employee.ser");
            ObjectInputStream ois = new ObjectInputStream(fis);
            Employee deserializedEmp = (Employee) ois.readObject();
            ois.close();
            fis.close();

            System.out.println("Name: " + deserializedEmp.name);
            System.out.println("Salary: " + deserializedEmp.salary);  // Will be 0 since `salary` was transient
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```
**#Output:**
```
Name: John
Salary: 0
```

---

### 27. **What is a Deadlock in Java?**

```java
class Resource1 {
    synchronized void method1(Resource2 r2) {
        System.out.println("Thread1: Locked Resource1");

        try { Thread.sleep(100); } catch (Exception e) {}

        System.out.println("Thread1: Trying to lock Resource2");
        r2.method2();
    }

    synchronized void method2() {
        System.out.println("Resource1 method2");
    }
}

class Resource2 {
    synchronized void method1(Resource1 r1) {
        System.out.println("Thread2: Locked Resource2");

        try { Thread.sleep(100); } catch (Exception e) {}

        System.out.println("Thread2: Trying to lock Resource1");
        r1.method2();
    }

    synchronized void method2() {
        System.out.println("Resource2 method2");
    }
}

public class Main extends Thread {
    Resource1 r1 = new Resource1();
    Resource2 r2 = new Resource2();

    public void run() {
        Thread t1 = new Thread(() -> r1.method1(r2));
        Thread t2 = new Thread(() -> r2.method1(r1));

        t1.start();
        t2.start();
    }

    public static void main(String[] args) {
        new Main().start();
    }
}
```
**#Output:**
```
Thread1: Locked Resource1
Thread2: Locked Resource2
Thread1: Trying to lock Resource2
Thread2: Trying to lock Resource1
```
(Note: This creates a **deadlock** as both threads are waiting on each other to release resources.)

---

### 28. **What is the `StringBuilder` class in Java?**

```java
public class Main {
    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder("Hello");
        
        // Append string
        sb.append(" World");
        System.out.println("After append: " + sb);

        // Insert at index
        sb.insert(5, " Java");
        System.out.println("After insert: " + sb);

        // Reverse the string
        sb.reverse();
        System.out.println("After reverse: " + sb);
    }
}
```
**#Output:**
```
After append: Hello World
After insert: Hello Java World
After reverse: dlroW avaJ olleH
```

---

### 29. **What is `try-with-resources` in Java?**

```java
import java.io.*;

public class Main {
    public static void main(String[] args) {
        // Try-with-resources: Automatically closes the resource after use
        try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
            String line;
            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```
**#Output:**
```
File content displayed line by line (if the file exists).
```

(Note: In this example, resources such as `BufferedReader` are automatically closed after use, even if an exception occurs.)

---

### 30. **What is the `Comparable` and `Comparator` interface in Java?**

#### Example of `Comparable`:
```java
import java.util.*;

class Student implements Comparable<Student> {
    String name;
    int marks;

    Student(String name, int marks) {
        this.name = name;
        this.marks = marks;
    }

    @Override
    public int compareTo(Student other) {
        return this.marks - other.marks;  // Sorting by marks
    }
}

public class Main {
    public static void main(String[] args) {
        List<Student> students = new ArrayList<>();
        students.add(new Student("John", 85));
        students.add(new Student("Alice", 90));
        students.add(new Student("Bob", 75));

        Collections.sort(students);  // Sort based on marks

        for (Student s : students) {
            System.out.println(s.name + ": " + s.marks);
        }
    }
}
```
**#Output:**
```
Bob: 75
John: 85
Alice: 90
```

#### Example of `Comparator`:
```java
import java.util.*;

class Student {
    String name;
    int marks;

    Student(String name, int marks) {
        this.name = name;
        this.marks = marks;
    }
}

class NameComparator implements Comparator<Student> {
```java
    @Override
    public int compare(Student s1, Student s2) {
        return s1.name.compareTo(s2.name);  // Sorting by name
    }
}

public class Main {
    public static void main(String[] args) {
        List<Student> students = new ArrayList<>();
        students.add(new Student("John", 85));
        students.add(new Student("Alice", 90));
        students.add(new Student("Bob", 75));

        // Sorting using NameComparator
        Collections.sort(students, new NameComparator());

        for (Student s : students) {
            System.out.println(s.name + ": " + s.marks);
        }
    }
}
```

**#Output:**
```
Alice: 90
Bob: 75
John: 85
```

---

### 31. **What is the `synchronized` keyword in Java?**

```java
class Counter {
    private int count = 0;

    // Synchronized method to increment the count
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        // Creating two threads that access the same counter object
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();

        // Wait for both threads to finish
        t1.join();
        t2.join();

        System.out.println("Final Count: " + counter.getCount());
    }
}
```
**#Output:**
```
Final Count: 2000
```

(In this example, `synchronized` ensures that only one thread increments the count at a time, preventing race conditions.)

---

### 32. **What is a Nested Class in Java?**

```java
class OuterClass {
    private String message = "Hello from OuterClass";

    // Static nested class
    static class StaticNestedClass {
        void display() {
            System.out.println("Inside StaticNestedClass");
        }
    }

    // Non-static inner class
    class InnerClass {
        void display() {
            System.out.println("Message from InnerClass: " + message);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Accessing static nested class
        OuterClass.StaticNestedClass staticNested = new OuterClass.StaticNestedClass();
        staticNested.display();

        // Accessing non-static inner class
        OuterClass outer = new OuterClass();
        OuterClass.InnerClass inner = outer.new InnerClass();
        inner.display();
    }
}
```
**#Output:**
```
Inside StaticNestedClass
Message from InnerClass: Hello from OuterClass
```

---

### 33. **What is the use of `instanceof` in Java?**

```java
class Animal {}
class Dog extends Animal {}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog();

        if (a instanceof Dog) {
            System.out.println("a is an instance of Dog");
        }

        if (a instanceof Animal) {
            System.out.println("a is an instance of Animal");
        }
    }
}
```
**#Output:**
```
a is an instance of Dog
a is an instance of Animal
```

---

### 34. **What is Method Overriding in Java?**

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog();
        a.sound();  // Overridden method from Dog class is called
    }
}
```
**#Output:**
```
Dog barks
```

---

### 35. **What is Java's `assert` keyword used for?**

```java
public class Main {
    public static void main(String[] args) {
        int x = 5;
        assert x > 10 : "x is not greater than 10";  // AssertionError will be thrown if false

        System.out.println("x is greater than 10");
    }
}
```
**#Output (with assertions enabled using `-ea`):**
```
Exception in thread "main" java.lang.AssertionError: x is not greater than 10
```

(Note: To run assertions in Java, you need to enable them with the `-ea` flag when running the program.)

---

### 36. **What is the use of the `native` keyword in Java?**

- The `native` keyword is used to declare methods that are implemented in platform-dependent code using languages like C or C++.

```java
class NativeDemo {
    // Declaration of native method (implementation is in C/C++)
    public native void displayMessage();

    static {
        System.loadLibrary("NativeDemo");  // Load native library (must be implemented in C/C++)
    }

    public static void main(String[] args) {
        new NativeDemo().displayMessage();  // Calls native method
    }
}
```
**#Output:**
```
(This will depend on the native code, which should be implemented in C/C++).
```

(Note: The actual implementation of the `displayMessage()` method is in native code, not Java.)

---

### 37. **What is the use of `Optional` in Java?**

```java
import java.util.Optional;

public class Main {
    public static void main(String[] args) {
        // Creating an Optional object
        Optional<String> optionalValue = Optional.ofNullable("Hello");

        // Checking if the value is present
        if (optionalValue.isPresent()) {
            System.out.println("Value: " + optionalValue.get());
        }

        // Using orElse to provide a default value
        String result = optionalValue.orElse("Default Value");
        System.out.println("Result: " + result);

        // Using ifPresent to execute a code block if value is present
        optionalValue.ifPresent(value -> System.out.println("Value using ifPresent: " + value));
    }
}
```
**#Output:**
```
Value: Hello
Result: Hello
Value using ifPresent: Hello
```

---

### 38. **What is a `Callable` interface in Java?**

```java
import java.util.concurrent.*;

class MyTask implements Callable<Integer> {
    public Integer call() throws Exception {
        int sum = 0;
        for (int i = 1; i <= 5; i++) {
            sum += i;
            Thread.sleep(500);  // Simulating a long-running task
        }
        return sum;
    }
}

public class Main {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newSingleThreadExecutor();
        Future<Integer> future = executor.submit(new MyTask());

        try {
            System.out.println("Result: " + future.get());  // Blocking call, waits for result
        } catch (InterruptedException | ExecutionException e) {
            e.printStackTrace();
        }

        executor.shutdown();
    }
}
```
**#Output:**
```
Result: 15
```

---

Sure! Let’s continue with more **Core Java interview questions**, along with their **code examples** and **#output**.

---

### 39. **What is the difference between `HashMap` and `Hashtable`?**

- **HashMap** is not synchronized and allows `null` keys and values.
- **Hashtable** is synchronized and does not allow `null` keys or values.

#### Example:
```java
import java.util.HashMap;
import java.util.Hashtable;

public class Main {
    public static void main(String[] args) {
        // HashMap example
        HashMap<String, String> hashMap = new HashMap<>();
        hashMap.put("Name", "John");
        hashMap.put(null, "NullKey");  // HashMap allows null keys

        System.out.println("HashMap: " + hashMap);

        // Hashtable example
        Hashtable<String, String> hashtable = new Hashtable<>();
        hashtable.put("Name", "Alice");
        
        try {
            hashtable.put(null, "NullKey");  // Hashtable does not allow null keys
        } catch (NullPointerException e) {
            System.out.println("Hashtable does not allow null keys");
        }
        
        System.out.println("Hashtable: " + hashtable);
    }
}
```
**#Output:**
```
HashMap: {null=NullKey, Name=John}
Hashtable does not allow null keys
Hashtable: {Name=Alice}
```

---

### 40. **What is a `TreeSet` in Java?**

```java
import java.util.TreeSet;

public class Main {
    public static void main(String[] args) {
        TreeSet<Integer> treeSet = new TreeSet<>();
        treeSet.add(5);
        treeSet.add(1);
        treeSet.add(10);
        treeSet.add(3);

        System.out.println("TreeSet (sorted): " + treeSet);

        // Operations
        System.out.println("First Element: " + treeSet.first());
        System.out.println("Last Element: " + treeSet.last());
        System.out.println("Subset (1 to 5): " + treeSet.subSet(1, 6));
    }
}
```
**#Output:**
```
TreeSet (sorted): [1, 3, 5, 10]
First Element: 1
Last Element: 10
Subset (1 to 5): [1, 3, 5]
```

(TreeSet sorts elements automatically in natural order.)

---

### 41. **What is the difference between `equals()` and `==` in Java?**

- `==` compares reference (memory location) of objects.
- `equals()` compares the content of objects.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        String s1 = new String("Hello");
        String s2 = new String("Hello");

        System.out.println("Using == : " + (s1 == s2));           // false
        System.out.println("Using equals() : " + s1.equals(s2));  // true
    }
}
```
**#Output:**
```
Using == : false
Using equals() : true
```

---

### 42. **What is Autoboxing and Unboxing in Java?**

- **Autoboxing**: Automatic conversion of primitive types to their corresponding wrapper classes.
- **Unboxing**: Automatic conversion of wrapper class objects to their primitive types.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        // Autoboxing
        int a = 10;
        Integer boxedA = a;  // Primitive int to Integer (autoboxing)
        
        // Unboxing
        Integer b = 20;
        int unboxedB = b;  // Integer to primitive int (unboxing)

        System.out.println("Boxed: " + boxedA);
        System.out.println("Unboxed: " + unboxedB);
    }
}
```
**#Output:**
```
Boxed: 10
Unboxed: 20
```

---

### 43. **What is `final`, `finally`, and `finalize()` in Java?**

1. **`final`**: A keyword used to declare constants, prevent inheritance, or prevent method overriding.
2. **`finally`**: A block used to execute important code (such as resource cleanup) even if an exception occurs.
3. **`finalize()`**: A method called by the Garbage Collector before destroying an object.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        // final variable
        final int x = 10;
        // x = 20;  // Error: Cannot reassign a final variable

        try {
            int result = 10 / 0;  // Will throw an exception
        } catch (ArithmeticException e) {
            System.out.println("Caught exception: " + e);
        } finally {
            System.out.println("Finally block executed.");
        }
    }

    @Override
    protected void finalize() throws Throwable {
        System.out.println("finalize() method called.");
    }
}
```
**#Output:**
```
Caught exception: java.lang.ArithmeticException: / by zero
Finally block executed.
finalize() method called. (Will be executed by GC when the object is destroyed)
```

---

### 44. **What is the use of `super` keyword in Java?**

- `super` is used to refer to the parent class's properties, methods, or constructor.

#### Example:
```java
class Animal {
    String name = "Animal";

    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    String name = "Dog";

    @Override
    void sound() {
        super.sound();  // Calling parent class method
        System.out.println("Dog barks");
    }

    void display() {
        System.out.println("Name: " + super.name);  // Accessing parent class property
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound();
        dog.display();
    }
}
```
**#Output:**
```
Animal makes sound
Dog barks
Name: Animal
```

---

### 45. **What is the `Object` class in Java?**

- The `Object` class is the root class for all Java classes.
- Every class in Java implicitly inherits from `Object`.

#### Example of `toString()` and `hashCode()` methods from `Object` class:
```java
class Person {
    String name;

    Person(String name) {
        this.name = name;
    }

    @Override
    public String toString() {
        return "Person's name is: " + name;
    }
}

public class Main {
    public static void main(String[] args) {
        Person p = new Person("John");
        System.out.println(p.toString());  // Uses Object's toString method
        System.out.println("HashCode: " + p.hashCode());  // Uses Object's hashCode method
    }
}
```
**#Output:**
```
Person's name is: John
HashCode: (A unique hashcode for the object)
```

---

### 46. **What are Anonymous Inner Classes in Java?**

- An **anonymous inner class** is a local class without a name and is declared and instantiated in a single statement.

#### Example:
```java
interface Greeting {
    void sayHello();
}

public class Main {
    public static void main(String[] args) {
        // Anonymous inner class implementing Greeting interface
        Greeting greeting = new Greeting() {
            @Override
            public void sayHello() {
                System.out.println("Hello, Anonymous Class!");
            }
        };

        greeting.sayHello();
    }
}
```
**#Output:**
```
Hello, Anonymous Class!
```

---

### 47. **What is the difference between `throw` and `throws`?**

- **`throw`**: Used to explicitly throw an exception in the code.
- **`throws`**: Used in method declarations to indicate that the method may throw exceptions.

#### Example:
```java
public class Main {
    // Using throws in method signature
    public static void divide(int a, int b) throws ArithmeticException {
        if (b == 0) {
            throw new ArithmeticException("Cannot divide by zero");  // Using throw to throw exception
        } else {
            System.out.println("Result: " + a / b);
        }
    }

    public static void main(String[] args) {
        try {
            divide(10, 0);  // This will throw ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println(e.getMessage());
        }
    }
}
```
**#Output:**
```
Cannot divide by zero
```

---

### 48. **What is Serialization in Java?**

- **Serialization** is the process of converting an object into a byte stream for storage or transmission.
- **Deserialization** is the reverse process, converting the byte stream back into an object.

#### Example:
```java
import java.io.*;

class Employee implements Serializable {
    String name;
    int salary;

    Employee(String name, int salary) {
        this.name = name;
        this.salary = salary;
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("Alice", 5000);

        // Serialize object to file
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("employee.ser"))) {
            oos.writeObject(emp);
            System.out
Sure! Continuing from where we left off, let's complete the **Serialization** example and provide more Core Java interview questions along with their code examples and outputs.

---

### 48. **Serialization in Java** (continued)

#### Example (continued):
```java
            System.out.println("Serialization successful");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Deserialize object from file
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("employee.ser"))) {
            Employee deserializedEmp = (Employee) ois.readObject();
            System.out.println("Deserialized Employee: " + deserializedEmp.name + ", Salary: " + deserializedEmp.salary);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

**#Output:**
```
Serialization successful
Deserialized Employee: Alice, Salary: 5000
```

---

### 49. **What is a `Runnable` interface in Java?**

- The `Runnable` interface is designed to represent a task that can be run by a thread. It contains a single method `run()`.

#### Example:
```java
class MyRunnable implements Runnable {
    @Override
    public void run() {
        System.out.println("Thread is running: " + Thread.currentThread().getName());
    }
}

public class Main {
    public static void main(String[] args) {
        Thread thread1 = new Thread(new MyRunnable());
        Thread thread2 = new Thread(new MyRunnable());

        thread1.start();
        thread2.start();
    }
}
```

**#Output:**
```
Thread is running: Thread-0
Thread is running: Thread-1
```

(Note: Output may vary as thread scheduling is non-deterministic.)

---

### 50. **What is a `Semaphore` in Java?**

- A `Semaphore` is a synchronization aid that restricts the number of threads that can access a particular resource.

#### Example:
```java
import java.util.concurrent.*;

class SemaphoreExample {
    private static final Semaphore semaphore = new Semaphore(2); // Allow 2 permits

    public void accessResource() {
        try {
            semaphore.acquire();
            System.out.println(Thread.currentThread().getName() + " acquired the permit.");
            Thread.sleep(1000); // Simulate resource access
        } catch (InterruptedException e) {
            e.printStackTrace();
        } finally {
            System.out.println(Thread.currentThread().getName() + " released the permit.");
            semaphore.release();
        }
    }
}

public class Main {
    public static void main(String[] args) {
        SemaphoreExample example = new SemaphoreExample();
        Runnable task = example::accessResource;

        for (int i = 0; i < 5; i++) {
            new Thread(task).start();  // Start 5 threads
        }
    }
}
```

**#Output:**
```
Thread-0 acquired the permit.
Thread-1 acquired the permit.
Thread-2 released the permit.
Thread-3 acquired the permit.
Thread-4 released the permit.
Thread-0 released the permit.
```

(Note: Output will vary due to thread scheduling and timing.)

---

### 51. **What is the `clone()` method in Java?**

- The `clone()` method is used to create a copy of an object. It is defined in the `Object` class and can be overridden in user-defined classes.

#### Example:
```java
class Person implements Cloneable {
    String name;

    Person(String name) {
        this.name = name;
    }

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone(); // Calls Object's clone method
    }
}

public class Main {
    public static void main(String[] args) {
        try {
            Person p1 = new Person("John");
            Person p2 = (Person) p1.clone(); // Cloning p1 to p2

            System.out.println("Original Person: " + p1.name);
            System.out.println("Cloned Person: " + p2.name);
        } catch (CloneNotSupportedException e) {
            e.printStackTrace();
        }
    }
}
```

**#Output:**
```
Original Person: John
Cloned Person: John
```

---

### 52. **What are Streams in Java?**

- Streams are a new abstraction introduced in Java 8 that allow for functional-style operations on collections of objects.

#### Example:
```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("John", "Alice", "Bob", "Diana");

        // Using Streams to filter and print names that start with 'D'
        names.stream()
            .filter(name -> name.startsWith("D"))
            .forEach(System.out::println);
    }
}
```

**#Output:**
```
Diana
```

---

### 53. **What are Lambda Expressions in Java?**

- Lambda expressions allow you to express instances of single-method interfaces (functional interfaces) in a clear and concise way.

#### Example:
```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("John", "Alice", "Bob", "Diana");

        // Using a lambda expression to sort names
        names.sort((s1, s2) -> s1.compareTo(s2));
        names.forEach(name -> System.out.println(name));
    }
}
```

**#Output:**
```
Alice
Bob
Diana
John
```

---

### 54. **What is a `Map` in Java?**

- A `Map` is an object that maps keys to values, with each key associated with exactly one value.

#### Example:
```java
import java.util.HashMap;
import java.util.Map;

public class Main {
    public static void main(String[] args) {
        Map<String, Integer> ageMap = new HashMap<>();
        ageMap.put("John", 30);
        ageMap.put("Alice", 25);
        ageMap.put("Bob", 22);

        // Iterating over the map
        for (Map.Entry<String, Integer> entry : ageMap.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

**#Output:**
```
John: 30
Alice: 25
Bob: 22
```

---

### 55. **What is the `volatile` keyword in Java?**

- The `volatile` keyword is used to indicate that a variable's value will be modified by different threads. It ensures visibility of changes to variables across threads.

#### Example:
```java
class SharedResource {
    private volatile boolean flag = false;

    public void setFlag() {
        flag = true; // Modifying the flag
    }

    public void checkFlag() {
        while (!flag) {
            // Busy waiting
        }
        System.out.println("Flag is set to true!");
    }
}

public class Main {
    public static void main(String[] args) {
        SharedResource resource = new SharedResource();

        new Thread(resource::checkFlag).start();
        try {
            Thread.sleep(1000); // Sleep for a while
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        resource.setFlag();
    }
}
```

**#Output:**
```
Flag is set to true!
```

---

### 56. **What is the difference between `StringBuilder` and `StringBuffer`?**

- **StringBuilder** is not synchronized and is faster but not thread-safe.
- **StringBuffer** is synchronized and thread-safe but slower.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        StringBuilder stringBuilder = new StringBuilder("Hello");
        stringBuilder.append(" World!");
        System.out.println("StringBuilder: " + stringBuilder.toString());

        StringBuffer stringBuffer = new StringBuffer("Hello");
        stringBuffer.append(" World!");
        System.out.println("StringBuffer: " + stringBuffer.toString());
    }
}
```

**#Output:**
```
StringBuilder: Hello World!
StringBuffer: Hello World!
```

---

### 57. **What is `try-with-resources` statement in Java?**

- The `try-with-resources` statement ensures that each resource is closed at the end of the statement. It simplifies error handling by automatically closing resources.

#### Example:
```java
import java.io.*;

public class Main {
    public static void main(String[] args) {
        // Using try-with-resources to read a file
        try (BufferedReader br = new BufferedReader(new FileReader("example.txt"))) {
            String line;
            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

(Note: Make sure to create `example.txt` file with some content for this example to work.)

**#Output:**
```
(Contents of the example.txt file)
```

---

### 58. **What is an `ExecutorService` in Java?**

- An `ExecutorService` is a higher-level replacement for managing threads. It provides a way to manage a pool of threads and execute tasks asynchronously.

#### Example:
```java
import java.util.concurrent.*;

public class Main {
    public static void main(String[] args) {
        ExecutorService executorService = Executors.newFixedThreadPool(2);

        Runnable task1 = () -> {
            System.out.println("Task 1 is running

Sure! Let's continue with the **ExecutorService** example and additional Core Java interview questions with their code examples and outputs.

---

### 58. **What is an `ExecutorService` in Java?** (continued)

#### Example (continued):
```java
            System.out.println("Task 1 is running: " + Thread.currentThread().getName());
        };

        Runnable task2 = () -> {
            System.out.println("Task 2 is running: " + Thread.currentThread().getName());
        };

        // Execute tasks
        executorService.execute(task1);
        executorService.execute(task2);

        // Shutdown the executor
        executorService.shutdown();
    }
}
```

**#Output:**
```
Task 1 is running: pool-1-thread-1
Task 2 is running: pool-1-thread-2
```

(Note: Output may vary due to thread scheduling.)

---

### 59. **What is the `CompletableFuture` in Java?**

- `CompletableFuture` is part of the Java Concurrency framework and allows for asynchronous programming. It can be used to run tasks in a non-blocking way.

#### Example:
```java
import java.util.concurrent.CompletableFuture;

public class Main {
    public static void main(String[] args) {
        CompletableFuture<String> future = CompletableFuture.supplyAsync(() -> {
            return "Hello from CompletableFuture!";
        });

        // Chaining a callback
        future.thenAccept(result -> {
            System.out.println(result);
        });

        // Ensure the main thread waits for the future to complete
        future.join();
    }
}
```

**#Output:**
```
Hello from CompletableFuture!
```

---

### 60. **What is the `default` keyword in Interfaces?**

- The `default` keyword allows you to create methods in interfaces with a body. This feature was introduced in Java 8.

#### Example:
```java
interface Greeting {
    default void sayHello() {
        System.out.println("Hello from default method!");
    }
}

class Main implements Greeting {
    public static void main(String[] args) {
        Main obj = new Main();
        obj.sayHello(); // Calls the default method
    }
}
```

**#Output:**
```
Hello from default method!
```

---

### 61. **What is the `static` keyword in Java?**

- The `static` keyword is used for memory management primarily. It can be applied to variables, methods, blocks, and nested classes. Static members belong to the class rather than any specific instance.

#### Example:
```java
class Counter {
    static int count = 0; // Static variable

    Counter() {
        count++;
    }

    static void displayCount() { // Static method
        System.out.println("Count: " + count);
    }
}

public class Main {
    public static void main(String[] args) {
        new Counter();
        new Counter();
        Counter.displayCount(); // Calling static method
    }
}
```

**#Output:**
```
Count: 2
```

---

### 62. **What is method overloading in Java?**

- Method overloading is a feature that allows a class to have more than one method with the same name, as long as the parameter types or the number of parameters are different.

#### Example:
```java
class MathOperations {
    // Method to add two integers
    int add(int a, int b) {
        return a + b;
    }

    // Method to add three integers
    int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        MathOperations math = new MathOperations();
        System.out.println("Sum of 2 numbers: " + math.add(10, 20));          // Calls first add
        System.out.println("Sum of 3 numbers: " + math.add(10, 20, 30));      // Calls second add
    }
}
```

**#Output:**
```
Sum of 2 numbers: 30
Sum of 3 numbers: 60
```

---

### 63. **What is method overriding in Java?**

- Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its superclass.

#### Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();
        animal.sound(); // Calls overridden method in Dog class
    }
}
```

**#Output:**
```
Dog barks
```

---

### 64. **What is an abstract class in Java?**

- An **abstract class** is a class that cannot be instantiated and may contain abstract methods (methods without a body) as well as concrete methods.

#### Example:
```java
abstract class Shape {
    abstract void draw(); // Abstract method
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing Circle");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape shape = new Circle();
        shape.draw(); // Calls the draw method of Circle
    }
}
```

**#Output:**
```
Drawing Circle
```

---

### 65. **What is an interface in Java?**

- An **interface** is a reference type in Java, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. Interfaces cannot contain instance fields or constructors.

#### Example:
```java
interface Animal {
    void eat(); // Method without body
}

class Cat implements Animal {
    public void eat() {
        System.out.println("Cat eats");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal cat = new Cat();
        cat.eat(); // Calls the eat method of Cat
    }
}
```

**#Output:**
```
Cat eats
```

---

### 66. **What is an Enum in Java?**

- An **Enum** (short for enumeration) is a special Java type used to define collections of constants. It provides a way to define a variable that can hold a set of predefined constants.

#### Example:
```java
enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY;
}

public class Main {
    public static void main(String[] args) {
        Day day = Day.MONDAY;

        switch (day) {
            case SUNDAY:
                System.out.println("It's Sunday!");
                break;
            case MONDAY:
                System.out.println("It's Monday!");
                break;
            default:
                System.out.println("Another day!");
                break;
        }
    }
}
```

**#Output:**
```
It's Monday!
```

---

### 67. **What is `this` keyword in Java?**

- The `this` keyword refers to the current instance of a class and is used to differentiate between class attributes and parameters with the same name.

#### Example:
```java
class Person {
    String name;

    Person(String name) {
        this.name = name; // 'this.name' refers to the instance variable
    }

    void display() {
        System.out.println("Name: " + this.name);
    }
}

public class Main {
    public static void main(String[] args) {
        Person person = new Person("John");
        person.display();
    }
}
```

**#Output:**
```
Name: John
```

---

### 68. **What is `super()` in Java?**

- The `super()` keyword is used to call the constructor of the parent class from a subclass constructor.

#### Example:
```java
class Animal {
    Animal() {
        System.out.println("Animal constructor");
    }
}

class Dog extends Animal {
    Dog() {
        super(); // Calls the constructor of Animal
        System.out.println("Dog constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
    }
}
```

**#Output:**
```
Animal constructor
Dog constructor
```

---

### 69. **What is the `finally` block in Java?**

- The `finally` block is used to execute important code such as resource cleanup. It executes regardless of whether an exception is thrown or not.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        try {
            int result = 10 / 0; // This will throw ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Caught an exception: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed.");
        }
    }
}
```

**#Output:**
```
Caught an exception: / by zero
Finally block executed.
```

---

### 70. **What is the `transient` keyword in Java?**

- The `transient` keyword is used in serialization. If you declare a variable as transient, it will not be serialized, meaning it won’t be saved during serialization.

#### Example:
```java
import java.io.*;

class Employee implements Serializable {
    String name;
    transient int salary; // This will not be serialized

    Employee(String name, int salary) {
        this.name = name;
        this.salary = salary;
    }
}

public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("Alice", 5000);

        // Serialize object to file
Certainly! Let's continue with the example for the `transient` keyword and provide more Core Java interview questions along with their code examples and outputs.

---

### 70. **What is the `transient` keyword in Java?** (continued)

#### Example (continued):
```java
        // Serialize object to file
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("employee.ser"))) {
            oos.writeObject(emp);
            System.out.println("Serialization successful");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Deserialize object from file
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("employee.ser"))) {
            Employee deserializedEmp = (Employee) ois.readObject();
            System.out.println("Deserialized Employee: " + deserializedEmp.name + ", Salary: " + deserializedEmp.salary);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

**#Output:**
```
Serialization successful
Deserialized Employee: Alice, Salary: 0
```

**Explanation:**
In the output, the `salary` is `0` after deserialization because it was marked as `transient`, indicating that it will not be saved in the serialized object.

---

### 71. **What is `synchronized` keyword in Java?**

- The `synchronized` keyword is used to lock a method or block of code so that only one thread can access it at a time. It is used to prevent thread interference.

#### Example:
```java
class Counter {
    private int count = 0;

    // Synchronized method
    synchronized void increment() {
        count++;
    }

    int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        // Creating multiple threads
        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();
        t1.join();
        t2.join();

        System.out.println("Final count: " + counter.getCount());
    }
}
```

**#Output:**
```
Final count: 2000
```

---

### 72. **What are `Collections` in Java?**

- The `Collections` framework is a set of classes and interfaces that implement commonly reusable collection data structures. It includes interfaces like `List`, `Set`, and `Map`.

#### Example:
```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<Integer> numbers = new ArrayList<>();
        numbers.add(3);
        numbers.add(1);
        numbers.add(2);

        // Sorting the list
        Collections.sort(numbers);
        System.out.println("Sorted List: " + numbers);
    }
}
```

**#Output:**
```
Sorted List: [1, 2, 3]
```

---

### 73. **What is the `HashMap` class in Java?**

- `HashMap` is a part of the Java Collections Framework and implements the `Map` interface. It stores data in key-value pairs and allows for fast retrieval based on keys.

#### Example:
```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> map = new HashMap<>();
        map.put("Alice", 25);
        map.put("Bob", 30);
        map.put("Charlie", 35);

        // Iterating through the HashMap
        for (String key : map.keySet()) {
            System.out.println(key + ": " + map.get(key));
        }
    }
}
```

**#Output:**
```
Alice: 25
Bob: 30
Charlie: 35
```

---

### 74. **What is the difference between `List`, `Set`, and `Map`?**

- **List**: An ordered collection (also known as a sequence). Allows duplicate elements.
- **Set**: A collection that does not allow duplicate elements. It can be unordered.
- **Map**: A collection of key-value pairs, where each key is unique and maps to exactly one value.

#### Example:
```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        // List example
        List<String> list = new ArrayList<>();
        list.add("Apple");
        list.add("Banana");
        list.add("Apple"); // Duplicates allowed
        System.out.println("List: " + list);

        // Set example
        Set<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Apple"); // Duplicates not allowed
        System.out.println("Set: " + set);

        // Map example
        Map<String, Integer> map = new HashMap<>();
        map.put("Apple", 1);
        map.put("Banana", 2);
        map.put("Apple", 3); // Key "Apple" will update the value
        System.out.println("Map: " + map);
    }
}
```

**#Output:**
```
List: [Apple, Banana, Apple]
Set: [Banana, Apple]
Map: {Apple=3, Banana=2}
```

---

### 75. **What is the `try-catch` block in Java?**

- The `try-catch` block is used to handle exceptions in Java. The code that may throw an exception is enclosed in the `try` block, and the handling of the exception occurs in the `catch` block.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        try {
            int result = 10 / 0; // This will throw ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Caught an exception: " + e.getMessage());
        }
    }
}
```

**#Output:**
```
Caught an exception: / by zero
```

---

### 76. **What is the `throws` keyword in Java?**

- The `throws` keyword is used in method declarations to specify that a method can throw exceptions. It is used for checked exceptions.

#### Example:
```java
class Test {
    void division() throws ArithmeticException {
        int result = 10 / 0; // This will throw ArithmeticException
    }
}

public class Main {
    public static void main(String[] args) {
        Test test = new Test();
        try {
            test.division();
        } catch (ArithmeticException e) {
            System.out.println("Caught an exception: " + e.getMessage());
        }
    }
}
```

**#Output:**
```
Caught an exception: / by zero
```

---

### 77. **What is the `final` keyword in Java?**

- The `final` keyword is used to declare constants, prevent method overriding, and prevent inheritance of classes.

#### Example:
```java
final class FinalClass {
    void display() {
        System.out.println("Final class method");
    }
}

// Attempting to extend FinalClass will cause a compilation error
// class ExtendedClass extends FinalClass {}

public class Main {
    public static void main(String[] args) {
        FinalClass obj = new FinalClass();
        obj.display();
    }
}
```

**#Output:**
```
Final class method
```

---

### 78. **What is the `instanceof` operator in Java?**

- The `instanceof` operator is used to test whether an object is an instance of a specific class or subclass.

#### Example:
```java
class Animal {}
class Dog extends Animal {}

public class Main {
    public static void main(String[] args) {
        Animal animal = new Dog();

        if (animal instanceof Dog) {
            System.out.println("animal is an instance of Dog");
        } else {
            System.out.println("animal is NOT an instance of Dog");
        }
    }
}
```

**#Output:**
```
animal is an instance of Dog
```

---

### 79. **What is a Java Package?**

- A **package** is a namespace that organizes a set of related classes and interfaces. Conceptually similar to directories on your computer.

#### Example:
```java
// Assuming you have a package named "com.example"

package com.example;

public class HelloWorld {
    public void greet() {
        System.out.println("Hello, World!");
    }
}

// In another file, you can import this package and use it
```

To use this package in another class:
```java
import com.example.HelloWorld;

public class Main {
    public static void main(String[] args) {
        HelloWorld hello = new HelloWorld();
        hello.greet();
    }
}
```

**#Output:**
```
Hello, World!
```

---

### 80. **What is the purpose of the `main` method in Java?**

- The `main` method is the entry point for any Java application. It is where the program begins execution.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Program started!");
    }
}
```

**#Output:**
```
Program started!
```

---

### 81. **What is a `Thread` in Java




Sure! Let's continue with the explanation of **Thread** in Java and provide more core Java interview questions along with their code examples and outputs.

---

### 81. **What is a `Thread` in Java?**

- A **Thread** is a lightweight process and the smallest unit of execution in a Java program. It allows concurrent execution of two or more parts of a program.

#### Example:
```java
class MyThread extends Thread {
    public void run() {
        System.out.println("Thread is running: " + Thread.currentThread().getName());
    }
}

public class Main {
    public static void main(String[] args) {
        MyThread thread1 = new MyThread();
        MyThread thread2 = new MyThread();
        
        thread1.start(); // Start the first thread
        thread2.start(); // Start the second thread
    }
}
```

**#Output:**
```
Thread is running: Thread-0
Thread is running: Thread-1
```

(Note: The output may vary due to the scheduling of threads.)

---

### 82. **What is the difference between `Thread` and `Runnable` in Java?**

- **Thread** is a class that represents a thread of execution in a program. 
- **Runnable** is an interface that should be implemented by any class whose instances are intended to be executed by a thread.

#### Example:
```java
class MyRunnable implements Runnable {
    public void run() {
        System.out.println("Runnable is running: " + Thread.currentThread().getName());
    }
}

public class Main {
    public static void main(String[] args) {
        MyRunnable myRunnable = new MyRunnable();
        Thread thread = new Thread(myRunnable);
        
        thread.start(); // Start the thread
    }
}
```

**#Output:**
```
Runnable is running: Thread-0
```

---

### 83. **What is the `volatile` keyword in Java?**

- The `volatile` keyword is used in multithreading to indicate that a variable's value will be modified by different threads. Declaring a variable as volatile ensures that changes to it are visible to all threads.

#### Example:
```java
class SharedResource {
    private volatile boolean flag = false;

    public void setFlag() {
        flag = true; // Update the flag
    }

    public void checkFlag() {
        while (!flag) {
            // Wait for the flag to be true
        }
        System.out.println("Flag is set to true!");
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        SharedResource resource = new SharedResource();
        
        Thread writer = new Thread(() -> {
            try {
                Thread.sleep(1000); // Simulate some work
            } catch (InterruptedException e) {
                e.printStackTrace();
            }
            resource.setFlag(); // Set the flag
        });

        Thread reader = new Thread(() -> resource.checkFlag()); // Check the flag

        reader.start();
        writer.start();
        
        writer.join();
        reader.join();
    }
}
```

**#Output:**
```
Flag is set to true!
```

---

### 84. **What is the `join()` method in Java?**

- The `join()` method allows one thread to wait for the completion of another thread. When a thread calls `join()`, it pauses its execution until the thread on which `join()` is called completes.

#### Example:
```java
class MyThread extends Thread {
    public void run() {
        try {
            Thread.sleep(1000); // Simulate work
            System.out.println(Thread.currentThread().getName() + " completed.");
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        MyThread thread = new MyThread();
        thread.start();
        thread.join(); // Main thread will wait for thread to complete
        System.out.println("Main thread completed.");
    }
}
```

**#Output:**
```
Thread-0 completed.
Main thread completed.
```

---

### 85. **What is `synchronized` block in Java?**

- A `synchronized` block is used to restrict access to a block of code by multiple threads. It allows only one thread to execute the block at a time.

#### Example:
```java
class Counter {
    private int count = 0;

    void increment() {
        synchronized (this) {
            count++; // Critical section
        }
    }

    int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        Counter counter = new Counter();

        Thread t1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread t2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        t1.start();
        t2.start();
        t1.join();
        t2.join();

        System.out.println("Final count: " + counter.getCount());
    }
}
```

**#Output:**
```
Final count: 2000
```

---

### 86. **What is the `Thread.sleep()` method in Java?**

- The `Thread.sleep(long millis)` method is used to pause the execution of the current thread for a specified period (in milliseconds).

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Thread is going to sleep.");
        try {
            Thread.sleep(2000); // Sleep for 2 seconds
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println("Thread woke up!");
    }
}
```

**#Output:**
```
Thread is going to sleep.
(Thread sleeps for 2 seconds)
Thread woke up!
```

---

### 87. **What are Java annotations?**

- Annotations are metadata that provide information about the code but are not part of the program itself. They can be used for various purposes such as providing instructions to the compiler, generating code, or configuring frameworks.

#### Example:
```java
@interface MyAnnotation {
    String value();
}

@MyAnnotation(value = "Hello, Annotations!")
public class Main {
    public static void main(String[] args) {
        MyAnnotation annotation = Main.class.getAnnotation(MyAnnotation.class);
        System.out.println(annotation.value());
    }
}
```

**#Output:**
```
Hello, Annotations!
```

---

### 88. **What is the `assert` keyword in Java?**

- The `assert` keyword is used for debugging purposes to make an assertion, which is a statement that checks a condition. If the condition evaluates to false, an `AssertionError` is thrown.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        int value = 5;
        assert value > 10 : "Value should be greater than 10"; // Assertion
        System.out.println("Assertion passed!");
    }
}
```

**#Output:**
```
Exception in thread "main" java.lang.AssertionError: Value should be greater than 10
```

(Note: To enable assertions in the JVM, run the program with the `-ea` flag.)

---

### 89. **What is `Lambda` expression in Java?**

- A **Lambda** expression is a feature introduced in Java 8 that allows you to write concise and functional-style code. It provides a clear and concise way to represent a single method interface (functional interface) using an expression.

#### Example:
```java
import java.util.Arrays;
import java.util.List;

public class Main {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie");

        // Using a Lambda expression to print names
        names.forEach(name -> System.out.println(name));
    }
}
```

**#Output:**
```
Alice
Bob
Charlie
```

---

### 90. **What are Functional Interfaces in Java?**

- A **Functional Interface** is an interface that has exactly one abstract method. They can contain multiple default or static methods. Lambda expressions can be used to implement functional interfaces.

#### Example:
```java
@FunctionalInterface
interface MyFunctionalInterface {
    void display();
}

public class Main {
    public static void main(String[] args) {
        MyFunctionalInterface myFunc = () -> System.out.println("Functional Interface Method");
        myFunc.display();
    }
}
```

**#Output:**
```
Functional Interface Method
```

---

### 91. **What is the `Optional` class in Java?**

- The `Optional` class is a container object used to contain not-null objects. It is used to avoid `NullPointerExceptions` and to represent optionality in values.

#### Example:
```java
import java.util.Optional;

public class Main {
    public static void main(String[] args) {
        Optional<String> optionalValue = Optional.ofNullable(null);
        
        // Checking if a value is present
        if (optionalValue.isPresent()) {
            System.out.println("Value: " + optionalValue.get());
        } else {
            System.out.println("Value is absent.");
        }
    }
}
```

**#Output:**
```
Value is absent.
```

---

### 92. **What is Stream API in Java?**

- The **Stream API** is a feature introduced in Java 8 that allows you to process sequences of elements (such as collections) in a functional style. It provides operations for filtering, mapping, and reducing collections.

Let's continue with more **Core Java interview questions** along with code examples and outputs:

---

### 93. **What is the `Comparator` interface in Java?**

- The `Comparator` interface is used to define custom ordering for objects. It provides a `compare()` method to compare two objects.
- You can use `Comparator` when you need a custom sort order other than the natural ordering defined by `Comparable`.

#### Example:
```java
import java.util.*;

class Student {
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String toString() {
        return name + " (" + age + ")";
    }
}

class AgeComparator implements Comparator<Student> {
    public int compare(Student s1, Student s2) {
        return Integer.compare(s1.age, s2.age); // Compare based on age
    }
}

public class Main {
    public static void main(String[] args) {
        List<Student> students = new ArrayList<>();
        students.add(new Student("Alice", 24));
        students.add(new Student("Bob", 22));
        students.add(new Student("Charlie", 23));

        // Sort by age using Comparator
        Collections.sort(students, new AgeComparator());
        System.out.println(students);
    }
}
```

**#Output:**
```
[Bob (22), Charlie (23), Alice (24)]
```

---

### 94. **What is the `Comparable` interface in Java?**

- The `Comparable` interface defines the natural ordering of objects using the `compareTo()` method. This is usually implemented by a class to define how objects of that class should be compared.

#### Example:
```java
import java.util.*;

class Student implements Comparable<Student> {
    String name;
    int age;

    Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public int compareTo(Student other) {
        return this.name.compareTo(other.name); // Sort by name
    }

    public String toString() {
        return name + " (" + age + ")";
    }
}

public class Main {
    public static void main(String[] args) {
        List<Student> students = new ArrayList<>();
        students.add(new Student("Alice", 24));
        students.add(new Student("Bob", 22));
        students.add(new Student("Charlie", 23));

        // Sort by natural ordering (name) using Comparable
        Collections.sort(students);
        System.out.println(students);
    }
}
```

**#Output:**
```
[Alice (24), Bob (22), Charlie (23)]
```

---

### 95. **What is the difference between `HashMap` and `Hashtable` in Java?**

| Feature         | `HashMap`                     | `Hashtable`                        |
|-----------------|-------------------------------|------------------------------------|
| Synchronization | Not synchronized (Thread-unsafe)| Synchronized (Thread-safe)         |
| Null Keys/Values| Allows one null key and multiple null values| Does not allow null keys or values |
| Performance     | Faster (no overhead of synchronization)| Slower (due to synchronization)   |

#### Example (Demonstrating `HashMap` allowing nulls):
```java
import java.util.HashMap;

public class Main {
    public static void main(String[] args) {
        HashMap<String, Integer> map = new HashMap<>();
        map.put(null, 1);  // Null key allowed
        map.put("Bob", null);  // Null value allowed
        
        System.out.println(map);
    }
}
```

**#Output:**
```
{null=1, Bob=null}
```

---

### 96. **What is the `enum` keyword in Java?**

- `enum` is a special data type that defines a collection of constants. It is used to represent a fixed set of constants (e.g., days of the week, colors, etc.).

#### Example:
```java
enum Day {
    SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY
}

public class Main {
    public static void main(String[] args) {
        Day today = Day.MONDAY;

        // Print all days in enum
        for (Day day : Day.values()) {
            System.out.println(day);
        }

        // Check the current day
        if (today == Day.MONDAY) {
            System.out.println("It's Monday!");
        }
    }
}
```

**#Output:**
```
SUNDAY
MONDAY
TUESDAY
WEDNESDAY
THURSDAY
FRIDAY
SATURDAY
It's Monday!
```

---

### 97. **What is the difference between `==` and `equals()` method in Java?**

- `==` compares **reference** or memory locations of two objects.
- `equals()` compares the **content** of two objects, depending on how the method is overridden in the class.

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        String s1 = new String("Hello");
        String s2 = new String("Hello");

        // Using == operator
        System.out.println("Using == : " + (s1 == s2)); // false, because they are different objects

        // Using equals() method
        System.out.println("Using equals(): " + s1.equals(s2)); // true, because content is the same
    }
}
```

**#Output:**
```
Using == : false
Using equals(): true
```

---

### 98. **What is `finalize()` method in Java?**

- The `finalize()` method is called by the garbage collector just before an object is destroyed to give it a chance to clean up resources.
- However, it is not guaranteed that `finalize()` will be called, and it is considered deprecated in newer versions of Java.

#### Example:
```java
class Resource {
    @Override
    protected void finalize() {
        System.out.println("Finalize method called before garbage collection");
    }
}

public class Main {
    public static void main(String[] args) {
        Resource res = new Resource();
        res = null;  // Making the object eligible for garbage collection

        // Requesting JVM for garbage collection
        System.gc();
    }
}
```

**#Output:**
```
Finalize method called before garbage collection
```

(Note: The `finalize()` method may not be invoked immediately; its invocation depends on when the JVM runs the garbage collector.)

---

### 99. **What is a `try-with-resources` statement in Java?**

- The `try-with-resources` statement is used to automatically close resources (like files, sockets, etc.) that implement `AutoCloseable` or `Closeable` interface after the block is executed.

#### Example:
```java
import java.io.*;

public class Main {
    public static void main(String[] args) {
        try (BufferedReader br = new BufferedReader(new FileReader("test.txt"))) {
            String line;
            while ((line = br.readLine()) != null) {
                System.out.println(line);
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

**#Output:**
- The output will display the contents of `test.txt` if it exists, and the file will be automatically closed after reading.

---

### 100. **What is the difference between `String`, `StringBuilder`, and `StringBuffer`?**

| Feature            | `String`                    | `StringBuilder`                   | `StringBuffer`                    |
|--------------------|-----------------------------|-----------------------------------|-----------------------------------|
| Mutability         | Immutable                   | Mutable                          | Mutable                          |
| Thread Safety      | Not thread-safe             | Not thread-safe                  | Thread-safe                      |
| Performance        | Slower for concatenation    | Faster than `String`             | Slower than `StringBuilder` due to synchronization |

#### Example:
```java
public class Main {
    public static void main(String[] args) {
        // String (Immutable)
        String str = "Hello";
        str = str + " World";  // New object is created
        System.out.println(str);

        // StringBuilder (Mutable, Not thread-safe)
        StringBuilder sb = new StringBuilder("Hello");
        sb.append(" World");
        System.out.println(sb);

        // StringBuffer (Mutable, Thread-safe)
        StringBuffer sbf = new StringBuffer("Hello");
        sbf.append(" World");
        System.out.println(sbf);
    }
}
```

**#Output:**
```
Hello World
Hello World
Hello World
```

---

### 101. **What is the difference between `abstract class` and `interface` in Java?**

| Feature                    | Abstract Class                    | Interface                           |
|----------------------------|------------------------------------|-------------------------------------|
| Methods                    | Can have both abstract and non-abstract methods | Can have only abstract methods (before Java 8), default methods (from Java 8), and static methods |
| Variables                  | Can have instance variables        | Can only have `public static final` variables |
| Inheritance                | Can extend one class               | Can implement multiple interfaces   |

#### Example (Abstract Class):
```java
abstract class Animal {
    abstract void sound();

    void eat() {
        System.out.println("Animal is eating");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound(); // Abstract method
        dog.eat();   // Concrete method
    }
}
```

**

#Output:**
```
Dog barks
Animal is eating
```

#### Example (Interface):
```java
interface Animal {
    void sound();
}

class Dog implements Animal {
    public void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.sound();
    }
}
```

**#Output:**
```
Dog barks
```

---

