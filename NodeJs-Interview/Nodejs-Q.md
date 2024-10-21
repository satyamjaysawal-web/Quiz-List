
---
---
Here is a table of advanced topics for Node.js, categorized for better understanding:

| **Category**                | **Advanced Topics**                                                                 |
|-----------------------------|-------------------------------------------------------------------------------------|
| **Concurrency & Performance**| - Event Loop and Non-blocking I/O                                                   |
|                             | - Cluster Module and Load Balancing                                                 |
|                             | - Worker Threads for Multithreading                                                 |
|                             | - Caching Strategies (e.g., Redis, in-memory caching)                               |
|                             | - Streaming and Buffering                                                           |
|                             | - Performance Optimization (profiling, monitoring, V8 optimizations)                |
|                             | - Benchmarking (using `autocannon`, `wrk`)                                          |
| **Asynchronous Programming** | - Promises and Async/Await                                                          |
|                             | - Async Control Flow with `async` library                                           |
|                             | - Handling Errors in Async Code (promise rejections, error boundaries)              |
|                             | - Async Iterators and Generators                                                    |
| **Security**                 | - JWT Authentication and Authorization                                             |
|                             | - Data Encryption and Hashing (bcrypt, crypto)                                      |
|                             | - SSL/TLS and HTTPS                                                                 |
|                             | - OWASP Top 10 and Node.js                                                          |
|                             | - Security Best Practices (Helmet.js, CSRF tokens)                                  |
|                             | - Securing REST APIs (rate limiting, IP whitelisting, OAuth 2.0)                    |
| **Networking**               | - WebSockets for Real-time Communication                                            |
|                             | - HTTP/2 in Node.js                                                                 |
|                             | - Socket.IO for Bidirectional Event-based Communication                             |
|                             | - gRPC for Efficient RPC Calls                                                      |
|                             | - Server-Sent Events (SSE)                                                          |
| **Microservices & Architecture** | - Microservices Design Patterns (e.g., Circuit Breakers, Saga)                |
|                             | - Service Discovery and Load Balancing in Node.js                                   |
|                             | - API Gateway (e.g., using Express, Fastify, NGINX)                                 |
|                             | - Message Brokers (RabbitMQ, Apache Kafka)                                          |
|                             | - Distributed Systems (consistency, fault tolerance)                                |
| **Database & ORMs**          | - Advanced Querying and Indexing (MongoDB, PostgreSQL)                             |
|                             | - ORMs like Sequelize, TypeORM                                                      |
|                             | - Database Transactions                                                             |
|                             | - NoSQL vs SQL Optimization in Node.js                                              |
|                             | - Connection Pooling                                                                |
| **Testing**                  | - Unit Testing and Test Coverage (Mocha, Jest, Chai)                               |
|                             | - E2E Testing with Cypress                                                          |
|                             | - Mocking and Stubbing (Sinon.js)                                                   |
|                             | - Load Testing (Artillery, Apache Benchmark)                                        |
|                             | - Integration Testing with Supertest and Postman                                    |
| **DevOps & Deployment**      | - Containerization with Docker                                                      |
|                             | - Kubernetes and Node.js Service Orchestration                                      |
|                             | - Continuous Integration/Continuous Deployment (CI/CD) Pipelines                    |
|                             | - Environment Variables and Secrets Management (dotenv, HashiCorp Vault)            |
|                             | - Cloud Deployment (AWS, GCP, Azure, Heroku)                                        |
|                             | - Monitoring and Logging (Winston, Morgan, Prometheus, ELK stack)                   |
| **Native Modules**           | - Native Addons in C++ with Node.js                                                 |
|                             | - Using `ffi-napi` for Foreign Function Interface                                   |
|                             | - Memory Management and Garbage Collection                                          |
|                             | - Node.js Internals and V8 Engine Integration                                       |
| **Package Management**       | - Monorepo Management (Lerna, Nx)                                                   |
|                             | - Custom npm Packages and Publishing                                                |
|                             | - Semantic Versioning and Dependency Management                                     |
|                             | - Handling Large Dependencies and Tree Shaking                                      |

These topics cover various aspects of Node.js at an advanced level, ranging from performance tuning to security, testing, and scaling applications.
---
---

### Node.js Tricky Questions

