# Tutorial: Mastering Conditional Rendering in React

In this tutorial, you'll delve into the art of conditional rendering in React, using examples inspired by the diverse world of superheroes. Conditional rendering allows you to show or hide components based on certain conditions. We'll start with the basics and gradually explore more advanced scenarios.

## Prerequisites

Before you begin, make sure you have the following installed on your computer:

1. Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).

## Step 1: Setting Up Your Development Environment

1. Open your terminal or command prompt.

2. Create a new directory for your React app:

   ```bash
   mkdir conditional-rendering-tutorial
   cd conditional-rendering-tutorial
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

## Step 3: Basic Conditional Rendering

In this step, you'll create a basic superhero-themed component to demonstrate conditional rendering.

1. Create a new file named `Superhero.js` in your project directory.

2. Open `Superhero.js` and add the following code:

```jsx
import React from 'react';

function Superhero(props) {
  return (
    <div>
      <h2>{props.name}</h2>
      {props.showAlias && <p>Alias: {props.alias}</p>}
    </div>
  );
}

export default Superhero;
```

## Step 4: Using Conditional Rendering

1. Create a new file named `App.js` in the same directory.

2. Open `App.js` and add the following code:

```jsx
import React from 'react';
import Superhero from './Superhero';

function App() {
  return (
    <div>
      <h1>Superhero Gallery</h1>
      <Superhero name="Iron Man" alias="Tony Stark" showAlias={true} />
      <Superhero name="Spider-Man" alias="Peter Parker" showAlias={false} />
      <Superhero name="Black Widow" alias="Natasha Romanoff" showAlias={true} />
    </div>
  );
}

export default App;
```

## Step 5: Running Your React App

1. Create an HTML file named `index.html` in your project directory.

2. Open `index.html` and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Conditional Rendering Tutorial</title>
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

5. Open your web browser and visit `http://localhost:3000`. You should see a gallery of superheroes with their names and aliases.

## Advanced Scenario: Dynamic Conditional Rendering

In this section, you'll explore dynamic conditional rendering based on a superhero's power level.

1. Modify the `Superhero.js` component as follows:

```jsx
import React from 'react';

function Superhero(props) {
  return (
    <div>
      <h2>{props.name}</h2>
      {props.powerLevel > 9000 ? (
        <p>Power Level: {props.powerLevel}</p>
      ) : (
        <p>Power Level: Classified</p>
      )}
    </div>
  );
}

export default Superhero;
```

2. Update `App.js`:

```jsx
import React from 'react';
import Superhero from './Superhero';

function App() {
  return (
    <div>
      <h1>Superhero Power Levels</h1>
      <Superhero name="Iron Man" powerLevel={12000} />
      <Superhero name="Spider-Man" powerLevel={7500} />
      <Superhero name="Black Widow" powerLevel={6000} />
    </div>
  );
}

export default App;
```

## Congratulations, You've Mastered Conditional Rendering in React!

You've successfully learned how to apply conditional rendering techniques in React, both in basic and dynamic scenarios. You've used superhero examples to make the learning process engaging and relatable. Now you can create more dynamic and interactive React applications that adapt to different conditions!

Happy coding, Dynamic Developer! 🦸‍♂️🦸‍♀️