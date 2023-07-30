# CSS Selectors Tutorial

## Introduction to CSS Selectors

CSS selectors are patterns used to select and apply styles to specific HTML elements. They allow you to target elements based on their attributes, types, classes, and relationships with other elements. Understanding CSS selectors is crucial for customizing the appearance of your web pages effectively.
![Data Types](../../Assets/CSS-Selectors.png)

## 1. Type Selector

The type selector selects elements based on their HTML tag name.

**Syntax:**
```
tagname {
    /* styles go here */
}
```

**Example:**
```
p {
    color: blue;
}
```

In this example, the type selector `p` selects all `<p>` elements and sets their text color to blue.

## 2. Class Selector

The class selector selects elements with a specific class attribute.

**Syntax:**
```
.classname {
    /* styles go here */
}
```

**Example:**
```
.highlight {
    background-color: yellow;
}
```

In this example, the class selector `.highlight` selects all elements with the `class="highlight"` attribute and sets their background color to yellow.

**HTML (sample.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Class Selector Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <p class="highlight">This paragraph has a yellow background.</p>
    <p>This paragraph does not have the 'highlight' class.</p>
</body>
</html>
```

## 3. ID Selector

The ID selector selects a single element with a unique ID attribute.

**Syntax:**
```
#idname {
    /* styles go here */
}
```

**Example:**
```
#header {
    font-size: 28px;
    font-weight: bold;
}
```

In this example, the ID selector `#header` selects the element with `id="header"` and makes the text larger and bold.

**HTML (sample.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>ID Selector Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1 id="header">This is a header with an ID.</h1>
    <p>This paragraph does not have an ID.</p>
</body>
</html>
```

## 4. Descendant Selector

The descendant selector selects elements that are descendants of a specific parent element.

**Syntax:**
```
parent descendant {
    /* styles go here */
}
```

**Example:**
```
ul li {
    list-style-type: square;
}
```

In this example, the descendant selector `ul li` selects all `<li>` elements that are descendants of a `<ul>` (unordered list) element and sets their list style to squares.

**HTML (sample.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Descendant Selector Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
    </ul>
</body>
</html>
```

## 5. Child Selector

The child selector selects elements that are direct children of a specific parent element.

**Syntax:**
```
parent > child {
    /* styles go here */
}
```

**Example:**
```
ul > li {
    font-weight: bold;
}
```

In this example, the child selector `ul > li` selects all `<li>` elements that are direct children of a `<ul>` (unordered list) element and makes their text bold.

**HTML (sample.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Child Selector Demo</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
    </ul>
</body>
</html>
```

## Additional Resources

1. [MDN Web Docs - CSS Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors): This comprehensive guide by MDN covers various CSS selectors with detailed explanations and examples.

2. [CSS Tricks - CSS Selectors](https://css-tricks.com/how-css-selectors-work/): CSS Tricks provides an interactive guide on how CSS selectors work, allowing you to experiment and learn visually.