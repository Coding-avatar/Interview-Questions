<h1 id="top">javascript Last minute questionaire</h1>
<h2>List of Topics</h2>
<ol type="a">
    <li>
        <details open>
            <summary><h3>JavaScript Basics & Fundamentals</h3></summary>
            <ol>
                <li><a href="#q1">What are Data Types in JavaScript (Primitive vs Reference)?</a></li>
                <li><a href="#q2">What is the difference between <code>var</code>, <code>let</code>, and <code>const</code>?</a></li>
                <li><a href="#q3">What is Type Coercion and Implicit vs Explicit conversion?</a></li>
                <li><a href="#q4">What is the difference between <code>==</code> and <code>===</code>?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Scopes & Closures</h3></summary>
            <ol>
                <li><a href="#q5">What is Scope (Global, Function, Block)?</a></li>
                <li><a href="#q6">What is Lexical Scope?</a></li>
                <li><a href="#q7">What is a Closure and what are its practical use cases?</a></li>
                <li><a href="#q8">What is Hoisting in JavaScript?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Objects, Functions & Prototypes</h3></summary>
            <ol>
                <li><a href="#q9">How does the <code>this</code> keyword work in JavaScript?</a></li>
                <li><a href="#q10">What is the difference between <code>call()</code>, <code>apply()</code>, and <code>bind()</code>?</a></li>
                <li><a href="#q11">What are Arrow Functions vs Regular Functions?</a></li>
                <li><a href="#q12">What is Prototype and Prototypal Inheritance?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Asynchronous JavaScript & Event Loop</h3></summary>
            <ol>
                <li><a href="#q13">What is the Event Loop, Call Stack, Microtask Queue, and Macrotask Queue?</a></li>
                <li><a href="#q14">What are Promises and Promise states?</a></li>
                <li><a href="#q15">What is <code>async/await</code> and how does error handling work?</a></li>
                <li><a href="#q16">What are the differences between <code>Promise.all</code>, <code>Promise.allSettled</code>, <code>Promise.race</code>, and <code>Promise.any</code>?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>ES6+ Modern Features</h3></summary>
            <ol>
                <li><a href="#q17">What is Destructuring Assignment (Arrays & Objects)?</a></li>
                <li><a href="#q18">What are Rest and Spread operators?</a></li>
                <li><a href="#q19">What are Modules (ESM vs CommonJS)?</a></li>
                <li><a href="#q20">What are Map, Set, WeakMap, and WeakSet?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>DOM Manipulation & Web Performance</h3></summary>
            <ol>
                <li><a href="#q21">What is Event Bubbling and Event Capturing?</a></li>
                <li><a href="#q22">What is Event Delegation?</a></li>
                <li><a href="#q23">What is the difference between <code>localStorage</code>, <code>sessionStorage</code>, and <code>cookies</code>?</a></li>
                <li><a href="#q24">What is Debouncing and Throttling?</a></li>
            </ol>
        </details>
    </li>
</ol>

<hr />
<h2>Answers Section</h2>

<!-- JavaScript Basics & Fundamentals -->
<h3 id="q1">1. What are Data Types in JavaScript (Primitive vs Reference)?</h3>
<p><strong>Short Answer:</strong> JavaScript has 7 primitive data types (String, Number, Boolean, Undefined, Null, Symbol, BigInt) stored directly by value in stack memory, and Reference types (Objects, Arrays, Functions) stored by memory reference in heap memory.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Primitive Types:</b> Immutable values passed by value. When assigned to another variable, a copy of the actual value is created.</p>

```javascript
let x = 10;
let y = x; // y gets a copy of 10
y = 20;    // x remains 10
```

<p><b>Reference Types:</b> Mutable complex structures (Objects, Arrays, Functions, Dates) passed by reference. Variables store a pointer to memory in the heap.</p>

