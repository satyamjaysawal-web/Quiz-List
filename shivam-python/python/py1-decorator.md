### **Python Decorators - Hinglish Mein Samajhiye**

#### **Decorator Kya Hai?**
Python me **decorator** ek aisi technique hai jo ek function, method, ya class ki behavior ko modify (badalne) ke kaam aata hai bina uska asli code change kiye. 

Decorator ek function ko "wrap" karta hai, uska kaam hai:
1. Function ke pehle ya baad kuch additional kaam karna.
2. Core logic ko touch kiye bina extra functionality add karna.

Python me decorators ka use `@` symbol ke saath hota hai. 

---

#### **Decorator Kaam Kaise Karta Hai?**

1. **Function ko Input Leta Hai:** 
   Ek decorator ek function ko as input leta hai.

2. **Wrapper Function:** 
   Us function ke upar ek aur function (wrapper) banata hai jo additional kaam karta hai.

3. **Modified Function Return Karta Hai:** 
   Jo function decorator ke andar wrap hota hai, usko modify karke wapas deta hai.

---

#### **Decorator Kyon Zaruri Hai?**
- Code ko clean aur reusable banata hai.
- Alag-alag functions ke liye common functionality (logging, timing, validation) bar-bar likhne ki zarurat nahi hoti.
- Functionality ko dynamically (runtime par) add kar sakte ho.

---

#### **Decorator Kab Istemaal Karein?**
- Jab aapko **logging** karni ho (e.g., function call record karna).
- Jab aapko **security** ke liye access control check karna ho.
- **Performance** track karna ho (e.g., execution time measure karna).
- **Code reuse** ke liye common features implement karne ho.

---

### **Python Decorator Kaise Banate Hain?**

#### **Simple Decorator Example**

```python
# Step 1: Decorator define karein
def my_decorator(func):
    def wrapper():
        print("Function ke pehle kaam ho raha hai.")
        func()  # Original function ko call karte hain
        print("Function ke baad kaam ho raha hai.")
    return wrapper

# Step 2: Decorator ko lagayein
@my_decorator
def say_hello():
    print("Hello, Duniya!")

# Step 3: Function call karein
say_hello()
```

**Output:**
```
Function ke pehle kaam ho raha hai.
Hello, Duniya!
Function ke baad kaam ho raha hai.
```

---

#### **Iska Breakdown (Working Process):**

1. `@my_decorator` likhne ka matlab hai `say_hello` function ko `my_decorator` ke andar wrap karna.
2. `my_decorator` ek wrapper function banata hai jo:
   - `func()` ke pehle aur baad kaam karta hai.
3. Wrapper function ko return kiya jaata hai aur original `say_hello` ki jagah use hota hai.

---

### **Arguments Ke Sath Decorator**

Kabhi kabhi hume decorator me arguments pass karne hote hain. Aise cases me ek decorator factory banate hain jo arguments le aur actual decorator ko return kare.

```python
# Step 1: Decorator with arguments banaiye
def repeat(times):
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(times):
                func(*args, **kwargs)  # Function ko repeat karo
        return wrapper
    return decorator

# Step 2: Apply karein
@repeat(times=3)
def greet(name):
    print(f"Hello, {name}!")

# Step 3: Function call karein
greet("Amit")
```

**Output:**
```
Hello, Amit!
Hello, Amit!
Hello, Amit!
```

---

#### **Built-in Decorators in Python**

Python me kuch pre-defined decorators milte hain:
1. `@staticmethod`: Method ko static method banata hai.
2. `@classmethod`: Class ke saath bound methods banata hai.
3. `@property`: Method ko ek property ki tarah treat karta hai.

---

### **Real-Life Example: Logging Decorator**

Ek practical example jisme hum function ke execution time ko measure karte hain:

```python
import time

def log_execution_time(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()  # Time start
        result = func(*args, **kwargs)  # Original function call
        end_time = time.time()  # Time end
        print(f"{func.__name__} executed in {end_time - start_time:.4f} seconds")
        return result
    return wrapper

@log_execution_time
def slow_function():
    time.sleep(2)  # 2 second ka delay
    print("Function khatam ho gaya")

slow_function()
```

**Output:**
```
Function khatam ho gaya
slow_function executed in 2.0001 seconds
```

---

### **Summary in Hinglish**

- **Kya Hai:** Decorator ek tarika hai kisi function ka behavior modify karne ka bina function ka asli code badle.
- **Kyon Use Karein:** Reusable code, clean logic, aur alag-alag tasks (logging, timing) ko automate karne ke liye.
- **Kaise Kaam Karta Hai:** Ek function ko wrap karta hai aur wrapper function additional kaam karta hai.
- **Example:** Timing track karna, arguments validate karna, ya koi repeated kaam automate karna.




****
****
