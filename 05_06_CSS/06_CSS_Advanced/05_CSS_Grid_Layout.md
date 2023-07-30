# CSS Grid Layout Tutorial

## Introduction to CSS Grid Layout

CSS Grid Layout is a powerful layout system that allows you to create two-dimensional grid-based layouts. It enables you to arrange elements in rows and columns, providing a more flexible and intuitive way to create complex web page layouts. Understanding CSS Grid Layout is essential for building modern, responsive, and adaptive web designs.

![Data Types](../../Assets/CSS-GRID-3.png)

## Prerequisites

Before diving into CSS Grid Layout, make sure you have a basic understanding of HTML and CSS. If you need to learn these topics, you can refer to the [HTML Introduction Tutorial](https://example.com/html-introduction) and the [CSS Introduction Tutorial](https://example.com/css-introduction) first.

## Types of CSS Grid Layout

Here are some common CSS Grid Layout techniques and their respective explanations:

### 1. Grid Container - `display: grid`

The `display: grid` property is used to define an element as a grid container. Once an element is a grid container, you can use additional grid properties to control the layout.

**Working Demo:**
```css
.container {
    display: grid;
    grid-template-columns: 100px 200px;
    grid-template-rows: 50px 100px;
}
```

**Explanation:**
In this example, the `.container` element will be displayed as a grid container with two columns, one with a width of 100 pixels and the other with a width of 200 pixels, and two rows, one with a height of 50 pixels and the other with a height of 100 pixels.

### 2. Grid Items - `grid-column` and `grid-row`

The `grid-column` and `grid-row` properties are used to place grid items (child elements of the grid container) into specific grid cells.

**Working Demo:**
```css
.item {
    grid-column: 1 / 3;
    grid-row: 2 / 3;
}
```

**Explanation:**
In this example, the `.item` element will span from the first column line to the third column line (covering two columns) and from the second row line to the third row line (covering one row).

### 3. Grid Gaps - `gap`

The `gap` property is used to create spacing between grid rows and columns.

**Working Demo:**
```css
.container {
    display: grid;
    grid-template-columns: 100px 200px;
    grid-template-rows: 50px 100px;
    gap: 10px;
}
```

**Explanation:**
In this example, the `.container` element will have a gap of 10 pixels between grid rows and columns, resulting in visually separated grid cells.

### 4. Grid Template Areas - `grid-template-areas`

The `grid-template-areas` property is used to define named grid areas within the grid layout.

**Working Demo:**
```css
.container {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar content";
}
```

**Explanation:**
In this example, the `.container` element will have named grid areas: "header," "sidebar," and "content." Grid items with specific `grid-area` property values can be placed within these named areas.

## Example Usage
 Here's an example of an HTML code snippet that demonstrates the use of CSS Grid Layout along with comments to explain each part:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Grid Layout Example</title>
    <style>
        /* Define the grid container */
        .grid-container {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr; /* Create three equal-width columns */
            grid-gap: 10px; /* Add a gap of 10px between grid items */
        }

        /* Define styles for grid items */
        .grid-item {
            background-color: lightblue;
            padding: 20px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="grid-container">
        <!-- Grid Item 1 -->
        <div class="grid-item">
            <p>Grid Item 1</p>
        </div>

        <!-- Grid Item 2 -->
        <div class="grid-item">
            <p>Grid Item 2</p>
        </div>

        <!-- Grid Item 3 -->
        <div class="grid-item">
            <p>Grid Item 3</p>
        </div>

        <!-- Grid Item 4 -->
        <div class="grid-item">
            <p>Grid Item 4</p>
        </div>

        <!-- Grid Item 5 -->
        <div class="grid-item">
            <p>Grid Item 5</p>
        </div>

        <!-- Grid Item 6 -->
        <div class="grid-item">
            <p>Grid Item 6</p>
        </div>
    </div>
</body>
</html>
```

In this example, we use CSS Grid Layout to create a simple grid with three columns and two rows:

1. `.grid-container`: This class defines the container that will display as a grid. We use `grid-template-columns` to create three equal-width columns, and `grid-gap` to add a gap of 10px between grid items.

2. `.grid-item`: This class defines the style for each grid item. We set a light blue background color, add padding, and center the text inside each grid item.

The container contains six divs with the class `.grid-item`, and they will be automatically arranged in the grid layout according to the defined grid template columns. The items will flow from left to right and wrap to the next row when the columns are filled.

The comments in the HTML and CSS code explain the purpose of each part and its contribution to creating the CSS Grid Layout.
## Summary

CSS Grid Layout is a versatile and powerful system for creating complex web layouts. By using the grid container and grid item properties like `grid-template-columns`, `grid-template-rows`, `grid-column`, `grid-row`, `gap`, and `grid-template-areas`, you can design responsive and adaptive grid-based layouts for your web pages.

## Additional Resources

1. [MDN Web Docs - CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout): This resource from MDN provides detailed explanations and examples of CSS Grid Layout.

2. [CSS-Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/): This comprehensive guide on CSS-Tricks offers practical examples and use cases for mastering CSS Grid Layout.

3. [CSS Grid Layout Module Level 1](https://www.w3.org/TR/css-grid-1/): This official documentation from W3C provides an in-depth specification of CSS Grid Layout and its properties.