```javascript
let obj1 = { name: "Alice" };
let obj2 = obj1; // obj2 shares the same reference
obj2.name = "Bob"; // obj1.name is now also "Bob"
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q2">2. What is the difference between <code>var</code>, <code>let</code>, and <code>const</code>?</h3>
<p><strong>Short Answer:</strong> <code>var</code> is function-scoped and hoisted with <code>undefined</code>. <code>let</code> and <code>const</code> are block-scoped, hoisted in the Temporal Dead Zone (TDZ), and <code>const</code> prevents re-assignment.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b><code>var</code>:</b> Function-scoped or globally scoped. Can be re-declared and updated. Hoisted and initialized to <code>undefined</code>.</li>
  <li><b><code>let</code>:</b> Block-scoped (<code>{}</code>). Can be updated but not re-declared within the same scope. Hoisted but not initialized (TDZ).</li>
  <li><b><code>const</code>:</b> Block-scoped. Cannot be updated or re-declared. Must be initialized at declaration time. Object properties inside a <code>const</code> object can still be mutated.</li>
</ul>

```javascript
// Block scope example
if (true) {
  var a = 1;
  let b = 2;
  const c = 3;
}
console.log(a); // 1 (accessible)
// console.log(b); // ReferenceError
// console.log(c); // ReferenceError
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q3">3. What is Type Coercion and Implicit vs Explicit conversion?</h3>
<p><strong>Short Answer:</strong> Type coercion is the automatic or manual conversion of values from one data type to another. Implicit coercion occurs automatically via JS operators, while Explicit conversion is developer-driven using functions like <code>Number()</code> or <code>String()</code>.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Implicit Coercion:</b></p>

```javascript
console.log("5" + 2); // "52" (number coerced to string due to + operator)
console.log("5" - 2); // 3    (string coerced to number due to - operator)
console.log(true + 1); // 2    (boolean coerced to 1)
```

<p><b>Explicit Conversion:</b></p>

```javascript
let str = "123";
let num = Number(str); // 123
let bool = Boolean(1);  // true
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q4">4. What is the difference between <code>==</code> and <code>===</code>?</h3>
<p><strong>Short Answer:</strong> <code>==</code> (abstract equality) performs implicit type coercion before comparison, whereas <code>===</code> (strict equality) compares both value and type without coercion.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
console.log(5 == "5");           // true (string "5" coerced to number 5)
console.log(5 === "5");          // false (different data types)
console.log(null == undefined);  // true
console.log(null === undefined); // false
```
<p><b>Best Practice:</b> Always use <code>===</code> to avoid unexpected bugs resulting from implicit type coercion.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Scopes & Closures -->
<h3 id="q5">5. What is Scope (Global, Function, Block)?</h3>
<p><strong>Short Answer:</strong> Scope determines the accessibility/visibility of variables in different parts of the code. JavaScript has Global Scope, Function Scope, and Block Scope.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Global Scope:</b> Variables declared outside any function or block are globally accessible.</li>
  <li><b>Function Scope:</b> Variables declared with <code>var</code> inside a function are accessible only within that function.</li>
  <li><b>Block Scope:</b> Variables declared with <code>let</code> and <code>const</code> inside curly braces <code>{}</code> are accessible only within that block.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q6">6. What is Lexical Scope?</h3>
<p><strong>Short Answer:</strong> Lexical scope means that variable resolution depends on where functions and blocks are physically written in the code structure at compile time, not where they are invoked.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>An inner function always has access to the outer function's scope variables due to lexical scoping linked at function creation time.</p>

