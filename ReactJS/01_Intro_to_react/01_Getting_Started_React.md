# React JS Props Tutorial

## Introduction to React JS Props

In React, **props** (short for properties) are a way to pass data from a parent component to a child component. Props are used to make your components dynamic and reusable by allowing them to receive values from the outside. In this tutorial, we will explore how to use props in React components, along with some basic and advanced examples.

## Prerequisites

Before we get started, make sure you have the following installed on your machine:

1. Node.js and npm (Node Package Manager) - to create and run React applications.
2. A code editor (e.g., Visual Studio Code) - to write and edit React code.

## Getting Started

Let's create a new React application using `create-react-app`. Open your terminal or command prompt and run the following command:

```bash
npx create-react-app react-props-tutorial
cd react-props-tutorial
```

This will create a new React application named `react-props-tutorial` and navigate you into the project directory.

## Understanding Basic Props

In this section, we'll create a basic React component that accepts props and renders them.

### Step 1: Create a new component

Open the `src` folder in your project, and create a new file named `AvengersInfo.js`. Add the following code to define the component:

```jsx
// AvengersInfo.js

import React from 'react';

const AvengersInfo = (props) => {
  return (
    <div>
      <h1>{props.name}</h1>
      <p>Alias: {props.alias}</p>
    </div>
  );
};

export default AvengersInfo;
```

In the above code, we defined a functional component called `AvengersInfo`. This component takes in a single argument `props`, which will hold the data passed from the parent component.

### Step 2: Using the component

Now, let's use the `AvengersInfo` component in the `App.js` file to pass props to it.

```jsx
// App.js

import React from 'react';
import AvengersInfo from './AvengersInfo';

function App() {
  return (
    <div>
      <h1>Avengers Information</h1>
      <AvengersInfo name="Iron Man" alias="Tony Stark" />
      <AvengersInfo name="Captain America" alias="Steve Rogers" />
    </div>
  );
}

export default App;
```

In the `App` component, we use the `AvengersInfo` component twice. We pass two sets of props - one for Iron Man and another for Captain America.

### Step 3: Run the application

To run the application, execute the following command in the terminal:

```bash
npm start
```

Expected Output:
```
Avengers Information
Iron Man
Alias: Tony Stark
Captain America
Alias: Steve Rogers
```

## Understanding Advanced Props

In this section, we'll create a more advanced example to understand how to use props for more complex scenarios.

### Step 1: Create a new component

Create a new file named `AvengersTeam.js` in the `src` folder. Add the following code:

```jsx
// AvengersTeam.js

import React from 'react';

const AvengersTeam = ({ teamName, members }) => {
  return (
    <div>
      <h1>{teamName}</h1>
      <ul>
        {members.map((member) => (
          <li key={member}>{member}</li>
        ))}
      </ul>
    </div>
  );
};

export default AvengersTeam;
```

In this component, we're destructuring the `props` object directly in the function parameters to access `teamName` and `members` directly.

### Step 2: Using the component

Let's use the `AvengersTeam` component in the `App.js` file:

```jsx
// App.js

import React from 'react';
import AvengersTeam from './AvengersTeam';

function App() {
  const avengers = ['Iron Man', 'Captain America', 'Thor', 'Hulk', 'Black Widow', 'Hawkeye'];

  return (
    <div>
      <h1>Avengers Teams</h1>
      <AvengersTeam teamName="Earth's Mightiest Heroes" members={avengers} />
    </div>
  );
}

export default App;
```

### Step 3: Run the application

To run the application again, execute the following command in the terminal:

```bash
npm start
```

Expected Output:
```
Avengers Teams
Earth's Mightiest Heroes
- Iron Man
- Captain America
- Thor
- Hulk
- Black Widow
- Hawkeye
```

## Conclusion

In this tutorial, you've learned how to use props in React components to pass data from parent to child components. Props are essential for making your components dynamic and reusable. You can use them to pass simple data like strings or numbers, as well as more complex data like arrays and objects.

Now you have a good understanding of React props, and you can start building more powerful and flexible React applications. Keep experimenting and learning to become proficient in React development!