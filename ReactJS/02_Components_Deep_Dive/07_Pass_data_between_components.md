# Tutorial: Passing Data Between Components in React

Welcome to the tutorial on how to pass data between components in React. In this tutorial, we'll explore the concept of using props to send and receive data between components, and we'll provide a hands-on example to illustrate the process.

![](../Assets/React/passing%20Props.webp)

## Using Props to Pass Data

Props (short for properties) are a way to pass data from a parent component to a child component. They allow you to make your components dynamic and reusable by providing different data each time they are used.

## Sample Demo Component Code

Building on top of the previous "Avenger" example, let's create a component that accepts the avenger's name as a prop:

```jsx
import React from 'react';

function Avenger(props) {
  return (
    <div>
      <h2>Avenger: {props.name}</h2>
      <p>{props.description}</p>
    </div>
  );
}

export default Avenger;
```

In this code, the `Avenger` component accepts two props: `name` and `description`. These props are used to customize the content of the Avenger card.

## Using Multiple Components with Props

Now, let's create an `App` component that uses the `Avenger` component multiple times with different props:

```jsx
import React from 'react';
import Avenger from './Avenger';

function App() {
  return (
    <div>
      <h1>Marvel Universe</h1>
      <Avenger name="Iron Man" description="Genius, billionaire, playboy, philanthropist." />
      <Avenger name="Captain America" description="Super-soldier and leader of the Avengers." />
      <Avenger name="Black Widow" description="Highly skilled spy and assassin." />
    </div>
  );
}

export default App;
```

In this example, the `App` component renders three `Avenger` components, each with different props. This showcases how props can be used to pass unique data to each instance of a component.

## Summary:

- Props allow data to be passed from parent to child components.
- They make components dynamic and reusable by providing varying data.
- Props are specified when rendering a component and accessed within the component.
- Props enable you to customize component behavior and content.
- Props can be strings, numbers, booleans, functions, or even other components.

Remember that props are a fundamental concept in React that facilitates communication and data sharing between components.

## Official Documentation Resources:

1. [React Official Documentation - Components and Props](https://reactjs.org/docs/components-and-props.html)