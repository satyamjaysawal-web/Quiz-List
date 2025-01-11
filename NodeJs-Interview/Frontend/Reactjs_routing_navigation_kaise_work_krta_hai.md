# React Router Notes

## Setting Up a Vite ReactJS Project with React Router

### 1. **Project Setup**
Run the following commands to set up a Vite ReactJS project:
```bash
npm create vite@latest my-react-app --template react
cd my-react-app
npm install
```

### 2. **Install React Router**
Install React Router and its dependencies:
```bash
npm install react-router-dom
```

### 3. **Project Structure**
Typical structure for a routing-enabled React app:
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

## Routing with React Router

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
          {/* Render Home component */}
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
Use `useParams` to access dynamic URL segments.

### Example (`Profile.jsx`):
```jsx
import React from "react";
import { useParams } from "react-router-dom";

function Profile() {
  const { username } = useParams(); // Access the dynamic parameter
  return (
    <div>
      <h2>Profile Page</h2>
      <p>Welcome to the profile of <b>{username}</b>!</p>
    </div>
  );
}

export default Profile;
```

- Navigating to `/profile/JohnDoe` will display "Profile of JohnDoe".

---

## Programmatic Navigation with `useNavigate`
Use `useNavigate` for dynamic navigation via code.

### Example (`Home.jsx`):
```jsx
import React from "react";
import { useNavigate } from "react-router-dom";

function Home() {
  const navigate = useNavigate();

  const goToAbout = () => {
    navigate("/about"); // Navigate to About page
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

- Clicking the button navigates to `/about`.

### Another Example (`Profile.jsx`):
Add a button to navigate back to the Home page:
```jsx
import React from "react";
import { useParams, useNavigate } from "react-router-dom";

function Profile() {
  const { username } = useParams();
  const navigate = useNavigate();

  const goToHome = () => {
    navigate("/"); // Navigate to Home page
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

## How Routing Works
1. **Route Matching**:
   - `path` in `Route` defines the URL to match.
   - `element` specifies the component to render for that URL.

2. **Example**:
   ```jsx
   <Route path="/about" element={<About />} />
   ```
   - Navigating to `/about` renders the `About` component.

3. **Redirects**:
   - Use `<Navigate to="/path" />` to programmatically redirect.

4. **404 Handling**:
   - Use `path="*"` for undefined routes.
   ```jsx
   <Route path="*" element={<div>Page Not Found</div>} />
   ```

---

## Project Execution

### Steps to Run:
1. **Install Dependencies**:
   ```bash
   npm install
   ```

2. **Start Development Server**:
   ```bash
   npm run dev
   ```

3. **Test Routes**:
   - `/` → Home Page
   - `/about` → About Page
   - `/redirect` → Redirects to `/about`
   - `/profile/JohnDoe` → Displays "Profile of JohnDoe"
   - Any other path → Displays "Page Not Found"
