## Styling in Next.js: Crafting Beautiful UIs with Ease

Styling plays a crucial role in creating visually appealing and user-friendly web applications. In this tutorial, we'll explore various styling techniques available in Next.js, including CSS Modules, Styled JSX, and using CSS-in-JS libraries like Styled Components.

### CSS Modules

CSS Modules is an approach that scopes styles to specific components, preventing global style pollution and class name conflicts.

1. **Create a CSS Module:**

   To create a CSS Module, create a CSS file with the `.module.css` extension. For example, `styles.module.css`.

   ```css
   /* styles.module.css */
   .container {
     padding: 20px;
     background-color: #f5f5f5;
   }

   .title {
     font-size: 24px;
     color: #333;
   }
   ```

2. **Use CSS Module in Component:**

   Import and use the CSS classes as object properties.

   ```jsx
   // MyComponent.js
   import React from 'react';
   import styles from './styles.module.css';

   function MyComponent() {
     return (
       <div className={styles.container}>
         <h1 className={styles.title}>Styled with CSS Module</h1>
       </div>
     );
   }

   export default MyComponent;
   ```

### Styled JSX

Styled JSX is a built-in styling solution in Next.js that allows you to write CSS directly in your JavaScript code.

1. **Using Styled JSX:**

   Simply write your styles within backticks in your component.

   ```jsx
   // MyComponent.js
   import React from 'react';

   function MyComponent() {
     return (
       <div>
         <h1>This is a regular heading</h1>
         <style jsx>{`
           h1 {
             color: blue;
           }
         `}</style>
       </div>
     );
   }

   export default MyComponent;
   ```

### CSS-in-JS Libraries (e.g., Styled Components)

CSS-in-JS libraries like Styled Components offer a powerful and flexible way to style your components by writing CSS directly in your JavaScript code.

1. **Installing Styled Components:**

   Install Styled Components using npm or yarn.

   ```bash
   npm install styled-components
   ```

2. **Using Styled Components:**

   Import `styled` from Styled Components and create styled components with ease.

   ```jsx
   // MyComponent.js
   import React from 'react';
   import styled from 'styled-components';

   const StyledContainer = styled.div`
     padding: 20px;
     background-color: #f5f5f5;
   `;

   const StyledTitle = styled.h1`
     font-size: 24px;
     color: #333;
   `;

   function MyComponent() {
     return (
       <StyledContainer>
         <StyledTitle>Styled with Styled Components</StyledTitle>
       </StyledContainer>
     );
   }

   export default MyComponent;
   ```

### Summary

Styling in Next.js is versatile and accommodating. You can choose between CSS Modules, Styled JSX, or CSS-in-JS libraries like Styled Components, depending on your preferences and project requirements. These techniques ensure maintainable and scoped styles for your components, leading to a more organized and visually appealing UI. In the upcoming tutorials, we'll explore other advanced styling techniques and best practices to enhance your Next.js applications' visual aesthetics.