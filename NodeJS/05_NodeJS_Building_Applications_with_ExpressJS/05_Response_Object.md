# Express.js Response Object: A Comprehensive Guide

In Express.js, the `response` object, often referred to as `res`, is a crucial part of handling HTTP requests. It allows you to send responses back to clients, set response headers, and manage the HTTP status code. This comprehensive guide explains the Express.js `response` object, its various methods and properties, and how to use them effectively.

![Response in nodejs](../Assets/Request%20and%20Response.jpg)
## Accessing the Response Object

In an Express.js application, you can access the `response` object in route handlers and middleware functions by including it as a parameter in the function's callback. Here's an example:

```javascript
app.get('/example', (req, res) => {
  // Access the response object (res) here
  // ...
});
```

## Key Methods and Properties of the Response Object

### 1. `res.send()`

The `res.send()` method is used to send a response to the client. It can send various types of responses, including HTML, plain text, JSON, and more. Express automatically sets the appropriate content-type header based on the data you provide.

```javascript
app.get('/hello', (req, res) => {
  res.send('Hello, Express!');
});
```

### 2. `res.json()`

The `res.json()` method sends a JSON response to the client. It automatically sets the `Content-Type` header to `application/json`.

```javascript
app.get('/api/data', (req, res) => {
  const data = { message: 'This is JSON data' };
  res.json(data);
});
```

### 3. `res.status()`

The `res.status()` method sets the HTTP status code of the response. You can use it to send specific status codes, such as 200 (OK), 404 (Not Found), or 500 (Internal Server Error).

```javascript
app.get('/not-found', (req, res) => {
  res.status(404).send('Page not found');
});
```

### 4. `res.setHeader()`

The `res.setHeader()` method is used to set custom response headers. You can specify the header name and its value.

```javascript
app.get('/custom-header', (req, res) => {
  res.setHeader('X-Custom-Header', 'Hello, Custom Header');
  res.send('Custom header set');
});
```

### 5. `res.redirect()`

The `res.redirect()` method is used to redirect the client to a different URL. You can provide either a relative or absolute URL.

```javascript
app.get('/redirect', (req, res) => {
  res.redirect('/new-location');
});
```

### 6. `res.cookie()`

The `res.cookie()` method is used to set cookies in the response. It allows you to specify the cookie name, value, and optional options.

```javascript
app.get('/set-cookie', (req, res) => {
  res.cookie('user', 'john_doe', { maxAge: 3600000, httpOnly: true });
  res.send('Cookie set');
});
```

### 7. `res.clearCookie()`

The `res.clearCookie()` method is used to clear cookies set in the response. You need to provide the cookie name.

```javascript
app.get('/clear-cookie', (req, res) => {
  res.clearCookie('user');
  res.send('Cookie cleared');
});
```

These are some of the key methods and properties of the Express.js `response` object. By understanding and utilizing these methods, you can effectively send responses, set headers, and manage HTTP status codes in your Express.js applications.