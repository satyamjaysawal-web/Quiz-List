# React Router Notes (Hinglish)

## Vite ReactJS Project Setup ke Saath React Router

### 1. **Project Setup**
Vite ReactJS project banane ke liye ye commands run karo:
```bash
npm create vite@latest my-react-app --template react
cd my-react-app
npm install
```

### 2. **React Router Install Karo**
React Router aur uske dependencies install karne ke liye:
```bash
npm install react-router-dom
```

### 3. **Project Structure**
Routing-enabled React app ka typical structure:
```
src/
├── components/
│   ├── Home.jsx
│   ├── About.jsx
│   ├── Profile.jsx
├── App.jsx
├── main.jsx
```

---

## React Router ke Saath Routing

### Basic Example (`App.jsx`):
```jsx
import React from "react";
import { BrowserRouter as Router, Routes, Route, Navigate } from "react-router-dom";
import Home from "./components/Home";
import About from "./components/About";
import Profile from "./components/Profile";

function App() {
  return (
    <Router>
      <div>
        <h1>Welcome to My React App</h1>
        <Routes>
          {/* Home component render karo */}
          <Route path="/" element={<Home />} />

          {/* About route */}
          <Route path="/about" element={<About />} />

          {/* Redirect example */}
          <Route path="/redirect" element={<Navigate to="/about" />} />

          {/* Route with URL parameter */}
          <Route path="/profile/:username" element={<Profile />} />

          {/* Default route (404 Page Not Found) */}
          <Route path="*" element={<div>Page Not Found</div>} />
        </Routes>
      </div>
    </Router>
  );
}

export default App;
```

---

## Dynamic Routes with URL Parameters
`useParams` ka use karke dynamic URL segments access karo.

### Example (`Profile.jsx`):
```jsx
import React from "react";
import { useParams } from "react-router-dom";

function Profile() {
  const { username } = useParams(); // Dynamic parameter access karo
  return (
    <div>
      <h2>Profile Page</h2>
      <p>Welcome to the profile of <b>{username}</b>!</p>
    </div>
  );
}

export default Profile;
```

- Agar `/profile/JohnDoe` pe navigate karoge to "Profile of JohnDoe" dikhayega.

---

## Programmatic Navigation with `useNavigate`
Dynamic navigation ke liye `useNavigate` ka use karo.

### Example (`Home.jsx`):
```jsx
import React from "react";
import { useNavigate } from "react-router-dom";

function Home() {
  const navigate = useNavigate();

  const goToAbout = () => {
    navigate("/about"); // About page pe navigate karo
  };

  return (
    <div>
      <h2>Home Page</h2>
      <p>Welcome to the home page of this React app!</p>
      <button onClick={goToAbout}>Go to About Page</button>
    </div>
  );
}

export default Home;
```

- Button click karne par `/about` pe navigate karega.

### Ek Aur Example (`Profile.jsx`):
Home page pe navigate karne ke liye ek button add karo:
```jsx
import React from "react";
import { useParams, useNavigate } from "react-router-dom";

function Profile() {
  const { username } = useParams();
  const navigate = useNavigate();

  const goToHome = () => {
    navigate("/"); // Home page pe navigate karo
  };

  return (
    <div>
      <h2>Profile Page</h2>
      <p>Welcome to the profile of <b>{username}</b>!</p>
      <button onClick={goToHome}>Go to Home Page</button>
    </div>
  );
}

export default Profile;
```

---

## Routing Kaise Work Karta Hai
1. **Route Matching**:
   - `path` jo `Route` me define kiya gaya hai, wo URL ko match karta hai.
   - `element` batata hai ki us URL ke liye kaunsa component render karna hai.

2. **Example**:
   ```jsx
   <Route path="/about" element={<About />} />
   ```
   - Agar `/about` pe navigate karte ho to `About` component render hoga.

3. **Redirects**:
   - Programmatically redirect karne ke liye `<Navigate to="/path" />` ka use karo.

4. **404 Handling**:
   - Undefined routes ke liye `path="*"` ka use karo.
   ```jsx
   <Route path="*" element={<div>Page Not Found</div>} />
   ```

---

## Project Execution

### Steps to Run:
1. **Dependencies Install Karo**:
   ```bash
   npm install
   ```

2. **Development Server Start Karo**:
   ```bash
   npm run dev
   ```

3. **Routes Test Karo**:
   - `/` → Home Page
   - `/about` → About Page
   - `/redirect` → Redirects to `/about`
   - `/profile/JohnDoe` → "Profile of JohnDoe" dikhayega
   - Any other path → "Page Not Found" dikhayega
