# React JS Props Tutorial

## Introduction

In React JS, **Props** (short for properties) are a way to pass data from a parent component to its child components. They allow you to customize and configure child components by providing them with data and functions from their parent component. Props are read-only and cannot be modified within the child component.

In this tutorial, we will cover the basics of React JS Props, including how to pass and use props, and then explore some advanced scenarios.

## Prerequisites

Before you begin, make sure you have the following installed:

1. Node.js and npm (Node Package Manager)
2. A code editor (e.g., Visual Studio Code)

## Basic Usage of Props

Let's create a simple React component that demonstrates the use of props.

### Step 1: Create a new React App

Open your terminal or command prompt and run the following command to create a new React app:

```bash
npx create-react-app avengers-app
cd avengers-app
```

### Step 2: Create Parent and Child Components

Inside the `src` folder, create two new files:

**ParentComponent.js**

```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const avengerName = "Iron Man";

  return (
    <div>
      <h1>Avengers Team</h1>
      <ChildComponent name={avengerName} />
    </div>
  );
}

export default ParentComponent;
```

**ChildComponent.js**

```jsx
import React from 'react';

const ChildComponent = (props) => {
  return (
    <div>
      <h2>Avenger Name: {props.name}</h2>
    </div>
  );
}

export default ChildComponent;
```

### Step 3: Render ParentComponent in App.js

Open `App.js` and replace its content with the following:

```jsx
import React from 'react';
import ParentComponent from './ParentComponent';

function App() {
  return (
    <div className="App">
      <ParentComponent />
    </div>
  );
}

export default App;
```

### Step 4: Run the App

Save the changes in your code editor and run the following command in your terminal:

```bash
npm start
```

Now, open your web browser and go to `http://localhost:3000`. You should see the Avengers Team title along with the Avenger Name displayed as "Iron Man".

## Advanced Usage of Props

In this advanced example, we will pass an array of Avengers' names to the child component and display them using the map function.

### Step 1: Update ParentComponent

Modify the `ParentComponent.js` file as follows:

```jsx
import React from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const avengerNames = ["Iron Man", "Thor", "Hulk", "Captain America", "Black Widow"];

  return (
    <div>
      <h1>Avengers Team</h1>
      {avengerNames.map((name, index) => (
        <ChildComponent key={index} name={name} />
      ))}
    </div>
  );
}

export default ParentComponent;
```

### Step 2: Update ChildComponent

Modify the `ChildComponent.js` file to remain the same as the basic example.

### Step 3: Run the App

Save the changes in your code editor if you haven't already, and run the app using:

```bash
npm start
```

Visit `http://localhost:3000` in your web browser, and you will now see a list of Avengers' names displayed under the Avengers Team title.

## Conclusion

In this tutorial, you learned how to use React JS Props to pass data from a parent component to its child components. You saw how to pass simple data like strings and more complex data like arrays. Props are a fundamental concept in React that allows you to build dynamic and reusable components.

Feel free to experiment with different props and data types to get a better understanding of how they work! Happy coding!