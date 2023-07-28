# CSS Media Queries Tutorial

## Introduction to CSS Media Queries

CSS Media Queries allow you to apply different styles to your web page based on the characteristics of the user's device or viewport. With media queries, you can create responsive designs that adapt to various screen sizes and devices, providing an optimal user experience on desktops, tablets, and smartphones. In this tutorial, we will explore the basics of CSS Media Queries and how to use them in your web designs.


## Understanding CSS Media Queries

Media queries allow you to specify different CSS styles based on certain conditions, such as screen width, device orientation, resolution, and more. When the condition specified in a media query matches the user's device or viewport, the associated styles are applied.

## Types of CSS Media Queries

There are several types of CSS Media Queries, allowing you to target specific device characteristics. Some common types of media queries are:

### 1. Screen Width

**Demo:**
```css
/* Apply styles when the screen width is 600 pixels or less */
@media (max-width: 600px) {
    body {
        font-size: 14px;
    }
}
```

**Explanation:**
In this example, we use a media query to apply the `font-size: 14px;` to the `body` element when the screen width is 600 pixels or less. This makes the text size smaller on smaller screens.

### 2. Device Orientation

**Demo:**
```css
/* Apply styles when the device is in landscape orientation */
@media (orientation: landscape) {
    header {
        display: none;
    }
}
```

**Explanation:**
In this example, we use a media query to hide the `header` element when the device is in landscape orientation. This can be helpful when you want to display different elements for portrait and landscape views.

### 3. Resolution

**Demo:**
```css
/* Apply styles when the device has a resolution of 2dppx or higher */
@media (min-resolution: 2dppx) {
    .high-res-image {
        background-image: url('image@2x.png');
    }
}
```

**Explanation:**
In this example, we use a media query to load a high-resolution image (`image@2x.png`) for devices with a resolution of 2 dots per pixel (2dppx) or higher. This ensures that high-resolution devices get a sharper image.

## Applying Media Queries

Media queries are written using the `@media` rule, followed by the condition in parentheses and the CSS styles inside the curly braces.

**Demo:**
```css
/* Apply styles when the screen width is 768 pixels or less */
@media (max-width: 768px) {
    .menu {
        display: none;
    }
}
```

**Explanation:**
In this example, we use a media query to hide the `.menu` element when the screen width is 768 pixels or less. This is useful for creating a mobile-friendly menu that disappears on smaller screens.

## Example Usage:
 Here's an example of an HTML code snippet that demonstrates the use of CSS variables (also known as CSS custom properties) along with comments to explain each part:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Variables (Custom Properties) Example</title>
    <style>
        /* Define CSS variables */
        :root {
            --primary-color: blue; /* Define a variable for primary color */
            --secondary-color: green; /* Define a variable for secondary color */
            --font-size: 16px; /* Define a variable for font size */
        }

        /* Use CSS variables */
        .custom-styles {
            color: var(--primary-color); /* Use the primary color variable for text color */
            background-color: var(--secondary-color); /* Use the secondary color variable for background color */
            font-size: var(--font-size); /* Use the font size variable */
        }
    </style>
</head>
<body>
    <!-- Element with custom styles using CSS variables -->
    <div class="custom-styles">
        <p>This text uses custom CSS variables for color and font size.</p>
    </div>
</body>
</html>
```

In this example:

1. `:root`: This is a pseudo-class that targets the root element of the document (in this case, the `<html>` element). Inside `:root`, we define CSS variables using the `--variable-name: value` syntax. Here, we define three variables: `--primary-color`, `--secondary-color`, and `--font-size`.

2. `.custom-styles`: This class is applied to an HTML element (in this case, a `<div>` element). We use the `var()` function to use the CSS variables defined in `:root`. The `var()` function allows us to reference the value of a CSS variable. In this example, we use the `--primary-color` variable for text color, `--secondary-color` for background color, and `--font-size` for the font size.

By using CSS variables, we can easily change the appearance of elements across the entire document by modifying the variable values defined in `:root`. This allows for more consistent and maintainable styles.

The comments in the HTML and CSS code explain the purpose of each part and its contribution to creating and using CSS variables.
## Summary

CSS Media Queries are a powerful tool for creating responsive web designs that adapt to various devices and screen sizes. By using media queries, you can target specific device characteristics and apply different styles to enhance the user experience on different devices.

## Additional Resources

1. [MDN Web Docs - Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries): This resource from MDN provides detailed explanations and examples of using media queries in CSS.

2. [CSS-Tricks - A Comprehensive Guide to CSS Media Queries](https://css-tricks.com/a-complete-guide-to-css-media-queries/): This CSS-Tricks guide covers various aspects of CSS media queries with practical examples and use cases to help you create responsive designs effectively.