```javascript
function outer() {
  const name = "JavaScript";
  function inner() {
    console.log(name); // Accesses `name` from outer lexical scope
  }
  inner();
}
outer(); // Output: "JavaScript"
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q7">7. What is a Closure and what are its practical use cases?</h3>
<p><strong>Short Answer:</strong> A closure is a function bundled together with references to its surrounding lexical environment, allowing an inner function to access variables from an outer scope even after the outer function has finished executing.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p><b>Example of Closure:</b></p>

```javascript
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
```

<p><b>Practical Use Cases:</b></p>
<ul>
  <li>Data privacy & encapsulation (private variables).</li>
  <li>Function currying and partial application.</li>
  <li>Event handlers maintaining state.</li>
  <li>Memoization and caching functions.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q8">8. What is Hoisting in JavaScript?</h3>
<p><strong>Short Answer:</strong> Hoisting is JavaScript's default behavior of lifting variable and function declarations to the top of their containing scope during the compilation phase before execution.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Function Declarations:</b> Hoisted completely with their definition, allowing them to be called before declaration.</li>
  <li><b><code>var</code>:</b> Hoisted and initialized to <code>undefined</code>.</li>
  <li><b><code>let</code> & <code>const</code>:</b> Hoisted into the Temporal Dead Zone (TDZ); accessing them before declaration throws a <code>ReferenceError</code>.</li>
</ul>

```javascript
console.log(x); // undefined (var hoisted)
var x = 5;

// console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Objects, Functions & Prototypes -->
<h3 id="q9">9. How does the <code>this</code> keyword work in JavaScript?</h3>
<p><strong>Short Answer:</strong> The value of <code>this</code> depends on how and where a function is invoked: implicit object binding, explicit binding (<code>call</code>/<code>apply</code>/<code>bind</code>), <code>new</code> constructor binding, or lexical binding (arrow functions).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Global context:</b> Points to <code>window</code> (browser) or <code>global</code> (Node.js), or <code>undefined</code> in strict mode.</li>
  <li><b>Object method:</b> Points to the owner object (`obj.method()`).</li>
  <li><b>Arrow functions:</b> Retain <code>this</code> lexically from their enclosing scope.</li>
  <li><b>Constructor function (<code>new</code>):</b> Points to the newly created instance object.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q10">10. What is the difference between <code>call()</code>, <code>apply()</code>, and <code>bind()</code>?</h3>
<p><strong>Short Answer:</strong> <code>call()</code> invokes a function setting <code>this</code> with arguments individually. <code>apply()</code> invokes it with arguments as an array. <code>bind()</code> returns a new function with bound <code>this</code> for future invocation.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
function greet(greeting, punctuation) {
  return `${greeting}, ${this.name}${punctuation}`;
}

const user = { name: "Alex" };

// call: arguments passed individually
console.log(greet.call(user, "Hello", "!")); // "Hello, Alex!"

// apply: arguments passed in an array
console.log(greet.apply(user, ["Hi", "."]));  // "Hi, Alex."

