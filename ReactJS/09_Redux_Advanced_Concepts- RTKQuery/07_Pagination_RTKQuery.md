# Invalidating and Refetching Data with RTK Query

In this tutorial, you'll learn how to manually invalidate cache to trigger refetching of data and how to use the `invalidates` option to define dependencies between endpoints in RTK Query. These features are valuable for keeping your data up-to-date and ensuring that changes are reflected across related parts of your application.

## Manually Invalidating Cache to Trigger Refetching

Invalidating the cache manually is useful when you want to force RTK Query to re-fetch data from the server, even if the cached data hasn't expired. This can be helpful in situations where you know that the data on the server has changed and you want to ensure that your app displays the most recent information.

### Step 1: Set Up Your API

Assuming you have the following endpoint defined in your API configuration:

```javascript
// api.js
export const api = createApi({
  endpoints: (builder) => ({
    getPosts: builder.query({
      query: () => 'posts',
    }),
  }),
});
```

### Step 2: Manually Invalidating Cache

You can manually invalidate the cache and trigger a re-fetch by using the `invalidateQueries` function from RTK Query:

```javascript
import { invalidateQueries } from '@reduxjs/toolkit/query/react';
import { api } from './api';

function RefreshPostsButton() {
  const handleClick = () => {
    invalidateQueries('getPosts');
  };

  return <button onClick={handleClick}>Refresh Posts</button>;
}

export default RefreshPostsButton;
```

In this example, the `RefreshPostsButton` component contains a button that, when clicked, triggers the invalidation of the `getPosts` query cache. This will lead to a re-fetch of the data from the server the next time the `useGetPostsQuery` hook is used.

## Using `invalidates` to Define Dependencies

The `invalidates` option allows you to define dependencies between different endpoints. When one endpoint's data changes, you can automatically invalidate the cache of another endpoint that depends on it.

### Step 1: Set Up Your API

Assuming you have two endpoints defined in your API configuration:

```javascript
// api.js
export const api = createApi({
  endpoints: (builder) => ({
    getPosts: builder.query({
      query: () => 'posts',
    }),
    createPost: builder.mutation({
      query: (newPost) => ({
        url: 'posts',
        method: 'POST',
        body: newPost,
      }),
      invalidates: ['getPosts'], // Define dependencies
    }),
  }),
});
```

In this example, the `createPost` mutation is defined with the `invalidates` option set to `['getPosts']`. This means that when a new post is created, the cache for the `getPosts` query will be automatically invalidated, triggering a re-fetch.

## Summary

You've learned how to manually invalidate cache to trigger refetching and how to use the `invalidates` option to define dependencies between endpoints in RTK Query. These features give you fine-grained control over how your application's data is updated and ensure that changes are properly reflected throughout the app. In the next sections of this tutorial, we'll continue exploring more advanced RTK Query features.