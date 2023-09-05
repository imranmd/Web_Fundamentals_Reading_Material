# Tutorial: Step by step tutorial for React Setup and Creating a Hello World App

Welcome to the tutorial on setting up a development environment and creating a simple "Hello World" application in ReactJS. This tutorial will guide you through the process of installing the necessary tools, creating a new React application, and displaying a basic message on the screen.

![](../Assets/React/setup_reactjs_logo.jpg)
## Step 1: Install Node.js and npm

1. Visit the [Node.js website](https://nodejs.org/) and download the latest LTS (Long-Term Support) version for your operating system.
2. Follow the installation instructions to install Node.js and npm (Node Package Manager).

## Step 2: Install Create React App

1. Open a terminal or command prompt.
2. Run the following command to install Create React App globally:
   ```
   npm install -g create-react-app
   ```

## Step 3: Create a New React Application

1. In the terminal, navigate to the directory where you want to create your React application.
2. Run the following command to create a new React application named "hello-world":
   ```
   npx create-react-app hello-world
   ```

## Step 4: Explore the Project Structure

1. Once the project is created, navigate to the "hello-world" directory:
   ```
   cd hello-world
   ```
2. Open the project in your preferred code editor.

## Step 5: Modify the App Component

1. Open the "src" directory and locate the "App.js" file.
2. Modify the contents of the file to display a "Hello World" message:
   ```jsx
   import React from 'react';

   function App() {
     return (
       <div>
         <h1>Hello World!</h1>
       </div>
     );
   }

   export default App;
   ```

## Step 6: Run the Application

1. In the terminal, make sure you are still inside the "hello-world" directory.
2. Run the following command to start the development server:
   ```
   npm start
   ```
3. Open your web browser and navigate to `http://localhost:3000`. You should see the "Hello World" message displayed on the screen.

## Summary:

- Install Node.js and npm to set up the development environment.
- Install Create React App globally to quickly scaffold React applications.
- Create a new React application using Create React App.
- Explore the project structure and familiarize yourself with the files and directories.
- Modify the `App.js` file to customize the content of your React component.
- Run the application using the development server and view it in your web browser.

Congratulations! You've successfully set up a React development environment, created a simple "Hello World" application, and displayed it in your browser. This basic example serves as a starting point for building more complex React applications in the future.

Happy coding!