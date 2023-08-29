# Tutorial: Higher Order Components (HOC) in React

Welcome to the tutorial on Higher Order Components (HOC) in React. In this tutorial, we will delve into the concept of Higher Order Components, understand their purpose, learn how to create them, and explore practical examples of using HOCs in your React applications.

## What are Higher Order Components?

Higher Order Components (HOCs) are a design pattern in React that enhance the behavior and capabilities of existing components. HOCs are functions that take a component as an argument and return a new component with added functionality.

## Creating a Higher Order Component

Creating an HOC involves creating a function that takes a component and returns a new component. Let's see an example of creating a simple logging HOC:

```jsx
import React from 'react';

const withLogger = WrappedComponent => {
  return class extends React.Component {
    componentDidMount() {
      console.log(`Component ${WrappedComponent.name} mounted.`);
    }

    render() {
      return <WrappedComponent {...this.props} />;
    }
  };
};

export default withLogger;
```

In this example, `withLogger` is an HOC that logs when a component it wraps is mounted.

## Using a Higher Order Component

To use an HOC, you wrap your component using the HOC function. Here's how you can use the `withLogger` HOC:

```jsx
import React from 'react';
import withLogger from './withLogger';

class MyComponent extends React.Component {
  render() {
    return <div>Hello from MyComponent</div>;
  }
}

const MyComponentWithLogger = withLogger(MyComponent);

export default MyComponentWithLogger;
```

In this code, `MyComponentWithLogger` is a new component with the added functionality of logging when it's mounted.

## Benefits of Higher Order Components

1. **Reusability:** HOCs allow you to encapsulate and reuse behaviors across multiple components.

2. **Composition:** You can compose multiple HOCs to add different functionalities to a component.

3. **Separation of Concerns:** HOCs promote separating concerns by keeping specific behaviors isolated.

## When to Use Higher Order Components

- Use HOCs when you need to add common behavior or functionality to multiple components.
- Use HOCs to separate concerns and avoid repeating code in multiple components.

## Summary:

- Higher Order Components (HOCs) are functions that take a component and return a new component with added functionality.
- HOCs are used to enhance the behavior and capabilities of existing components.
- Creating an HOC involves creating a function that returns a new component that wraps the original component.
- HOCs promote reusability, composition, and separation of concerns in your React application.

## Official Documentation Resources:

1. [React Official Documentation - Higher Order Components](https://reactjs.org/docs/higher-order-components.html)
2. [A Comprehensive Guide to React Higher-Order Components](https://www.robinwieruch.de/react-higher-order-components) by Robin Wieruch