// bind: returns a new function
const boundGreet = greet.bind(user, "Hey");
console.log(boundGreet("?"));               // "Hey, Alex?"
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q11">11. What are Arrow Functions vs Regular Functions?</h3>
<p><strong>Short Answer:</strong> Arrow functions provide shorter syntax and bind <code>this</code> lexically. Unlike regular functions, they lack their own <code>this</code>, <code>arguments</code> object, <code>super</code>, and cannot be used as constructors with <code>new</code>.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
const obj = {
  name: "JS",
  regularFn: function() {
    console.log(this.name); // "JS"
  },
  arrowFn: () => {
    console.log(this.name); // undefined (lexical `this` from outer scope)
  }
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q12">12. What is Prototype and Prototypal Inheritance?</h3>
<p><strong>Short Answer:</strong> Every JavaScript object has an internal link to a prototype object (`[[Prototype]]`). Prototypal inheritance allows objects to inherit properties and methods from other objects along the prototype chain.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>When accessing a property on an object, JavaScript first looks at the object itself. If not found, it traverses up the prototype chain until the property is found or <code>null</code> is reached.</p>

```javascript
const parent = { greet() { return "Hello"; } };
const child = Object.create(parent);

console.log(child.greet()); // "Hello" (inherited from parent prototype)
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Asynchronous JavaScript & Event Loop -->
<h3 id="q13">13. What is the Event Loop, Call Stack, Microtask Queue, and Macrotask Queue?</h3>
<p><strong>Short Answer:</strong> The Event Loop enables single-threaded JS to perform non-blocking operations. It executes synchronous code on the Call Stack, then processes all Microtasks (Promises), and finally executes Macrotasks (<code>setTimeout</code>, I/O).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Call Stack:</b> Executes synchronous function execution contexts.</li>
  <li><b>Microtask Queue:</b> Holds microtask callbacks (Promises, <code>queueMicrotask</code>, <code>MutationObserver</code>). Processed completely after current stack empties.</li>
  <li><b>Macrotask Queue:</b> Holds macrotasks (<code>setTimeout</code>, <code>setInterval</code>, <code>requestAnimationFrame</code>, I/O). One macrotask is executed per event loop iteration.</li>
</ul>

```javascript
console.log('1'); // Synchronous
setTimeout(() => console.log('2'), 0); // Macrotask
Promise.resolve().then(() => console.log('3')); // Microtask
console.log('4'); // Synchronous

// Output order: 1, 4, 3, 2
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q14">14. What are Promises and Promise states?</h3>
<p><strong>Short Answer:</strong> A Promise is an object representing the eventual completion or failure of an asynchronous operation. A Promise can be in one of three states: <code>pending</code>, <code>fulfilled</code>, or <code>rejected</code>.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Pending:</b> Initial state, neither fulfilled nor rejected.</li>
  <li><b>Fulfilled:</b> Asynchronous operation completed successfully (`resolve()`).</li>
  <li><b>Rejected:</b> Asynchronous operation failed (`reject()`).</li>
</ul>
<p>Once settled (`fulfilled` or `rejected`), a Promise becomes immutable and state cannot change.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q15">15. What is <code>async/await</code> and how does error handling work?</h3>
<p><strong>Short Answer:</strong> <code>async/await</code> is syntactic sugar built on Promises, allowing asynchronous code to be written synchronously. Error handling is managed using standard <code>try...catch</code> blocks.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    return data;
  } catch (error) {
    console.error('Error fetching data:', error);
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q16">16. What are the differences between <code>Promise.all</code>, <code>Promise.allSettled</code>, <code>Promise.race</code>, and <code>Promise.any</code>?</h3>
<p><strong>Short Answer:</strong></p>
<ul>
  <li><code>Promise.all</code>: Fails fast on first rejection; resolves when all succeed.</li>
  <li><code>Promise.allSettled</code>: Resolves when all promises settle (fulfilled or rejected).</li>
  <li><code>Promise.race</code>: Settles as soon as the first promise settles.</li>
  <li><code>Promise.any</code>: Resolves as soon as the first promise fulfills; rejects if all reject.</li>
</ul>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Method</th>
      <th>Resolves When</th>
      <th>Rejects When</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>Promise.all</code></td>
      <td>All promises resolve</td>
      <td>Any promise rejects (fails fast)</td>
    </tr>
    <tr>
      <td><code>Promise.allSettled</code></td>
      <td>All promises finish (fulfill or reject)</td>
      <td>Never rejects</td>
    </tr>
    <tr>
      <td><code>Promise.race</code></td>
      <td>First promise settles (fulfills/rejects)</td>
      <td>First promise settles (fulfills/rejects)</td>
    </tr>
    <tr>
      <td><code>Promise.any</code></td>
      <td>First promise fulfills</td>
      <td>All promises reject (AggregateError)</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- ES6+ Modern Features -->
<h3 id="q17">17. What is Destructuring Assignment (Arrays & Objects)?</h3>
<p><strong>Short Answer:</strong> Destructuring is an ES6 syntax that allows extracting values from arrays or properties from objects into distinct variables cleanly.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
// Object Destructuring
const user = { name: "John", age: 30 };
const { name, age: userAge } = user;

// Array Destructuring
const colors = ["red", "green", "blue"];
const [firstColor, secondColor] = colors;
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q18">18. What are Rest and Spread operators?</h3>
<p><strong>Short Answer:</strong> The <code>...</code> syntax acts as Spread when expanding elements/properties, and as Rest when collecting multiple values into a single array/object parameter.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
// Spread: expands elements
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4]; // [1, 2, 3, 4]