1. **Event Loop Kya Hai?**
   - Explain karo ki Node.js ka event loop kaise kaam karta hai. Iske different phases kya hain?

2. **Callback Hell Kya Hota Hai?**
   - Callback hell se aap kaise bachein? Iska ek example do aur usse kaise avoid kar sakte hain?

3. **Asynchronous vs Synchronous Code:**
   - Asynchronous aur synchronous code mein kya differences hain? Ek example do jismein aap dono types ka use karte ho.

4. **Promises Kya Hain?**
   - Promises kaise kaam karte hain? Ek example do jismein promise ka use kiya gaya ho.

5. **Async/Await Kya Hai?**
   - Async/await kaise kaam karta hai aur isse kaise use karte hain? Ek chota sa example do.

6. **Memory Leak Kya Hota Hai?**
   - Memory leak ka kya matlab hai? Aap isse kaise identify aur fix kar sakte hain?

7. **EventEmitter Ki Limitations:**
   - Kya aap EventEmitter ke kuch limitations bata sakte hain? Aur iska alternative kya ho sakta hai?

8. **Stream Kya Hota Hai?**
   - Node.js mein stream kya hota hai? Iske types aur use cases kya hain?

9. **Middleware Kya Hai?**
   - Middleware ka kya role hota hai Express.js applications mein? Ek example do.

10. **Buffer Kya Hota Hai?**
    - Node.js mein Buffer ka kya use hota hai? Ek example ke sath samjhao.

11. **Cluster Module Kya Hai?**
    - Cluster module ka kya use hai Node.js applications mein? Isse kaise implement karte hain?

12. **CORS Kya Hota Hai?**
    - Cross-Origin Resource Sharing (CORS) kya hai aur aap isse kaise handle karte hain?

13. **Error Handling Kaise Karein?**
    - Node.js mein error handling ke best practices kya hain? Ek example do.

14. **Process vs Thread:**
    - Node.js mein process aur thread ka kya difference hai? Kya aap inke advantages aur disadvantages bata sakte hain?

15. **Single Threaded vs Multi-Threaded:**
    - Node.js single-threaded hai. Iska kya matlab hai aur iske advantages kya hain?

16. **NPM Kya Hai?**
    - Node Package Manager (NPM) kya hai aur aap isse kaise use karte hain? 

17. **Deployment Best Practices:**
    - Node.js applications ko deploy karne ke best practices kya hain?

18. **How to Handle Uncaught Exceptions?**
    - Uncaught exceptions ko handle karne ke liye kya approach lena chahiye?

19. **Environment Variables Kya Hote Hain?**
    - Environment variables ka kya use hai? Kaise set aur retrieve karte hain?

20. **API Rate Limiting Kya Hai?**
    - API rate limiting kya hai aur aap isse kaise implement karte hain?


---
---
---
### JWT (JSON Web Token) in Node.js

**JWT (JSON Web Token)** ek **compact**, **URL-safe**, aur **self-contained token** hota hai jo user authentication aur authorization ke liye widely use hota hai. Ye mainly stateless authentication ko handle karne ke liye hota hai, jahan user ko authenticate karne ke baad ek token diya jata hai, jo client-side par store hota hai aur har request ke sath server ko bheja jata hai.

#### 1. **Key Points:**
- **Compact**: JSON Web Token ka size small hota hai, jo ise fast aur efficient banata hai.
- **Self-contained**: Token ke andar hi user information encode hoti hai, jise server ko dobara database access karne ki zarurat nahi hoti.
- **Stateless**: JWT ko server-side sessions ke bina use kiya ja sakta hai, kyunki server ko session data maintain nahi karna padta.

#### 2. **JWT Structure**:
JWT mainly 3 parts mein divided hota hai, aur ye base64-encoded hota hai:
1. **Header**: Algorithm aur token type ko define karta hai (e.g., HS256).
2. **Payload**: User-related information ko contain karta hai (like `userId`, `email`, etc.).
3. **Signature**: Isse token ko verify karne ke liye use kiya jata hai.

```plaintext
header.payload.signature
```

#### 3. **JWT Flow**:
1. User login karta hai aur credentials ko send karta hai.
2. Server credentials verify karta hai aur agar valid hote hain, to ek JWT generate karta hai.
3. Client JWT ko store karta hai (usually in **localStorage** or **cookies**).
4. Har request ke sath, client JWT ko **Authorization** header mein bhejta hai.
5. Server JWT ko verify karta hai aur agar valid hota hai, to request process karta hai.

