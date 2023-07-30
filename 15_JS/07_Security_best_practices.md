# Security Best Practices in JavaScript: Do's and Don'ts

Ensuring the security of your JavaScript code is of utmost importance to protect your users and applications from various vulnerabilities and attacks. In this tutorial, we will explore five security best practices in JavaScript that you should follow to build secure and robust applications. Each practice will be accompanied by example code snippets with comments and explained using simple language.

## Best Practice 1: Input Validation and Sanitization

Always validate and sanitize user inputs to prevent malicious data from entering your application. Input validation checks if the data adheres to the expected format, while sanitization removes or escapes potentially harmful characters.

### Example: Input Validation

```javascript
// Bad - lack of input validation
function getUsername() {
  return document.getElementById("usernameInput").value;
}
```

```javascript
// Good - input validation using regular expression
function isValidUsername(username) {
  const regex = /^[a-zA-Z0-9_-]{3,16}$/;
  return regex.test(username);
}

function getUsername() {
  const username = document.getElementById("usernameInput").value;
  if (isValidUsername(username)) {
    return username;
  } else {
    // Handle invalid username
  }
}
```

In this example, we use a regular expression to validate the username input, ensuring it contains only alphanumeric characters, hyphens, and underscores and is between 3 to 16 characters long.

### Example: Input Sanitization

```javascript
// Bad - lack of input sanitization
function displayMessage(message) {
  document.getElementById("messageBox").innerHTML = message;
}
```

```javascript
// Good - input sanitization using DOMPurify library
function displayMessage(message) {
  const sanitizedMessage = DOMPurify.sanitize(message);
  document.getElementById("messageBox").innerHTML = sanitizedMessage;
}
```

In this example, we use the DOMPurify library to sanitize the message before displaying it in the message box, preventing potential XSS (Cross-Site Scripting) attacks.

## Best Practice 2: Avoid `eval()` and `Function()` Constructor

Avoid using `eval()` and the `Function()` constructor with user-supplied data, as they can execute arbitrary code and lead to code injection vulnerabilities.

### Example: Avoiding `eval()`

```javascript
// Bad - using eval() with user-supplied data
function evaluateExpression(expression) {
  return eval(expression);
}

const userExpression = prompt("Enter an expression:");
const result = evaluateExpression(userExpression);
```

```javascript
// Good - using a safer alternative
function evaluateExpression(expression) {
  return Function('"use strict";return (' + expression + ')')();
}

const userExpression = prompt("Enter an expression:");
const result = evaluateExpression(userExpression);
```

In the good example, we use the `Function()` constructor with strict mode to evaluate the user expression safely.

## Best Practice 3: Avoid Storing Sensitive Data in JavaScript

Avoid storing sensitive information like passwords, tokens, or API keys directly in your JavaScript code. Instead, use server-side authentication and authorization mechanisms.

```javascript
// Bad - storing sensitive data in JavaScript
const apiKey = "YOUR_API_KEY";
```

```javascript
// Good - using server-side authentication and authorization
// Example: Retrieve API key from the server using a secure request
fetch("/api/getApiKey")
  .then((response) => response.text())
  .then((apiKey) => {
    // Use the retrieved API key securely
  })
  .catch((error) => {
    // Handle error
  });
```

By retrieving sensitive data from the server through secure requests, you can protect it from being exposed in your JavaScript code.

## Best Practice 4: Enable CORS (Cross-Origin Resource Sharing)

Configure Cross-Origin Resource Sharing (CORS) properly to restrict unauthorized access to your server's resources from other domains.

```javascript
// Bad - allowing all origins (unsafe)
app.use(function(req, res, next) {
  res.header("Access-Control-Allow-Origin", "*");
  res.header("Access-Control-Allow-Methods", "GET, POST, PUT, DELETE");
  res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
  next();
});
```

```javascript
// Good - restrict allowed origins
const allowedOrigins = ["https://example.com", "https://api.example.com"];

app.use(function(req, res, next) {
  const origin = req.headers.origin;
  if (allowedOrigins.includes(origin)) {
    res.header("Access-Control-Allow-Origin", origin);
    res.header("Access-Control-Allow-Methods", "GET, POST, PUT, DELETE");
    res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
  }
  next();
});
```

By restricting allowed origins using the `Access-Control-Allow-Origin` header, you can prevent unauthorized access to your server's resources.

## Best Practice 5: Protect Against Cross-Site Scripting (XSS) Attacks

Prevent Cross-Site Scripting (XSS) attacks by escaping and sanitizing user-generated content before rendering it in the browser.

```javascript
// Bad - displaying user-generated content without sanitization
function displayUserContent(content) {
  document.getElementById("userContent").innerHTML = content;
}
```

```javascript
// Good - sanitizing user-generated content using DOMPurify library
function displayUserContent(content) {
  const sanitizedContent = DOMPurify.sanitize(content);
  document.getElementById("userContent").innerHTML = sanitizedContent;
}
```

By using the DOMPurify library to sanitize user-generated content, you can prevent malicious scripts from being executed.

## Summary

Security is a critical aspect of JavaScript development, and following these five best practices will help you build more secure and trustworthy applications. Always validate and sanitize user inputs, avoid potentially dangerous functions like `eval()`, and use secure authentication and authorization mechanisms. Additionally, properly configure CORS and protect against XSS attacks to safeguard your users and data. By prioritizing security in your JavaScript code, you can ensure a safer experience for your users and protect your application from potential vulnerabilities and threats. Happy coding!