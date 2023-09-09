## API Routes in Next.js: Building Serverless Backend for Your App

API Routes in Next.js allow you to create your own API endpoints directly within your application. In this tutorial, we'll explore how to create API routes, handle server-side logic, and fetch data from these routes.

### Creating API Routes

API Routes in Next.js are defined in the `pages/api` directory. Each file in this directory corresponds to an API endpoint.

1. **Create an API Route:**

   Inside the `pages/api` directory, create a file named `hello.js`.

   ```jsx
   // pages/api/hello.js
   export default function handler(req, res) {
     res.status(200).json({ message: 'Hello, API Route!' });
   }
   ```

   This simple API route responds with a JSON message.

### Handling Server-side Logic

API Routes can handle complex server-side logic and interact with databases, external APIs, or any other server-side tasks.

1. **Create a Dynamic API Route:**

   Inside the `pages/api` directory, create a file named `users/[id].js`.

   ```jsx
   // pages/api/users/[id].js
   export default function handler(req, res) {
     const { id } = req.query;
     // Fetch user data from a database or API
     const userData = fetchUserDataById(id);

     res.status(200).json(userData);
   }
   ```

   In this dynamic API route, the `[id].js` file name indicates that it handles requests like `/api/users/1`.

### Fetching Data from API Routes

You can fetch data from your API routes using client-side methods like `fetch` or `axios`.

1. **Fetching Data from an API Route:**

   In your component, use `fetch` to retrieve data from your API route.

   ```jsx
   // components/UserInfo.js
   import React, { useState, useEffect } from 'react';

   function UserInfo({ userId }) {
     const [userData, setUserData] = useState(null);

     useEffect(() => {
       async function fetchUserData() {
         const response = await fetch(`/api/users/${userId}`);
         const data = await response.json();
         setUserData(data);
       }

       fetchUserData();
     }, [userId]);

     if (!userData) {
       return <p>Loading...</p>;
     }

     return (
       <div>
         <h2>{userData.name}</h2>
         <p>Email: {userData.email}</p>
       </div>
     );
   }

   export default UserInfo;
   ```

### Summary

API Routes in Next.js enable you to build powerful serverless APIs directly within your application. You can create various API endpoints, handle server-side logic, and fetch data seamlessly. This feature allows you to keep your frontend and backend code together, simplifying development and deployment. By mastering API Routes, you can build robust web applications with integrated APIs for various purposes, enhancing the functionality and user experience of your Next.js app.