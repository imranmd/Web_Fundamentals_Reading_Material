# Using Query Results with RTK Query

## Accessing Data, Error, and isLoading States

In this part of the tutorial, we'll dive deeper into using the results of queries fetched with RTK Query. We'll explore how to access the fetched data, handle errors, and manage the loading state using the hooks generated by RTK Query.

### Accessing Data, Error, and isLoading States from the Query Hook

When you use a query hook generated by RTK Query, it returns an object with various properties that help you handle the different states of the query:

- `data`: The fetched data, if the query is successful.
- `error`: An error object, if the query encounters an error.
- `isLoading`: A boolean flag that indicates whether the query is still loading.

Let's use these properties to create a dynamic user experience in your components.

### Displaying Fetched Data in Components

To display the fetched data in your components, you can use the `data` property returned by the query hook. Let's say we're building a simple app that displays a list of posts. Here's how you can use the `useGetPostsQuery` hook to fetch and display posts:

```javascript
import React from 'react';
import { useGetPostsQuery } from './api';

function PostList() {
  const { data: posts, error, isLoading } = useGetPostsQuery();

  if (isLoading) {
    return <p>Loading...</p>;
  }

  if (error) {
    return <p>Error: {error.message}</p>;
  }

  return (
    <div>
      <h2>Latest Posts</h2>
      <ul>
        {posts.map((post) => (
          <li key={post.id}>{post.title}</li>
        ))}
      </ul>
    </div>
  );
}

export default PostList;
```

In this example, when `isLoading` is true, the component displays a loading message. If an error occurs, it displays an error message. Otherwise, it maps over the fetched `posts` array and displays each post's title.

### Handling Loading and Error UI Feedback

Handling the loading and error states helps create a smoother user experience. You can show loading spinners or error messages while waiting for data. RTK Query's `isLoading` and `error` properties make this easy.

By rendering different UI elements based on these states, you ensure that your users are aware of the application's status. For example, you can use CSS spinners to indicate loading, or you can style error messages to draw attention to issues.

```javascript
import React from 'react';
import { useGetPostsQuery } from './api';

function PostList() {
  const { data: posts, error, isLoading } = useGetPostsQuery();

  if (isLoading) {
    return <div className="loader">Loading...</div>;
  }

  if (error) {
    return <div className="error">Error: {error.message}</div>;
  }

  return (
    <div>
      <h2>Latest Posts</h2>
      <ul>
        {posts.map((post) => (
          <li key={post.id}>{post.title}</li>
        ))}
      </ul>
    </div>
  );
}

export default PostList;
```

In this updated example, we've added CSS classes (`loader` and `error`) to style the loading and error messages. This way, users get clear feedback about the application's status.

## Summary

You've learned how to access the data, error, and isLoading states returned by RTK Query's query hooks. By utilizing these states, you can create more user-friendly and responsive components. This knowledge will empower you to build applications that handle data fetching, loading, and error scenarios gracefully. In the next sections of this tutorial, we'll explore more advanced features of RTK Query, such as pagination, mutations, and caching. Stay tuned for more exciting learning!