**HTML Lists**

**Introduction:**

HTML lists are used to organize and display related content in a structured manner. Lists are essential for presenting information in a readable and organized format. There are three types of lists in HTML: ordered lists, unordered lists, and definition lists. In this tutorial documentation, we will learn about each type of list, their syntax, and how to use them to create organized content on a webpage.

**Understanding HTML Lists:**

1. **Ordered Lists (`<ol>`):** Ordered lists are used to create numbered lists, where each item is assigned a sequential number. The order of the items matters in an ordered list.

2. **Unordered Lists (`<ul>`):** Unordered lists are used to create bullet-point lists, where each item is preceded by a bullet or a similar marker. The order of the items does not matter in an unordered list.

3. **Definition Lists (`<dl>`):** Definition lists are used to create a list of terms and their corresponding definitions. Each term is defined using a `<dt>` (definition term) tag, and its definition is provided using a `<dd>` (definition description) tag.

**Syntax for HTML Lists:**

**Ordered List (`<ol>`):**
```html
<!DOCTYPE html>
<html>
<head>
  <title>Ordered List Example</title>
</head>
<body>
  <ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ol>
</body>
</html>
```

**Unordered List (`<ul>`):**
```html
<!DOCTYPE html>
<html>
<head>
  <title>Unordered List Example</title>
</head>
<body>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</body>
</html>
```

**Definition List (`<dl>`):**
```html
<!DOCTYPE html>
<html>
<head>
  <title>Definition List Example</title>
</head>
<body>
  <dl>
    <dt>Term 1</dt>
    <dd>Definition 1</dd>
    <dt>Term 2</dt>
    <dd>Definition 2</dd>
    <dt>Term 3</dt>
    <dd>Definition 3</dd>
  </dl>
</body>
</html>
```

**Working Example:**

Let's create a working example to demonstrate how to use different types of lists in HTML.

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Lists Example</title>
</head>
<body>
  <h1>Types of Fruits</h1>

  <!-- Ordered List -->
  <h2>Ordered List</h2>
  <ol>
    <li>Apple</li>
    <li>Orange</li>
    <li>Banana</li>
  </ol>

  <!-- Unordered List -->
  <h2>Unordered List</h2>
  <ul>
    <li>Mango</li>
    <li>Grapes</li>
    <li>Watermelon</li>
  </ul>

  <!-- Definition List -->
  <h2>Definition List</h2>
  <dl>
    <dt>Strawberry</dt>
    <dd>A red, juicy fruit.</dd>
    <dt>Pineapple</dt>
    <dd>A tropical fruit with a spiky skin.</dd>
  </dl>
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - Lists: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul
2. W3Schools - HTML Lists: https://www.w3schools.com/html/html_lists.asp

**Summary:**

HTML lists are used to organize and present related content in a structured manner. Ordered lists are used for numbered items, unordered lists for bullet-pointed items, and definition lists for terms and their definitions. By using the appropriate HTML list elements, you can create well-structured and readable content on your webpage. Experiment with different types of lists to enhance the presentation of your content. Happy listing!