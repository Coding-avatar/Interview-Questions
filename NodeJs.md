<h1 id="top">Node.js Last Minute Questionnaire</h1>
<h2>List of Topics</h2>
<ol type="a">
    <li>
        <details open>
            <summary><h3>Node.js Architecture & Core Internals</h3></summary>
            <ol>
                <li><a href="#q1">What is Node.js and how does it work under the hood (V8 + Libuv)?</a></li>
                <li><a href="#q2">How does non-blocking I/O and asynchronous event-driven architecture work in Node.js?</a></li>
                <li><a href="#q3">What is Libuv, thread pool (UV_THREADPOOL_SIZE), and how does Node.js handle heavy CPU vs I/O tasks?</a></li>
                <li><a href="#q4">What are the phases of the Node.js Event Loop?</a></li>
                <li><a href="#q5">How do process.nextTick(), setImmediate(), and setTimeout() differ in execution priority?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Core Modules, Streams & File System</h3></summary>
            <ol>
                <li><a href="#q6">What are Streams in Node.js and what are the 4 main types?</a></li>
                <li><a href="#q7">What is backpressure in Node.js streams and how do you handle it?</a></li>
                <li><a href="#q8">What is the difference between fs.readFile, fs.createReadStream, and fs.readFileSync?</a></li>
                <li><a href="#q9">How do Buffers and Binary Data work in Node.js?</a></li>
                <li><a href="#q10">What is the EventEmitter module and how does event-driven communication work?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Server Side Web Development & Middleware</h3></summary>
            <ol>
                <li><a href="#q11">How do you build a native HTTP/HTTPS server in Node.js without frameworks?</a></li>
                <li><a href="#q12">What is Express.js middleware architecture and how does the middleware pipeline work?</a></li>
                <li><a href="#q13">How do you handle request body parsing, streaming file uploads, and large payload limits?</a></li>
                <li><a href="#q14">How do you handle error propagation in asynchronous Express routes and global error middleware?</a></li>
                <li><a href="#q15">What is RESTful API architecture best practice in Node.js (Controller-Service-Repository pattern)?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Concurrency, Clustering & Multithreading</h3></summary>
            <ol>
                <li><a href="#q16">What is the Cluster module in Node.js and how does IPC work?</a></li>
                <li><a href="#q17">What are Worker Threads (worker_threads) and when should you use them?</a></li>
                <li><a href="#q18">What is the child_process module (spawn, exec, execFile, fork) and their differences?</a></li>
                <li><a href="#q19">How do PM2 and process managers handle zero-downtime reloads and cluster mode?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Security, Performance & Optimization</h3></summary>
            <ol>
                <li><a href="#q20">How do you prevent Denial of Service (DoS) and Event Loop blocking in Node.js?</a></li>
                <li><a href="#q21">What are essential security best practices in Node.js (Helmet, Rate Limiting, CORS)?</a></li>
                <li><a href="#q22">How do you handle authentication using JWTs, Refresh Tokens, and HTTP-only cookies?</a></li>
                <li><a href="#q23">How do memory leaks occur in Node.js and how do you debug them?</a></li>
                <li><a href="#q24">How do you optimize database connection pools (Postgres, MongoDB, Redis)?</a></li>
            </ol>
        </details>
    </li>
    <li>
        <details open>
            <summary><h3>Microservices, Real-Time & Deployment</h3></summary>
            <ol>
                <li><a href="#q25">How do WebSockets and Server-Sent Events (SSE) work for real-time applications?</a></li>
                <li><a href="#q26">How do Message Queues (BullMQ, RabbitMQ) handle background job processing?</a></li>
                <li><a href="#q27">What is Graceful Shutdown in Node.js (SIGINT, SIGTERM) and why is it essential?</a></li>
                <li><a href="#q28">How do environment configuration and structured logging (Winston/Pino) work in production?</a></li>
            </ol>
        </details>
    </li>
</ol>

<hr />
<h2>Answers Section</h2>

<!-- Node.js Architecture & Core Internals -->
<h3 id="q1">1. What is Node.js and how does it work under the hood (V8 + Libuv)?</h3>
<p><strong>Short Answer:</strong> Node.js is an open-source, cross-platform JavaScript runtime environment built on Google Chrome's V8 JavaScript engine and Libuv. V8 compiles JavaScript directly into native machine code, while Libuv provides an event loop and worker pool to execute asynchronous I/O operations non-blockingly.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Core Components of Node.js:</b></p>
<ul>
  <li><b>V8 Engine:</b> Google's high-performance C++ engine that parses, optimizes, and compiles JS code into machine code using JIT (Just-In-Time) compilation.</li>
  <li><b>Libuv:</b> A multi-platform C library that handles the Event Loop, asynchronous I/O (file system, networking, DNS), thread pool management, and child processes.</li>
  <li><b>Node Core C++ Bindings:</b> Wrappers (`node::binding`) that expose low-level C/C++ OS system calls to JavaScript modules (`fs`, `net`, `crypto`).</li>
  <li><b>Node Standard Library:</b> Built-in JavaScript modules (`http`, `path`, `stream`, `events`) consumed by developers.</li>
