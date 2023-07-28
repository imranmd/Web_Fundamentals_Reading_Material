# CSS Font and Properties Tutorial

## Introduction to CSS Font

The CSS `font` property is used to control the font-related properties of text within an element. It allows you to specify the font family, size, weight, style, and more.


## CSS Font Properties

There are several properties related to the CSS `font` property. Let's explore each of them in detail and provide working examples for better understanding:

### 1. Font Family

The `font-family` property sets the font family for text within an element. It allows you to specify multiple font families in order of priority.

**Syntax:**
```
selector {
    font-family: font-family-name, fallback-font, sans-serif;
}
```

**Example:**
```
p {
    font-family: "Helvetica Neue", Arial, sans-serif;
}
```

In this example, the text inside `<p>` elements will use the font "Helvetica Neue" if available, otherwise, it will fall back to Arial, and finally, to a generic sans-serif font.

### 2. Font Size

The `font-size` property sets the size of the text.

**Syntax:**
```
selector {
    font-size: size;
}
```

**Example:**
```
h1 {
    font-size: 36px;
}
```

In this example, the text inside `<h1>` elements will have a font size of 36 pixels.

### 3. Font Weight

The `font-weight` property sets the thickness of the text.

**Syntax:**
```
selector {
    font-weight: normal | bold | bolder | lighter | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
}
```

**Example:**
```
strong {
    font-weight: bold;
}
```

In this example, the text inside `<strong>` elements will have a bold font weight.

### 4. Font Style

The `font-style` property sets the style of the text, such as italic or normal.

**Syntax:**
```
selector {
    font-style: normal | italic | oblique;
}
```

**Example:**
```
em {
    font-style: italic;
}
```

In this example, the text inside `<em>` elements will be italicized.

### 5. Font Variant

The `font-variant` property sets whether the text should be displayed in small-caps.

**Syntax:**
```
selector {
    font-variant: normal | small-caps;
}
```

**Example:**
```
span {
    font-variant: small-caps;
}
```

In this example, the text inside `<span>` elements will be displayed in small caps.

### 6. Text Decoration

The `text-decoration` property sets the decoration of the text, such as underline, overline, or line-through.

**Syntax:**
```
selector {
    text-decoration: none | underline | overline | line-through;
}
```

**Example:**
```
a {
    text-decoration: underline;
}
```

In this example, the text inside `<a>` elements will be underlined.

## Example Usage
 Below is an HTML code snippet that demonstrates various CSS font properties, with comments explaining each property:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Font Properties</title>
    <style>
        /* Add some basic styles for demonstration purposes */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .box {
            border: 2px solid #333;
            margin: 20px;
            padding: 20px;
        }
    </style>
</head>
<body>
    <!-- Demonstrating various CSS Font Properties -->

    <!-- Font Family -->
    <div class="box" style="font-family: 'Arial', sans-serif;">
        Font Family: Arial, sans-serif
    </div>

    <!-- Font Size -->
    <div class="box" style="font-size: 20px;">
        Font Size: 20px
    </div>

    <!-- Font Weight -->
    <div class="box" style="font-weight: bold;">
        Font Weight: Bold
    </div>

    <!-- Font Style (Italic) -->
    <div class="box" style="font-style: italic;">
        Font Style: Italic
    </div>

    <!-- Text Decoration (Underline) -->
    <div class="box" style="text-decoration: underline;">
        Text Decoration: Underline
    </div>

    <!-- Text Decoration (Line-through) -->
    <div class="box" style="text-decoration: line-through;">
        Text Decoration: Line-through
    </div>

    <!-- Text Decoration (Overline) -->
    <div class="box" style="text-decoration: overline;">
        Text Decoration: Overline
    </div>

    <!-- Text Transform (Uppercase) -->
    <div class="box" style="text-transform: uppercase;">
        Text Transform: Uppercase
    </div>

    <!-- Text Transform (Lowercase) -->
    <div class="box" style="text-transform: lowercase;">
        Text Transform: Lowercase
    </div>

    <!-- Text Transform (Capitalize) -->
    <div class="box" style="text-transform: capitalize;">
        Text Transform: Capitalize
    </div>

    <!-- Text Align (Center) -->
    <div class="box" style="text-align: center;">
        Text Align: Center
    </div>

    <!-- Text Align (Right) -->
    <div class="box" style="text-align: right;">
        Text Align: Right
    </div>

    <!-- Text Align (Justify) -->
    <div class="box" style="text-align: justify;">
        Text Align: Justify
    </div>

    <!-- Line Height -->
    <div class="box" style="line-height: 1.5;">
        Line Height: 1.5
    </div>

    <!-- Letter Spacing -->
    <div class="box" style="letter-spacing: 2px;">
        Letter Spacing: 2px
    </div>

    <!-- Word Spacing -->
    <div class="box" style="word-spacing: 4px;">
        Word Spacing: 4px
    </div>

    <!-- Text Indent -->
    <div class="box" style="text-indent: 30px;">
        Text Indent: 30px
    </div>

    <!-- Font Variant (Small Caps) -->
    <div class="box" style="font-variant: small-caps;">
        Font Variant: Small Caps
    </div>

</body>
</html>
```

Explanation:
- The `box` class sets some basic styles for the demonstration purposes, including border, margin, and padding.
- Each div demonstrates a different CSS font property and its behavior.

When you run this HTML code, you will see each box demonstrating different CSS font properties, making it easier to understand how they affect the appearance of text on a web page.
## Summary

The CSS Font and its properties allow you to customize the appearance of text within your web page. By setting the font family, size, weight, style, variant, and text decoration, you can create visually appealing and well-styled content.

## Additional Resources

1. [MDN Web Docs - CSS Fonts](https://developer.mozilla.org/en-US/docs/Web/CSS/font): This resource from MDN provides detailed explanations and examples of CSS Font properties.

2. [W3Schools - CSS Fonts](https://www.w3schools.com/css/css_font.asp): W3Schools offers a comprehensive guide on CSS Fonts, along with interactive examples and exercises to practice your understanding.