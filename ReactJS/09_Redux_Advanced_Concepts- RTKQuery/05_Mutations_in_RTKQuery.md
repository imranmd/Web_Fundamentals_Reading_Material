# Mutations with RTK Query

In this tutorial, we'll explore how to use mutations in RTK Query to perform actions that modify data on the server. Mutations are essential for tasks like adding, updating, or deleting data. We'll cover the process of defining mutations, using the generated `useMutation` hook, and handling loading, error, and success states.

## Defining Mutations with `mutation`

Mutations in RTK Query are defined using the `mutation` function provided by the `createApi` function. A mutation consists of a request to modify data on the server, and it often involves sending data along with the request. Let's create an example where we'll add a new post to a list of posts on the server.

### Step 1: Set Up Your API

First, set up your API using `createApi` and define a mutation:

```javascript
// api.js
import { createApi, fetchBaseQuery } from '@reduxjs/toolkit/query/react';

export const api = createApi({
  baseQuery: fetchBaseQuery({ baseUrl: 'https://jsonplaceholder.typicode.com' }),
  endpoints: (builder) => ({
    addPost: builder.mutation({
      query: (newPost) => ({
        url: 'posts',
        method: 'POST',
        body: newPost,
      }),
    }),
  }),
});

export const { useAddPostMutation } = api;
```

### Step 2: Using the `useAddPostMutation` Hook

Now you can use the `useAddPostMutation` hook in your component to perform the mutation:

```javascript
import React, { useState } from 'react';
import { useAddPostMutation } from './api';

function AddPostForm() {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');

  const [addPost, { isLoading, isError, isSuccess }] = useAddPostMutation();

  const handleSubmit = async (e) => {
    e.preventDefault();

    try {
      await addPost({ title, body });
    } catch (error) {
      console.error('Error adding post:', error);
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      <div>
        <label>Title:</label>
        <input type="text" value={title} onChange={(e) => setTitle(e.target.value)} />
      </div>
      <div>
        <label>Body:</label>
        <textarea value={body} onChange={(e) => setBody(e.target.value)} />
      </div>
      <button type="submit" disabled={isLoading}>
        {isLoading ? 'Adding...' : 'Add Post'}
      </button>
      {isError && <p>Error adding post.</p>}
      {isSuccess && <p>Post added successfully!</p>}
    </form>
  );
}

export default AddPostForm;
```

### Step 3: Handling Loading, Error, and Success States

In this example, we've created an `AddPostForm` component that uses the `useAddPostMutation` hook to handle adding a new post. The `useAddPostMutation` hook returns several values:

- `addPost`: The function to trigger the mutation.
- `isLoading`: A boolean indicating if the mutation is in progress.
- `isError`: A boolean indicating if the mutation resulted in an error.
- `isSuccess`: A boolean indicating if the mutation was successful.

We use these values to provide user feedback based on the state of the mutation.

## Summary

Congratulations! You've learned how to define mutations with RTK Query, use the generated `useMutation` hook, and handle loading, error, and success states. Mutations are a crucial part of interacting with APIs to modify data. With RTK Query, handling mutations becomes more streamlined and less error-prone. You can now implement various types of mutations in your application to manage data effectively. In the next sections of this tutorial, we'll delve into more advanced RTK Query features.