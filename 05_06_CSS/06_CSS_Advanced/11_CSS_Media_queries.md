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

## Example Usage
 Below is an example of an HTML code snippet that demonstrates the use of CSS media queries along with comments to explain each part:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Media Queries Example</title>
    <style>
        /* Default styles for all screen sizes */
        body {
            font-size: 16px;
            background-color: lightgray;
        }

        /* Media query for screens with a maximum width of 600 pixels */
        @media (max-width: 600px) {
            body {
                font-size: 14px; /* Reduce font size for smaller screens */
                background-color: lightblue; /* Change background color for smaller screens */
            }
        }

        /* Media query for screens with a minimum width of 1200 pixels */
        @media (min-width: 1200px) {
            body {
                font-size: 20px; /* Increase font size for larger screens */
                background-color: lightgreen; /* Change background color for larger screens */
            }
        }
    </style>
</head>
<body>
    <h1>Responsive Design with CSS Media Queries</h1>
    <p>This is some text that will adjust based on the screen size.</p>
</body>
</html>
```

In this example:

1. `body`: This defines the default styles for the `<body>` element, setting the font size to 16 pixels and the background color to light gray.

2. `@media (max-width: 600px)`: This media query targets screens with a maximum width of 600 pixels. Inside this media query, we override the default styles for the `<body>` element, reducing the font size to 14 pixels, and changing the background color to light blue for smaller screens.

3. `@media (min-width: 1200px)`: This media query targets screens with a minimum width of 1200 pixels. Inside this media query, we override the default styles for the `<body>` element, increasing the font size to 20 pixels, and changing the background color to light green for larger screens.

When you resize your browser window, the text size and background color will change based on the screen size. The comments in the HTML and CSS code explain the purpose of each part and its contribution to creating responsive design with CSS media queries.
## Summary

CSS Media Queries are a powerful tool for creating responsive web designs that adapt to various devices and screen sizes. By using media queries, you can target specific device characteristics and apply different styles to enhance the user experience on different devices.

## Additional Resources

1. [MDN Web Docs - Using media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries): This resource from MDN provides detailed explanations and examples of using media queries in CSS.

2. [CSS-Tricks - A Comprehensive Guide to CSS Media Queries](https://css-tricks.com/a-complete-guide-to-css-media-queries/): This CSS-Tricks guide covers various aspects of CSS media queries with practical examples and use cases to help you create responsive designs effectively.