# Changing CSS and HTML using JavaScript

## Introduction

JavaScript allows you to dynamically change the CSS and HTML of an HTML document, providing a way to create dynamic and interactive web pages. By manipulating CSS properties and modifying the HTML content, you can change the appearance and behavior of elements on the page in response to user actions or application logic. In this tutorial, we will explore how to change CSS and HTML using JavaScript with simple code snippets and comments to explain each step.

## Changing CSS Using JavaScript

To change CSS properties of elements using JavaScript, you can access the `style` property of the element and modify its CSS attributes. Here's an example:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Changing CSS Using JavaScript</title>
  <style>
    .box {
      width: 200px;
      height: 200px;
      background-color: red;
    }
  </style>
</head>
<body>
  <div class="box"></div>

  <script>
    // Find the element
    const boxElement = document.querySelector(".box");

    // Change CSS properties
    boxElement.style.backgroundColor = "blue";
    boxElement.style.width = "300px";
    boxElement.style.height = "300px";
  </script>
</body>
</html>
```

In the example above, we have a CSS class `.box` with a red background color, and a `<div>` element with that class applied. Using JavaScript, we access the element and change its background color, width, and height.

## Changing HTML Content Using JavaScript

To change the HTML content of an element, you can use the `innerHTML` or `textContent` properties. Here's an example:

```html
<!DOCTYPE html>
<html>
<head>
  <title>Changing HTML Content Using JavaScript</title>
</head>
<body>
  <div id="container">
    <p>Hello, World!</p>
  </div>

  <script>
    // Find the element
    const containerElement = document.getElementById("container");

    // Change HTML content using innerHTML
    containerElement.innerHTML = "<p>Hello, JavaScript!</p>";

    // Change HTML content using textContent
    // Note: textContent will remove any HTML tags and display the text as plain text.
    containerElement.textContent = "Hello, Text Content!";
  </script>
</body>
</html>
```

In the example above, we have a `<div>` element with the ID "container" containing a `<p>` element with the text "Hello, World!". Using JavaScript, we change the HTML content of the "container" element using both `innerHTML` and `textContent`.

## Summary

In this tutorial, you learned how to change CSS and HTML using JavaScript to create dynamic and interactive web pages. By manipulating CSS properties and modifying HTML content, you can change the appearance and behavior of elements on the page in response to user actions or application logic. With these techniques, you can create visually appealing and engaging web applications. Happy coding!