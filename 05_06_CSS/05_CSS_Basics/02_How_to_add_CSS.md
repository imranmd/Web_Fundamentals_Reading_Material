# How to Add CSS to Your HTML Document

## Introduction

CSS (Cascading Style Sheets) is used to style and format the content of your HTML documents. It allows you to control the appearance of elements, such as fonts, colors, margins, and layout. There are three ways to add CSS to an HTML document: inline, internal, and external. In this tutorial, we'll explore each method and provide examples to help you understand how to use CSS effectively.


## 1. Inline CSS

Inline CSS is added directly to an HTML element using the `style` attribute. This method is suitable for applying styles to a single element.

**Syntax:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Inline CSS Example</title>
</head>
<body>
    <h1 style="color: blue; font-size: 24px;">Hello, World!</h1>
</body>
</html>
```

In the example above, the `h1` element has inline CSS added to it, setting the text color to blue and the font size to 24 pixels.

## 2. Internal CSS

Internal CSS is placed within the `style` element in the `head` section of your HTML document. This method is useful when you want to apply styles to multiple elements within the same document.

**Syntax:**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Internal CSS Example</title>
    <style>
        h1 {
            color: blue;
            font-size: 24px;
        }
    </style>
</head>
<body>
    <h1>Hello, World!</h1>
</body>
</html>
```

In this example, the `style` element contains CSS rules targeting the `h1` element, setting the text color to blue and the font size to 24 pixels.

## 3. External CSS

External CSS is stored in a separate `.css` file and linked to your HTML document using the `link` element. This method is ideal for applying styles across multiple HTML documents, making it easier to maintain and update your styles.

**HTML (index.html):**
```html
<!DOCTYPE html>
<html>
<head>
    <title>External CSS Example</title>
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

In this example, we have an HTML file named `index.html`, and the CSS rules are stored in a separate file named `styles.css`. The `link` element in the `head` section links the HTML file to the CSS file, applying the defined styles to the `h1` element.

