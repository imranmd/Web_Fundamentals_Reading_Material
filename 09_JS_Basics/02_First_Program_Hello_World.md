# Writing Your First JavaScript Program - "Hello World"

In this tutorial, we will guide you through the process of writing your first JavaScript program that prints "Hello, World!" to the console.

## Prerequisites

To get started with writing JavaScript code, you need a web browser and a basic text editor. Most modern web browsers come with built-in developer tools that include a JavaScript console where you can run your code and see the output.

## Step 1: Setting Up the HTML File

1. Open your favorite text editor (e.g., Notepad, VSCode, Sublime Text).
2. Create a new file and save it with a `.html` extension (e.g., `index.html`).
3. Add the basic structure of an HTML file:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First JavaScript Program</title>
</head>
<body>
    <!-- Your JavaScript code will go here -->
</body>
</html>
```

## Step 2: Adding JavaScript Code

1. Inside the `<body>` element, add a `<script>` tag to include your JavaScript code:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First JavaScript Program</title>
</head>
<body>
    <script>
        // Your JavaScript code will go here
    </script>
</body>
</html>
```

2. Inside the `<script>` tag, write the following JavaScript code to display "Hello, World!" in the console:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First JavaScript Program</title>
</head>
<body>
    <script>
        // Step 2: Write your JavaScript code here
        console.log("Hello, World!");
    </script>
</body>
</html>
```

## Step 3: Running the Program

1. Save the `index.html` file.
2. Open the saved file in your web browser (double-click the file or drag it into the browser).

## Step 4: Viewing the Output

1. Right-click anywhere on the page.
2. Select "Inspect" or "Inspect Element" from the context menu to open the developer tools.
3. In the developer tools, navigate to the "Console" tab.
4. You should see the output "Hello, World!" displayed in the console.

## Summary

Congratulations! You have successfully written and executed your first JavaScript program that prints "Hello, World!" to the console. This simple example introduces you to the basics of JavaScript and how to run code in the browser using a script tag. From here, you can explore more JavaScript concepts and gradually build more complex applications. Keep practicing and experimenting to become proficient in JavaScript programming. Happy coding!

# Writing Your First JavaScript Program - "Hello World"

In this tutorial, we will guide you through writing and running your first JavaScript program that prints "Hello World" to the console. We will use Visual Studio Code (VSCode) to create and execute the JavaScript file. Let's get started!

## Prerequisites

Before we begin, make sure you have the following installed on your computer:

1. [Visual Studio Code (VSCode)](https://code.visualstudio.com/download)
2. [Node.js](https://nodejs.org/) (Includes npm - Node Package Manager)

## Step 1: Set Up the Project

1. Open Visual Studio Code (VSCode).

2. Create a new folder for your project. Right-click anywhere in the Explorer panel on the left side of VSCode, select "New Folder," and name it something like "HelloWorldJS."

3. Inside the newly created folder, create a new file and name it "app.js". This will be our JavaScript file where we'll write our "Hello World" program.

## Step 2: Write the "Hello World" Program

Now, let's write the JavaScript code to print "Hello World" to the console.

1. Open the "app.js" file in VSCode.

2. Add the following code:

```javascript
// This is a simple JavaScript program that prints "Hello World" to the console.
console.log("Hello World");
```

## Step 3: Run the Program

1. Save the "app.js" file by pressing `Ctrl + S` (Windows/Linux) or `Cmd + S` (Mac).

2. Open the integrated terminal in VSCode by clicking on "View" in the menu and selecting "Terminal" or by using the keyboard shortcut `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac).

3. In the terminal, make sure you are inside the "HelloWorldJS" folder. You can change directories using the `cd` command (e.g., `cd path/to/HelloWorldJS`).

4. Once you are inside the correct folder, type the following command to run the JavaScript program:

```bash
node app.js
```

5. Press the `Enter` key, and you should see the output "Hello World" in the terminal.

Congratulations! You've successfully written and executed your first JavaScript program that prints "Hello World" to the console.

## Summary

In this tutorial, you learned how to set up a simple JavaScript project using Visual Studio Code, write a basic "Hello World" program in JavaScript, and execute it using Node.js in the integrated terminal. This is the first step in your journey to becoming a JavaScript developer. From here, you can explore more complex JavaScript concepts and build exciting web applications. Happy coding!