# Building Your First Express.js Program: A Step-by-Step Guide

Creating your first Express.js program is an exciting milestone in your web development journey. In this beginner-friendly tutorial, you'll learn how to set up a basic Express.js application, define routes, and run your server.

## Embarking on Your Express.js Journey: Your First Program

Creating your first Express.js program introduces you to the fundamental concepts of building web applications.

## Step 1: Setting Up Your Project

Before diving into coding, make sure you have Node.js and npm installed on your system. You can download them from the official Node.js website: [Node.js Official Website](https://nodejs.org/).

## Step 2: Creating a Project Directory

Create a new directory for your Express.js project. Open your terminal and navigate to your desired location:

```sh
mkdir my-first-express-app
cd my-first-express-app
```

## Step 3: Initializing Your Project

In the terminal, initiate your Node.js project by running the following command:

```sh
npm init -y
```

This command creates a `package.json` file to manage your project's dependencies.

## Step 4: Installing Express.js

Install Express.js as a project dependency using npm:

```sh
npm install express
```

## Step 5: Building Your First Express Program

Create a file named `app.js` in your project directory and open it in your code editor. This is where you'll build your Express.js application.

```javascript
// app.js

// Import the Express.js module
const express = require('express');

// Create an instance of Express.js
const app = express();

// Define a route for the root URL
app.get('/', (req, res) => {
    res.send('Hello, Express!');
});

// Start the server
const port = process.env.PORT || 3000;
app.listen(port, () => {
    console.log(`Server started on port ${port}`);
});
```

## Step 6: Running Your Server

In your terminal, navigate to your project directory and run the server using the following command:

```sh
node app.js
```

Your Express.js server is now running. Open your web browser and visit `http://localhost:3000` to see the "Hello, Express!" message.

## Conclusion

Congratulations! You've successfully created your first Express.js program. By setting up your project, installing Express.js, defining routes, and running your server, you've taken the first step toward building web applications using this powerful framework. As you continue your journey, explore more features of Express.js, such as route handling, middleware, and template engines, to create robust and dynamic web applications that cater to various user needs.