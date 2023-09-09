## Routing with Pages Directory in Next.js: Navigating Through Your App

Routing is a fundamental aspect of web applications, and Next.js simplifies it with its file-based routing system. In this tutorial, we'll explore basic routing using the `pages` directory, dynamic routing, handling nested routes, and creating links between pages.

### Basic Routing with `pages` Directory

In Next.js, each file in the `pages` directory corresponds to a route. For example:

```
pages/
|-- index.js   // maps to "/"
|-- about.js   // maps to "/about"
|-- contact.js // maps to "/contact"
```

Let's create a few simple pages:

1. **Create `index.js`:**

   Inside the `pages` directory, create a file named `index.js`.

   ```jsx
   // pages/index.js
   import React from 'react';

   function HomePage() {
     return (
       <div>
         <h1>Welcome to the Home Page</h1>
       </div>
     );
   }

   export default HomePage;
   ```

2. **Create `about.js`:**

   Similarly, create an `about.js` file.

   ```jsx
   // pages/about.js
   import React from 'react';

   function AboutPage() {
     return (
       <div>
         <h1>About Us</h1>
         <p>This is the about page.</p>
       </div>
     );
   }

   export default AboutPage;
   ```

### Dynamic Routing

Next.js supports dynamic routing, allowing you to create routes with variables.

1. **Create `posts/[id].js`:**

   Inside the `pages` directory, create a subdirectory named `posts`. Inside the `posts` directory, create a file named `[id].js`.

   ```jsx
   // pages/posts/[id].js
   import React from 'react';
   import { useRouter } from 'next/router';

   function PostPage() {
     const router = useRouter();
     const { id } = router.query;

     return (
       <div>
         <h1>Post {id}</h1>
       </div>
     );
   }

   export default PostPage;
   ```

   Now, you can access dynamic routes like `/posts/1`, `/posts/2`, and so on.

### Nested Routes

You can create nested routes by organizing files in subdirectories.

1. **Create `products/index.js`:**

   Inside the `pages` directory, create a subdirectory named `products`. Inside the `products` directory, create an `index.js` file.

   ```jsx
   // pages/products/index.js
   import React from 'react';

   function ProductsPage() {
     return (
       <div>
         <h1>Products</h1>
       </div>
     );
   }

   export default ProductsPage;
   ```

2. **Create `products/[id].js`:**

   Inside the `products` directory, create a file named `[id].js`.

   ```jsx
   // pages/products/[id].js
   import React from 'react';
   import { useRouter } from 'next/router';

   function ProductPage() {
     const router = useRouter();
     const { id } = router.query;

     return (
       <div>
         <h1>Product {id}</h1>
       </div>
     );
   }

   export default ProductPage;
   ```

### Linking Between Pages

Next.js provides the `Link` component for navigating between pages without a full page refresh.

1. **Using the `Link` Component:**

   Use the `Link` component to navigate between pages.

   ```jsx
   // pages/index.js
   import React from 'react';
   import Link from 'next/link';

   function HomePage() {
     return (
       <div>
         <h1>Welcome to the Home Page</h1>
         <Link href="/about">About Us</Link>
       </div>
     );
   }

   export default HomePage;
   ```

### Summary

Next.js makes routing intuitive with its file-based approach. You can create routes simply by organizing files in the `pages` directory. Dynamic routing, nested routes, and the `Link` component enhance your ability to navigate between pages and create complex application structures. In the next tutorials, we'll explore more advanced routing techniques and features offered by Next.js.