</ul>

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Layer</th>
      <th>Responsibilities</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>JS Application Code</b></td>
      <td>Business logic, Express routes, modules</td>
    </tr>
    <tr>
      <td><b>Node.js API</b></td>
      <td>`fs`, `http`, `crypto`, `stream` core modules</td>
    </tr>
    <tr>
      <td><b>C++ Bindings</b></td>
      <td>Bridge between V8 JS objects and C++ functions</td>
    </tr>
    <tr>
      <td><b>V8 & Libuv</b></td>
      <td>JS Execution (V8) + Event Loop & Thread Pool (Libuv)</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q2">2. How does non-blocking I/O and asynchronous event-driven architecture work in Node.js?</h3>
<p><strong>Short Answer:</strong> Node.js operates on a single-threaded main loop that delegates non-blocking I/O operations (network requests, file operations) to the OS kernel or Libuv worker threads. When operations finish, callbacks/promises are pushed to the Event Loop queues for processing.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Blocking vs Non-Blocking Execution:</b></p>

```js
// Synchronous (Blocking) - Main thread halts until file read completes
const data = fs.readFileSync('/path/file.txt');
console.log(data);
console.log('Next operation');

// Asynchronous (Non-Blocking) - Main thread continues immediately
fs.readFile('/path/file.txt', (err, data) => {
  if (err) throw err;
  console.log(data);
});
console.log('Next operation'); // Executed BEFORE file data callback!
```

<p><b>How Non-Blocking I/O Works:</b></p>
<ol>
  <li>The JS main thread initiates an asynchronous call (e.g. `fs.readFile` or `http.get`).</li>
  <li>Node.js hands off the task to Libuv. Libuv uses native OS kernel async interfaces (like `epoll` on Linux, `kqueue` on macOS, IOCP on Windows) whenever available.</li>
  <li>The main thread continues executing subsequent lines of code without waiting.</li>
  <li>When the I/O completes, the OS or thread pool notifies Libuv, which adds the callback to the Event Loop task queue.</li>
  <li>When the Call Stack becomes empty, the Event Loop picks up the callback and executes it.</li>
</ol>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q3">3. What is Libuv, thread pool (UV_THREADPOOL_SIZE), and how does Node.js handle heavy CPU vs I/O tasks?</h3>
<p><strong>Short Answer:</strong> Libuv provides a default thread pool of 4 threads used for tasks that cannot be handled asynchronously at the OS kernel level (e.g., file system I/O, DNS lookup, crypto functions, compression). Heavy CPU tasks block the main thread and should be offloaded to Worker Threads or external background services.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Libuv Thread Pool Tasks:</b></p>
<ul>
  <li><b>File System Operations:</b> `fs.readFile`, `fs.writeFile`, `fs.stat`</li>
  <li><b>Crypto Tasks:</b> `crypto.pbkdf2`, `crypto.randomBytes`, `crypto.scrypt`</li>
  <li><b>DNS Lookups:</b> `dns.lookup` (uses system getaddrinfo)</li>
  <li><b>Zlib Compression:</b> `zlib.gzip`, `zlib.deflate`</li>
</ul>

<p><b>Configuring Thread Pool Size:</b></p>

```bash
# Increase Libuv thread pool size (Max: 1024, Default: 4)
UV_THREADPOOL_SIZE=12 node server.js
```

```js
// In JS code (must be set before calling any async threadpool functions)
process.env.UV_THREADPOOL_SIZE = 8;
```

<p><b>Handling CPU-Bound Tasks vs I/O Tasks:</b></p>
<ul>
  <li><b>I/O-Bound (High Concurrency):</b> Node.js excels here because thousands of connections wait in OS kernel queues without requiring a thread per connection.</li>
  <li><b>CPU-Bound (Hashing, Image Processing, Heavy Math):</b> Blocks the single main event loop. Fix using `worker_threads`, Worker processes (`child_process.fork`), or offloading to Redis/RabbitMQ background workers.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q4">4. What are the phases of the Node.js Event Loop?</h3>
