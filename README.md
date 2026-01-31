# Node.js Interview Questions and Answers

## 1. What is Node.js?
Node.js is a runtime environment built on Chrome’s V8 JavaScript engine that allows you to run JavaScript code outside the browser, often used to build scalable network applications.

## 2. What are the advantages of using Node.js?
- Asynchronous and event-driven  
- Single-threaded but handles multiple requests  
- High performance due to V8 engine  
- Large ecosystem with npm packages

## 3. What is the difference between Node.js and JavaScript?
- JavaScript: Programming language that runs in browsers  
- Node.js: Runtime environment for executing JavaScript outside browsers

## 4. What are callbacks in Node.js?
Callbacks are functions passed as arguments to other functions, executed after an asynchronous operation is completed.

## 5. What is Event Loop in Node.js?
The event loop is a mechanism that allows Node.js to perform non-blocking I/O operations by offloading operations to the system kernel whenever possible.

## 6. What is the difference between setImmediate() and process.nextTick()?
- `process.nextTick()`: Executes immediately after the current operation completes.  
- `setImmediate()`: Executes in the next iteration of the event loop.

## 7. What is a Stream in Node.js?
Streams are objects that enable reading/writing data piece by piece (chunks) instead of all at once. Types: Readable, Writable, Duplex, Transform.

## 8. What are Node.js modules?
Modules are reusable blocks of code that can be imported/exported. Node.js supports CommonJS (`require`) and ES Modules (`import`).

## 9. What is middleware in Node.js?
Middleware is a function that has access to request and response objects and can modify them before passing control to the next middleware.

## 10. What are global objects in Node.js?
Some global objects: `__dirname`, `__filename`, `process`, `Buffer`, `console`.

## 11. What is the difference between fs.readFile and fs.createReadStream?
- `fs.readFile`: Reads the whole file into memory before processing.  
- `fs.createReadStream`: Reads data in chunks (streaming).

## 12. How does Node.js handle child processes?
Using the `child_process` module (`exec`, `spawn`, `fork`) to run external commands or scripts.

## 13. What is clustering in Node.js?
Clustering allows Node.js to utilize multiple CPU cores by creating worker processes.

## 14. Explain package.json file.
`package.json` contains project metadata (name, version, dependencies, scripts) and is essential for managing a Node.js project.

## 15. What is the difference between npm and npx?
- `npm`: Package manager for installing and managing dependencies.  
- `npx`: Tool to execute binaries from npm packages without installing them globally.


# Express.js Interview Questions and Answers

## 1. What is Express.js?
Express.js is a fast, unopinionated, and minimalist web framework for Node.js, used for building APIs and web applications.

## 2. What are the features of Express.js?
- Middleware support  
- Routing system  
- Template engines  
- HTTP helpers  
- Easy integration with databases

## 3. What is middleware in Express?
Middleware functions are functions that have access to req, res, and next. They can execute code, modify requests/responses, and end or continue the request-response cycle.

## 4. How does routing work in Express.js?
Routing refers to how an application’s endpoints respond to client requests using methods like `app.get()`, `app.post()`, etc.

## 5. What is the difference between app.use() and app.get()?
- `app.use()`: Mounts middleware at the specified path.  
- `app.get()`: Handles GET requests for a specific route.

## 6. How do you handle errors in Express.js?
By creating error-handling middleware with four arguments `(err, req, res, next)`.

## 7. What is the difference between res.send(), res.json(), and res.end()?
- `res.send()`: Sends response (string, object, buffer).  
- `res.json()`: Sends JSON response.  
- `res.end()`: Ends response without any data.

## 8. How do you implement static files in Express?
Using `app.use(express.static('public'))` to serve static files like CSS, JS, and images.

## 9. What is the difference between app.locals and res.locals?
- `app.locals`: Variables available throughout the app.  
- `res.locals`: Variables scoped to a single response.

## 10. How to enable CORS in Express?
Using `cors` middleware:  
```js
const cors = require('cors');
app.use(cors());
```

## 11. What are query parameters and route parameters in Express?
- Query parameters: `/users?id=1` → `req.query.id`  
- Route parameters: `/users/:id` → `req.params.id`

## 12. How do you structure an Express.js project?
Common structure:  
- `routes/` → route definitions  
- `controllers/` → request handling logic  
- `models/` → database models  
- `middlewares/` → custom middleware  
- `server.js` → entry point

## 13. What is body-parser in Express?
Body-parser is middleware that parses incoming request bodies (JSON, URL-encoded) before handlers process them.

## 14. How do you handle 404 errors in Express?
By adding a middleware at the end:  
```js
app.use((req, res) => {
  res.status(404).send('Page Not Found');
});
```

## 15. What is the difference between Express.js and Node.js?
- Node.js: Runtime environment for executing JavaScript.  
- Express.js: Web framework built on Node.js to simplify server development.
