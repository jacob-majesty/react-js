Cheatsheet to help you get started with **React + Vite**. It covers the basics, setup, and essential concepts for building React applications with Vite.

---

### **1. Setting Up a React Vite Project**
```bash
# Create a new React project with Vite
npm create vite@latest my-react-app --template react

# Navigate to the project directory
cd my-react-app

# Install dependencies
npm install

# Start the development server
npm run dev
```

---

### **2. Project Structure**
```
my-react-app/
├── public/            # Static assets
├── src/
│   ├── assets/        # Images, fonts, etc.
│   ├── components/    # Reusable components
│   ├── App.jsx        # Main App component
│   ├── main.jsx       # Entry point
│   └── index.css      # Global styles
├── .gitignore
├── index.html         # Root HTML file
├── package.json
├── vite.config.js     # Vite configuration
└── README.md
```

---

### **3. Key Files**
- **`index.html`**: The root HTML file where the React app is mounted.
- **`main.jsx`**: Entry point for the React app.
- **`App.jsx`**: Main component where your app starts.
- **`vite.config.js`**: Configuration file for Vite.

---

### **4. Basic React Concepts**
#### **Components**
```jsx
// Functional Component
function MyComponent() {
  return <div>Hello, World!</div>;
}

export default MyComponent;
```

#### **Props**
```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}!</h1>;
}

// Usage
<Greeting name="John" />
```

#### **State (using Hooks)**
```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

#### **Effects (using Hooks)**
```jsx
import { useEffect } from 'react';

function MyComponent() {
  useEffect(() => {
    console.log('Component mounted or updated');
    return () => console.log('Component unmounted');
  }, []); // Empty dependency array means it runs only on mount
}
```

---

### **5. Styling**
#### **CSS Modules**
```jsx
import styles from './MyComponent.module.css';

function MyComponent() {
  return <div className={styles.container}>Styled with CSS Modules</div>;
}
```

#### **Inline Styles**
```jsx
function MyComponent() {
  return <div style={{ color: 'red', fontSize: '20px' }}>Inline Styled</div>;
}
```

---

### **6. Routing (using React Router)**
```bash
# Install React Router
npm install react-router-dom
```

```jsx
import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';

function App() {
  return (
    <Router>
      <nav>
        <Link to="/">Home</Link>
        <Link to="/about">About</Link>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </Router>
  );
}
```

---

### **7. Environment Variables**
- Create a `.env` file in the root:
  ```
  VITE_API_KEY=your_api_key
  ```
- Access in your code:
  ```js
  const apiKey = import.meta.env.VITE_API_KEY;
  ```

---

### **8. Vite Configuration**
- **`vite.config.js`**:
  ```js
  import { defineConfig } from 'vite';
  import react from '@vitejs/plugin-react';

  export default defineConfig({
    plugins: [react()],
    server: {
      port: 3000, // Custom port
    },
  });
  ```

---

### **9. Building for Production**
```bash
# Build the project
npm run build

# Preview the production build locally
npm run preview
```

---

### **10. Useful Vite Features**
- **Hot Module Replacement (HMR)**: Instant updates without reloading.
- **Fast Builds**: Optimized for speed.
- **CSS Preprocessors**: Supports SCSS, LESS, etc.
- **TypeScript**: Built-in support.

---

### **11. Additional Libraries**
- **State Management**: Redux, Zustand, Recoil.
- **Form Handling**: Formik, React Hook Form.
- **UI Libraries**: Material-UI, TailwindCSS, Chakra UI.

---
