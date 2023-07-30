# Comparison Operators in JavaScript

Comparison operators in JavaScript are used to compare values and determine the relationship between them. These operators return a Boolean value (`true` or `false`) based on whether the comparison is true or false. Understanding comparison operators is essential for making decisions in your JavaScript code based on different conditions. 
In this tutorial, we'll explore all the comparison operators available in JavaScript.

## List of Comparison Operators

Here's a table listing all the comparison operators in JavaScript:

| Operator | Description                   | Example       |
| -------- | ----------------------------- | ------------- |
| `==`     | Equal to                      | `2 == 2`      |
| `!=`     | Not equal to                  | `3 != 5`      |
| `===`    | Equal value and type          | `2 === '2'`   |
| `!==`    | Not equal value or type       | `3 !== '3'`   |
| `>`      | Greater than                  | `5 > 2`       |
| `<`      | Less than                     | `3 < 10`      |
| `>=`     | Greater than or equal to      | `8 >= 8`      |
| `<=`     | Less than or equal to         | `4 <= 5`      |

## Examples of Comparison Operators

Now, let's see examples of how to use these comparison operators:

### 1. Equal to (`==`)

```javascript
const num1 = 2;
const num2 = 2;

// Checking if two numbers are equal
const isEqual = num1 == num2;

// Output: true
console.log(isEqual);
```

### 2. Not equal to (`!=`)

```javascript
const num1 = 3;
const num2 = 5;

// Checking if two numbers are not equal
const isNotEqual = num1 != num2;

// Output: true
console.log(isNotEqual);
```

### 3. Equal value and type (`===`)

```javascript
const num1 = 2;
const strNum = '2';

// Checking if two values are equal in value and type
const isEqualValueAndType = num1 === strNum;

// Output: false
console.log(isEqualValueAndType);
```

### 4. Not equal value or type (`!==`)

```javascript
const num1 = 3;
const strNum = '3';

// Checking if two values are not equal in value or type
const isNotEqualValueOrType = num1 !== strNum;

// Output: true
console.log(isNotEqualValueOrType);
```

### 5. Greater than (`>`)

```javascript
const num1 = 5;
const num2 = 2;

// Checking if the first number is greater than the second number
const isGreater = num1 > num2;

// Output: true
console.log(isGreater);
```

### 6. Less than (`<`)

```javascript
const num1 = 3;
const num2 = 10;

// Checking if the first number is less than the second number
const isLess = num1 < num2;

// Output: true
console.log(isLess);
```

### 7. Greater than or equal to (`>=`)

```javascript
const num1 = 8;
const num2 = 8;

// Checking if the first number is greater than or equal to the second number
const isGreaterOrEqual = num1 >= num2;

// Output: true
console.log(isGreaterOrEqual);
```

### 8. Less than or equal to (`<=`)

```javascript
const num1 = 4;
const num2 = 5;

// Checking if the first number is less than or equal to the second number
const isLessOrEqual = num1 <= num2;

// Output: true
console.log(isLessOrEqual);
```

## Using Comparison Operators in Conditions

Comparison operators are often used in conditional statements (`if`, `else if`, `else`) to make decisions based on different conditions.

```javascript
const num1 = 10;
const num2 = 5;

if (num1 > num2) {
  console.log("num1 is greater than num2");
} else if (num1 < num2) {
  console.log("num1 is less than num2");
} else {
  console.log("num1 is equal to num2");
}

// Output: "num1 is greater than num2"
```

## Summary

In this tutorial, we explored all the comparison operators available in JavaScript, including equal to, not equal to, equal value and type, not equal value or type, greater than, less than, greater than or equal to, and less than or equal to. Comparison operators play a crucial role in decision-making and logic implementation in JavaScript code. 

Understanding these operators will help you write more effective and interactive JavaScript applications. Happy coding!