#### 4. **Example: JWT in Node.js**

Pehle hume `jsonwebtoken` aur `express` install karna hoga:

```bash
npm install express jsonwebtoken body-parser
```

#### 5. **Code Example:**

```javascript
// Required modules ko import kar rahe hain
const express = require('express');
const jwt = require('jsonwebtoken');
const bodyParser = require('body-parser');

const app = express();
const PORT = 3000;

// Middleware to parse JSON body
app.use(bodyParser.json());

// Secret key (Isse aap apni marzi se set kar sakte hain)
const SECRET_KEY = 'your_secret_key';

// Login route (Token generate karne ke liye)
app.post('/login', (req, res) => {
    const { username, password } = req.body;

    // Normally, aapko yahan actual database check karna hoga
    if (username === 'john' && password === 'password123') {
        // Payload mein user-related data store kar rahe hain
        const payload = {
            username: username,
            role: 'admin'
        };

        // JWT generate karte hain (valid for 1 hour)
        const token = jwt.sign(payload, SECRET_KEY, { expiresIn: '1h' });

        res.json({ message: 'Login successful', token: token });
    } else {
        res.status(401).json({ message: 'Invalid credentials' });
    }
});

// Protected route (JWT ko verify karna)
app.get('/protected', (req, res) => {
    // Token Authorization header se nikal rahe hain
    const token = req.headers['authorization'];

    if (!token) {
        return res.status(403).json({ message: 'Token is missing' });
    }

    // JWT verify kar rahe hain
    jwt.verify(token, SECRET_KEY, (err, decoded) => {
        if (err) {
            return res.status(403).json({ message: 'Invalid token' });
        }

        // Agar token valid hai, to ye message return karega
        res.json({ message: 'Access granted', user: decoded });
    });
});

// Server ko listen kar rahe hain
app.listen(PORT, () => {
    console.log(`Server running on http://localhost:${PORT}`);
});
```

### #output
1. **Login Route**:
   - Agar aap `/login` route par `POST` request bhejte hain with correct username and password, to ye response milega:
   ```json
   {
       "message": "Login successful",
       "token": "your_jwt_token_here"
   }
   ```

2. **Protected Route**:
   - Agar aap `/protected` route par request bhejte hain aur `Authorization` header mein JWT send karte hain, to response kuch aisa hoga:
   ```json
   {
       "message": "Access granted",
       "user": {
           "username": "john",
           "role": "admin",
           "iat": 1629800000,
           "exp": 1629803600
       }
   }
   ```

3. Agar JWT invalid ya missing hota hai, to error response aayega:
   ```json
   {
       "message": "Invalid token"
   }
   ```
---
Yahan par **Authentication** aur **Authorization** ke beech ka comparison table format mein diya gaya hai:

| **Aspect**                | **Authentication**                                    | **Authorization**                                     |
|---------------------------|------------------------------------------------------|-------------------------------------------------------|
| **Definition**            | User ki identity verify karna.                       | User ko specific resources ya actions ka access dena. |
| **Purpose**               | Ensure karta hai ki user kaun hai.                  | Ensure karta hai ki user ko kya karne ki permission hai. |
| **Process**               | Credentials (username/password, tokens) ko check karta hai. | User ki permissions ko check karta hai (roles, access levels). |
| **Outcome**               | User ko verify kiya jata hai ya reject kiya jata hai. | User ko resources ya actions ko access dene ya deny karne ka faisla hota hai. |
| **Examples**              | Login process, biometric verification (fingerprint). | User roles (admin, user, guest) ke through resource access. |
| **When it Happens**       | Sabse pehle user login hone par.                      | Authentication ke baad, jab user resource access karne ki koshish karta hai. |
| **Implementation**        | Usually involves passwords, tokens, or biometric data. | Usually involves access control lists (ACLs), roles, and permissions. |
| **Tools/Protocols**       | OAuth, OpenID, SAML, LDAP.                           | Role-Based Access Control (RBAC), Attribute-Based Access Control (ABAC). |

### Summary:
- **Authentication** ka focus user ki identity par hai, jabki **Authorization** ka focus user ke access rights par hai.
- Authentication ke bina authorization ka kaam nahi hota, kyunki pehle user ko verify karna zaruri hai, phir hi uski permissions check ki ja sakti hain.

Agar aapko kisi aur detail ki zarurat hai ya koi specific question hai, to bataiye!
### 6. **JWT Security Concerns**:
- **Secret Key**: Hamesha strong aur random secret key use karein.
- **HTTPS**: JWT ko sensitive data ke sath use karte waqt **HTTPS** zarur use karein, taki token sniffing avoid ho.
- **Short Expiry**: Token ko chhote time ke liye valid rakhein (jaise 1 hour), taki security breaches ko minimize kiya ja sake.

### 7. **Use Cases**:
- **Authentication**: JWT ko widely use kiya jata hai user authentication ke liye.
- **Authorization**: Token ke through user ke role ya access level ko define kiya ja sakta hai.
- **Stateless APIs**: JWT ko stateless REST APIs mein commonly use kiya jata hai.

Agar aapko JWT ke baare mein aur detail chahiye ya kisi specific topic par baat karni hai, to bataiye!

---
---


Node.js mein events ka concept bahut important hai, kyunki yeh asynchronous programming ko manage karne mein help karta hai. Node.js ek event-driven architecture use karta hai, jismein events ka creation aur handling hota hai. Yeh process asynchronous hota hai, matlab ki jab ek event fire hota hai, tab application kisi doosri task ko execute kar sakta hai bina wait kiye. 

### Node.js Mein Events Kaise Kaam Karte Hain:

1. **EventEmitter Class**:
   Node.js mein `events` module hota hai, jismein `EventEmitter` class define ki gayi hai. Iska use custom events create karne aur unhe handle karne ke liye hota hai.

2. **Events Ko Emit Karna**:
   Aap events ko emit (fire) kar sakte hain jab bhi aapko koi specific action perform karna hota hai.

3. **Event Listeners**:
   Aap events ke liye listeners attach karte hain, jo specific events hone par execute hote hain.

### Example:

Chalo ek simple example dekhte hain jismein hum `EventEmitter` ka use karte hain:

```javascript
// 'events' module ko require karna
const EventEmitter = require('events');

