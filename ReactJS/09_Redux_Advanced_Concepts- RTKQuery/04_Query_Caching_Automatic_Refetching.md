# Query Caching and Automatic Re-fetching with RTK Query

## Understanding Caching Behavior in RTK Query

In this section of the tutorial, we'll explore the powerful caching capabilities of RTK Query. Caching helps optimize your application's performance by storing previously fetched data and reusing it. RTK Query handles caching for you, making your app faster and reducing unnecessary network requests.

### How Caching Works

RTK Query automatically caches the results of your API calls. When you make a query using one of the generated query hooks, RTK Query first checks if the data for that query is already in the cache. If it's present and hasn't expired, RTK Query returns the cached data, saving you from making a redundant network request.

This caching mechanism is a huge advantage, as it improves your app's responsiveness and decreases load times, especially when fetching the same data multiple times.

## Automatic Re-fetching and Cache Invalidation

One of the amazing features of RTK Query is its ability to automatically re-fetch data and invalidate the cache when the underlying data changes. This ensures that your app always displays up-to-date information without requiring manual intervention.

### Automatic Re-fetching

Let's say you have a query that fetches a list of posts, and you're displaying these posts in your application. If a new post is added to the server, you don't want your users to see outdated data. With RTK Query, you don't need to worry about this.

When you use a query hook, RTK Query automatically sets up polling to re-fetch the data at regular intervals. This means that your app will periodically check for updates and display the latest information.


### Example: Fetching Posts

Let's illustrate this with an example. Imagine you have a query that fetches a list of posts, and you're displaying these posts in a list.


let's create a step-by-step tutorial with sample code to demonstrate query caching, automatic re-fetching

## Step-by-Step Tutorial: Query Caching and Automatic Re-fetching with RTK Query

In this tutorial, we'll build a simple app that fetches a list of posts from an API using RTK Query. We'll demonstrate how RTK Query's caching and automatic re-fetching work.

### Step 1: Setting Up RTK Query

Install the required packages:

```bash
npm install @reduxjs/toolkit
npm install @reduxjs/toolkit/query
```

### Step 2: Configuring the API Endpoints

Create an `api.js` file and set up your API using `createApi`:

```javascript
// api.js
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react';

export const api = createApi({
  baseQuery: fetchBaseQuery({ baseUrl: 'https://jsonplaceholder.typicode.com' }),
  endpoints: (builder) => ({
    getPosts: builder.query({
      query: () => 'posts',
    }),
  }),
});

export const { useGetPostsQuery } = api;
```

### Step 3: Using the Query in a Component

Create a `PostList.js` file for your component:

```javascript
// PostList.js
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

### Step 4: Implementing Automatic Re-fetching and Setting up Polling

In your `PostList.js` component, RTK Query's automatic re-fetching is already set up. It will periodically re-fetch the posts to ensure the displayed data is up-to-date.

Setting up polling configuration for re-fetching with RTK Query is straightforward. Polling allows you to automatically re-fetch data at regular intervals, ensuring that your application always displays the latest information without manual intervention. To achieve this, you'll need to use the `polling` option in your query configuration.

Here's how you can set up polling configuration in RTK Query:

```javascript
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react';

export const api = createApi({
  baseQuery: fetchBaseQuery({ baseUrl: 'https://jsonplaceholder.typicode.com' }),
  endpoints: (builder) => ({
    getPosts: builder.query({
      query: () => 'posts',
      // Set up polling with the desired interval in milliseconds
      pollingInterval: 10000, // Fetch every 10 seconds
    }),
  }),
});

export const { useGetPostsQuery } = api;
```

In this example, we've added the `pollingInterval` option to the `getPosts` query. This option specifies the time interval (in milliseconds) at which the query should be automatically re-fetched.

Here are the key steps to set up polling configuration:

1. Add the `pollingInterval` option to your query configuration.
2. Specify the time interval (in milliseconds) for automatic re-fetching.
3. RTK Query will take care of re-fetching the data at the specified interval.

Keep in mind that polling can have an impact on the performance of your application and the server. Be cautious not to set the polling interval too frequently, as it could lead to unnecessary network requests. Consider the nature of your application and the data you're fetching when setting the polling interval.

By adding the `pollingInterval` option, you enable RTK Query to handle automatic re-fetching for you, ensuring that your application always displays the most up-to-date data without requiring manual user interaction.


### Step 6: Using the Components

In your `App.js` file, use both `PostList` and `AddPost` components:

```javascript
// App.js
import React from 'react';
import PostList from './PostList';
import AddPost from './AddPost';

function App() {
  return (
    <div className="App">
      <h1>RTK Query Demo</h1>
      <PostList />
      <AddPost />
    </div>
  );
}

export default App;
```

### Step 7: Run the Application

Run your application:

```bash
npm start
```

### Summary

Congratulations! You've built a simple app that demonstrates query caching, automatic re-fetching, and cache invalidation using RTK Query. The `PostList` component automatically re-fetches posts periodically, ensuring the data is up-to-date. The `AddPost` component simulates cache invalidation by adding a new post and triggering a re-fetch of the posts. This showcases the power of RTK Query in managing data fetching and caching effortlessly.