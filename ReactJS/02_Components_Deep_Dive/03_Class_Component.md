# Tutorial: Class Components in React

Welcome to the tutorial on Class Components in React. In this tutorial, we will explore class components, explain their characteristics, provide a sample code for creating a class component, discuss the lifecycle methods they have, compare lifecycle methods with React Hooks[Which we will learn in next session]

## What are Class Components?

Class components are a type of component in React that are defined as JavaScript classes. They were the primary way of creating components in React before the introduction of functional components and React Hooks.

## Sample Class Component Code

Here's an example of a simple class component in React:

```jsx
import React, { Component } from 'react';

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  componentDidMount() {
    console.log('Component mounted');
  }

  componentDidUpdate(prevProps, prevState) {
    console.log('Component updated');
  }

  componentWillUnmount() {
    console.log('Component will unmount');
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>Increment</button>
      </div>
    );
  }
}

export default Counter;
```

In this code, we've defined a class component named `Counter` that manages a `count` state and provides methods to update it.

## Lifecycle Methods of Class Components

The lifecycle methods of a class component are executed in a specific order:

1. **Constructor:** Initializes the component's state and binds event handlers.

2. **render:** Returns JSX to define the component's UI.

3. **componentDidMount:** Executed after the component is inserted into the DOM. Useful for fetching data or setting up timers.

4. **componentDidUpdate:** Executed whenever the component updates. Useful for responding to changes.

5. **componentWillUnmount:** Executed before the component is removed from the DOM. Used for cleaning up resources.

import React, { Component } from 'react';

class LifecycleExample extends Component {
  constructor(props) {
    super(props);
    console.log('Constructor');
    this.state = { count: 0 };
  }

  componentDidMount() {
    console.log('ComponentDidMount');
  }

  componentDidUpdate() {
    console.log('ComponentDidUpdate');
  }

  componentWillUnmount() {
    console.log('ComponentWillUnmount');
  }

  render() {
    console.log('Render');
    return <div>Component Lifecycle Example</div>;
  }
}

export default LifecycleExample;
```

## Comparing Lifecycle Methods with Hooks

- **Lifecycle Methods:** Class components use lifecycle methods to manage state and respond to changes. Lifecycle methods can lead to complex component structures and make code harder to follow.

- **Hooks:** React Hooks are a modern alternative to lifecycle methods. They allow you to manage state and other functionalities within functional components. Hooks make code more readable and easier to maintain.

## Summary:

- Class components are defined as ES6 classes in React.
- They are used to create UI elements and manage state.
- Class components have lifecycle methods for managing component behavior.
- Lifecycle methods execute in a specific order: constructor, render, componentDidMount, componentDidUpdate, componentWillUnmount.
- React Hooks provide a modern alternative to lifecycle methods for managing state and functionality in functional components.

## Documentation and Article Resources:

1. [React Official Documentation - Component Lifecycle](https://reactjs.org/docs/react-component.html)
2. [A Guide to the React Component Lifecycle](https://www.digitalocean.com/community/tutorials/react-react-component-lifecycle) by DigitalOcean