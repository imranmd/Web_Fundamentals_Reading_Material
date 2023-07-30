# Memoization

## Introduction

Memoization is an optimization technique used to improve the performance of functions by caching the results of expensive function calls and returning the cached result when the same inputs occur again. It is particularly useful for functions that have costly calculations or recursive calls with overlapping subproblems. In JavaScript, memoization is implemented using closures and data structures like objects or Maps. In this tutorial, we will explore the definition and syntax of memoization, provide an example code snippet with comments, explain when to use it, and use simple words to explain the concept.

## Memoization

### Definition and Syntax

Memoization is the process of caching the results of function calls based on their input parameters and reusing the cached result when the same inputs occur again. It is often used to avoid redundant computations and improve the overall performance of the function.

```javascript
function memoize(func) {
  const cache = {};
  return function (...args) {
    const key = JSON.stringify(args);
    if (cache[key]) {
      return cache[key];
    } else {
      const result = func.apply(this, args);
      cache[key] = result;
      return result;
    }
  };
}
```

In the code above, we define a `memoize` function that takes another function `func` as an argument. It returns a new function that wraps `func` with memoization logic. The `cache` object is used to store the results of function calls based on their input parameters. When the wrapped function is called, it checks if the result for the current input parameters exists in the cache. If it does, it returns the cached result; otherwise, it calculates the result, stores it in the cache, and returns the result.

## Example: Fibonacci with Memoization

Let's use memoization to optimize the calculation of Fibonacci numbers, a classic example that benefits from memoization due to overlapping subproblems.

```javascript
function fibonacci(n) {
  if (n <= 1) {
    return n;
  } else {
    return fibonacci(n - 1) + fibonacci(n - 2);
  }
}

const memoizedFibonacci = memoize(fibonacci);

console.log(memoizedFibonacci(10)); // Output: 55 (Cached result used)
console.log(memoizedFibonacci(15)); // Output: 610 (Cached result used)
console.log(memoizedFibonacci(10)); // Output: 55 (Cached result reused)
```

In the code above, we have a simple recursive implementation of the Fibonacci function. However, when calculating Fibonacci(10) and Fibonacci(15), the function recalculates overlapping subproblems multiple times, resulting in redundant computations. By applying memoization using the `memoize` function, the results for each input are cached, and subsequent calls with the same input reuse the cached results, significantly improving performance.

## When to Use Memoization

Memoization is a useful optimization technique in scenarios where a function's outputs depend only on its inputs and the function has expensive calculations or repetitive recursive calls with overlapping subproblems. Common use cases for memoization include:

1. **Recursive Functions:** Memoization can significantly speed up recursive functions by avoiding redundant recursive calls.

2. **Costly Computations:** Functions with complex calculations or time-consuming operations can benefit from memoization to cache results and reduce computation time.

3. **Dynamic Programming Algorithms:** Many dynamic programming algorithms, like Fibonacci and factorial, involve overlapping subproblems, making them ideal candidates for memoization.

## Summary

Memoization is a powerful optimization technique in JavaScript that allows you to cache the results of function calls based on their input parameters, reducing redundant computations and improving performance. By implementing memoization using closures and data structures like objects or Maps, you can enhance the efficiency of functions that involve costly calculations or recursive calls with overlapping subproblems.

However, it's essential to use memoization judiciously, as caching results consume memory, and the trade-off between computation time and memory usage should be considered. When used appropriately, memoization can be a valuable tool to optimize your JavaScript applications and create faster, more responsive code. Happy coding!