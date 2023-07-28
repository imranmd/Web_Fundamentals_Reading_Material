**HTML Tables**

**Introduction:**

HTML tables are used to organize data into rows and columns, making it easier to present structured information on a webpage. Tables are commonly used for displaying tabular data, such as pricing lists, schedules, and comparison charts. In this tutorial documentation, we will learn about creating HTML tables, their syntax, and how to use them to display data effectively.

**Understanding HTML Tables:**

HTML tables are created using the `<table>` element, which contains one or more rows represented by the `<tr>` (table row) element. Each row contains data cells represented by the `<td>` (table data) element for normal cells or the `<th>` (table header) element for header cells. `<th>` elements are used to create header rows at the beginning of the table.

**Syntax for HTML Tables:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Table Example</title>
</head>
<body>
  <table>
    <tr>
      <th>Heading 1</th>
      <th>Heading 2</th>
    </tr>
    <tr>
      <td>Data 1</td>
      <td>Data 2</td>
    </tr>
    <!-- Add more rows and cells as needed -->
  </table>
</body>
</html>
```

**Working Example:**

Let's create a working example to demonstrate how to create a simple HTML table.

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Table Example</title>
</head>
<body>
  <h1>Product Prices</h1>
  <table>
    <tr>
      <th>Product</th>
      <th>Price</th>
    </tr>
    <tr>
      <td>Product A</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>Product B</td>
      <td>$80</td>
    </tr>
    <tr>
      <td>Product C</td>
      <td>$120</td>
    </tr>
  </table>
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - HTML Tables: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table
2. W3Schools - HTML Tables: https://www.w3schools.com/html/html_tables.asp

**Summary:**

HTML tables are a useful way to organize and display tabular data on a webpage. By using the `<table>`, `<tr>`, `<td>`, and `<th>` elements, you can create structured tables to present information in a readable and organized format. Experiment with different table layouts and styles to effectively display data on your webpages. Happy table designing!