# ReactJS Hooks Tutorial Documentation

## Table of Contents

1. Introduction to ReactJS Hooks
2. Why Use ReactJS Hooks?
3. Commonly Used ReactJS Hooks
   - useState
   - useEffect
   - useContext
   - useMemo
   - useCallback
   - useRef
   - useReducer
4. Rules of Using ReactJS Hooks
5. Custom Hooks
6. Conclusion

## 1. Introduction to ReactJS Hooks

ReactJS Hooks are a feature introduced in React 16.8 that allow you to use state and other React features without writing a class. Hooks provide a more concise and intuitive way to manage state and side effects in your React components. They make it easier to reuse component logic and create more modular and maintainable code.

## 2. Why Use ReactJS Hooks?

Before the introduction of Hooks, complex logic and state management in React components were often achieved using higher-order components (HOCs) or render props. Hooks simplify this process by allowing you to encapsulate stateful logic within functional components themselves, improving code readability and reusability. Hooks also address some of the performance optimization concerns that were common with class components.

## 3. Commonly Used ReactJS Hooks

### a. useState

`useState` is used to add state to a functional component. It returns a state variable and a function to update that variable.

Example:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

### b. useEffect

`useEffect` is used to perform side effects in functional components, such as fetching data, subscribing to events, or updating the DOM.

Example:

```jsx
import React, { useState, useEffect } from 'react';

function DataFetcher() {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data));
  }, []);

  return (
    <ul>
      {data.map(item => (
        <li key={item.id}>{item.name}</li>
      ))}
    </ul>
  );
}
```

### c. useContext

`useContext` is used to consume context within a functional component, providing access to values defined higher up in the component tree.

Example:

```jsx
import React, { useContext } from 'react';

const UserContext = React.createContext();

function UserInfo() {
  const user = useContext(UserContext);

  return <p>Hello, {user.name}!</p>;
}
```

### d. useMemo

`useMemo` is used to memoize expensive calculations, preventing unnecessary re-renders.

Example:

```jsx
import React, { useMemo } from 'react';

function ExpensiveComponent({ data }) {
  const result = useMemo(() => {
    // Perform heavy calculations using data
    return calculateResult(data);
  }, [data]);

  return <p>Result: {result}</p>;
}
```

### e. useCallback

`useCallback` is used to memoize callback functions, optimizing performance in child components.

Example:

```jsx
import React, { useCallback } from 'react';

function ParentComponent() {
  const handleClick = useCallback(() => {
    console.log('Button clicked');
  }, []);

  return <ChildComponent onClick={handleClick} />;
}
```

### f. useRef

`useRef` is used to access and interact with DOM elements or to store mutable values that do not trigger re-renders.

Example:

```jsx
import React, { useRef } from 'react';

function InputFocus() {
  const inputRef = useRef();

  const focusInput = () => {
    inputRef.current.focus();
  };

  return (
    <div>
      <input ref={inputRef} />
      <button onClick={focusInput}>Focus Input</button>
    </div>
  );
}
```

### g. useReducer

`useReducer` is an alternative to `useState` for managing more complex state logic. It's often used for state transitions that involve multiple actions.

Example:

```jsx
import React, { useReducer } from 'react';

const initialState = { count: 0 };

function countReducer(state, action) {
  switch (action.type) {
    case 'increment':
      return { count: state.count + 1 };
    case 'decrement':
      return { count: state.count - 1 };
    default:
      return state;
  }
}

function CounterWithReducer() {
  const [state, dispatch] = useReducer(countReducer, initialState);

  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={() => dispatch({ type: 'increment' })}>Increment</button>
      <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button>
    </div>
  );
}
```

## 4. Rules of Using ReactJS Hooks

- Hooks can only be used in functional components or other custom hooks.
- Hooks must be called at the top level of a component or a custom hook; they cannot be conditionally called.
- Hooks should always have the same order when called in every render of a component.

## 5. Custom Hooks

Custom hooks are functions that encapsulate specific behavior or logic, allowing you to reuse that logic across different components.

Example:

```jsx
import { useState, useEffect } from 'react';

function useFetchData(url) {
  const [data, setData] = useState([]);

  useEffect(() => {
    fetch(url)
      .then(response => response.json())
      .then(data => setData(data));
  }, [url]);

  return data;
}
```

## 6. Conclusion

ReactJS Hooks provide a modern and efficient way to manage state and side effects in your React applications. By understanding and utilizing the various hooks available, you can create more readable, maintainable, and reusable code. Remember to follow the rules of using hooks and explore the possibilities of custom hooks to further enhance your React development experience.