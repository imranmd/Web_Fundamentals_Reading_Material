# Templating in Express: A Comprehensive Guide

## What is a Template Engine?

A template engine is a tool or library that simplifies the process of generating dynamic HTML content in web applications. It allows you to create reusable HTML templates with placeholders for data and then fill in those placeholders with actual data when rendering a web page. This approach enables you to generate web pages dynamically, incorporating data from your server, databases, or other sources, without manually crafting HTML for each page.

## Why Use Template Engines in Express.js?

Express.js is a popular web framework for Node.js used to build web applications and APIs. When building web applications with Express, you often need to generate HTML content dynamically. This is where template engines come in handy. They provide the following benefits:

1. **Separation of Concerns**: Template engines encourage a clear separation between the logic of your application and the presentation layer (HTML). This separation makes your code more maintainable and easier to collaborate on with front-end developers.

2. **Reusability**: You can create reusable templates for common page elements (headers, footers, navigation bars) and use them across multiple pages, reducing duplication of code.

3. **Dynamic Data**: Template engines allow you to inject dynamic data into your HTML templates, making it easy to display user-specific information, product details, or any other data from your server.

4. **Consistency**: Templating ensures a consistent look and feel across your web application by using predefined templates and components.

## List of Different Template Engines for Express.js

Express.js supports various template engines, each with its own syntax and features. Here are some popular template engines you can use with Express:

1. **EJS (Embedded JavaScript)**:
   - Website: https://ejs.co/
   - Syntax: Uses `<% %>` and `<%= %>` to embed JavaScript code within HTML.

2. **Pug (formerly Jade)**:
   - Website: https://pugjs.org/
   - Syntax: Indentation-based, minimalistic, and concise syntax.

3. **Handlebars**:
   - Website: https://handlebarsjs.com/
   - Syntax: Uses `{{ }}` for placeholders and partials for reusing templates.

4. **Mustache**:
   - Website: https://mustache.github.io/
   - Syntax: Simple and logic-less, uses `{{ }}` for placeholders.

5. **Nunjucks**:
   - Website: https://mozilla.github.io/nunjucks/
   - Syntax: Jinja2-inspired, supports template inheritance and macros.


Choose the template engine that best suits your project's requirements and your team's familiarity with its syntax. Each template engine offers unique features and advantages, so it's essential to evaluate them based on your specific needs.

## Using Template Engines in Express.js

Express.js supports various template engines, such as EJS (Embedded JavaScript), Pug (formerly Jade), Handlebars, and more. In this guide, we'll use EJS as an example template engine in Express.

### Step 1: Install the Template Engine

Install the template engine you want to use as a dependency in your Express.js application. For EJS, you can run:

```
npm install ejs --save
```

### Step 2: Configure Express to Use the Template Engine

In your Express app, set the view engine to the chosen template engine. This tells Express to use the specified engine for rendering views. For EJS, add the following code to your `app.js` or main server file:

```javascript
const express = require('express');
const app = express();

// Set the view engine to EJS
app.set('view engine', 'ejs');

// ... Other middleware and routes
```

### Step 3: Create HTML Templates with the Template Engine Syntax

Create HTML templates using the chosen template engine's syntax. In EJS, you can embed JavaScript code within HTML using `<% %>` and `<%= %>` delimiters. For example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title><%= pageTitle %></title>
</head>
<body>
  <h1>Welcome to <%= pageTitle %></h1>
  <ul>
    <% for (const item of items) { %>
      <li><%= item %></li>
    <% } %>
  </ul>
</body>
</html>
```

### Step 4: Render Templates in Express Routes

In your Express route handlers, use the `res.render()` method to render templates and pass data to them. For example:

```javascript
app.get('/', (req, res) => {
  const pageTitle = 'Express EJS Example';
  const items = ['Item 1', 'Item 2', 'Item 3'];

  res.render('index', { pageTitle, items });
});
```

In this code, `res.render('index', { pageTitle, items })` renders the `index.ejs` template and injects the `pageTitle` and `items` variables into the template.

### Step 5: Create and Organize More Templates

As your application grows, create additional templates for different pages or components. Organize your templates in a folder (commonly named `views`) to keep your project structured.

## Conclusion

Using template engines in Express.js simplifies the process of generating dynamic HTML content for your web applications. Whether you choose EJS, Pug, Handlebars, or another template engine, they all offer similar benefits: clean separation of concerns, reusability, dynamic data rendering, and consistent styling. Experiment with different template engines to determine which one best fits your project's requirements and your personal preferences.