// Ek instance create karna
const myEmitter = new EventEmitter();

// Event listener define karna
myEmitter.on('event', () => {
    console.log('An event occurred!');
});

// Event emit karna
myEmitter.emit('event');
```

### Code Explanation:

1. **Require Events Module**: Pehle hum `events` module ko require karte hain.
2. **Create EventEmitter Instance**: Fir hum `EventEmitter` ka instance create karte hain.
3. **Define Event Listener**: `on` method ka use karke hum listener define karte hain, jo `event` name ka event hone par execute hoga.
4. **Emit Event**: `emit` method ka use karke hum event ko fire karte hain, jisse console par message print hota hai.

### Asynchronous Events

Node.js mein kuch built-in asynchronous events bhi hote hain, jaise ki HTTP requests, file system events, etc. Yeh events callbacks ke through handle kiye jaate hain.

### Conclusion

Node.js ka event-driven model applications ko efficient aur scalable banata hai. Agar aapko aur detailed information chahiye ya koi specific use case hai, toh batayein!


---

Chalo, ek choti si kahani ke zariye samjhte hain ki Node.js mein events kaise kaam karte hain.

### Kahani: Rohan ka Birthday Party

Ek baar ki baat hai, Rohan apna birthday party organize kar raha tha. Usne apne doston ko bulaya aur unko alag-alag tasks diye. Rohan ko pata tha ki agar sab log apne-apne tasks par dhyan denge, toh party bahut acchi hogi. Yeh kahani Rohan aur uski dosti ko events aur listeners ki tarah represent karegi.

#### Characters:
- **Rohan**: EventEmitter (party organizer)
- **Doston**: Event Listeners (tasks perform karne wale)

#### Scene 1: Party Ka Announcement

Rohan ne sab doston ko invite kiya aur unse kaha ki "Party hone wali hai! Aap sabko aana hai!"

```javascript
const EventEmitter = require('events');
const birthdayParty = new EventEmitter();

// Doston ke liye listener define karte hain
birthdayParty.on('partyInvite', (name) => {
    console.log(`${name} ko party ka invite mila!`);
});

