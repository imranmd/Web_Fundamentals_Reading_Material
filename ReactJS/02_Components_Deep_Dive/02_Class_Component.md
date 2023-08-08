# Tutorial: Building React JS Class Components with Examples

In this tutorial, you'll embark on a journey to master React JS Class Components using examples inspired by mighty heroes. Class components are a fundamental part of React, allowing you to create reusable and stateful components. We'll start from the basics and gradually delve into more advanced concepts.

## Prerequisites

Before you begin, ensure you have the following installed on your computer:

1. Node.js: Download and install Node.js from [nodejs.org](https://nodejs.org/).

## Step 1: Setting Up Your Development Environment

1. Open your terminal or command prompt.

2. Create a new directory for your React app:

   ```bash
   mkdir react-class-components-tutorial
   cd react-class-components-tutorial
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

## Step 3: Creating Your First Class Component

In this step, we'll create a basic class component using a superhero theme.

1. Create a new file named `Hero.js` in your project directory.

2. Open `Hero.js` and add the following code:

```jsx
import React, { Component } from 'react';

class Hero extends Component {
  render() {
    return (
      <div>
        <h2>{this.props.name}</h2>
        <p>Alias: {this.props.alias}</p>
      </div>
    );
  }
}

export default Hero;
```

## Step 4: Using Class Components in Your App

1. Create a new file named `App.js` in the same directory.

2. Open `App.js` and add the following code:

```jsx
import React, { Component } from 'react';
import Hero from './Hero';

class App extends Component {
  render() {
    return (
      <div>
        <h1>Heroic Squad</h1>
        <Hero name="Iron Man" alias="Tony Stark" />
        <Hero name="Spider-Man" alias="Peter Parker" />
        <Hero name="Black Widow" alias="Natasha Romanoff" />
      </div>
    );
  }
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
  <title>React Class Components Tutorial</title>
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

5. Open your web browser and visit `http://localhost:3000`. You should see a list of heroes along with their aliases.

## Advanced Concepts: State and Lifecycle

In this section, we'll explore more advanced class component concepts.

1. Modify the `Hero.js` component to include a state:

```jsx
import React, { Component } from 'react';

class Hero extends Component {
  constructor(props) {
    super(props);
    this.state = {
      power: 'Unknown',
    };
  }

  render() {
    return (
      <div>
        <h2>{this.props.name}</h2>
        <p>Alias: {this.props.alias}</p>
        <p>Power: {this.state.power}</p>
      </div>
    );
  }
}

export default Hero;
```

2. Update the `App.js` component to include the new state:

```jsx
import React, { Component } from 'react';
import Hero from './Hero';

class App extends Component {
  render() {
    return (
      <div>
        <h1>Heroic Squad</h1>
        <Hero name="Iron Man" alias="Tony Stark" />
        <Hero name="Spider-Man" alias="Peter Parker" />
        <Hero name="Black Widow" alias="Natasha Romanoff" />
      </div>
    );
  }
}

export default App;
```

## Congratulations, You've Mastered React Class Components!

You've successfully learned how to create and use React class components, exploring both the basics and more advanced concepts. With the power of class components, you can now build dynamic and interactive applications. Keep exploring and building your own heroic React apps!

Happy coding, Super Dev! 🦸‍♂️🦸‍♀️