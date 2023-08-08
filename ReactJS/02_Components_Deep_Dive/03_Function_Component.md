# Tutorial: Getting Started with React JS Function Components

In this tutorial, you will learn how to create and use React JS function components. We'll start with the basics and gradually introduce more advanced concepts, all while keeping an exciting Avengers theme.

## Prerequisites

Before you begin, make sure you have the following installed on your computer:

1. Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).

## Step 1: Setting Up Your Development Environment

1. Open your terminal or command prompt.

2. Create a new directory for your React app:

   ```bash
   mkdir react-function-components
   cd react-function-components
   ```

3. Initialize a new Node.js project:

   ```bash
   npm init -y
   ```

## Step 2: Installing React and React DOM

1. Install React and React DOM packages:

   ```bash
   npm install react react-dom
   ```

## Step 3: Creating Your First Function Component

1. Create a new file named `AvengerCard.js` in your project directory.

2. Open `AvengerCard.js` and add the following code:

```jsx
import React from 'react';

// Function component: AvengerCard
function AvengerCard(props) {
  return (
    <div className="avenger-card">
      <h2>{props.name}</h2>
      <p>Alias: {props.alias}</p>
    </div>
  );
}

export default AvengerCard;
```

## Step 4: Using Your Function Component

1. Create a new file named `App.js` in the same directory.

2. Open `App.js` and add the following code:

```jsx
import React from 'react';
import AvengerCard from './AvengerCard';

function App() {
  return (
    <div>
      <h1>Avenger Squad</h1>
      <AvengerCard name="Iron Man" alias="Tony Stark" />
      <AvengerCard name="Spider-Man" alias="Peter Parker" />
      <AvengerCard name="Black Widow" alias="Natasha Romanoff" />
    </div>
  );
}

export default App;
```

## Step 5: Styling Your Components (Advanced)

1. Create a new file named `styles.css` in your project directory.

2. Open `styles.css` and add the following CSS to give your AvengerCards some style:

```css
.avenger-card {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  background-color: #f9f9f9;
}
```

3. Import the CSS file in your `App.js`:

```jsx
import './styles.css';
```

## Step 6: Running Your React App

1. Create an HTML file named `index.html` in your project directory.

2. Open `index.html` and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>React Function Components</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
```

3. Open your terminal/command prompt and navigate to your project directory.

4. Start your development server:

   ```bash
   npm start
   ```

5. Open your web browser and visit `http://localhost:3000`. You should see a list of Avengers displayed using your function component.

## Congratulations! You've Mastered React Function Components!

You've successfully learned how to create and use React function components to build a simple Avengers-themed app. You've covered both basic and advanced concepts, allowing you to create more interactive and visually appealing components. Now you're ready to take your React skills to the next level and build amazing applications!

Happy coding, Super Developer! 🚀🦸‍♂️🦸‍♀️