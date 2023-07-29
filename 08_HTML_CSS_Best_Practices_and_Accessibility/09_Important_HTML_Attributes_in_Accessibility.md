Below is a list of HTML attributes related to accessibility along with sample code snippets in HTML:

1. **`alt` Attribute (for Images)**

   The `alt` attribute provides alternative text for images, making them accessible to users who cannot see the images.

   Sample Code:
   ```html
   <img src="image.jpg" alt="A beautiful sunset over the mountains">
   ```

2. **`title` Attribute**

   The `title` attribute provides additional information about an element, such as a tooltip, which can improve accessibility for users with disabilities.

   Sample Code:
   ```html
   <a href="#" title="Click here to read more">Read More</a>
   ```

3. **`aria-label` Attribute**

   The `aria-label` attribute defines a concise label for an element when a visible label is not present, making it accessible to assistive technologies.

   Sample Code:
   ```html
   <button aria-label="Close" onclick="closeModal()">X</button>
   ```

4. **`aria-labelledby` Attribute**

   The `aria-labelledby` attribute associates an element with another element (usually an `<h1>` or `<h2>`) to provide a meaningful label for assistive technologies.

   Sample Code:
   ```html
   <div id="section-title">Section 1</div>
   <div aria-labelledby="section-title">This is the content of Section 1.</div>
   ```

5. **`aria-describedby` Attribute**

   The `aria-describedby` attribute points to an element that provides a description or additional information about the current element.

   Sample Code:
   ```html
   <input type="text" aria-describedby="username-help">
   <span id="username-help">Please enter your username.</span>
   ```

6. **`role` Attribute**

   The `role` attribute defines the role of an element, which can help assistive technologies understand the purpose of the element.

   Sample Code:
   ```html
   <nav role="navigation">
     <ul>
       <li><a href="#">Home</a></li>
       <li><a href="#">About</a></li>
     </ul>
   </nav>
   ```

7. **`tabindex` Attribute**

   The `tabindex` attribute determines the order in which elements receive focus when users navigate using the Tab key.

   Sample Code:
   ```html
   <input type="text" tabindex="1">
   <input type="submit" tabindex="2">
   ```

8. **`aria-haspopup` Attribute**

   The `aria-haspopup` attribute indicates that an element has a popup menu or dialog.

   Sample Code:
   ```html
   <button aria-haspopup="true" aria-expanded="false">Open Menu</button>
   ```

9. **`aria-expanded` Attribute**

   The `aria-expanded` attribute indicates whether a collapsible element (e.g., accordion) is expanded or collapsed.

   Sample Code:
   ```html
   <button aria-expanded="true" aria-controls="content">Show Details</button>
   <div id="content">Details here...</div>
   ```

10. **`aria-hidden` Attribute**

    The `aria-hidden` attribute hides an element from assistive technologies when set to "true".

    Sample Code:
    ```html
    <div aria-hidden="true">This content is hidden from screen readers.</div>
    ```

These attributes play a crucial role in making web content accessible to all users, including those with disabilities. It's important to use them properly and thoughtfully to ensure a positive user experience for everyone.