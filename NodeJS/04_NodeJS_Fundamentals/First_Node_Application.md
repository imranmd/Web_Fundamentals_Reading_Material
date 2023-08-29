# Your First Node.js Application: Step-by-Step Guide

Creating your first Node.js application is an exciting step in your journey as a developer. In this comprehensive tutorial, we'll walk you through the process of building and running your first Node.js application. From installation to writing code, this guide covers all the essential steps to get you started on the right foot.

## Your First Node.js Application: Step-by-Step Guide

### Step 1: Install Node.js

First, you need to install Node.js on your machine. Visit the official Node.js website (https://nodejs.org/) and download the latest stable version suitable for your operating system. Follow the installation instructions provided.

### Step 2: Create a Project Folder

Create a new folder for your Node.js application. Open your terminal or command prompt and navigate to the directory where you want to create the folder. Then, use the following command to create the folder:

```bash
mkdir first-node-app
```

### Step 3: Navigate to the Project Folder

Navigate into the newly created folder using the `cd` command:

```bash
cd first-node-app
```

### Step 4: Initialize a Node.js Application

Initialize a Node.js application by creating a `package.json` file. This file contains metadata about your application and its dependencies. Run the following command and follow the prompts:

```bash
npm init
```

### Step 5: Create Your First JavaScript File

Create a new file named `app.js` within your project folder. This file will contain your Node.js application code.

### Step 6: Write Your First Node.js Code

Open the `app.js` file in a text editor of your choice and add the following code:

```javascript
// Load the built-in 'http' module
const http = require('http');

// Create a basic HTTP server
const server = http.createServer((req, res) => {
    res.writeHead(200, {'Content-Type': 'text/plain'});
    res.end('Hello, Node.js!');
});

// Listen on port 3000
server.listen(3000, () => {
    console.log('Server is running on http://localhost:3000');
});
```

### Step 7: Run Your Node.js Application

Back in your terminal, ensure you're in the `first-node-app` directory and run the following command to start your Node.js application:

```bash
node app.js
```

### Step 8: Access Your Application

Open your web browser and navigate to http://localhost:3000. You should see the message "Hello, Node.js!" displayed in your browser.

## Conclusion

Congratulations! You've successfully built and run your first Node.js application. In this step-by-step guide, you've learned how to install Node.js, create a project folder, write a simple Node.js application, and run it using the Node.js runtime. This is just the beginning of your Node.js journey, and you're now equipped with the foundational knowledge to explore more advanced topics and build more sophisticated applications using the Node.js platform.