<p><strong>Short Answer:</strong> The Event Loop has 6 distinct phases executed in a cycle: Timers, Pending Callbacks, Idle/Prepare, Poll, Check, and Close Callbacks. Microtasks (`process.nextTick` and Promise resolution queues) are executed between phase transitions.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Phases of the Event Loop:</b></p>
<ol>
  <li><b>Timers Phase:</b> Executes callbacks scheduled by `setTimeout()` and `setInterval()` whose threshold has elapsed.</li>
  <li><b>Pending Callbacks Phase:</b> Executes I/O callbacks deferred from previous iterations (e.g. TCP error types like `ECONNREFUSED`).</li>
  <li><b>Idle / Prepare Phase:</b> Internal phase used only by Node.js core.</li>
  <li><b>Poll Phase:</b> Retrieves new I/O events; executes I/O related callbacks (almost all callbacks except timers, `setImmediate`, and close callbacks). If empty, it waits for incoming I/O events or moves to Check phase if `setImmediate()` is scheduled.</li>
  <li><b>Check Phase:</b> Executes callbacks scheduled by `setImmediate()`.</li>
  <li><b>Close Callbacks Phase:</b> Executes socket/handle close events (e.g., `socket.on('close', ...)`).</li>
</ol>

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Phase</th>
      <th>Executes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>Timers</b></td>
      <td>`setTimeout()`, `setInterval()` callbacks</td>
    </tr>
    <tr>
      <td><b>Poll</b></td>
      <td>Incoming I/O data, connection callbacks, file reads</td>
    </tr>
    <tr>
      <td><b>Check</b></td>
      <td>`setImmediate()` callbacks</td>
    </tr>
    <tr>
      <td><b>Close</b></td>
      <td>`socket.on('close')` handlers</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q5">5. How do process.nextTick(), setImmediate(), and setTimeout() differ in execution priority?</h3>
<p><strong>Short Answer:</strong> `process.nextTick()` fires immediately after the current operation finishes, before moving to the next Event Loop phase. `Promise.then()` microtasks run right after `nextTick()`. `setImmediate()` runs in the Check phase, while `setTimeout(fn, 0)` runs in the Timers phase on the next loop iteration.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Execution Priority Ranking:</b></p>
<ol>
  <li>Current Synchronous Execution (Call Stack)</li>
  <li>`process.nextTick()` Queue (NextTick Queue)</li>
  <li>Promise Microtask Queue (`Promise.resolve()`, `async/await`)</li>
  <li>Macrotask Queues (Event Loop Phases: Timers -> Poll -> Check -> Close)</li>
</ol>

```js
console.log('1: Sync Log');

setTimeout(() => console.log('2: setTimeout (Timers Phase)'), 0);
setImmediate(() => console.log('3: setImmediate (Check Phase)'));

Promise.resolve().then(() => console.log('4: Promise Microtask'));
process.nextTick(() => console.log('5: process.nextTick'));

console.log('6: Sync Log End');

// Output:
// 1: Sync Log
// 6: Sync Log End
// 5: process.nextTick
// 4: Promise Microtask
// 2: setTimeout (or 3 depending on timer resolution if outside I/O cycle)
// 3: setImmediate
```

<p><b>Key Difference inside I/O Callbacks:</b> Inside an I/O callback (e.g. `fs.readFile`), `setImmediate()` is ALWAYS executed before `setTimeout(fn, 0)` because the poll phase transitions immediately to the check phase.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Core Modules, Streams & File System -->
<h3 id="q6">6. What are Streams in Node.js and what are the 4 main types?</h3>
<p><strong>Short Answer:</strong> Streams are collections of data that might not be available all at once and don't fit entirely in memory. Streams process data chunk-by-chunk in a memory-efficient manner. The 4 types are Readable, Writable, Duplex, and Transform.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>The 4 Stream Types:</b></p>
<ul>
  <li><b>Readable:</b> Source of data from which data can be consumed (e.g., `fs.createReadStream`, `req` in HTTP server).</li>
  <li><b>Writable:</b> Destination to which data can be written (e.g., `fs.createWriteStream`, `res` in HTTP response).</li>
  <li><b>Duplex:</b> Stream that is both Readable and Writable independently (e.g., TCP socket, WebSocket).</li>
  <li><b>Transform:</b> Duplex stream where output is computed by modifying the input data (e.g., `zlib.createGzip`, `crypto.createCipheriv`).</li>
</ul>

```js
const fs = require('fs');
const zlib = require('zlib');

// Piping Streams: Read -> Compress (Transform) -> Write
fs.createReadStream('input.txt')
  .pipe(zlib.createGzip())
  .pipe(fs.createWriteStream('input.txt.gz'));
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q7">7. What is backpressure in Node.js streams and how do you handle it?</h3>
<p><strong>Short Answer:</strong> Backpressure occurs when a Writable stream cannot consume incoming data as fast as a Readable stream is sending it, filling the internal buffer (`highWaterMark`). Handle backpressure using `.pipe()` or `stream.pipeline()`, or by listening to `write()` returning `false` and pausing the reader until the `'drain'` event fires.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Manual Backpressure Handling:</b></p>

```js
const reader = fs.createReadStream('huge_file.iso');
const writer = fs.createWriteStream('copy.iso');

