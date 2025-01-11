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




****
****
****
****
****


# React Router Notes

## React Router ka Basic
React Router ek library hai jo React applications mein navigation handle karne ke liye use hoti hai.

### Key Components:
- **`<Routes>`**: Saare route definitions ka container.
- **`<Route>`**: Path aur render hone wale component ko define karta hai.
- **`<Navigate>`**: Kisi doosre route par redirect karta hai.
- **`useNavigate()`**: Programmatic navigation ke liye hook.
- **`useParams()`**: URL ke dynamic parameters ko access karne ka hook.
- **`useSearchParams()`**: Query parameters ko handle karne ka hook.
- **`Outlet`**: Nested routes ke liye placeholder.

### Example:
```jsx
import React from "react";
import { BrowserRouter as Router, Routes, Route, Navigate } from "react-router-dom";

function App() {
  return (
    <Router>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/redirect" element={<Navigate to="/about" />} />
        <Route path="/profile/:username" element={<Profile />} />
        <Route path="*" element={<NotFound />} />
      </Routes>
    </Router>
  );
}
```

---

## Advanced Scenarios

### 1. Authentication aur Protected Routes
Routes ko authentication status ke basis par restrict kar sakte ho.

```jsx
const ProtectedRoute = ({ isAuthenticated }) => {
  return isAuthenticated ? <Outlet /> : <Navigate to="/login" />;
};

<Routes>
  <Route path="/login" element={<Login />} />
  <Route element={<ProtectedRoute isAuthenticated={true} />}>
    <Route path="/dashboard" element={<Dashboard />} />
  </Route>
</Routes>
```

---

### 2. Nested Routes
Layouts ya complex structures handle karne ke liye nested routes ka use hota hai.

```jsx
<Routes>
  <Route path="/" element={<MainLayout />}>
    <Route path="about" element={<About />} />
    <Route path="profile/:username" element={<Profile />} />
  </Route>
</Routes>

// MainLayout.jsx
function MainLayout() {
  return (
    <div>
      <h1>Main Layout</h1>
      <Outlet /> {/* Nested routes yahan render honge */}
    </div>
  );
}
```

---

### 3. Query Parameters
Query parameters ko handle karne ke liye `useSearchParams()` ka use hota hai.

```jsx
const SearchPage = () => {
  const [searchParams] = useSearchParams();
  const query = searchParams.get("query");
  return <h1>Search Results for: {query}</h1>;
};

<Routes>
  <Route path="/search" element={<SearchPage />} />
</Routes>
```

---

### 4. Lazy Loading Components
Performance optimize karne ke liye components ko demand par load karte ho.

```jsx
import React, { lazy, Suspense } from "react";

const Home = lazy(() => import("./Home"));
const About = lazy(() => import("./About"));

<Routes>
  <Route
    path="/"
    element={
      <Suspense fallback={<div>Loading...</div>}>
        <Home />
      </Suspense>
    }
  />
  <Route
    path="/about"
    element={
      <Suspense fallback={<div>Loading...</div>}>
        <About />
      </Suspense>
    }
  />
</Routes>
```

---

### 5. Custom 404 Pages
Unmatched routes ke liye ek custom component provide karo.

```jsx
<Routes>
  <Route path="/" element={<Home />} />
  <Route path="*" element={<NotFound />} /> {/* Custom 404 */}
</Routes>

// NotFound.jsx
const NotFound = () => <h1>404 - Page Not Found</h1>;
```

---

### 6. Programmatic Navigation with State
`state` ka use karke routes ke beech data pass karte ho.

```jsx
// Navigate with state
navigate("/profile", { state: { username: "JohnDoe" } });

// Destination component mein state access karo
const Profile = () => {
  const location = useLocation();
  const { username } = location.state || {};
  return <h1>Profile of {username}</h1>;
};
```

---

### 7. Scroll Restoration
Navigate karte waqt page ko top par scroll karne ke liye.

```jsx
import { useEffect } from "react";
import { useLocation } from "react-router-dom";

const ScrollToTop = () => {
  const { pathname } = useLocation();
  useEffect(() => {
    window.scrollTo(0, 0);
  }, [pathname]);
  return null;
};

<Router>
  <ScrollToTop />
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
  </Routes>
</Router>
```

---

### 8. Dynamic Nested Routes
Dynamic parameters ke saath deeply nested routes create karte ho.

```jsx
<Routes>
  <Route path="/dashboard" element={<Dashboard />}>
    <Route path="settings" element={<Settings />} />
    <Route path="users/:id" element={<UserDetails />} />
  </Route>
</Routes>

// Dashboard.jsx
const Dashboard = () => (
  <div>
    <h1>Dashboard</h1>
    <Outlet /> {/* Nested routes yahan render honge */}
  </div>
);
```

---

### 9. Transition Animations
Routes ke beech animations add karne ke liye `framer-motion` jaise libraries ka use karte ho.

```jsx
import { motion } from "framer-motion";

const PageTransition = ({ children }) => (
  <motion.div
    initial={{ opacity: 0 }}
    animate={{ opacity: 1 }}
    exit={{ opacity: 0 }}
  >
    {children}
  </motion.div>
);

<Routes>
  <Route
    path="/"
    element={
      <PageTransition>
        <Home />
      </PageTransition>
    }
  />
  <Route
    path="/about"
    element={
      <PageTransition>
        <About />
      </PageTransition>
    }
  />
</Routes>
```

---

### 10. Multi-Step Forms
Multi-step forms create karne ke liye routes ka use karo.

```jsx
<Routes>
  <Route path="/form/step1" element={<Step1 />} />
  <Route path="/form/step2" element={<Step2 />} />
  <Route path="/form/step3" element={<Step3 />} />
</Routes>;



****
****
****
****
****
