// Rest: collects arguments
function sum(...numbers) {
  return numbers.reduce((acc, curr) => acc + curr, 0);
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q19">19. What are Modules (ESM vs CommonJS)?</h3>
<p><strong>Short Answer:</strong> CommonJS uses <code>require()</code> and <code>module.exports</code> (synchronous/Node legacy). ESM uses <code>import</code> and <code>export</code> (static/asynchronous/modern standard).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>CommonJS:</b> Loaded at runtime synchronously. Dynamic imports supported natively.</li>
  <li><b>ES Modules (ESM):</b> Parsed statically at compile time, enabling tree-shaking (dead code elimination) and async loading natively in modern browsers.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q20">20. What are Map, Set, WeakMap, and WeakSet?</h3>
<p><strong>Short Answer:</strong> <code>Map</code> stores key-value pairs (any data type keys). <code>Set</code> stores unique values. <code>WeakMap</code> and <code>WeakSet</code> hold weak references to object keys only, allowing garbage collection when no other references exist.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Map:</b> Key-value pairs maintaining insertion order. Keys can be primitives or objects.</li>
  <li><b>Set:</b> Collection of unique values of any type.</li>
  <li><b>WeakMap / WeakSet:</b> Keys must be objects. Cannot be iterated and prevent memory leaks when binding temporary metadata to objects/DOM nodes.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- DOM Manipulation & Web Performance -->
<h3 id="q21">21. What is Event Bubbling and Event Capturing?</h3>
<p><strong>Short Answer:</strong> Capturing phase trickles event down from the window to the target element. Bubbling phase propagates event up from target element back to window. Events bubble by default.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<p>In <code>addEventListener(event, handler, useCapture)</code>, setting <code>useCapture = true</code> listens during the capturing phase, whereas <code>false</code> (default) listens during bubbling.</p>
<p>Call <code>event.stopPropagation()</code> to prevent further propagation.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q22">22. What is Event Delegation?</h3>
<p><strong>Short Answer:</strong> Event Delegation is a pattern of attaching a single event listener to a parent element to handle events triggered on current or dynamic child elements using event bubbling.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```javascript
document.getElementById("parent-list").addEventListener("click", (event) => {
  if (event.target && event.target.nodeName === "LI") {
    console.log("List item clicked:", event.target.innerText);
  }
});
```
<p><b>Benefits:</b> Reduces total memory usage and eliminates the need to attach listeners to newly added dynamic DOM nodes.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q23">23. What is the difference between <code>localStorage</code>, <code>sessionStorage</code>, and <code>cookies</code>?</h3>
<p><strong>Short Answer:</strong></p>
<ul>
  <li><code>localStorage</code>: Persists permanently until manually cleared (~5-10MB limit).</li>
  <li><code>sessionStorage</code>: Persists until tab/window is closed (~5MB limit).</li>
  <li><code>cookies</code>: Sent with HTTP requests, smaller size limit (~4KB), supports expiration & security flags (<code>HttpOnly</code>, <code>SameSite</code>).</li>
</ul>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Feature</th>
      <th>localStorage</th>
      <th>sessionStorage</th>
      <th>Cookies</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Expiration</b></td>
      <td>Never (until cleared)</td>
      <td>On tab close</td>
      <td>Manually set expiration</td>
    </tr>
    <tr>
      <td><b>Capacity</b></td>
      <td>~5-10MB</td>
      <td>~5MB</td>
      <td>~4KB</td>
    </tr>
    <tr>
      <td><b>Server Transmission</b></td>
      <td>No</td>
      <td>No</td>
      <td>Yes (sent automatically with requests)</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q24">24. What is Debouncing and Throttling?</h3>
<p><strong>Short Answer:</strong> Debouncing delays function execution until a specified delay has elapsed since the last event invocation. Throttling limits function execution to once per specified time interval.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>
<ul>
  <li><b>Debounce:</b> Best for search auto-complete inputs or window resizing where action should run only after the user stops typing.</li>
  <li><b>Throttle:</b> Best for infinite scrolling or mousemove tracking where execution is throttled to regular intervals.</li>
</ul>

```javascript
// Debounce implementation
function debounce(fn, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />
