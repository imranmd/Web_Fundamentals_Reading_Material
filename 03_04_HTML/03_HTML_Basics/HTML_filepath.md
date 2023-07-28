**HTML File Path**

**Introduction:**

In HTML, a file path is used to specify the location of external files, such as images, stylesheets, scripts, etc., that are linked to a webpage. Understanding file paths is essential for correctly referencing and including external resources in your HTML document. In this tutorial documentation, we will learn about different types of file paths, their syntax, and how to use them in HTML.

**Understanding HTML File Paths:**

There are three types of file paths used in HTML:

1. **Relative File Path:** A relative file path specifies the location of a file relative to the current webpage's location. It is typically used when the external file is in the same directory as the HTML document or in a subdirectory.

2. **Absolute File Path:** An absolute file path specifies the complete URL or file path from the root directory to the file. It is used when the external file is located at a specific URL or file path on the server.

3. **Root-Relative File Path:** A root-relative file path specifies the location of a file from the root directory of the website. It is used when the external file is located at a fixed position in the website's directory structure.

**Syntax for HTML File Paths:**

1. **Relative File Path:**
```html
<!-- File in the same directory -->
<img src="image.jpg" alt="Image">

<!-- File in a subdirectory -->
<img src="images/image.jpg" alt="Image">
```

2. **Absolute File Path:**
```html
<!-- Absolute URL -->
<img src="https://example.com/images/image.jpg" alt="Image">

<!-- Absolute file path -->
<img src="/root/images/image.jpg" alt="Image">
```

3. **Root-Relative File Path:**
```html
<!-- Root-relative file path -->
<img src="/images/image.jpg" alt="Image">
```

**Working Example:**

Let's create a working example to demonstrate how to use different types of file paths in HTML.

Assume you have the following directory structure:
```
- index.html
- images
  - image.jpg
```

**HTML Example:**
```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML File Path Example</title>
</head>
<body>
  <h1>File Path Example</h1>

  <!-- Relative File Path -->
  <img src="images/image.jpg" alt="Image">

  <!-- Absolute File Path -->
  <img src="/images/image.jpg" alt="Image">

  <!-- Root-Relative File Path -->
  <img src="/images/image.jpg" alt="Image">
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - HTML File Paths: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/Dealing_with_files
2. W3Schools - HTML File Paths: https://www.w3schools.com/html/html_filepaths.asp

**Summary:**

Understanding HTML file paths is crucial for correctly linking external files to your webpages. Relative file paths are used for files in the same or subdirectories, absolute file paths for specific URLs or file paths, and root-relative file paths for files at fixed positions in the website's directory structure. By using the appropriate file path, you can include images, stylesheets, scripts, and other external resources in your HTML document. Happy coding!