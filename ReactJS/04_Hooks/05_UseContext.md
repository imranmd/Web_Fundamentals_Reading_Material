# ReactJS `useContext` Tutorial Documentation

## Table of Contents

1. Introduction to `useContext`
2. What is React Context?
3. Using `useContext` Hook
   - Step 1: Creating a Context
   - Step 2: Providing Context
   - Step 3: Consuming Context
4. When and Where to Use `useContext`
   - Managing Global State
   - Avoiding Prop Drilling
5. Conclusion

## 1. Introduction to `useContext`

ReactJS is a popular JavaScript library for building user interfaces. It provides a way to create reusable components and manage state efficiently. `useContext` is one of the built-in hooks provided by React that allows you to consume data from a React Context.

In this tutorial, we will explore what React Context is, how to use the `useContext` hook, and when and where you should use it in your applications.

## 2. What is React Context?

React Context is a mechanism that allows you to share data, such as state or configuration, across the component tree without having to pass the data explicitly through props at every level. It helps solve the problem of prop drilling, which can make the code harder to maintain and understand.

Context provides a way to create a global state that can be accessed by components nested deeply in the component tree.

## 3. Using `useContext` Hook

### Step 1: Creating a Context

To use `useContext`, you need to create a Context first. This is typically done by using the `createContext` function provided by React.

```jsx
// MyContext.js
import React from 'react';

const MyContext = React.createContext();

export default MyContext;
```

### Step 2: Providing Context

To make the context data available to components, you need to wrap a part of your component tree with the `Context.Provider` component.

```jsx
// App.js
import React from 'react';
import MyContext from './MyContext';

const App = () => {
  const contextData = {
    // your context data here
  };

  return (
    <MyContext.Provider value={contextData}>
      {/* Your component tree */}
    </MyContext.Provider>
  );
};

export default App;
```

### Step 3: Consuming Context

Now that you've created and provided the context, you can consume it in any component using the `useContext` hook.

```jsx
// SomeComponent.js
import React, { useContext } from 'react';
import MyContext from './MyContext';

const SomeComponent = () => {
  const contextData = useContext(MyContext);

  // Now you can use contextData in your component
};

export default SomeComponent;
```

## 4. When and Where to Use `useContext`

### Managing Global State

`useContext` is particularly useful when you need to manage global state that is shared among multiple components. Examples include user authentication status, theme preferences, or language settings. Instead of passing this data through multiple levels of props, you can use `useContext` to access it directly.

### Avoiding Prop Drilling

When you find yourself passing down props through multiple levels of components, `useContext` can help eliminate this prop drilling. It makes your codebase cleaner and easier to maintain by reducing the complexity of your component relationships.

## 5. Conclusion

In this tutorial, you've learned about the `useContext` hook in ReactJS. You now understand how to create a context, provide context data, and consume it using the `useContext` hook. You've also seen scenarios where using `useContext` can be beneficial, such as managing global state and avoiding prop drilling.

By using `useContext`, you can improve the organization and efficiency of your React applications, making them easier to develop and maintain. Happy coding!