// Rohan invites sabko
birthdayParty.emit('partyInvite', 'Rahul');
birthdayParty.emit('partyInvite', 'Sneha');
birthdayParty.emit('partyInvite', 'Amit');
```

**Explanation**: Rohan ne sabko invite kiya (event emit kiya), aur doston ne apne reactions diye (listeners). Jab Rohan ne event emit kiya, toh sab doston ka response aaya.

#### Scene 2: Tasks Assign Karna

Rohan ne decide kiya ki alag-alag tasks assign karega, jaise ki cake lana, decorations karna, aur games arrange karna.

```javascript
birthdayParty.on('bringCake', () => {
    console.log('Cake lekar aana!');
});

birthdayParty.on('decorate', () => {
    console.log('Party ke liye decorations kar rahe hain!');
});

birthdayParty.on('arrangeGames', () => {
    console.log('Games arrange ho rahe hain!');
});

// Tasks ko emit karte hain
birthdayParty.emit('bringCake');
birthdayParty.emit('decorate');
birthdayParty.emit('arrangeGames');
```

**Explanation**: Rohan ne tasks ko emit kiya, aur doston ne apne tasks ko execute kiya. Jaise hi tasks emit hue, doston ne apne kaam shuru kiye.

#### Scene 3: Party Ka Time

Jab sab kuch tayaar ho gaya, Rohan ne announce kiya, "Party shuru ho gayi!"

```javascript
birthdayParty.on('startParty', () => {
    console.log('Party shuru ho gayi! Sab aake enjoy karo!');
});

// Party start karte hain
birthdayParty.emit('startParty');
```

**Explanation**: Rohan ne last event emit kiya, jisse sab doston ne party ka maza lena shuru kiya. 

### Moral of the Story

Jaise Rohan ne apni party ko manage kiya events aur listeners ki tarah, waise hi Node.js mein events aur callbacks ka use hota hai. Har ek event kisi action ya task ko represent karta hai, aur jab woh event fire hota hai, toh listeners apna kaam karte hain. Is tarah se hum asynchrony ko handle karte hain aur ek organized tarike se kaam karte hain.

Agar aapko aur koi example chahiye ya aur kuch samajhna hai, toh bata sakte hain!






---
---





1. **Answer** -  
**Non-blocking I/O operations** ka matlab hota hai ki jab Node.js koi **I/O task** (jaise file read karna, database request, etc.) perform karta hai, toh voh **CPU** ko block nahi karta. Instead, voh process ko continue karta hai jab tak task complete nahi hota, aur jab task finish hoti hai toh callback ya **event** ke through result return karta hai. Isse **asynchronous** execution possible hoti hai.

2. **Uses in short** -  
- **Performance** increase karta hai, kyunki CPU idle nahi hota.
- **Multiple requests** ko handle kar sakta hai bina wait kiye.
- **Efficient resource usage** hota hai, jo real-time applications ke liye zaroori hai.

3. **Types** -  
- **I/O Operations**: File handling, network requests.
- **Non-blocking APIs**: HTTP, File system, Streams.

4. **Example**:

```javascript
const fs = require('fs');

// Non-blocking I/O file read
fs.readFile('file.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log(data);
});

console.log("File reading started!");

#output:
#File reading started!
#(file content will be printed here after some time)
```

In this example, **file read operation** non-blocking hai, toh "File reading started!" pehle print hoga, aur jab file read complete hoti hai tab callback execute hoga aur file ka data print hoga.


## ---

1. **Event Loop** Kya Hai?  
Node.js ka **Event Loop** ek **asynchronous** programming concept hai jo **non-blocking I/O** operations ko manage karta hai. Ye continuous cycle me kaam karta hai, jo system ke har event ko execute karne ke liye responsible hota hai. **Event-driven** architecture ke through Node.js apne tasks efficiently handle karta hai bina poori system ko block kiye.

**Simple words** me, jab Node.js koi **async** task execute karta hai (jaise file read, API request), toh wo task Event Loop ke paas bhej diya jata hai. Jab task complete hota hai, Event Loop uss result ko handle karta hai.

2. **Uses in short**:  
- **Non-blocking tasks** ko efficiently execute karne ke liye.
- **Real-time applications** me high performance dene ke liye.
- **Concurrency** ko handle karne ke liye bina multiple threads ke.

3. **Phases of Event Loop**:

**Node.js** me Event Loop ke different phases hote hain, jaha har phase me specific tasks perform hote hain. Main phases:

1. **Timers**:  
   Yahaan pe **setTimeout()** aur **setInterval()** jaise scheduled callbacks execute hote hain.

2. **I/O Callbacks**:  
   Non-blocking I/O operations ke callbacks ko handle karta hai.

3. **Idle, prepare**:  
   Internally system ke functions execute hote hain, mostly user code yaha nahi hota.

4. **Poll**:  
   Yahaan pe system events jaise incoming connections, data receive, etc., ko handle kiya jata hai.

5. **Check**:  
   Yahaan **setImmediate()** ke callbacks ko execute kiya jata hai.

6. **Close Callbacks**:  
   Yahaan file stream jaise close callbacks ko handle kiya jata hai.

### **Diagram** (Step-by-step loop of Event Loop):

```
Timers → I/O Callbacks → Idle, Prepare → Poll → Check → Close Callbacks → (Repeat)
```

4. **Example**:

```javascript
console.log('Start');