reader.on('data', (chunk) => {
  const canContinue = writer.write(chunk);
  if (!canContinue) {
    // Buffer is full (exceeded highWaterMark), pause reading
    reader.pause();
  }
});

writer.on('drain', () => {
  // Buffer flushed, resume reading
  reader.resume();
});
```

<p><b>Recommended Modern Approach (`stream.pipeline`):</b> Always use `pipeline` from `stream/promises` because it automatically handles backpressure and cleans up all stream handles if an error occurs.</p>

```js
const { pipeline } = require('stream/promises');

async function processFile() {
  await pipeline(
    fs.createReadStream('huge_file.txt'),
    zlib.createGzip(),
    fs.createWriteStream('huge_file.txt.gz')
  );
  console.log('Pipeline succeeded without memory overload');
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q8">8. What is the difference between fs.readFile, fs.createReadStream, and fs.readFileSync?</h3>
<p><strong>Short Answer:</strong> `fs.readFileSync` blocks the main thread completely until the entire file is loaded into memory. `fs.readFile` reads asynchronously into a single buffer after loading the whole file. `fs.createReadStream` loads the file chunk-by-chunk using minimal RAM, ideal for large files.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Method</th>
      <th>Execution Type</th>
      <th>Memory Usage</th>
      <th>Best Used For</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>`fs.readFileSync`</b></td>
      <td>Sync (Blocking)</td>
      <td>High (Entire File)</td>
      <td>App startup configs only</td>
    </tr>
    <tr>
      <td><b>`fs.readFile`</b></td>
      <td>Async (Callback/Promise)</td>
      <td>High (Entire File)</td>
      <td>Small files (< 10MB)</td>
    </tr>
    <tr>
      <td><b>`fs.createReadStream`</b></td>
      <td>Async (Streaming)</td>
      <td>Low (Chunk-by-chunk)</td>
      <td>Large files (GBs), video/audio, logs</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q9">9. How do Buffers and Binary Data work in Node.js?</h3>
<p><strong>Short Answer:</strong> `Buffer` is a built-in Node.js class representing a fixed-length sequence of raw binary bytes stored outside the V8 V8 heap memory. Buffers are used when dealing with binary streams, file handling, cryptographic operations, and TCP network sockets.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Buffer Operations:</b></p>

```js
// Allocate a buffer of 10 zero-filled bytes
const buf1 = Buffer.alloc(10);

// Allocate a buffer from a UTF-8 string
const buf2 = Buffer.from('Hello World', 'utf-8');

console.log(buf2); // <Buffer 48 65 6c 6c 6f 20 57 6f 72 6c 64>
console.log(buf2.toString('hex')); // 48656c6c6f20576f726c64
console.log(buf2.toString('base64')); // SGVsbG8gV29ybGQ=

// Buffer Slicing shares memory window!
const subBuf = buf2.subarray(0, 5);
console.log(subBuf.toString()); // Hello
```

<p><b>Security Note:</b> Never use the deprecated `new Buffer()` constructor because uninitialized buffers can leak sensitive unallocated memory bytes.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q10">10. What is the EventEmitter module and how does event-driven communication work?</h3>
<p><strong>Short Answer:</strong> The `EventEmitter` class (`events` module) implements the Publisher-Subscriber pattern in Node.js. Objects emit named events that trigger registered listener functions synchronously in the order they were attached.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const EventEmitter = require('events');

class OrderService extends EventEmitter {
  createOrder(orderId, amount) {
    console.log(`Order ${orderId} created`);
    // Emit event with payload
    this.emit('orderCreated', { orderId, amount });
  }
}

const orderService = new OrderService();

// Listener 1: Send Notification
orderService.on('orderCreated', (data) => {
  console.log(`Sending email for order ${data.orderId}`);
});

// Listener 2: Update Inventory (One-time listener)
orderService.once('orderCreated', (data) => {
  console.log(`Inventory updated for order ${data.orderId}`);
});

orderService.createOrder('ORD-101', 250);
```

<p><b>Preventing Memory Leaks:</b> Always clean up event listeners when component instances are destroyed (`removeListener` or `off`). If an EventEmitter exceeds default `maxListeners` (10), Node prints a memory leak warning.</p>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Server Side Web Development & Middleware -->
<h3 id="q11">11. How do you build a native HTTP/HTTPS server in Node.js without frameworks?</h3>
<p><strong>Short Answer:</strong> Use the native `http` or `https` module to instantiate a server with `http.createServer((req, res) => { ... })` and listen on a port. The request parameter is a `ReadableStream` (`IncomingMessage`) and the response parameter is a `WritableStream` (`ServerResponse`).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const http = require('http');

const server = http.createServer((req, res) => {
  const { method, url } = req;

  // Basic Routing
  if (url === '/api/health' && method === 'GET') {
    res.writeHead(200, { 'Content-Type': 'application/json' });
    return res.end(JSON.stringify({ status: 'UP', timestamp: new Date() }));
  }

  if (url === '/api/data' && method === 'POST') {
    let body = '';
    
    // Read stream chunks
    req.on('data', (chunk) => { body += chunk.toString(); });
    
    req.on('end', () => {
      const payload = JSON.parse(body);
      res.writeHead(201, { 'Content-Type': 'application/json' });
      res.end(JSON.stringify({ message: 'Received', data: payload }));
    });
    return;
  }

  res.writeHead(404, { 'Content-Type': 'text/plain' });
  res.end('Not Found');
});

server.listen(3000, () => {
  console.log('Native HTTP Server running on port 3000');
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q12">12. What is Express.js middleware architecture and how does the middleware pipeline work?</h3>
<p><strong>Short Answer:</strong> Express middleware functions have access to the Request object (`req`), Response object (`res`), and the `next` function. Middleware functions execute sequentially in the order registered, performing tasks like logging, authentication, request validation, or ending the request-response cycle.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Middleware Execution Pipeline:</b></p>

```js
const express = require('express');
const app = express();

// Middleware 1: Logger
app.use((req, res, next) => {
  console.log(`[${new Date().toISOString()}] ${req.method} ${req.url}`);
  next(); // Pass control to next middleware
});

// Middleware 2: Authentication Guard
const authenticate = (req, res, next) => {
  const authHeader = req.headers['authorization'];
  if (!authHeader) {
    return res.status(401).json({ error: 'Unauthorized' }); // End cycle
  }
  req.user = { id: 123, role: 'admin' };
  next();
};

// Route using middleware pipeline
app.get('/api/protected', authenticate, (req, res) => {
  res.json({ message: 'Secret Data', user: req.user });
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q13">13. How do you handle request body parsing, streaming file uploads, and large payload limits?</h3>
<p><strong>Short Answer:</strong> Body parsing (`express.json({ limit: '1mb' })`) parses JSON/URL-encoded payloads. For multipart file uploads, avoid buffering files entirely in RAM; instead, stream them directly to disk or S3 using libraries like `multer` or `busboy`.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const express = require('express');
const multer = require('multer');
const app = express();

// Protect against Payload Too Large DoS attacks
app.use(express.json({ limit: '100kb' })); 

// Configure file storage stream with Multer
const upload = multer({
  limits: { fileSize: 5 * 1024 * 1024 }, // 5MB limit
  storage: multer.diskStorage({
    destination: './uploads/',
    filename: (req, file, cb) => cb(null, `${Date.now()}-${file.originalname}`)
  })
});

app.post('/api/upload', upload.single('avatar'), (req, res) => {
  res.json({ file: req.file.filename, size: req.file.size });
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q14">14. How do you handle error propagation in asynchronous Express routes and global error middleware?</h3>
<p><strong>Short Answer:</strong> Express 4 does not automatically catch rejected async promises. Wrap async handlers in try-catch blocks passing errors to `next(err)`, or use `express-async-errors` / Express 5. Define a global error-handling middleware with 4 parameters: `(err, req, res, next)`.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const express = require('express');
const app = express();

// Async Handler Wrapper Helper
const asyncHandler = (fn) => (req, res, next) => {
  Promise.resolve(fn(req, res, next)).catch(next);
};

app.get('/api/users/:id', asyncHandler(async (req, res) => {
  const user = await db.findUser(req.params.id);
  if (!user) {
    const error = new Error('User Not Found');
    error.statusCode = 404;
    throw error; // Caught by asyncHandler and sent to global error middleware
  }
  res.json(user);
}));

// Global Error Middleware (MUST have 4 arguments!)
app.use((err, req, res, next) => {
  console.error(err.stack);
  const status = err.statusCode || 500;
  res.status(status).json({
    error: {
      message: err.message || 'Internal Server Error',
      status: status
    }
  });
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q15">15. What is RESTful API architecture best practice in Node.js (Controller-Service-Repository pattern)?</h3>
<p><strong>Short Answer:</strong> Separate concerns into layers: Routes handle HTTP endpoints, Controllers process req/res and status codes, Services implement core business logic, and Repositories handle database interactions (ORMs/ODMs).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Layered Architecture Breakdown:</b></p>
<ul>
  <li><b>Controller Layer:</b> Reads params/body, delegates to Service, returns HTTP status (200, 201, 400).</li>
  <li><b>Service Layer:</b> Pure business logic, authorization validation, email triggers, third-party API integration.</li>
  <li><b>Repository/DAO Layer:</b> Database queries (Prisma, Mongoose, TypeORM, Knex).</li>
</ul>

```js
// UserService.js (Service Layer)
class UserService {
  constructor(userRepository) {
    this.userRepository = userRepository;
  }

  async registerUser(userData) {
    const existing = await this.userRepository.findByEmail(userData.email);
    if (existing) throw new Error('Email already registered');
    
    userData.password = await hashPassword(userData.password);
    return await this.userRepository.create(userData);
  }
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Concurrency, Clustering & Multithreading -->
<h3 id="q16">16. What is the Cluster module in Node.js and how does IPC work?</h3>
<p><strong>Short Answer:</strong> The `cluster` module enables spawning multiple worker processes (typically one per CPU core) that share the same server port. Worker processes run in separate V8 instances and communicate with the primary process via Inter-Process Communication (IPC) IPC messaging.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const cluster = require('cluster');
const http = require('http');
const os = require('os');

if (cluster.isPrimary) {
  const numCPUs = os.cpus().length;
  console.log(`Primary ${process.pid} spawning ${numCPUs} workers...`);

  for (let i = 0; i < numCPUs; i++) {
    cluster.fork(); // Spawn worker process
  }

  cluster.on('exit', (worker, code, signal) => {
    console.log(`Worker ${worker.process.pid} died. Respawning...`);
    cluster.fork();
  });
} else {
  // Workers share the TCP socket!
  http.createServer((req, res) => {
    res.writeHead(200);
    res.end(`Handled by worker PID: ${process.pid}
`);
  }).listen(8000);
}
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q17">17. What are Worker Threads (worker_threads) and when should you use them?</h3>
<p><strong>Short Answer:</strong> The `worker_threads` module allows running CPU-intensive JavaScript execution in parallel inside the same process using multiple threads. Unlike Cluster processes, Worker Threads can efficiently share memory via `ArrayBuffer` or `SharedArrayBuffer` without serialization overhead.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
// main.js
const { Worker } = require('worker_threads');

function runCpuTask(data) {
  return new Promise((resolve, reject) => {
    const worker = new Worker('./worker.js', { workerData: data });
    worker.on('message', resolve);
    worker.on('error', reject);
    worker.on('exit', (code) => {
      if (code !== 0) reject(new Error(`Worker stopped with code ${code}`));
    });
  });
}

// worker.js
const { parentPort, workerData } = require('worker_threads');

// Perform heavy computation (e.g., Fibonacci or image processing)
let result = 0;
for (let i = 0; i < workerData.iterations; i++) {
  result += i;
}

parentPort.postMessage(result);
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q18">18. What is the child_process module (spawn, exec, execFile, fork) and their differences?</h3>
<p><strong>Short Answer:</strong> `child_process` spawns OS subprocesses. `spawn` streams data from long-running commands, `exec` buffers shell outputs, `execFile` executes binaries without spawning a shell, and `fork` spawns a new Node.js process with a built-in IPC channel.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<table border="1" cellpadding="6">
  <thead>
    <tr>
      <th>Method</th>
      <th>Shell Spawns?</th>
      <th>Data Transport</th>
      <th>Best Used For</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><b>`spawn()`</b></td>
      <td>No</td>
      <td>Stream (Chunks)</td>
      <td>Large outputs, CLI binaries (ffmpeg)</td>
    </tr>
    <tr>
      <td><b>`exec()`</b></td>
      <td>Yes</td>
      <td>Buffered String</td>
      <td>Small shell scripts (`ls -la`)</td>
    </tr>
    <tr>
      <td><b>`execFile()`</b></td>
      <td>No</td>
      <td>Buffered String</td>
      <td>Executing executable binaries safely</td>
    </tr>
    <tr>
      <td><b>`fork()`</b></td>
      <td>No</td>
      <td>IPC Channel (`send`/`on`)</td>
      <td>Node.js to Node.js subprocess tasks</td>
    </tr>
  </tbody>
</table>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q19">19. How do PM2 and process managers handle zero-downtime reloads and cluster mode?</h3>
<p><strong>Short Answer:</strong> PM2 manages Node.js process lifecycles, monitoring CPU/RAM, restarting crashed processes automatically, and performing zero-downtime reloads (`pm2 reload`) by restarting cluster instances one by one while active instances handle traffic.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```bash
# Start Node app in cluster mode using all CPU cores
pm2 start server.js -i max --name "node-api"

# Perform zero-downtime rolling reload
pm2 reload node-api

# Monitor logs and system performance
pm2 monit
```

<p><b>Ecosystem File (`ecosystem.config.js`):</b></p>

```js
module.exports = {
  apps: [{
    name: 'api-server',
    script: './server.js',
    instances: 'max',
    exec_mode: 'cluster',
    max_memory_restart: '500M',
    env: { NODE_ENV: 'production' }
  }]
};
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Security, Performance & Optimization -->
<h3 id="q20">20. How do you prevent Denial of Service (DoS) and Event Loop blocking in Node.js?</h3>
<p><strong>Short Answer:</strong> Prevent DoS by avoiding blocking synchronous methods (`readFileSync`, `JSON.parse` on huge inputs), limiting request body sizes, applying rate limiting, setting HTTP timeouts, avoiding ReDoS (Regular Expression DoS), and offloading heavy tasks.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Key Prevention Techniques:</b></p>
<ul>
  <li><b>Avoid ReDoS:</b> Dangerous nested quantifiers in regex like `(a+)+$` cause exponential CPU backtracking. Use `safe-regex` tools.</li>
  <li><b>Set Server Timeouts:</b> Set `server.headersTimeout` and `server.requestTimeout` to prevent Slowloris attacks.</li>
  <li><b>Enforce Rate Limits:</b> Use `express-rate-limit` to restrict IPs exceeding quota.</li>
  <li><b>Never Use Sync FS Methods in Servers:</b> Avoid `fs.readFileSync` inside request routes.</li>
</ul>
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q21">21. What are essential security best practices in Node.js (Helmet, Rate Limiting, CORS)?</h3>
<p><strong>Short Answer:</strong> Secure Node.js apps by setting HTTP security headers with `helmet()`, enabling strict CORS origins, enforcing rate limits, sanitizing inputs against NoSQL/SQL Injection, hiding server technologies (`x-powered-by`), and running process as non-root users.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const express = require('express');
const helmet = require('helmet');
const cors = require('cors');
const rateLimit = require('express-rate-limit');

const app = express();

// 1. HTTP Security Headers
app.use(helmet());

// 2. Strict CORS Configuration
app.use(cors({
  origin: ['https://app.mydomain.com'],
  methods: ['GET', 'POST', 'PUT', 'DELETE'],
  credentials: true
}));

// 3. Rate Limiter (100 requests per 15 minutes)
app.use(rateLimit({
  windowMs: 15 * 60 * 1000,
  max: 100,
  message: 'Too many requests from this IP'
}));
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q22">22. How do you handle authentication using JWTs, Refresh Tokens, and HTTP-only cookies?</h3>
<p><strong>Short Answer:</strong> Store short-lived Access Tokens in memory or response payload, and store long-lived Refresh Tokens in `httpOnly`, `Secure`, `SameSite` cookies to mitigate XSS and CSRF attacks.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
// Login Route issuing Cookie & Token
app.post('/api/login', async (req, res) => {
  const user = await authenticateUser(req.body);

  const accessToken = jwt.sign({ userId: user.id }, process.env.ACCESS_SECRET, { expiresIn: '15m' });
  const refreshToken = jwt.sign({ userId: user.id }, process.env.REFRESH_SECRET, { expiresIn: '7d' });

  // Store Refresh Token in HTTP-Only Cookie
  res.cookie('refreshToken', refreshToken, {
    httpOnly: true,
    secure: process.env.NODE_ENV === 'production',
    sameSite: 'strict',
    maxAge: 7 * 24 * 60 * 60 * 1000
  });

  res.json({ accessToken });
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q23">23. How do memory leaks occur in Node.js and how do you debug them?</h3>
<p><strong>Short Answer:</strong> Memory leaks occur when objects remain referenced in the V8 heap when no longer needed. Common causes include uncleaned EventListeners, growing global variables/caches, and unclosed timers. Debug using `--inspect` and Chrome DevTools Heap Snapshots.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Common Causes of Memory Leaks:</b></p>
<ul>
  <li><b>Global Caches:</b> Storing objects in global Arrays/Objects without eviction policies (use `LRU-Cache` instead).</li>
  <li><b>Forgotten Event Listeners:</b> `emitter.on()` without corresponding `removeListener()`.</li>
  <li><b>Uncleared `setInterval()`:</b> Timers keeping enclosing scope variables referenced.</li>
</ul>

```bash
# Debugging Node.js Memory Heap
node --inspect server.js
# Open chrome://inspect in browser to capture and compare Heap Snapshots
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q24">24. How do you optimize database connection pools (Postgres, MongoDB, Redis)?</h3>
<p><strong>Short Answer:</strong> Reuse a single shared database connection pool instance across requests instead of opening new connections per HTTP request. Configure `max` connections, `idleTimeoutMillis`, and keep-alive parameters according to database resource limits.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
// PostgreSQL Pool Optimization (pg)
const { Pool } = require('pg');

const pool = new Pool({
  host: process.env.DB_HOST,
  max: 20, // Maximum pool size
  idleTimeoutMillis: 30000,
  connectionTimeoutMillis: 2000,
});

module.exports = pool; // Export single pool instance
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<!-- Microservices, Real-Time & Deployment -->
<h3 id="q25">25. How do WebSockets and Server-Sent Events (SSE) work for real-time applications?</h3>
<p><strong>Short Answer:</strong> WebSockets (`ws`, `socket.io`) provide bi-directional, full-duplex persistent connections over TCP. Server-Sent Events (SSE) provide lightweight, mono-directional HTTP streaming from server to client.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

<p><b>Server-Sent Events (SSE) Implementation:</b></p>

```js
app.get('/api/events', (req, res) => {
  res.writeHead(200, {
    'Content-Type': 'text/event-stream',
    'Cache-Control': 'no-cache',
    'Connection': 'keep-alive'
  });

  const intervalId = setInterval(() => {
    res.write(`data: ${JSON.stringify({ time: new Date() })}

`);
  }, 1000);

  req.on('close', () => clearInterval(intervalId));
});
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q26">26. How do Message Queues (BullMQ, RabbitMQ) handle background job processing?</h3>
<p><strong>Short Answer:</strong> Offload asynchronous, heavy tasks (email delivery, video encoding) from the HTTP request thread by publishing jobs to Redis/RabbitMQ queues. Separate Worker processes consume and execute jobs asynchronously with retries.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
// Queue Producer (Express Server)
const { Queue } = require('bullmq');
const emailQueue = new Queue('emailQueue', { connection: redisConfig });

app.post('/api/register', async (req, res) => {
  const user = await createUser(req.body);
  // Add job to queue, respond instantly to user
  await emailQueue.add('sendWelcomeEmail', { email: user.email });
  res.status(201).json({ message: 'User created' });
});

// Queue Consumer (Background Worker)
const { Worker } = require('bullmq');
const worker = new Worker('emailQueue', async (job) => {
  console.log(`Processing email for ${job.data.email}`);
  await sendMail(job.data.email);
}, { connection: redisConfig });
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q27">27. What is Graceful Shutdown in Node.js (SIGINT, SIGTERM) and why is it essential?</h3>
<p><strong>Short Answer:</strong> Graceful shutdown ensures that when a server receives a termination signal (`SIGTERM`, `SIGINT`), it stops accepting new connections, finishes processing existing active requests, closes database pools, and terminates cleanly without corrupting data.</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const server = app.listen(3000);

function gracefulShutdown(signal) {
  console.log(`Received ${signal}. Starting graceful shutdown...`);

  // Stop accepting new HTTP requests
  server.close(async () => {
    console.log('HTTP server closed.');
    
    try {
      // Close Database Pools & Redis Clients
      await db.pool.end();
      console.log('Database connections closed.');
      process.exit(0);
    } catch (err) {
      console.error('Error during shutdown:', err);
      process.exit(1);
    }
  });

  // Force shutdown after 10 seconds if connections hang
  setTimeout(() => {
    console.error('Forced shutdown due to timeout');
    process.exit(1);
  }, 10000);
}

process.on('SIGTERM', () => gracefulShutdown('SIGTERM'));
process.on('SIGINT', () => gracefulShutdown('SIGINT'));
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />

<h3 id="q28">28. How do environment configuration and structured logging (Winston/Pino) work in production?</h3>
<p><strong>Short Answer:</strong> Validate environment variables at application startup using schemas (e.g. `zod` or `joi`). Use structured JSON loggers (`pino` or `winston`) instead of `console.log` for high-throughput, machine-readable logs compatible with log aggregators (Datadog, ELK).</p>
<details>
<summary><b>Detailed Answer</b></summary>
<br/>

```js
const pino = require('pino');
const logger = pino({ level: process.env.LOG_LEVEL || 'info' });

// Structured JSON Logging (Fast & Non-blocking)
logger.info({ userId: 123, action: 'LOGIN_SUCCESS' }, 'User logged in');
logger.error({ err: new Error('DB Connection Failed') }, 'Database error');
```
</details>
<p><a href="#top">⬆ Go to top</a></p>
<hr />
