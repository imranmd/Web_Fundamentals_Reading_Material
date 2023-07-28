# CSS Pseudo-elements Tutorial

## Introduction to CSS Pseudo-elements

CSS Pseudo-elements are special selectors that target specific parts of an element, allowing you to style them independently. Pseudo-elements provide a way to add decorative or stylistic elements to your content without the need for extra HTML markup. In this tutorial, we'll explore six types of CSS Pseudo-elements and provide working examples to help you understand their usage.



## Types of CSS Pseudo-elements

### 1. ::before

The `::before` pseudo-element allows you to insert content before the content of an element.

**Syntax:**
```
selector::before {
    /* styles go here */
}
```

**Example:**
```
/* Add a double quotation mark before every <blockquote> element */
blockquote::before {
    content: '"';
}
```

In this example, the `::before` pseudo-element adds a double quotation mark before the content of every `<blockquote>` element.

### 2. ::after

The `::after` pseudo-element allows you to insert content after the content of an element.

**Syntax:**
```
selector::after {
    /* styles go here */
}
```

**Example:**
```
/* Add " - The End" after every <h1> element */
h1::after {
    content: ' - The End';
}
```

In this example, the `::after` pseudo-element adds " - The End" after the content of every `<h1>` element.

### 3. ::first-line

The `::first-line` pseudo-element targets the first line of text within an element.

**Syntax:**
```
selector::first-line {
    /* styles go here */
}
```

**Example:**
```
/* Apply bold font weight to the first line of every <p> element */
p::first-line {
    font-weight: bold;
}
```

In this example, the `::first-line` pseudo-element applies a bold font weight to the first line of every `<p>` element.

### 4. ::first-letter

The `::first-letter` pseudo-element targets the first letter of text within an element.

**Syntax:**
```
selector::first-letter {
    /* styles go here */
}
```

**Example:**
```
/* Apply a larger font size and color to the first letter of every <h2> element */
h2::first-letter {
    font-size: 1.5em;
    color: red;
}
```

In this example, the `::first-letter` pseudo-element increases the font size and changes the color of the first letter in every `<h2>` element.

### 5. ::selection

The `::selection` pseudo-element targets the portion of text that is selected by the user.

**Syntax:**
```
::selection {
    /* styles go here */
}
```

**Example:**
```
/* Change the background color of selected text to yellow and the text color to black */
::selection {
    background-color: yellow;
    color: black;
}
```

In this example, the `::selection` pseudo-element changes the background color of selected text to yellow and the text color to black.

### 6. ::placeholder

The `::placeholder` pseudo-element targets the placeholder text in an input field.

**Syntax:**
```
input::placeholder {
    /* styles go here */
}
```

**Example:**
```
/* Change the color of the placeholder text to light gray */
input::placeholder {
    color: lightgray;
}
```

In this example, the `::placeholder` pseudo-element changes the color of the placeholder text in an input field to light gray.

## Example Usage
 Here's an HTML code snippet that demonstrates the usage of all types of pseudo-elements:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Pseudo-Elements</title>
    <style>
        /* Pseudo-element ::before */
        p::before {
            content: "Before content - ";
            font-weight: bold;
            color: red;
        }

        /* Pseudo-element ::after */
        p::after {
            content: " - After content";
            font-weight: bold;
            color: blue;
        }

        /* Pseudo-element ::first-line */
        .first-line::first-line {
            text-transform: uppercase;
        }

        /* Pseudo-element ::first-letter */
        .first-letter::first-letter {
            font-size: 2rem;
            color: purple;
        }

        /* Pseudo-element ::selection */
        p::selection {
            background-color: yellow;
            color: black;
        }
    </style>
</head>
<body>
    <p>This is a paragraph with pseudo-elements demonstration.</p>
    <p class="first-line">This is another paragraph to demonstrate ::first-line pseudo-element.</p>
    <p class="first-letter">And this one to demonstrate ::first-letter pseudo-element.</p>
    <p>Select some text in this paragraph to demonstrate ::selection pseudo-element.</p>
</body>
</html>
```

Explanation:
- The `::before` pseudo-element is used to insert content before the content of the `<p>` element and style it with a red color and bold text.
- The `::after` pseudo-element is used to insert content after the content of the `<p>` element and style it with a blue color and bold text.
- The `::first-line` pseudo-element is used to style the first line of the paragraph with uppercase text.
- The `::first-letter` pseudo-element is used to style the first letter of the paragraph with a larger font size and purple color.
- The `::selection` pseudo-element is used to style the selected text within the paragraph with a yellow background and black text color.

When you run this HTML code, you will see the various pseudo-elements in action, each demonstrating its specific behavior.
## Summary

CSS Pseudo-elements allow you to target specific parts of an element and style them independently. By using `::before`, `::after`, `::first-line`, `::first-letter`, `::selection`, and `::placeholder`, you can add decorative elements and enhance the visual appearance of your web pages.

## Additional Resources

1. [MDN Web Docs - Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements): This resource from MDN provides detailed explanations and examples of CSS Pseudo-elements.

2. [CSS-Tricks - Pseudo-elements](https://css-tricks.com/almanac/selectors/a/after-and-before/): CSS-Tricks offers a comprehensive guide on Pseudo-elements, covering various use cases and creative styling techniques.