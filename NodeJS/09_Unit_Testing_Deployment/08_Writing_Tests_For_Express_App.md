# Creating a Simple Node.js Express Application with MVC Components

In this tutorial, we will guide you through the process of creating a simple Node.js Express application using the Model-View-Controller (MVC) architectural pattern. You will create a basic web application with one view, one controller, one middleware, and one model component.

## Prerequisites

Before we begin, ensure you have the following prerequisites installed on your machine:

- Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).
- npm (Node Package Manager): npm is included with Node.js. You can verify its installation by running `npm -v` in your terminal.

## Step 1: Create a New Node.js Project

Let's start by creating a new Node.js project folder and navigating to it:

```bash
# Create a new directory for your project
mkdir simple-express-mvc-app

# Navigate to your project folder
cd simple-express-mvc-app
```

## Step 2: Initialize Your Node.js Project

Initialize your Node.js project by running the following command and accepting the default options:

```bash
npm init -y
```

This will create a `package.json` file for your project.

## Step 3: Install Express

We'll use the Express framework to build our web application. Install it as a dependency:

```bash
npm install express --save
```

## Step 4: Create Directory Structure

To organize your project, create the following directory structure:

```plaintext
simple-express-mvc-app/
  |- views/
  |   |- index.ejs
  |- controllers/
  |   |- mainController.js
  |- middleware/
  |   |- customMiddleware.js
  |- models/
  |   |- userModel.js
  |- app.js
```

- The `views` directory will store your view templates.
- The `controllers` directory will hold your controller logic.
- The `middleware` directory will contain custom middleware functions.
- The `models` directory will store your data models.
- The `app.js` file is the main entry point for your Express application.

## Step 5: Create the `index.ejs` View

Create a basic view template in the `views` directory. Let's name it `index.ejs`:

```html
<!-- views/index.ejs -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Express MVC App</title>
</head>
<body>
    <h1>Welcome to Express MVC App</h1>
    <p><%= message %></p>
</body>
</html>
```

## Step 6: Create the `customMiddleware.js` Middleware

In the `middleware` directory, create a file named `customMiddleware.js`:

```javascript
// middleware/customMiddleware.js

function customMiddleware(req, res, next) {
  console.log('Custom middleware executed.');
  next();
}

module.exports = customMiddleware;
```

## Step 7: Create the `userModel.js` Model

In the `models` directory, create a file named `userModel.js`. For this example, we'll create a simple model that represents a user:

```javascript
// models/userModel.js

const users = [
  { id: 1, name: 'John Doe' },
  { id: 2, name: 'Jane Smith' },
];

function getUserById(id) {
  return users.find(user => user.id === id);
}

module.exports = { getUserById };
```

## Step 8: Create the `mainController.js` Controller

In the `controllers` directory, create a file named `mainController.js`. This controller will handle requests and render the view using the model and middleware:

```javascript
// controllers/mainController.js

const { getUserById } = require('../models/userModel');

function home(req, res) {
  const user = getUserById(1); // Get a user by ID from the model
  const message = `Hello, ${user.name}!`;
  res.render('index', { message });
}

module.exports = { home };
```

## Step 9: Configure Your Express Application

Now, let's configure your Express application in the `app.js` file:

```javascript
// app.js

const express = require('express');
const app = express();
const customMiddleware = require('./middleware/customMiddleware');
const { home } = require('./controllers/mainController');

// Set the view engine to EJS
app.set('view engine', 'ejs');
app.set('views', 'views');

// Middleware
app.use(customMiddleware);

// Routes
app.get('/', home);

// Start the Express server
const port = process.env.PORT || 3000;
app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
```

## Step 10: Install EJS

Since we're using the EJS template engine, install it as a dependency:

```bash
npm install ejs --save
```

## Step 11: Run Your Express Application

To start your Express application, run the following command:

```bash
node app.js
```

Your Express server will start, and you can access the application in your web browser at `http://localhost:3000`. You should see the welcome message from the `index.ejs` view.


Congratulations! You've successfully created a simple Node.js Express application following the MVC architectural pattern. You have one view, one controller, one middleware, and one model component working together. You can expand and customize this basic structure to build more complex web applications.

# Adding Unit Testing to Your Express MVC Application

In this tutorial, we will extend the previous Express MVC application by adding unit tests for each part of the application: views, controllers, middleware, and models. We'll use the Jest testing framework to create and run these tests.

## Prerequisites

Before we begin, make sure you have completed the previous tutorial to create the Express MVC application. You should also have the following prerequisites installed:

- Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).
- npm (Node Package Manager): npm is included with Node.js. You can verify its installation by running `npm -v` in your terminal.

## Step 1: Install Jest for Testing

We'll use Jest as our testing framework. Install it as a development dependency in your project:

```bash
npm install jest --save-dev
```

## Step 2: Configure Jest

To configure Jest for your project, create a `jest.config.js` file in your project's root directory with the following content:

```javascript
// jest.config.js

module.exports = {
  testEnvironment: 'node',
};
```

This configuration tells Jest to run tests in a Node.js environment.

## Step 3: Create a Test Directory

Create a new directory named `tests` in your project's root directory to store your test files:

```bash
mkdir tests
```

## Step 4: Writing Unit Tests for Views

Let's start by writing unit tests for your views. In the `tests` directory, create a new file named `views.test.js`. We'll use the `supertest` library to test the views:

```javascript
// tests/views.test.js

const request = require('supertest');
const app = require('../app');

test('GET / should render the index view', async () => {
  const response = await request(app).get('/');
  expect(response.status).toBe(200);
  expect(response.text).toContain('Welcome to Express MVC App');
});
```

In this test case, we use `supertest` to send a GET request to the root URL (`/`) and assert that the response contains the expected text.

## Step 5: Writing Unit Tests for Controllers

Create a new test file for your controllers. In the `tests` directory, create a file named `controllers.test.js`. We'll test the controller's behavior using Jest's mocking capabilities:

```javascript
// tests/controllers.test.js

const { home } = require('../controllers/mainController');
const { getUserById } = require('../models/userModel');

jest.mock('../models/userModel');

test('home controller should render the index view with a user', async () => {
  const user = { id: 1, name: 'John Doe' };
  getUserById.mockReturnValue(user);

  const res = {
    render: jest.fn(),
  };

  await home({}, res);

  expect(res.render).toHaveBeenCalledWith('index', {
    message: `Hello, ${user.name}!`,
  });
});
```

In this test case, we mock the `getUserById` function from the `userModel` module to control its behavior during testing. We then create a mock response object (`res`) and use Jest's `jest.fn()` to spy on the `res.render` function.

## Step 6: Writing Unit Tests for Middleware

Create a new test file for your middleware. In the `tests` directory, create a file named `middleware.test.js`. We'll test the middleware function by spying on its behavior:

```javascript
// tests/middleware.test.js

const customMiddleware = require('../middleware/customMiddleware');

test('customMiddleware should call next', () => {
  const req = {};
  const res = {};
  const next = jest.fn();

  customMiddleware(req, res, next);

  expect(next).toHaveBeenCalled();
});
```

In this test case, we create mock request (`req`), response (`res`), and `next` functions. We then call the `customMiddleware` function and assert that `next` was called.

## Step 7: Writing Unit Tests for Models

Create a new test file for your models. In the `tests` directory, create a file named `models.test.js`. We'll test the model's functionality by asserting its behavior:

```javascript
// tests/models.test.js

const { getUserById } = require('../models/userModel');

test('getUserById should return a user by ID', () => {
  const users = [
    { id: 1, name: 'John Doe' },
    { id: 2, name: 'Jane Smith' },
  ];

  const user = getUserById(1, users);
  expect(user).toEqual({ id: 1, name: 'John Doe' });
});
```

In this test case, we call the `getUserById` function with a user ID and an array of mock users. We then assert that the function returns the correct user.

## Step 8: Running Your Unit Tests

Execute your unit tests by running the following command from your project's root directory:

```bash
npx jest
```

Jest will discover and run all the test files in the `tests` directory and display the test results in the terminal.

## Code Coverage

Code coverage is a metric that indicates how much of your codebase is covered by your unit tests. It helps you identify areas of your code that are untested or under-tested. When you run your tests with Jest, it provides a code coverage report that shows which lines, functions, and branches of your code were executed during the tests.

Here's how to interpret the code coverage information when you run your tests with Jest for the Express MVC application we discussed:

1. **Line Coverage:** This metric tells you the percentage of lines of code that were executed during the tests. A high line coverage indicates that most of your code has been tested.

2. **Function Coverage:** It shows the percentage of functions in your code that were executed. It's essential to ensure that not only lines of code but also functions are covered by your tests.

3. **Branch Coverage:** Branch coverage indicates the percentage of code branches that were exercised during the tests. This is particularly important for conditional statements (e.g., if-else) where different code paths can be taken.

When you run your Jest tests with code coverage, you will see a summary in the terminal that looks like this:

```
-------------------|---------|----------|---------|---------|-------------------
File               | % Stmts | % Branch | % Funcs | % Lines | Uncovered Line #s
-------------------|---------|----------|---------|---------|-------------------
All files          |   X%    |    X%    |   X%    |   X%    |
 app.js            |   X%    |    X%    |   X%    |   X%    | X, X, X-X, X
 controllers/      |   X%    |    X%    |   X%    |   X%    |
  mainController.js|   X%    |    X%    |   X%    |   X%    | X, X-X, X-X, X-X
 middleware/       |   X%    |    X%    |   X%    |   X%    |
  customMiddleware.js|   X%    |    X%    |   X%    |   X%    | X, X
 models/           |   X%    |    X%    |   X%    |   X%    |
  userModel.js     |   X%    |    X%    |   X%    |   X%    | X-X-X, X-X-X
-------------------|---------|----------|---------|---------|-------------------
```

- `% Stmts` represents line coverage.
- `% Branch` represents branch coverage.
- `% Funcs` represents function coverage.
- `% Lines` represents coverage at the line level.
- `Uncovered Line #s` shows which lines of code were not executed during the tests.

In the summary, you'll see the coverage percentage for each file, directory, and the overall project. You can then review the "Uncovered Line #s" section to identify specific lines of code that were not covered by your tests.

To improve code coverage, you can write additional tests to cover the untested code paths. Aim for as close to 100% coverage as possible, as it helps ensure that your code is thoroughly tested and less prone to bugs. However, achieving 100% coverage may not always be practical or necessary in some cases.

## Summary

You have successfully added unit tests to your Express MVC application for each part of the application: views, controllers, middleware, and models. Testing is a crucial practice in software development that helps ensure the correctness and reliability of your code. You can now continue to expand your application and add more tests to maintain code quality and catch issues early in the development process.