// setTimeout runs in Timer phase
setTimeout(() => {
  console.log('Timeout callback');
}, 0);

// setImmediate runs in Check phase
setImmediate(() => {
  console.log('Immediate callback');
});

console.log('End');

#output:
#Start
#End
#Immediate callback
#Timeout callback
```

In this example:
- **setTimeout()** Timer phase me run hota hai.
- **setImmediate()** Check phase me run hota hai.


---
---

1. **Callback Hell Kya Hota Hai?**  
**Callback Hell** tab hota hai jab **asynchronous** operations ko handle karne ke liye multiple **nested callbacks** use kiye jaate hain. Jaise jaise callbacks ek dusre ke andar nest hote jaate hain, code ka structure complex aur difficult to read ho jaata hai. Yeh code ko samajhna aur debug karna mushkil bana deta hai.

**Callback Hell** ka structure kuch aisa hota hai:

```javascript
firstFunction(() => {
  secondFunction(() => {
    thirdFunction(() => {
      fourthFunction(() => {
        // aur deeply nested callbacks...
      });
    });
  });
});
```

**Problem:** Is tarah ka deeply nested structure readability ko affect karta hai, aur agar ek bhi callback fail ho jaye, toh error handling mushkil ho jati hai.

2. **Callback Hell se Kaise Bachen?**
Callback Hell se bachne ke liye kai tarike hain:

- **Promises ka use karo:** Promises async code ko handle karna easier aur readable banate hain.
- **Async/Await:** Ye Promises ka hi cleaner version hai jo synchronous code ki tarah lagta hai, but asynchronous operations handle karta hai.
- **Modularize your code:** Badi functions ko chhote modules me tod do, taaki har function independently kaam kare.

3. **Example: Callback Hell**

```javascript
// Callback Hell example
function firstTask(callback) {
  setTimeout(() => {
    console.log('First task done');
    callback();
  }, 1000);
}

function secondTask(callback) {
  setTimeout(() => {
    console.log('Second task done');
    callback();
  }, 1000);
}

function thirdTask(callback) {
  setTimeout(() => {
    console.log('Third task done');
    callback();
  }, 1000);
}

// Callbacks inside callbacks (Callback Hell)
firstTask(() => {
  secondTask(() => {
    thirdTask(() => {
      console.log('All tasks done');
    });
  });
});

#output:
#First task done
#Second task done
#Third task done
#All tasks done
```

**Solution: Using Promises to avoid Callback Hell:**

```javascript
// Promises example to avoid Callback Hell
function firstTask() {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log('First task done');
      resolve();
    }, 1000);
  });
}

function secondTask() {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log('Second task done');
      resolve();
    }, 1000);
  });
}

function thirdTask() {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log('Third task done');
      resolve();
    }, 1000);
  });
}

// Promise chain
firstTask()
  .then(secondTask)
  .then(thirdTask)
  .then(() => {
    console.log('All tasks done');
  });

#output:
#First task done
#Second task done
#Third task done
#All tasks done
```

**Solution: Using Async/Await for Cleaner Code:**

```javascript
// Async/Await example to avoid Callback Hell
async function runTasks() {
  await firstTask();
  await secondTask();
  await thirdTask();
  console.log('All tasks done');
}

runTasks();

