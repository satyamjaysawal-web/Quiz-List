### **"Hoist Hona" Ka Matlab Kya Hai?**

JavaScript mein **"hoisting"** ka matlab hota hai **variable aur function declarations ka code ke execution ke pehle unke scope ke top pe move ho jaana**.  

Yeh JavaScript ka **default behavior** hai, jisse aisa lagta hai ki variables aur functions unke declare hone se pehle hi access ho rahe hain.  

---

## 🔎 **"Hoist Hona" Ka Matlab Samajhne Ke Liye**  

1. **JavaScript ke compilation phase ke time pe**:
   - **Variables ke declarations ko upar move kiya jata hai**, par unko initialize nahi kiya jata.  
   - **Function declarations ko poore ke poore upar move kar diya jata hai**.  

2. **Code ke execution ke time pe**:
   - Variables agar `var` se declare kiye gaye hain, toh unka value `undefined` hota hai jab tak unhe initialize nahi karte.  
   - `let` aur `const` wale variables bhi hoist hote hain, par unka **use karna TDZ (Temporal Dead Zone)** ke wajah se error deta hai.

---

### **Example ke Saath Samajhte Hain**  

#### 1️⃣ **Hoisting with `var`**  
```javascript
console.log(a); // Output: undefined  
var a = 10;  
console.log(a); // Output: 10  
```

**JavaScript ka behavior (hoisting ke baad):**  
```javascript
var a;           // Declaration hoist ho gaya top pe  
console.log(a);  // undefined (abhi value assign nahi hui)  
a = 10;          // Value yahan assign hui  
console.log(a);  // 10  
```

---

#### 2️⃣ **Hoisting with `let` aur `const`**  

```javascript
console.log(b); // ReferenceError: Cannot access 'b' before initialization
let b = 20;  
```

**Explanation:**  
- Yahan `let` ka declaration hoist hota hai, **par use karne pe error deta hai** kyunki yeh "Temporal Dead Zone" (TDZ) mein hota hai.  

**TDZ ka matlab:** Code ke woh section jisme variable declare toh ho gaya hota hai, lekin usse use karna allowed nahi hota.  

---

#### 3️⃣ **Hoisting with Functions**  

```javascript
sayHello(); // Output: Hello, World!

function sayHello() {
    console.log("Hello, World!");
}
```

**Explanation:**  
- Pure function declaration ko JavaScript top pe le jata hai. Isliye `sayHello()` function ko declare hone se pehle bhi call kar sakte ho.  

---

#### 4️⃣ **Hoisting with Function Expressions**  

```javascript
sayHi(); // TypeError: sayHi is not a function

var sayHi = function() {
    console.log("Hi!");
};
```

**Explanation:**  
- Yahan sirf `sayHi` ka variable declaration hoist hota hai (`undefined` ki tarah).  
- Function assignment baad mein hota hai.  

---

### 🎯 **Hoisting Ka Summary**  

1. **Variables**:  
   - `var`: Declaration hoist hoti hai, par value `undefined` hota hai.  
   - `let` aur `const`: Hoist hoti hain, lekin unka use TDZ ke wajah se error deta hai.  

2. **Functions**:  
   - **Function declarations**: Pure functions hoist hote hain.  
   - **Function expressions**: Sirf variable ka declaration hoist hota hai, assignment nahi.  

3. **Classes**:  
   - Classes bhi hoist hote hain, par use karne pe TDZ ki wajah se error aata hai.  

---

### 🚀 **Samajhne Ka Easy Example**  

```javascript
console.log(x); // undefined
var x = 5;

sayHello(); // Hello, World!
function sayHello() {
    console.log("Hello, World!");
}

console.log(y); // ReferenceError
let y = 10;
```

**Output:**
```text
undefined
Hello, World!
ReferenceError: Cannot access 'y' before initialization
```

---

### 🤔 **"Hoist Hona" Ka Matlab Ek Line Mein**  
"Hoisting ka matlab hai **JavaScript compiler ke andar variables aur functions ka declaration automatically code ke top pe move ho jaana**, execution ke pehle."  
