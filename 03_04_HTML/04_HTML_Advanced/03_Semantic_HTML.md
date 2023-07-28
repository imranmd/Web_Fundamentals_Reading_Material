**Semantic HTML**

**Introduction:**

Semantic HTML is an approach to writing HTML code that focuses on the meaning and structure of content rather than just presentation. It involves using HTML elements that convey the purpose and significance of the content they enclose. Semantic HTML not only improves the accessibility and search engine optimization (SEO) of a webpage but also makes the code more readable and maintainable.

![URL](../../Assets/SemanticHTML.png) 

**Why We Need Semantic HTML:**

Semantic HTML is essential for several reasons:

1. **Accessibility:** By using semantic elements, assistive technologies like screen readers can better understand the content, making the webpage more accessible to people with disabilities.

2. **SEO (Search Engine Optimization):** Search engines give higher importance to semantic HTML, which can improve the webpage's ranking in search results.

3. **Readability and Maintainability:** Semantic HTML makes the code easier to read and understand for developers, making it simpler to maintain and collaborate on projects.

**Example: Non-Semantic HTML (DIV Soup):**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Non-Semantic HTML (DIV Soup)</title>
</head>
<body>
  <div>
    <div>
      <h1>Welcome to Our Website</h1>
      <p>Here is some important information about us.</p>
      <div>
        <h2>About Us</h2>
        <p>We are a company that provides various services.</p>
      </div>
      <div>
        <h2>Contact Us</h2>
        <p>You can reach us through email or phone.</p>
      </div>
    </div>
  </div>
</body>
</html>
```

**Converting to Semantic HTML:**

In the above example, we can replace the `<div>` elements with more meaningful semantic elements.

**Example: Semantic HTML**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Semantic HTML Example</title>
</head>
<body>
  <header>
    <h1>Welcome to Our Website</h1>
    <p>Here is some important information about us.</p>
  </header>
  <main>
    <section>
      <h2>About Us</h2>
      <p>We are a company that provides various services.</p>
    </section>
    <section>
      <h2>Contact Us</h2>
      <p>You can reach us through email or phone.</p>
    </section>
  </main>
</body>
</html>
```

**List of All Semantic Elements:**

- `<header>`: Represents the header of a section or page.
- `<nav>`: Represents a section containing navigation links.
- `<main>`: Represents the main content of the page.
- `<article>`: Represents a self-contained article or piece of content.
- `<section>`: Represents a generic section of content.
- `<aside>`: Represents content that is tangentially related to the content around it.
- `<footer>`: Represents the footer of a section or page.
- `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`: Represents headings of different levels.
- `<p>`: Represents a paragraph of text.
- `<ul>`: Represents an unordered list.
- `<ol>`: Represents an ordered list.
- `<li>`: Represents a list item.
- `<a>`: Represents a hyperlink.
- `<img>`: Represents an image.

**Summary:**

Using semantic HTML is a best practice for writing meaningful and accessible webpages. By employing semantic elements like `<header>`, `<main>`, `<section>`, and others, we can enhance the structure and readability of our HTML code. Remember to choose the appropriate semantic elements that best describe the content and purpose of each section on your webpage. Happy coding!