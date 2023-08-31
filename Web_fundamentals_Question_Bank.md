# HTML
### Beginner Questions: [2 Point Each]

1. What are attributes? Give an Example
2. What are empty elements?
3. What is semantic HTML?
4. What is the use of the alt attribute in HTML?
5. What is the use of the title attribute in HTML?
6. What is the difference between HTML elements and tags?
7. What are meta tags, their significance and give code snippets where we use couple of meta tags?
8. What is the difference between the id and class attributes in HTML?
9. What is the difference between the `<ol>` and `<ul>` elements?


### Intermediate Questions: [4 Points each]

1. Describe the difference between a cookie, sessionStorage and localStorage? Write sample pseudo code snippets for each.
2. What are semantic and non-semantic elements? Write sample pseudo code snippets for each.
3. What does a `<DOCTYPE html>` do? 
4. What is the purpose of main element? 
5. Write code snippet for semantic HTML blog article.
6. When should you use section, div or article? 
7. What is an iframe and how it works? Write sample pseudo code snippets for each.
What is the difference between the `<article>` and `<section>` elements?


## Advanced Questions: [10 Points each]

1. How can I get indexed better by search engines? Write/explain sample pseudo code snippets for each.
2. Ways to improve website performance? You are given with a website like Amazon, too heavy on assets and resources, how do you improve the performance of the website? Write sample pseudo code snippets for each.
3. What does async and defer refer to in script tag? Describe the difference between `<script>`, `<script async>` and `<script defer>`. Write sample code snippets for each.
4. Create a responsive HTML blog article that includes a header, a main content section, and a footer. The main content section should include a featured image, a title, a subtitle, and a body text. The article should also include a related articles section that displays links to other articles on the same topic.
5. Create a responsive HTML form with validation that includes the following fields: name, email, password, and confirm password. The form should have a submit button that is disabled until all fields are valid.
6. Implement 8X8 Chessboard with HTML and CSS


# CSS

## Easy Questions: [2 Points each]

1. What is the difference between a class and an ID selector in CSS? Explain with sample code snippet.
2. What is the difference between padding and margin in CSS? Explain with sample code snippet
3. What is the box model in CSS? Explain with sample code snippet
4. What is the difference between display: none and visibility: hidden in CSS?
5. How to center align a div inside another div?
6. How to center align a paragraph?



## Medium Questions: [4 Points each]

1. How do you make a web page responsive? What are all the ways?
2. What are different type of Selectors, with sample code snippet
3. What is the difference between position: relative and position: absolute in CSS? Explain with sample code snippet
4. What is the purpose of the z-index property in CSS?
5. What is the difference between em and rem units in CSS?
6. What is the difference between justify-content and align-items in CSS?
7. What are the pros and cons of using absolute positioning?





## Hard Questions: [10 Points each]
1. How to draw a triangle? a circle? a colored square?
2. What are the advantages/disadvantages of using CSS preprocessors?
3. What is Combinator selector?
4. What is the purpose of the @media rule in CSS? Explain with sample code snippet.
5. What is the difference between block / inline / inline-block element?
6. What is the purpose of the transform property in CSS? Explain with sample code snippet.
7. What is the difference between the float and clear properties in CSS? Explain with sample code snippet.
8. What is the difference between the :nth-child() and :nth-of-type() selectors in CSS? Explain with sample code snippet. 

# JS

## Easy Questions: [2 Points each]

1. What does `this` refer to in JavaScript? Give all different dynamic context examples
2. What is hoisting in JavaScript? Explain with an example.
3. What is the difference between `let`, `const`, and `var` in JavaScript?
4. What is the difference between `==` and `===` in JavaScript?
5. What is the purpose of the `this` keyword in JavaScript?
6. What is the difference between a function declaration and a function expression in JavaScript?
7. What is the difference between synchronous and asynchronous code in JavaScript?
8. What is the difference between bubbling and capturing in JavaScript?
9. What is the JavaScript Event Loop in JavaScript?
9. Explain Scope in JS.


## Medium Questions: [4 Points each]

1. Explain Callback hell with example
2. Explain Call, Bind and Apply with example
3. Explain Closure with example
4. What is the purpose of the Object.create() method in JavaScript?
5. What is the purpose of the async and await keywords in JavaScript?
6. What's the output?

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```

7. What's the output? Explain why

```javascript
let c = { greeting: 'Hey!' };
let d;

d = c;
c.greeting = 'Hello';
console.log(d.greeting);
```

8. What's the output? Explain why

```javascript
let a = 3;
let b = new Number(3);
let c = 3;

console.log(a == b);
console.log(a === b);
console.log(b === c);
```

9. What's the output? Explain why

```javascript
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
```

10. What's the output?  Explain why

```javascript
function getAge() {
  'use strict';
  age = 21;
  console.log(age);
}

getAge();
```

## Hard Questions: [10 Points each]

1. Write a currying function that returns a sum of two numbers
2. Explain Event Bubbling with example
3. Explain difference between Callbacks, Promises and Async Await with example
4. Explain OOPS Concepts with ES6
5. Write a polyfill function for map or reduce or filter.
6. Explain JS Modules and communication between them with example

