<h1 id="top">React Last Minute Questionnaire</h1>
<h2>List of Topics</h2>
<ol type="a">
    <li>
        <details open>
            <summary><h3>React Basics & Core Concepts</h3></summary>
            <ol>
                <li><a href="#q1">What is React?</a></li>
                <li><a href="#q2">What is Virtual DOM? How is it different from Real DOM and Shadow DOM?</a></li>
                <li><a href="#q3">What are Props and State in React?</a></li>
                <li><a href="#q4">What are React Hooks and what are the rules of Hooks?</a></li>
                <li><a href="#q5">What is Micro-frontend architecture?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>State Management</h3></summary>
            <ol>
                <li><a href="#q6">What is Context API and when should you use it?</a></li>
                <li><a href="#q7">What is Redux and Redux Toolkit?</a></li>
                <li><a href="#q8">What is Middleware in Redux (Thunk vs Saga)?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Data Fetching & Asynchronous Operations</h3></summary>
            <ol>
                <li><a href="#q9">How do you handle race conditions in React when fetching data?</a></li>
                <li><a href="#q10">How do you handle file uploads in React using Axios or Fetch?</a></li>
                <li><a href="#q11">How do you handle file downloads in React using Axios or Fetch?</a></li>
                <li><a href="#q12">How do you handle binary data in React using Axios or Fetch?</a></li>
                <li><a href="#q13">How do you implement a file upload progress bar in React?</a></li>
                <li><a href="#q14">How do you implement a file download progress bar in React?</a></li>
                <li><a href="#q15">How do you handle JSON Web Tokens (JWT) when fetching data?</a></li>
                <li><a href="#q16">How do you implement retries and exponential backoff when fetching data?</a></li>
                <li><a href="#q17">How do you handle request timeouts when fetching data?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Performance Optimization</h3></summary>
            <ol>
                <li><a href="#q18">How do you optimize a React application?</a></li>
                <li><a href="#q19">How do you handle data caching in React to reduce network requests?</a></li>
                <li><a href="#q20">How do you implement optimistic updates in React?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Securing React Applications</h3></summary>
            <ol>
                <li><a href="#q21">What are SAST and DAST security scans in React development?</a></li>
                <li><a href="#q22">What is Template Injection (XSS) in React and how to prevent it?</a></li>
                <li><a href="#q23">What is Content Security Policy (Trust Policy)?</a></li>
                <li><a href="#q24">How do you whitelist components securely in React?</a></li>
                <li><a href="#q25">What is Insecure Direct Object Reference (IDOR)?</a></li>
                <li><a href="#q26">What is CSRF (Cross-Site Request Forgery) and how to prevent it?</a></li>
            </ol>
        </details>
    </li>
</ol>

<hr />
<h2>Answers Section</h2>

<!-- React Basics & Core Concepts -->
<h3 id="q1">1. What is React?</h3>
<p><strong>Short Answer:</strong> React is an open-source JavaScript library developed by Meta for building declarative, efficient, and component-based user interfaces for web and native applications.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Core Features:</b></p>
<ul>
  <li><b>Component-Based Architecture:</b> UIs are built using isolated, reusable components that manage their own state.</li>
  <li><b>Declarative UI:</b> You describe how the UI should look for a given state, and React handles efficient rendering.</li>
  <li><b>Virtual DOM:</b> Uses an in-memory representation of DOM nodes to perform fast diffing and batch actual DOM updates.</li>
  <li><b>Unidirectional Data Flow:</b> Data flows top-down from parent to child components via props, making state changes predictable.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q2">2. What is Virtual DOM? How is it different from Real DOM and Shadow DOM?</h3>
