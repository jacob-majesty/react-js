### React Cheat Sheet: Quick Overview  

#### **What is React?**  
React is a JavaScript library for building user interfaces. Developed by Facebook, it focuses on efficiently updating and rendering components using a virtual DOM.  
<br>
Official Documentation: https://react.dev/ 
---

### **Key Features**  

#### **Core Concepts**
- **Component-Based Architecture**:  
  Break UI into reusable, self-contained components.  
- **Virtual DOM**:  
  Optimized updates by reconciling changes in memory before rendering in the real DOM.  
- **Unidirectional Data Flow**:  
  Data flows from parent to child via props, simplifying state management.

#### **Key Elements**
- **JSX**:  
  A syntax extension that combines JavaScript with HTML-like code for creating UI.  
  ```jsx
  const element = <h1>Hello, World!</h1>;
  ```  
- **Props**:  
  Pass data from parent to child components. Props are immutable.  
- **State**:  
  Internal, mutable data within a component to track dynamic values.  
- **Children**:  
  Nest components or elements using the special `children` prop.  

#### **Advanced Features**
- **Hooks**:  
  Enable state and lifecycle methods in functional components.  
  - `useState`, `useEffect`, `useContext`, `useRef`, etc.  
- **Context API**:  
  Share data across components without prop drilling.  
- **Refs**:  
  Access DOM elements or component instances directly.  
- **Portals**:  
  Render children into a DOM node outside the parent hierarchy.  

#### **Efficiency and Error Handling**
- **Keys**:  
  Unique IDs for elements in lists to optimize rendering.  
- **Error Boundaries**:  
  Catch errors in components and provide fallback UIs.  

#### **Styling and Miscellaneous**
- **Fragments**:  
  Group elements without adding extra DOM nodes.  
  ```jsx
  <React.Fragment>
    <h1>Hello</h1>
    <p>World!</p>
  </React.Fragment>
  ```  
- **Controlled Components**:  
  Form elements where React controls the value.  
- **Strict Mode**:  
  Helps detect potential issues in an application.  
- **Suspense**:  
  Handle asynchronous rendering, often for lazy-loaded components.  

---

This cheat sheet is your quick reference for studying and using React!




### React Cheat Sheet: Key Features  

- **Components**:  
  Reusable, independent pieces of UI logic encapsulated as functions or classes.  

- **JSX (JavaScript XML)**:  
  A syntax extension that combines JavaScript and HTML-like code for writing UI components.  

- **Curly Braces**:  
  Embed dynamic JavaScript expressions within JSX. Example: `{expression}`.

- **Fragments**:  
  Group multiple JSX elements without adding extra DOM nodes. Use `<></>` or `<React.Fragment>`.  

- **Props (Properties)**:  
  Read-only data passed from parent to child components for customization.  

- **Children**:  
  Special `props` for nesting elements or components within another component.  

- **Keys**:  
  Unique identifiers for efficient list rendering and reconciliation.  

- **Rendering**:  
  React efficiently updates and renders UI changes via a virtual DOM.  

- **Event Handling**:  
  Use camelCase syntax for events, e.g., `onClick`. Event handlers receive synthetic events.  

- **State**:  
  Mutable data managed within components to track changes.  

- **Controlled Components**:  
  Components where React controls input values via state.  

- **Hooks**:  
  Functions like `useState`, `useEffect` enable state and lifecycle management in functional components.  

- **Purity**:  
  React components should act like pure functions, producing the same output for the same input.  

- **Strict Mode**:  
  Highlights potential issues by performing additional checks in development mode.  

- **Effects**:  
  Side effects (e.g., API calls) are handled with `useEffect`.  

- **Refs**:  
  Provide access to DOM elements or component instances directly via `useRef`.  

- **Context**:  
  Enables sharing state across components without prop drilling using `React.createContext`.  

- **Portals**:  
  Render components outside the DOM hierarchy using `ReactDOM.createPortal`.  

- **Suspense**:  
  Handles asynchronous rendering, often used with lazy-loaded components.  

- **Error Boundaries**:  
  Components that catch JavaScript errors in the component tree and display fallback UIs.
