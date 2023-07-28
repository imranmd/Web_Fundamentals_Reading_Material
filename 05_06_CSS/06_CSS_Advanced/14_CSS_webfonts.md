# CSS Web Fonts Tutorial

## Introduction to CSS Web Fonts

CSS Web Fonts allow you to use custom fonts on your website, enabling you to create unique and visually appealing typography. By using web fonts, you can break away from the standard set of fonts installed on users' devices and enhance the overall look and feel of your web page. In this tutorial, we will explore different methods to use web fonts in CSS.


## Types of CSS Web Fonts

There are several ways to use web fonts in CSS:

### 1. Using Google Fonts

**Demo:**
```html
<!DOCTYPE html>
<html>
<head>
    <link href="https://fonts.googleapis.com/css2?family=Open+Sans&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Open Sans', sans-serif;
        }
    </style>
</head>
<body>
    <p>This is a paragraph with a custom Google Font.</p>
</body>
</html>
```

**Explanation:**
In this example, we use the Google Fonts API to import the 'Open Sans' font into our web page. We link to the Google Fonts stylesheet in the `<head>` section of the HTML document. Then, in the CSS, we set the `font-family` of the `body` to 'Open Sans', which applies the custom font to all text within the body.

### 2. Using Self-Hosted Fonts

**Demo:**
```css
@font-face {
    font-family: 'CustomFont';
    src: url('path/to/font.woff2') format('woff2'),
         url('path/to/font.woff') format('woff');
}

body {
    font-family: 'CustomFont', sans-serif;
}
```

**Explanation:**
In this example, we define a `@font-face` rule that specifies the font-family ('CustomFont') and the location of the font files in different formats (woff2 and woff). Then, in the CSS, we use `font-family: 'CustomFont'` to apply the self-hosted font to the body.

### 3. Using System Fonts

**Demo:**
```css
body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
```

**Explanation:**
In this example, we use a list of system fonts as the `font-family` property. The browser will use the first available font from the list, ensuring a consistent font rendering across different platforms and devices.

## Example Usage
 Here's an example of an HTML code snippet that demonstrates the use of CSS webfonts along with comments to explain each part:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Webfonts Example</title>
    <style>
        /* Import the Google Fonts stylesheet */
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

        /* Use the webfont */
        .custom-font-text {
            font-family: 'Roboto', sans-serif; /* Use the Roboto font family from Google Fonts or fallback to a sans-serif font */
        }
    </style>
</head>
<body>
    <!-- Text with the webfont -->
    <p class="custom-font-text">This text uses a webfont from Google Fonts.</p>
</body>
</html>
```

In this example:

1. `@import`: This CSS rule imports the Google Fonts stylesheet for the 'Roboto' font family. The `url()` function specifies the URL of the stylesheet provided by Google Fonts. The font weights specified are 400 (regular) and 700 (bold).

2. `.custom-font-text`: This class is applied to an HTML element (in this case, a `<p>` element). We use the `font-family` property to apply the 'Roboto' webfont to this text. If the 'Roboto' font is not available, the browser will fall back to a sans-serif font.

When using webfonts, you can import them from external sources like Google Fonts, Adobe Fonts, or other font providers. This allows you to use a wide variety of custom fonts on your website without requiring users to have the font installed on their local systems.

The comments in the HTML and CSS code explain the purpose of each part and its contribution to using webfonts with CSS.
## Summary

CSS Web Fonts provide a powerful way to add custom fonts to your web page, enhancing its visual appeal and typography. You can use Google Fonts, self-hosted fonts, or a combination of system fonts to create a unique and engaging reading experience for your users.

## Additional Resources

1. [MDN Web Docs - Web Fonts](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts): This resource from MDN provides detailed explanations and examples of CSS Web Fonts.

2. [Google Fonts](https://fonts.google.com/): Google Fonts offers a vast collection of free and easy-to-use web fonts that you can add to your web page.

3. [CSS-Tricks - Understanding Web Fonts and Getting Them To Work](https://css-tricks.com/snippets/css/using-font-face/): This CSS-Tricks article provides a comprehensive guide on using `@font-face` to load custom fonts and other tips related to web fonts.