<p><strong>Short Answer:</strong> Virtual DOM is a lightweight JS object tree representing the UI used by React for fast diffing. Real DOM is the actual browser render tree. Shadow DOM is a browser technology for scoping CSS and encapsulating DOM elements inside Web Components.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Feature</th>
      <th>Virtual DOM</th>
      <th>Real DOM</th>
      <th>Shadow DOM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Definition</b></td>
      <td>In-memory JS abstraction of the DOM</td>
      <td>Actual browser HTML document tree</td>
      <td>Browser standard for Web Component encapsulation</td>
    </tr>
    <tr>
      <td><b>Performance</b></td>
      <td>Fast (batches updates via Diffing/Reconciliation)</td>
      <td>Slow (triggers expensive layout reflows/repaints)</td>
      <td>Fast (isolated sub-tree rendering)</td>
    </tr>
    <tr>
      <td><b>CSS Isolation</b></td>
      <td>No built-in CSS scoping (requires CSS Modules/Styled-Components)</td>
      <td>Global stylesheet scope</td>
      <td>Native scope isolation (styles inside don't leak out)</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q3">3. What are Props and State in React?</h3>
<p><strong>Short Answer:</strong> Props (properties) are read-only inputs passed down from parent to child components. State is a mutable, internal data structure managed within a component that triggers re-renders when modified.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
// Parent passing Props
function Parent() {
  return <Child name="Alice" />;
}

// Child receiving Props & managing State
function Child({ name }) {
  const [count, setCount] = useState(0); // State

  return (
    <div>
      <p>Hello {name}, Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q4">4. What are React Hooks and what are the rules of Hooks?</h3>
<p><strong>Short Answer:</strong> Hooks are functions (e.g. <code>useState</code>, <code>useEffect</code>, <code>useContext</code>) that let functional components use state and lifecycle features. Rules: 1) Only call Hooks at the top level. 2) Only call Hooks from React function components or custom Hooks.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Rules of Hooks:</b></p>
<ol>
  <li><b>Call Hooks at the Top Level:</b> Don't call Hooks inside loops, conditions, or nested functions to preserve Hook call order across renders.</li>
  <li><b>Only Call Hooks from React Functions:</b> Don't call Hooks from regular JS functions.</li>
</ol>

```jsx
function MyComponent() {
  // Correct: Top level
  const [data, setData] = useState(null);
  
  useEffect(() => {
    // Side effect logic
  }, []);
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q5">5. What is Micro-frontend architecture?</h3>
<p><strong>Short Answer:</strong> Micro-frontends extend the concept of microservices to the frontend, enabling modular and scalable development by breaking monolithic applications into smaller, independently deployable frontend applications.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>This is commonly achieved using <b>Webpack Module Federation</b> or single-spa frameworks. Different teams can develop, test, and deploy separate React applications independently, which are then stitched together at runtime inside a container application.</p>
<p>Reference: <a href="https://medium.com/@chirag.dave/a-complete-guide-to-react-micro-frontends-930229dc812a" target="_blank">A Complete Guide to React Micro-Frontends</a></p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- State Management -->
<h3 id="q6">6. What is Context API and when should you use it?</h3>
<p><strong>Short Answer:</strong> Context API is a built-in feature allowing global state sharing across the component tree without prop drilling. It is best suited for low-frequency updates like authentication status, user profile, theme, or language settings.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>Avoid using Context API for frequently changing state (e.g., complex dashboards, real-time data feeds) because every consuming component re-renders whenever the context value updates. In those cases, prefer Redux Toolkit, Zustand, or Jotai.</p>

```jsx
import React, { createContext, useContext, useState } from 'react';

const UserContext = createContext(undefined);

export function UserProvider({ children }) {
  const [user, setUser] = useState(null);

  const login = (userData) => setUser(userData);
  const logout = () => setUser(null);

  return (
    <UserContext.Provider value={{ user, login, logout }}>
      {children}
    </UserContext.Provider>
  );
}

export const useUser = () => useContext(UserContext);
```

<p><b>Good Use Cases:</b> Authentication state, Theme (Dark/Light), Language (i18n), User permissions, Global feature flags.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q7">7. What is Redux and Redux Toolkit?</h3>
<p><strong>Short Answer:</strong> Redux is a centralized state management library for JS apps using actions and pure reducer functions. Redux Toolkit (RTK) is the official standard set of utilities that eliminates boilerplate and simplifies store setup.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
import { createSlice, configureStore } from '@reduxjs/toolkit';

const counterSlice = createSlice({
  name: 'counter',
  initialState: { value: 0 },
  reducers: {
    increment: state => { state.value += 1; }, // Immer handles immutability
    decrement: state => { state.value -= 1; }
  }
});

export const { increment, decrement } = counterSlice.actions;
export const store = configureStore({ reducer: { counter: counterSlice.reducer } });
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q8">8. What is Middleware in Redux (Thunk vs Saga)?</h3>
<p><strong>Short Answer:</strong> Middleware provides a third-party extension point between dispatching an action and the moment it reaches the reducer. Redux Thunk uses async functions for side effects, while Redux Saga uses generator functions (<code>yield</code>) for complex asynchronous workflows.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Redux Thunk:</b> Standard built-in middleware for simple async logic (Promises/async-await). Action creators return a function instead of an action object.</li>
  <li><b>Redux Saga:</b> Uses ES6 Generator functions (<code>yield call()</code>, <code>yield put()</code>) for advanced control flow like cancellation, race conditions, debouncing, and complex background tasks.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Data Fetching & Asynchronous Operations -->
<h3 id="q9">9. How do you handle race conditions in React when fetching data?</h3>
<p><strong>Short Answer:</strong> Handle race conditions by cancelling out-of-order pending network requests using <code>AbortController</code> in <code>useEffect</code> cleanup, tracking sequence IDs, or using data-fetching libraries like TanStack Query (React Query).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
useEffect(() => {
  const controller = new AbortController();
  
  async function fetchData() {
    try {
      const response = await fetch(`/api/data?query=${query}`, {
        signal: controller.signal
      });
      const data = await response.json();
      setResults(data);
    } catch (err) {
      if (err.name !== 'AbortError') {
        setError(err);
      }
    }
  }

  fetchData();

  // Cleanup aborts stale previous requests
  return () => controller.abort();
}, [query]);
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q10">10. How do you handle file uploads in React using Axios or Fetch?</h3>
<p><strong>Short Answer:</strong> Create a <code>FormData</code> instance, append the file binary, and send it with an HTTP POST request setting the <code>Content-Type</code> header to <code>multipart/form-data</code>.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
const handleFileUpload = async (file) => {
  const formData = new FormData();
  formData.append('file', file);

  try {
    await axios.post('/api/upload', formData, {
      headers: { 'Content-Type': 'multipart/form-data' }
    });
  } catch (error) {
    console.error('Upload failed:', error);
  }
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q11">11. How do you handle file downloads in React using Axios or Fetch?</h3>
<p><strong>Short Answer:</strong> Request the file with <code>responseType: 'blob'</code>, convert the returned data into an Object URL via <code>URL.createObjectURL(blob)</code>, and programmatically trigger an anchor download click.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
const downloadFile = async () => {
  const response = await axios.get('/api/download', { responseType: 'blob' });
  const url = window.URL.createObjectURL(new Blob([response.data]));
  const link = document.createElement('a');
  link.href = url;
  link.setAttribute('download', 'file.pdf');
  document.body.appendChild(link);
  link.click();
  link.remove();
  window.URL.revokeObjectURL(url);
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q12">12. How do you handle binary data in React using Axios or Fetch?</h3>
<p><strong>Short Answer:</strong> Set the request option <code>responseType</code> to <code>'arraybuffer'</code> or <code>'blob'</code> in Axios/Fetch options to process raw binary streams like images, PDFs, or audio files.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
const fetchImage = async () => {
  const response = await fetch('/api/image', { headers: { Accept: 'image/png' } });
  const blob = await response.blob();
  const imageUrl = URL.createObjectURL(blob);
  setImageSrc(imageUrl);
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q13">13. How do you implement a file upload progress bar in React?</h3>
<p><strong>Short Answer:</strong> Use the <code>onUploadProgress</code> callback in Axios to monitor loaded bytes vs total bytes and update progress percentage state in the UI.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
const uploadWithProgress = (file) => {
  const formData = new FormData();
  formData.append('file', file);

  axios.post('/api/upload', formData, {
    onUploadProgress: (progressEvent) => {
      const percentCompleted = Math.round(
        (progressEvent.loaded * 100) / progressEvent.total
      );
      setProgress(percentCompleted);
    }
  });
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q14">14. How do you implement a file download progress bar in React?</h3>
<p><strong>Short Answer:</strong> Use the <code>onDownloadProgress</code> callback in Axios (or read response body stream chunks in Fetch) to track downloaded bytes against the <code>Content-Length</code> header and update UI progress.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
axios.get('/api/file', {
  responseType: 'blob',
  onDownloadProgress: (progressEvent) => {
    const percent = Math.round((progressEvent.loaded * 100) / progressEvent.total);
    setDownloadProgress(percent);
  }
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q15">15. How do you handle JSON Web Tokens (JWT) when fetching data?</h3>
<p><strong>Short Answer:</strong> Store the JWT securely and append it to the HTTP <code>Authorization</code> header using the format <code>Bearer &lt;token&gt;</code> on requests, typically using Axios interceptors.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
// Axios Interceptor for JWT
axios.interceptors.request.use((config) => {
  const token = localStorage.getItem('authToken');
  if (token) {
    config.headers.Authorization = `Bearer ${token}`;
  }
  return config;
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q16">16. How do you implement retries and exponential backoff when fetching data?</h3>
<p><strong>Short Answer:</strong> Implement retries by catching errors inside a loop and delaying successive attempts exponentially (e.g., 1s, 2s, 4s, 8s) using a <code>setTimeout</code> promise helper.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
async function fetchWithRetry(url, retries = 3, backoff = 1000) {
  try {
    return await fetch(url);
  } catch (err) {
    if (retries === 0) throw err;
    await new Promise(res => setTimeout(res, backoff));
    return fetchWithRetry(url, retries - 1, backoff * 2);
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q17">17. How do you handle request timeouts when fetching data?</h3>
<p><strong>Short Answer:</strong> Specify a <code>timeout</code> configuration option in Axios, or pass an <code>AbortSignal.timeout(ms)</code> signal into standard <code>fetch()</code> options.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
// Fetch with AbortSignal Timeout
try {
  const response = await fetch('/api/data', {
    signal: AbortSignal.timeout(5000) // 5 second timeout
  });
} catch (err) {
  if (err.name === 'TimeoutError') {
    console.error('Request timed out');
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Performance Optimization -->
<h3 id="q18">18. How do you optimize a React application?</h3>
<p><strong>Short Answer:</strong> Optimize React apps by using code splitting (<code>React.lazy</code>/<code>Suspense</code>), memoizing components (<code>React.memo</code>, <code>useMemo</code>, <code>useCallback</code>), list virtualization (<code>react-window</code>), and reducing re-renders.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Code Splitting:</b> Load route components lazily using dynamic imports and <code>React.lazy()</code>.</li>
  <li><b>Memoization:</b> Wrap pure components with <code>React.memo</code> and cache expensive calculations with <code>useMemo</code> and callbacks with <code>useCallback</code>.</li>
  <li><b>List Virtualization:</b> Render only visible window items for huge lists using <code>react-window</code> or <code>react-virtualized</code>.</li>
  <li><b>State Colocation:</b> Keep state as close to where it is used as possible to limit re-render scope.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q19">19. How do you handle data caching in React to reduce network requests?</h3>
<p><strong>Short Answer:</strong> Use specialized server-state management libraries like React Query (TanStack Query), RTK Query, or SWR, which provide automatic caching, request deduplication, and stale-while-revalidate strategies.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>These libraries maintain an in-memory cache map keyed by query identifiers. If a query is requested again, cached data is served instantly while fetching fresh data in the background if stale.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q20">20. How do you implement optimistic updates in React?</h3>
<p><strong>Short Answer:</strong> Update the UI state immediately before receiving the server confirmation. If the server request fails, catch the error and revert the UI state back to its previous snapshot.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
const handleAddTodo = async (newTodo) => {
  const previousTodos = todos;
  setTodos(prev => [...prev, newTodo]); // Optimistic update

  try {
    await api.post('/todos', newTodo);
  } catch (error) {
    setTodos(previousTodos); // Rollback on error
  }
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Securing React Applications -->
<h3 id="q21">21. What are SAST and DAST security scans in React development?</h3>
<p><strong>Short Answer:</strong> SAST (Static Application Security Testing) inspects source code for security flaws at rest during development. DAST (Dynamic Application Security Testing) tests the live running app for runtime vulnerabilities from the outside.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>SAST:</b> Tools like SonarQube, ESLint security plugins, and Snyk analyze source code before building/deploying.</li>
  <li><b>DAST:</b> Tools like OWASP ZAP scan deployed endpoints, evaluating HTTP responses, cookies, and headers for real-world exploits.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q22">22. What is Template Injection (XSS) in React and how to prevent it?</h3>
<p><strong>Short Answer:</strong> Cross-Site Scripting (XSS) occurs when untrusted user input is rendered as executable code. React automatically escapes strings in JSX, but using <code>dangerouslySetInnerHTML</code> bypassing escaping creates XSS risks. Prevent it using <code>DOMPurify</code>.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
import DOMPurify from 'dompurify';

// Safe rendering of raw HTML
function SafeHTML({ dirtyHtml }) {
  const cleanHtml = DOMPurify.sanitize(dirtyHtml);
  return <div dangerouslySetInnerHTML={{ __html: cleanHtml }} />;
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q23">23. What is Content Security Policy (Trust Policy)?</h3>
<p><strong>Short Answer:</strong> Content Security Policy (CSP) is an HTTP security header that restricts the resources (scripts, styles, images) the browser is allowed to load for a given web page, mitigating XSS and data injection attacks.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```http
Content-Security-Policy: default-src 'self'; script-src 'self' https://trustedscripts.example.com;
```
<p>CSP restricts inline script execution and unapproved third-party domains.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q24">24. How do you whitelist components securely in React?</h3>
<p><strong>Short Answer:</strong> Securely whitelist dynamic components by creating an explicit lookup object mapping allowed string identifiers to validated component references instead of using <code>eval()</code> or unsafe dynamic evaluation.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```jsx
import AdminWidget from './AdminWidget';
import UserWidget from './UserWidget';

const ALLOWED_COMPONENTS = {
  admin: AdminWidget,
  user: UserWidget
};

function DynamicComponent({ type }) {
  const ComponentToRender = ALLOWED_COMPONENTS[type];
  if (!ComponentToRender) return <div>Invalid Component</div>;
  return <ComponentToRender />;
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q25">25. What is Insecure Direct Object Reference (IDOR)?</h3>
<p><strong>Short Answer:</strong> IDOR occurs when an application exposes internal object references (e.g., database IDs in API URLs like <code>/user/123</code>) without verifying if the requesting user is authorized to access that object.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Mitigation:</b> Always enforce strict server-side authorization checks for every requested resource ID based on the authenticated session identity, regardless of frontend UI validation.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q26">26. What is CSRF (Cross-Site Request Forgery) and how to prevent it?</h3>
<p><strong>Short Answer:</strong> CSRF tricks an authenticated user's browser into sending unauthorized requests to a target website. Prevent it using <code>SameSite</code> cookie attributes (<code>Strict</code>/<code>Lax</code>), anti-CSRF tokens, and checking custom HTTP request headers.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>SameSite Cookies:</b> Set <code>Set-Cookie: session=123; SameSite=Strict; Secure; HttpOnly</code> to prevent browsers from sending cookies on cross-site requests.</li>
  <li><b>Anti-CSRF Tokens:</b> Send a unique cryptographically signed token in headers (e.g. <code>X-CSRF-Token</code>) with modifying requests (POST, PUT, DELETE).</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />