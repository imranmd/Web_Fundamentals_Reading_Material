# React Performance - Using Memoization (useMemo)

## Introduction

In React applications, performance optimization is crucial to ensure smooth and efficient rendering of components. One of the techniques to achieve better performance is by utilizing the `useMemo` hook, a built-in React hook that allows you to memoize the results of expensive calculations or function calls.

In this tutorial, we will explore what React Performance - `useMemo` is, why and when you should use it, and how to implement it in your React components.

## Table of Contents

1. What is React Performance - `useMemo`?
2. Why Use `useMemo`?
3. When to Use `useMemo`?
4. Implementing `useMemo` in React Components
   - Basic Usage
   - Advanced Example
5. Conclusion

## 1. What is React Performance - `useMemo`?

React Performance - `useMemo` is a built-in hook in React that helps optimize your components by memoizing the results of function calls. It prevents unnecessary re-computation of values by caching the result of a function and returning the cached value when the inputs to that function have not changed.

## 2. Why Use `useMemo`?

React components re-render whenever their state or props change. However, sometimes a component may re-render even if the computed values within it haven't changed. This can lead to unnecessary performance overhead.

By using `useMemo`, you can optimize your components by telling React to skip re-evaluating a function and using the cached result instead if the inputs have not changed. This can lead to significant performance improvements, especially in components that involve heavy calculations or complex data transformations.

## 3. When to Use `useMemo`?

You should consider using `useMemo` in the following scenarios:

- **Expensive Calculations**: When your component involves expensive calculations, such as complex mathematical computations or data transformations.
- **Rendering Optimization**: To prevent unnecessary re-renders caused by values that haven't changed.
- **Memoizing Callbacks**: When passing callbacks as props to child components to prevent unnecessary re-creation of callback functions.
- **Optimizing Component Props**: When working with components that receive props that change frequently, but the rendering logic depends only on specific props.

## 4. Implementing `useMemo` in React Components

### Basic Usage

Let's start with a simple example. Suppose you have a component that displays the square of a number passed as a prop.

```jsx
import React, { useMemo } from 'react';

const SquareComponent = ({ number }) => {
  const squaredValue = useMemo(() => {
    console.log('Calculating square...');
    return number * number;
  }, [number]);

  return (
    <div>
      {number} squared is {squaredValue}
    </div>
  );
};

export default SquareComponent;
```

In this example, the `useMemo` hook ensures that the square calculation is only performed when the `number` prop changes. If the `number` prop remains the same, the cached result is returned, avoiding unnecessary recalculations.

### Advanced Example

Consider a more complex example where you want to optimize a list of items. Suppose you have a list of products and you want to display the total price of selected items.

```jsx
import React, { useState, useMemo } from 'react';

const ProductList = ({ products }) => {
  const [selectedProducts, setSelectedProducts] = useState([]);

  const totalPrice = useMemo(() => {
    console.log('Calculating total price...');
    return selectedProducts.reduce((sum, product) => sum + product.price, 0);
  }, [selectedProducts]);

  const handleProductSelect = (product) => {
    setSelectedProducts((prevSelected) =>
      prevSelected.includes(product)
        ? prevSelected.filter((p) => p !== product)
        : [...prevSelected, product]
    );
  };

  return (
    <div>
      <h2>Product List</h2>
      {products.map((product) => (
        <div key={product.id}>
          <label>
            <input
              type="checkbox"
              checked={selectedProducts.includes(product)}
              onChange={() => handleProductSelect(product)}
            />
            {product.name} - ${product.price}
          </label>
        </div>
      ))}
      <p>Total Price: ${totalPrice}</p>
    </div>
  );
};

export default ProductList;
```

In this example, the `useMemo` hook is used to memoize the total price calculation based on the `selectedProducts` array. It ensures that the calculation is performed only when the selected products change, preventing unnecessary recalculations during re-renders.

## 5. Conclusion

React Performance - `useMemo` is a powerful tool for optimizing your React components by memoizing expensive calculations and preventing unnecessary re-evaluations. By using `useMemo` strategically, you can significantly improve the performance of your application.

Remember to apply `useMemo` judiciously, focusing on areas where expensive calculations or rendering optimizations are required. This will help you achieve a smoother and more efficient React application.

In this tutorial, we covered the basics of React Performance - `useMemo`, its benefits, and how to implement it in your components. Armed with this knowledge, you can now start using `useMemo` effectively to enhance the performance of your React applications.