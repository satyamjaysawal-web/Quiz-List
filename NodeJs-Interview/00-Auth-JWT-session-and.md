

---
---

---
---

Yahan par session, cookie, JWT, aur bcrypt ke working flow steps ko table format mein diya gaya hai:

| Feature  | Steps                                                                                         |
|----------|-----------------------------------------------------------------------------------------------|
| **Session** | User Login → Session Creation → Session ID Generation → Subsequent Requests → Session Validation → Access Control |
| **Cookie**  | Set Cookie → Store Cookie → Send Cookie → Read Cookie → Expire Cookie                     |
| **JWT**     | User Login → Token Generation → Send Token → Store Token → Subsequent Requests → Token Verification → Access Control |
| **Bcrypt**  | User Registration → Hash Password → Store Hashed Password → User Login → Hash Input Password → Compare Passwords → Authentication Result |

Agar aur koi sawaal ho ya aur kuch detail chahiye ho, toh batao!

---
---
Yahan par session, cookie, JWT, aur bcrypt ke working flow steps ko table format mein diya gaya hai:

| **Feature** | **Working Flow Steps** |
|-------------|------------------------|
| **Session** | 1. **User Login:** User application par login karta hai.<br>2. **Session Creation:** Server user ke liye ek session create karta hai aur session ID ko server par store karta hai.<br>3. **Session ID Generation:** Server session ID generate karta hai aur use response ke sath client (browser) ko bhejta hai (usually cookies ke through).<br>4. **Subsequent Requests:** Client har request ke sath session ID ko bhejta hai (cookie ke zariye).<br>5. **Session Validation:** Server session ID ko check karta hai aur user ke session data ko retrieve karta hai.<br>6. **Access Control:** Agar session valid hai, toh server request ko process karta hai; agar nahi, toh error ya redirect karta hai. |
| **Cookie** | 1. **Set Cookie:** Server client ko response bhejte waqt cookie set karta hai, jisme user preferences ya authentication tokens ho sakte hain.<br>2. **Store Cookie:** Client browser par cookie ko store karta hai.<br>3. **Send Cookie:** Client har subsequent request mein cookie ko server ko bhejta hai.<br>4. **Read Cookie:** Server cookie ko read karta hai aur uske contents ko use karta hai (jaise user preferences ya session info).<br>5. **Expire Cookie:** Cookie ki expiration date set ki ja sakti hai, jab tak wo expire nahi hoti, cookie valid rahegi. |
| **JWT (JSON Web Token)** | 1. **User Login:** User application par login karta hai.<br>2. **Token Generation:** Server user ke information ko lekar ek JWT generate karta hai, jo user ki identity aur permissions ko encode karta hai.<br>3. **Send Token:** Server JWT ko client ko bhejta hai (usually Authorization header ya response body ke through).<br>4. **Store Token:** Client JWT ko localStorage ya sessionStorage mein store karta hai.<br>5. **Subsequent Requests:** Client har request ke sath Authorization header mein JWT ko bhejta hai.<br>6. **Token Verification:** Server JWT ko verify karta hai (signature aur expiration check karta hai).<br>7. **Access Control:** Agar token valid hai, toh server request ko process karta hai; agar nahi, toh error ya unauthorized response bhejta hai. |
| **Bcrypt** | 1. **User Registration:** User registration form fill karta hai aur password enter karta hai.<br>2. **Hash Password:** Server bcrypt library ka use karke password ko hash karta hai (salt generate karta hai aur password ko hash karta hai).<br>3. **Store Hashed Password:** Server hashed password ko database mein store karta hai.<br>4. **User Login:** User login attempt karta hai aur password enter karta hai.<br>5. **Hash Input Password:** Server input password ko bcrypt ke through hash karta hai (same hashing process).<br>6. **Compare Passwords:** Server hashed password (database se) aur input hashed password ko compare karta hai.<br>7. **Authentication Result:** Agar passwords match karte hain, toh user authenticated hota hai; agar nahi, toh error message diya jata hai. |

Agar tumhe kisi specific feature ya step ka aur detail chahiye ya koi aur sawaal hai, toh zaroor puchho!
---
---
Yahan par session, cookie, JWT, aur bcrypt ka working flow steps aur uses ke sath ek table format mein diya gaya hai. Har feature ke liye flow steps aur implementation ke steps diye gaye hain.

| Feature          | Working Flow Steps                                           | Uses                                                   | Steps to Code                                                   |
|------------------|------------------------------------------------------------|--------------------------------------------------------|----------------------------------------------------------------|
| **Session**      | 1. User logs in. <br> 2. Server creates a session. <br> 3. Session ID is sent to client. <br> 4. Client stores session ID in cookies. <br> 5. On subsequent requests, client sends session ID. <br> 6. Server verifies session ID. | - User authentication <br> - User-specific data storage | 1. Import express and session module. <br> 2. Set up session middleware. <br> 3. Create login route. <br> 4. Store user data in session. <br> 5. Create protected routes. |
| **Cookie**       | 1. Server sets a cookie in the response. <br> 2. Browser stores the cookie. <br> 3. On subsequent requests, browser sends the cookie. <br> 4. Server retrieves cookie data for processing. | - Store user preferences <br> - Remember user sessions | 1. Import express module. <br> 2. Set cookie using `res.cookie()`. <br> 3. Read cookie using `req.cookies`. <br> 4. Create routes to set and get cookies. |
| **JWT**          | 1. User logs in. <br> 2. Server verifies credentials. <br> 3. Server generates a JWT token. <br> 4. Client stores the token. <br> 5. On subsequent requests, client sends the token in the Authorization header. <br> 6. Server verifies the token. | - Stateless authentication <br> - API authentication | 1. Install jsonwebtoken package. <br> 2. Create login route to generate JWT. <br> 3. Set token in client storage (localStorage). <br> 4. Create middleware to verify JWT. |
| **Bcrypt**       | 1. User creates a password. <br> 2. Password is hashed using bcrypt. <br> 3. Hashed password is stored in the database. <br> 4. When user logs in, the input password is hashed and compared with the stored hash. | - Securely store passwords <br> - Protect against password cracking | 1. Install bcrypt package. <br> 2. Use `bcrypt.hash()` to hash passwords. <br> 3. Store hashed password in database. <br> 4. Use `bcrypt.compare()` to verify password on login. |

