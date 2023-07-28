**HTML Introduction and Page Structure**

**Introduction:**

HTML (Hypertext Markup Language) is the foundational language of the World Wide Web. It allows web developers to create the structure and content of web pages, making them readable and interactive. In this tutorial documentation, we will provide a simple and beginner-friendly introduction to HTML and explain the basic structure of an HTML page.

![URL](../../Assets/HTML-5-now.gif) 

**What is HTML?**

HTML is a markup language used to create the structure and content of web pages. It uses a system of tags and elements to mark up different parts of the content, such as headings, paragraphs, images, and links. These tags tell web browsers how to display the content, making it visually appealing and easily accessible.

**Basic HTML Page Structure:**

An HTML document is a file containing HTML code. Every HTML page has a basic structure that consists of several essential elements. Let's explore these elements step by step:

**1. Document Type Declaration:**
   Every HTML page should begin with a document type declaration, which tells the browser what type of HTML version is being used. For HTML5, the declaration is as follows:

   ```html
   <!DOCTYPE html>
   ```

**2. HTML Element:**
   The `<html>` element is the root element of an HTML document. It encloses all other elements on the page.

   ```html
   <html>
     <!-- Other elements go here -->
   </html>
   ```

**3. Head Element:**
   The `<head>` element contains meta-information about the HTML document, such as the page title, character encoding, and links to external resources.

   ```html
   <head>
     <!-- Meta-information and links go here -->
   </head>
   ```

**4. Title Element:**
   The `<title>` element sets the title of the webpage, which appears in the browser's title bar or tab.

   ```html
   <title>My Webpage</title>
   ```

**5. Body Element:**
   The `<body>` element contains the visible content of the webpage, including text, images, links, and other elements.

   ```html
   <body>
     <!-- Content goes here -->
   </body>
   ```

**Basic HTML Tags:**

HTML tags are used to define different elements and content on the webpage. Here are some common HTML tags:

- **Headings:**
  HTML provides six levels of headings, from `<h1>` (highest level) to `<h6>` (lowest level).

  ```html
  <h1>This is the Main Heading</h1>
  <h2>This is a Subheading</h2>
  ```

- **Paragraphs:**
  The `<p>` tag is used to define paragraphs of text.

  ```html
  <p>This is a paragraph of text.</p>
  ```

- **Images:**
  The `<img>` tag is used to embed images in the webpage.

  ```html
  <img src="image.jpg" alt="Image Description">
  ```

- **Links:**
  The `<a>` tag creates hyperlinks to other web pages or resources.

  ```html
  <a href="https://www.example.com">Visit Example Website</a>
  ```

**Creating a Simple HTML Page:**

Let's create a simple HTML page that includes headings, paragraphs, an image, and a link:

```html
<!DOCTYPE html>
<html>
<head>
  <title>My First Webpage</title>
</head>
<body>

  <h1>Welcome to My First Webpage</h1>
  <p>This is the first paragraph of my webpage.</p>
  <img src="image.jpg" alt="Image Description">
  <p>Here is a link to <a href="https://www.example.com">Example Website</a>.</p>

</body>
</html>
```

**Summary:**

HTML is the building block of web development, allowing you to create structured and interactive web pages. By understanding HTML's basic syntax and using its elements and tags, you can start creating simple web pages and eventually advance to more complex websites. Combine HTML with CSS and JavaScript to add styling and interactivity to your web pages. Keep practicing and exploring to become a proficient web developer. Happy coding!