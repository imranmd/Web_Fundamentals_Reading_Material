# Tutorial: Understanding ReactJS Pure Components and Higher-Order Components (HOCs) with Examples

In this tutorial, we will delve into ReactJS concepts of Pure Components and Higher-Order Components (HOCs) using examples inspired by iconic superheroes. We will begin with the basics and gradually explore more advanced concepts to enhance your understanding.

## Prerequisites

Before we begin, make sure you have the following installed on your computer:

1. Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).

## Step 1: Setting Up Your Development Environment

1. Open your terminal or command prompt.

2. Create a new directory for your React app:

   ```bash
   mkdir react-pure-hoc-tutorial
   cd react-pure-hoc-tutorial
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

## Step 3: Creating a Simple Component

To understand Pure Components and HOCs, let's create a simple component.

1. Create a new file named `Hero.js` in your project directory.

2. Open `Hero.js` and add the following code:

```jsx
import React from 'react';

function Hero(props) {
  return (
    <div>
      <h2>{props.name}</h2>
      <p>Alias: {props.alias}</p>
    </div>
  );
}

export default Hero;
```

## Step 4: Creating a Pure Component

1. Create a new file named `PureHero.js` in the same directory.

2. Open `PureHero.js` and add the following code:

```jsx
import React, { PureComponent } from 'react';

class PureHero extends PureComponent {
  render() {
    return (
      <div>
        <h2>{this.props.name}</h2>
        <p>Alias: {this.props.alias}</p>
      </div>
    );
  }
}

export default PureHero;
```

## Step 5: Creating a Higher-Order Component (HOC)

1. Create a new file named `withPower.js` in the same directory.

2. Open `withPower.js` and add the following code:

```jsx
import React from 'react';

const withPower = (WrappedComponent, power) => {
  return (props) => (
    <div>
      <WrappedComponent {...props} />
      <p>Power: {power}</p>
    </div>
  );
};

export default withPower;
```

## Step 6: Using Components and HOC

1. Create a new file named `App.js` in the same directory.

2. Open `App.js` and add the following code:

```jsx
import React from 'react';
import Hero from './Hero';
import PureHero from './PureHero';
import withPower from './withPower';

const IronMan = withPower(Hero, 'Genius-level intellect and powered armor suit');
const SpiderMan = withPower(PureHero, 'Agility, wall-crawling, and web-shooters');

function App() {
  return (
    <div>
      <h1>Superhero Components</h1>
      <Hero name="Iron Man" alias="Tony Stark" />
      <PureHero name="Captain America" alias="Steve Rogers" />
      <IronMan name="Iron Man" alias="Tony Stark" />
      <SpiderMan name="Spider-Man" alias="Peter Parker" />
    </div>
  );
}

export default App;
```

## Step 7: Running Your React App

1. Create an HTML file named `index.html` in your project directory.

2. Open `index.html` and add the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>React Pure Components and HOCs Tutorial</title>
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

5. Open your web browser and visit `http://localhost:3000`. You should see a list of superheroes and their powers displayed in different ways.

## Congratulations, You've Learned React Pure Components and HOCs!

You've successfully learned about React's Pure Components and Higher-Order Components. You've seen how Pure Components can optimize rendering and how HOCs can add additional functionality to your components. Apply these concepts to create efficient and modular React applications!

Happy coding, Super Coder! 🚀🦸‍♂️🦸‍♀️