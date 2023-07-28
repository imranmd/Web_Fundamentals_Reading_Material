**HTML Favicon**

**Introduction:**

In HTML, a favicon (short for "favorite icon") is a small, iconic image that appears in the browser's tab or bookmark bar when a user visits a website. Favicons help users quickly identify and distinguish different websites when multiple tabs are open. In this tutorial documentation, we will learn about the HTML favicon, its purpose, syntax, and how to add it to a webpage.

**Understanding HTML Favicon:**

The favicon is typically a square image with a size of 16x16 pixels or 32x32 pixels and is saved in ICO (icon) format. It is placed in the root directory of a website and linked using the HTML `<link>` tag. Modern browsers automatically fetch and display the favicon when a user visits the webpage.

**Syntax for Adding Favicon:**

To add a favicon to your HTML document, you need to use the `<link>` tag in the `<head>` section. The `rel` attribute is set to "icon" or "shortcut icon," and the `href` attribute contains the path to the favicon image.

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Favicon Example</title>
  <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
  <!-- Content of the webpage goes here -->
</body>
</html>
```

**Working Example:**

Let's create a simple working example to demonstrate how to add a favicon to a webpage.

1. Create a 16x16 pixels favicon.ico image and save it in the root directory of your website.

2. Use the following HTML code in the `<head>` section of your HTML document:

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Favicon Example</title>
  <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a sample webpage with a favicon.</p>
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - Favicon: https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/favicon
2. W3Schools - HTML Favicons: https://www.w3schools.com/tags/att_link_rel.asp

**Summary:**

The HTML favicon is a small, iconic image that appears in the browser's tab or bookmark bar when a user visits a website. It helps users quickly identify and distinguish different websites. By using the `<link>` tag with the appropriate `rel` and `href` attributes, you can easily add a favicon to your HTML document. Make sure to use a square favicon image in ICO format for best results. Happy branding!