# CSS Introduction Tutorial

## What is CSS?

CSS stands for "Cascading Style Sheets." It is a language used to control the presentation and layout of web documents written in HTML. CSS allows you to apply styles, such as colors, fonts, margins, and positioning, to HTML elements. With CSS, you can make your web pages visually appealing and control how they look on different devices.

## Getting Started

To use CSS, you need a basic understanding of HTML. If you're new to HTML, you may want to check out the HTML Introduction Tutorial before proceeding.

## Writing CSS

CSS is written in the form of rules, where each rule defines how a specific HTML element should be styled. A rule consists of a selector and a set of properties and values.

**Syntax:**
```
selector {
    property1: value1;
    property2: value2;
    /* Add more properties and values as needed */
}
```

- **Selector:** The selector is an HTML element to which you want to apply styles. It can be a tag name (e.g., `p`, `h1`, `div`), a class (e.g., `.my-class`), or an ID (e.g., `#my-id`). The selector tells the browser which HTML elements the rule applies to.

- **Properties and Values:** Inside the curly braces, you define one or more properties and their corresponding values. Each property represents a style attribute (e.g., `color`, `font-size`, `margin`) that you want to change, and the value specifies the new setting for that attribute.

## Hello World Example

Let's create a simple "Hello, World!" example using HTML and CSS.

**HTML:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello, World!</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Hello, World!</h1>
</body>
</html>
```

**CSS (styles.css):**
```
h1 {
    color: blue;
    font-size: 24px;
}
```

In this example, we have an HTML file with a single `h1` heading element. We link our external CSS file (`styles.css`) in the `head` section of the HTML. In the CSS file, we apply two styles to the `h1` element: set the text color to blue and increase the font size to 24 pixels.

Save the HTML and CSS code in separate files in the same folder and open the HTML file in a web browser. You should see a blue "Hello, World!" heading with an increased font size.

## Additional Resources

1. [MDN Web Docs - CSS Introduction](https://developer.mozilla.org/en-US/docs/Web/CSS/): This comprehensive guide by MDN provides an in-depth introduction to CSS, covering everything from basic concepts to advanced topics.

2. [W3Schools CSS Tutorial](https://www.w3schools.com/css/): W3Schools offers a beginner-friendly CSS tutorial with live examples and an interactive editor, making it easy to experiment with CSS code.