#output:
#First task done
#Second task done
#Third task done
#All tasks done
```

**Summary**: 
- **Callback Hell** occurs due to deeply nested callbacks.
- **Avoid it** by using **Promises** or **Async/Await** which make the code much more readable and easier to maintain.

---
---
1. **Synchronous vs Asynchronous Code**:  
Synchronous aur Asynchronous code ke beech ka main difference unka execution style hai. Let's explore:

- **Synchronous Code**:
  - **Blocking** hota hai. Matlab, ek operation ke complete hone ke baad hi next operation execute hota hai.
  - Sab kuch sequentially hota hai.
  - Agar ek task slow hai, toh poora program uska wait karega aur next task tab tak nahi chalega jab tak current task complete na ho jaye.

- **Asynchronous Code**:
  - **Non-blocking** hota hai. Matlab, ek operation ke complete hone ka wait nahi karta, balki agle task par chala jaata hai.
  - Jo operations time-consuming hote hain (like I/O tasks, network requests), wo background me chal sakte hain aur baaki code continue run karta hai.
  - Jab background task complete hota hai, tab callback ya promise ke through result handle kiya jaata hai.

2. **Differences in short**:

| **Synchronous** | **Asynchronous** |
|-----------------|------------------|
| Blocking code execution | Non-blocking code execution |
| Sequential execution | Parallel or background execution |
| Code ek hi time pe ek task handle karta hai | Multiple tasks ko efficiently handle karta hai |
| Slow or time-consuming operations poora program block kar sakte hain | Time-consuming operations background me chalti hain |
| Example: Simple for-loop | Example: API call, file reading |

3. **Example**:

**Synchronous Code Example**:  
```javascript
console.log("Start");

// Synchronous loop
for (let i = 0; i < 3; i++) {
  console.log(i);
}

console.log("End");

#output:
#Start
#0
#1
#2
#End
```

**Explanation**:  
Yahaan loop sequentially chalta hai, har iteration ke baad agla execute hota hai. Jab tak loop finish nahi hoga, "End" console pe nahi dikhega.

---

**Asynchronous Code Example**:  
```javascript
console.log("Start");

// Asynchronous code using setTimeout
setTimeout(() => {
  console.log("Inside Timeout");
}, 1000);

console.log("End");

#output:
#Start
#End
#Inside Timeout
```

**Explanation**:  
Yahaan `setTimeout()` ek **asynchronous** function hai, jo 1000ms (1 second) baad run hoga. Code pehle "Start" print karta hai, fir immediately "End" print karta hai, bina timeout ke complete hone ka wait kiye. Jab timeout complete hota hai, tab "Inside Timeout" print hota hai.

**Asynchronous Code with Callback Hell Avoidance using Promises**:

```javascript
console.log("Start");

function asyncTask() {
  return new Promise((resolve) => {
    setTimeout(() => {
      console.log("Async Task Done");
      resolve();
    }, 1000);
  });
}

// Handling asynchronous task with promise
asyncTask().then(() => {
  console.log("End");
});

#output:
#Start
#Async Task Done
#End
```

**Explanation**:  
Yahaan **Promises** ka use karke asynchronous task ko handle kiya gaya hai. Asynchronous task complete hone ke baad "End" print hota hai, bina nested callbacks ke (Callback Hell se bachne ke liye).

---

**Summary**:
- **Synchronous** code sequential aur blocking hota hai.
- **Asynchronous** code non-blocking hota hai, jo parallelly tasks handle karta hai without stopping the main program.
- Promises aur async/await ka use karke asynchronous code ko zyada readable aur maintainable banaya jaa sakta hai.

---
---
1. **Answer** -  
**Memory leak** tab hota hai jab koi program **memory allocate** karta hai lekin us memory ko **free** nahi karta jab voh use nahi ho rahi hoti. Iska matlab ye hai ki program kaafi memory consume karta rahta hai jo use nahi ho rahi, aur dheere-dheere system ke resources khatam hone lagte hain, jisse **performance degrade** hota hai ya program crash kar sakta hai.

2. **Uses in short** (Memory Leak ko Identify aur Fix karna) -  
- **Identify**:  
  - **Memory usage continuously increase** ho rahi ho bina kisi reason ke.
  - **Profiling tools** ka use karein (like Chrome DevTools, Node.js memory profiling).
  - **Heap snapshots** le ke unused objects ya variables ko identify karein.
  
- **Fix**:  
  - **Unused objects ko dereference** karna (i.e., `null` set karna jab object use na ho).
  - **Garbage collector** ko sahi se kaam karne dena, manual memory management avoid karein.

3. **Types of Causes**:
   - **Global Variables**: Jo kabhi memory free nahi karte.
   - **Closures**: Functions jo unnecessary memory hold karte hain.
   - **Event listeners**: Remove na karne pe unnecessary memory use hoti rahti hai.

4. **Example**:

```javascript
let bigArray = [];

