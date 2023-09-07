# Getting Started with Jest: Setup and Writing Your First Test Case

Jest is a popular JavaScript testing framework used for unit testing, integration testing, and even snapshot testing. In this tutorial, we'll walk you through setting up Jest and writing your first test case in a Node.js environment.

## Prerequisites

Before you get started, make sure you have the following prerequisites:

- Node.js installed on your machine.
- A code editor like Visual Studio Code or any other of your choice.

## Step 1: Create a New Node.js Project

Let's start by creating a new Node.js project. Open your terminal and follow these commands:

```bash
# Create a new directory for your project
mkdir jest-tutorial

# Navigate to your project folder
cd jest-tutorial

# Initialize a new Node.js project
npm init -y
```

## Step 2: Install Jest

Now, we'll install Jest as a development dependency in your project:

```bash
npm install jest --save-dev
```

## Step 3: Create a Simple JavaScript File

Let's create a simple JavaScript file that we want to test. For this example, we'll create a file named `math.js` with a simple function:

```javascript
// math.js

function add(a, b) {
  return a + b;
}

module.exports = { add };
```

## Step 4: Writing Your First Test

Now, let's write your first test case for the `add` function. Create a new file named `math.test.js` in the same directory as `math.js`. This naming convention is essential for Jest to automatically discover your test files.

```javascript
// math.test.js

const { add } = require('./math');

test('addition of 1 + 2 should equal 3', () => {
  expect(add(1, 2)).toBe(3);
});
```

In this test case, we:

- Import the `add` function from `math.js`.
- Use the `test` function to define a test case. The first argument is a descriptive string, and the second argument is a function containing the test code.
- Inside the test, we use the `expect` function to define our expectation and the `toBe` matcher to specify the expected result.

## Step 5: Running Your Tests

To run your tests, execute the following command in your terminal:

```bash
npx jest
```

Jest will automatically discover and run all test files with the `.test.js` or `.spec.js` extension in your project directory.

You should see output indicating that your test passed:

```
PASS  ./math.test.js
  ✓ addition of 1 + 2 should equal 3 (2 ms)

Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        0.743 s, estimated 1 s
```

Congratulations! You've successfully set up Jest and written your first test case.

## Summary

Jest is a powerful and easy-to-use testing framework for JavaScript. In this tutorial, you learned how to set up Jest in a Node.js project, write your first test case, and run your tests. As you continue developing your applications, Jest will help you ensure the correctness and reliability of your code through automated testing.