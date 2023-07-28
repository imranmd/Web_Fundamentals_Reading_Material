# CSS Alignment Tutorial

## Introduction to CSS Alignment

CSS Alignment refers to the process of positioning and aligning elements within their parent containers. It allows you to control how elements are distributed, spaced, and centered both horizontally and vertically. Proper alignment enhances the visual appearance and readability of your web page.


## CSS Alignment Properties

There are several CSS properties that enable you to align elements:

### 1. Horizontal Alignment - `text-align`

The `text-align` property is used to horizontally align text within a block-level element. It also affects inline elements inside that block-level element.

**Syntax:**
```
selector {
    text-align: left | right | center | justify;
}
```

### Working Demo

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Alignment Demo</title>
    <style>
        .container {
            width: 300px;
            border: 1px solid black;
            padding: 20px;
        }

        .left {
            text-align: left;
        }

        .right {
            text-align: right;
        }

        .center {
            text-align: center;
        }

        .justify {
            text-align: justify;
        }
    </style>
</head>
<body>
    <div class="container left">
        This text is aligned to the left.
    </div>

    <div class="container right">
        This text is aligned to the right.
    </div>

    <div class="container center">
        This text is centered.
    </div>

    <div class="container justify">
        This text is justified, meaning it spreads across the entire width of the container, except for the last line.
    </div>
</body>
</html>
```

In this example, we have a `.container` div with different alignment classes. The text inside each container is aligned differently based on the `text-align` property.

### Explanation:

- `.left`: The text is aligned to the left, and it starts at the left edge of the container.

- `.right`: The text is aligned to the right, and it starts at the right edge of the container.

- `.center`: The text is centered horizontally within the container.

- `.justify`: The text is justified, meaning it spreads across the entire width of the container, except for the last line.

### 2. Vertical Alignment - `vertical-align`

The `vertical-align` property is used to vertically align inline-level and table-cell elements within their parent containers.

**Syntax:**
```
selector {
    vertical-align: baseline | sub | super | top | text-top | middle | bottom | text-bottom;
}
```

### Working Demo

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Alignment Demo</title>
    <style>
        .container {
            height: 150px;
            display: table-cell;
            vertical-align: middle;
            border: 1px solid black;
        }
    </style>
</head>
<body>
    <div class="container">
        This text is vertically centered.
    </div>
</body>
</html>
```

In this example, we have a `.container` div with `display: table-cell` and `vertical-align: middle`. This will vertically center the text within the container.

### Explanation:

- `vertical-align: middle`: The text is vertically centered within the container.

## Example Usage
Sure, here's an example of an HTML code snippet that demonstrates various CSS alignment properties along with comments to explain each part:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Alignment Properties Example</title>
    <style>
        /* Center the container horizontally and vertically within the viewport */
        body {
            height: 100vh; /* Set the body height to the full viewport height */
            display: flex; /* Use flexbox to center the container */
            justify-content: center; /* Center the container horizontally */
            align-items: center; /* Center the container vertically */
            margin: 0; /* Remove default body margin */
        }

        /* Basic container styles */
        .container {
            width: 300px;
            height: 200px;
            background-color: lightblue;
            border: 1px solid darkblue;
        }

        /* Center the content horizontally and vertically within the container */
        .centered-content {
            display: flex; /* Use flexbox to center the content */
            justify-content: center; /* Center the content horizontally */
            align-items: center; /* Center the content vertically */
            height: 100%; /* Occupy the full height of the container */
        }

        /* Align content to the left */
        .align-left {
            text-align: left; /* Align the text to the left */
        }

        /* Align content to the right */
        .align-right {
            text-align: right; /* Align the text to the right */
        }

        /* Justify content */
        .justify-content {
            text-align: justify; /* Justify the text */
        }
    </style>
</head>
<body>
    <!-- Centered container -->
    <div class="container">
        <div class="centered-content">
            <p>This content is centered both horizontally and vertically.</p>
        </div>
    </div>

    <!-- Left-aligned container -->
    <div class="container align-left">
        <div class="centered-content">
            <p>This content is aligned to the left.</p>
        </div>
    </div>

    <!-- Right-aligned container -->
    <div class="container align-right">
        <div class="centered-content">
            <p>This content is aligned to the right.</p>
        </div>
    </div>

    <!-- Justified content container -->
    <div class="container justify-content">
        <div class="centered-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur id scelerisque velit.</p>
        </div>
    </div>
</body>
</html>
```

In this example, we use CSS to demonstrate four alignment properties:

1. `justify-content: center;`: Horizontally centers the container within the viewport.
2. `align-items: center;`: Vertically centers the container within the viewport.
3. `text-align: left;`: Aligns the content within the container to the left.
4. `text-align: right;`: Aligns the content within the container to the right.
5. `text-align: justify;`: Justifies the text within the container.

The example uses a flexbox layout to achieve most of the alignments. The different containers demonstrate different alignment behaviors for their content.
## Summary

CSS Alignment properties play a crucial role in positioning and aligning elements on your web page. By using `text-align` for horizontal alignment and `vertical-align` for vertical alignment, you can achieve visually appealing and well-structured layouts.

## Additional Resources

1. [MDN Web Docs - CSS Layout - Alignment](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Layout/Alignment): This resource from MDN provides detailed explanations and examples of CSS Alignment.

2. [W3Schools - CSS Alignment](https://www.w3schools.com/css/css_align.asp): W3Schools offers a comprehensive guide on CSS Alignment, along with interactive examples and exercises to practice your understanding.