// Memory leak ho raha hai, kyunki array ko kabhi empty nahi kar rahe
setInterval(() => {
  bigArray.push(new Array(1000).fill('*'));
  console.log('Array size:', bigArray.length);
}, 1000);

// Fix: setInterval ke ander array ko clear kar dena jab use na ho
```

Is example me **`bigArray`** continuously grow karta hai, lekin clear nahi hota, toh memory continuously increase hoti rahegi aur **memory leak** hoga.

#output:  
Memory keep increasing without freeing

---
---
1. **Answer** -  
**Stream** ek data handling concept hai jo Node.js me continuous data flow ko efficiently process karne ke liye use hota hai. Streams **chunks** me data handle karte hain, na ki poora data ek saath. Isse aap **large data sets** ko bhi efficiently process kar sakte hain bina memory ko block kiye.

2. **Uses in short** -  
- Large files (video/audio) ko **read** ya **write** karna.
- **Data transfer** during HTTP requests/responses.
- **Real-time applications** like live video streaming.
- **Memory efficient** operations kyunki poora data ek saath memory me nahi load hota.

3. **Types in short**:
   - **Readable Stream**: Jo data ko **read** karta hai, jaise file reading or HTTP requests.
   - **Writable Stream**: Jo data ko **write** karta hai, jaise file writing or HTTP responses.
   - **Duplex Stream**: Jo **read** aur **write** dono kar sakta hai, jaise TCP sockets.
   - **Transform Stream**: Jo data ko **read** aur **write** karta hai, aur saath me **transform** bhi karta hai, jaise compression ya encryption.

4. **Example**:

```javascript
const fs = require('fs');

// Readable stream se file data read kar rahe hain
const readableStream = fs.createReadStream('input.txt', 'utf8');

readableStream.on('data', (chunk) => {
  console.log('Received chunk:', chunk);
});

readableStream.on('end', () => {
  console.log('Finished reading file.');
});

#output:
#Received chunk: (data in chunks)
#Finished reading file.
```

Is example me hum **`fs.createReadStream`** use kar rahe hain jo ek **readable stream** hai. Ye file se data **chunks** me read karta hai aur memory efficient way me process karta hai.



---
---
1. **Answer** -  
**Middleware** ek function hota hai jo **Express.js** me **request** aur **response** ke beech mein aata hai. Ye function incoming **HTTP requests** ko process karne, manipulate karne, aur aage route handler ya next middleware ko pass karne ke liye use hota hai. Middleware ka kaam **logic apply karna** hota hai jaise authentication, logging, error handling, etc.

2. **Uses in short** -  
- **Request logging** ke liye.
- **Authentication** aur **authorization** ke liye.
- **Error handling**.
- **Data parsing** (like JSON, URL-encoded data).

3. **Types in short** -  
- **Application-level middleware**: Specific routes ya app ke liye.
- **Router-level middleware**: Express router ke routes ke liye.
- **Error-handling middleware**: Jab error occur ho tab use hota hai.
- **Built-in middleware**: Express ke saath aata hai, jaise `express.json()`, `express.static()`.
- **Third-party middleware**: External modules, jaise `body-parser`, `morgan`, etc.

4. **Example**:

```javascript
const express = require('express');
const app = express();

// Simple middleware function
app.use((req, res, next) => {
  console.log('Request URL:', req.url);
  next();  // Next middleware or route ko call karna
});

// Route handler
app.get('/', (req, res) => {
  res.send('Hello, Middleware!');
});

app.listen(3000, () => {
  console.log('Server running on port 3000');
});

#output:
#Request URL: /
#Hello, Middleware!
```

Is example me ek simple **middleware** function hai jo har incoming request pe **URL log** karta hai, phir **next()** call karke request ko aage route handler ko pass karta hai.


---
---


---
---