### Example Code for Each Feature:

#### Session Example
```javascript
const express = require('express'); // Express framework ko import kar rahe hain
const session = require('express-session'); // Session middleware ko import karte hain
const app = express(); // Express application create kar rahe hain

app.use(session({
    secret: 'mySecret', // Session ko secure karne ke liye secret key
    resave: false, // Session ko har request par dobara save nahi karna
    saveUninitialized: false // Uninitialized sessions ko save nahi karna
}));

app.post('/login', (req, res) => {
    // #Hinglish: User login details ko check karte hain
    req.session.user = { id: 1, name: 'User' }; // #Hinglish: User data ko session mein store karte hain
    res.send('Logged in!'); // #Hinglish: Login success message dikhate hain
});

app.get('/dashboard', (req, res) => {
    // #Hinglish: Dashboard access karne ke liye session check karte hain
    if (req.session.user) {
        res.send('Welcome to your dashboard!'); // #Hinglish: Dashboard ka message dikhate hain
    } else {
        res.send('Please log in first.'); // #Hinglish: Agar login nahi hai toh message dikhate hain
    }
});

app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000'); // #Hinglish: Server ka message
});
```

#### Cookie Example
```javascript
const express = require('express'); // Express framework ko import kar rahe hain
const cookieParser = require('cookie-parser'); // Cookie parser ko import karte hain
const app = express(); // Express application create kar rahe hain

app.use(cookieParser()); // #Hinglish: Cookie parser middleware ko use karte hain

app.get('/setcookie', (req, res) => {
    // #Hinglish: Cookie set karte hain
    res.cookie('username', 'User', { maxAge: 900000, httpOnly: true }); // Cookie ko set karte hain
    res.send('Cookie has been set!'); // #Hinglish: Cookie set hone ka message dikhate hain
});

app.get('/getcookie', (req, res) => {
    // #Hinglish: Cookie ko read karte hain
    const username = req.cookies.username; // #Hinglish: Cookie se username ko get karte hain
    res.send(`Username from cookie is: ${username}`); // #Hinglish: Cookie se username dikhate hain
});

app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000'); // #Hinglish: Server ka message
});
```

#### JWT Example
```javascript
const express = require('express'); // Express framework ko import kar rahe hain
const jwt = require('jsonwebtoken'); // JWT package ko import karte hain
const app = express(); // Express application create kar rahe hain

const secretKey = 'mySecretKey'; // #Hinglish: JWT ke liye secret key

app.use(express.json()); // #Hinglish: JSON data ko parse karne ke liye

app.post('/login', (req, res) => {
    // #Hinglish: User login details ko check karte hain
    const user = { id: 1, name: 'User' }; // #Hinglish: User object
    const token = jwt.sign(user, secretKey); // #Hinglish: JWT token generate karte hain
    res.json({ token }); // #Hinglish: Token client ko bhejte hain
});

app.get('/protected', (req, res) => {
    // #Hinglish: Protected route
    const token = req.headers['authorization']; // #Hinglish: Authorization header se token lete hain
    if (token) {
        jwt.verify(token, secretKey, (err, user) => {
            // #Hinglish: Token ko verify karte hain
            if (err) {
                return res.sendStatus(403); // #Hinglish: Agar token invalid hai toh forbidden response
            }
            res.send('Protected content!'); // #Hinglish: Protected content dikhate hain
        });
    } else {
        res.sendStatus(401); // #Hinglish: Agar token nahi hai toh unauthorized response
    }
});

app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000'); // #Hinglish: Server ka message
});
```

#### Bcrypt Example
```javascript
const express = require('express'); // Express framework ko import kar rahe hain
const bcrypt = require('bcrypt'); // Bcrypt package ko import karte hain
const app = express(); // Express application create kar rahe hain

app.use(express.json()); // #Hinglish: JSON data ko parse karne ke liye

app.post('/register', async (req, res) => {
    // #Hinglish: User registration route
    const password = req.body.password; // #Hinglish: User se password lete hain
    const hashedPassword = await bcrypt.hash(password, 10); // #Hinglish: Password ko hash karte hain
    // #Hinglish: Hashed password ko database mein store karte hain
    res.send('User registered with hashed password!'); // #Hinglish: Registration success message dikhate hain
});

app.post('/login', async (req, res) => {
    // #Hinglish: User login route
    const { password, hashedPassword } = req.body; // #Hinglish: User se password aur hashed password lete hain
    const match = await bcrypt.compare(password, hashedPassword); // #Hinglish: Password ko verify karte hain
    if (match) {
        res.send('Login successful!'); // #Hinglish: Login success message
    } else {
        res.send('Invalid password!'); // #Hinglish: Invalid password message
    }
});

app.listen(3000, () => {
    console.log('Server is running on http://localhost:3000'); // #Hinglish: Server ka message
});
```

Agar tumhe in features ke bare mein aur detail chahiye ya koi aur sawaal hai, toh zaroor puchho!



---
---

---
---


---
---
