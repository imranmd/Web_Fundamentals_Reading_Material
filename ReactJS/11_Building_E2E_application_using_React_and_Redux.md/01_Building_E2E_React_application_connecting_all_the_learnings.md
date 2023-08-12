# Building an End-to-End React Application: Connecting All Learnings

In this tutorial, we will walk through the process of building an End-to-End (E2E) React application that connects various concepts and technologies we have learned. By the end of this tutorial, you will have a solid understanding of how to create a fully functional React application that incorporates front-end development, state management, API integration, routing, and more.

## Prerequisites

Before we start, make sure you have the following prerequisites installed:

1. Node.js and npm: To run JavaScript code and manage packages.
2. Git: Version control system.
3. Text editor or Integrated Development Environment (IDE) of your choice.

## Table of Contents

1. Setting Up the Project
2. Creating Components and Views
3. Managing State with Redux
4. Fetching Data from an API
5. Implementing Routing
6. Styling with CSS and CSS Modules
7. Building and Deploying the Application

## 1. Setting Up the Project

1. Create a new directory for your project: `mkdir e2e-react-app`
2. Navigate into the project directory: `cd e2e-react-app`
3. Initialize a new Node.js project: `npm init -y`
4. Install React and ReactDOM: `npm install react react-dom`
5. Install Redux: `npm install redux react-redux`
6. Install React Router: `npm install react-router-dom`
7. Install Axios for making API requests: `npm install axios`

## 2. Creating Components and Views

1. Create a `src` directory in the project folder.
2. Inside `src`, create a `components` directory for your React components.
3. Create a simple component: `Header.js`

```jsx
// src/components/Header.js
import React from 'react';

const Header = () => {
  return <header>My E2E React App</header>;
};

export default Header;
```

4. Create a main application component: `App.js`

```jsx
// src/App.js
import React from 'react';
import Header from './components/Header';

const App = () => {
  return (
    <div>
      <Header />
      <main>Content goes here</main>
    </div>
  );
};

export default App;
```

## 3. Managing State with Redux

1. Inside the `src` directory, create a `redux` directory.
2. Create a Redux store, actions, and reducers.

```jsx
// src/redux/actions.js
export const SET_USERNAME = 'SET_USERNAME';

export const setUsername = (username) => {
  return {
    type: SET_USERNAME,
    payload: username,
  };
};
```

```jsx
// src/redux/reducers.js
import { SET_USERNAME } from './actions';

const initialState = {
  username: '',
};

const rootReducer = (state = initialState, action) => {
  switch (action.type) {
    case SET_USERNAME:
      return {
        ...state,
        username: action.payload,
      };
    default:
      return state;
  }
};

export default rootReducer;
```

```jsx
// src/redux/store.js
import { createStore } from 'redux';
import rootReducer from './reducers';

const store = createStore(rootReducer);

export default store;
```

3. Integrate Redux in your `App.js` component.

```jsx
// src/App.js
import React from 'react';
import { Provider } from 'react-redux';
import store from './redux/store';
import Header from './components/Header';

const App = () => {
  return (
    <Provider store={store}>
      <div>
        <Header />
        <main>Content goes here</main>
      </div>
    </Provider>
  );
};

export default App;
```

## 4. Fetching Data from an API

1. Create a service for API requests: `src/services/api.js`

```jsx
// src/services/api.js
import axios from 'axios';

const API_BASE_URL = 'https://api.example.com';

export const fetchUserData = async (userId) => {
  try {
    const response = await axios.get(`${API_BASE_URL}/users/${userId}`);
    return response.data;
  } catch (error) {
    throw error;
  }
};
```

2. Create a user profile component: `src/components/UserProfile.js`

```jsx
// src/components/UserProfile.js
import React, { useEffect, useState } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { setUsername } from '../redux/actions';
import { fetchUserData } from '../services/api';

const UserProfile = () => {
  const dispatch = useDispatch();
  const username = useSelector((state) => state.username);
  const [userData, setUserData] = useState(null);

  useEffect(() => {
    const userId = '123'; // Replace with an actual user ID
    fetchUserData(userId)
      .then((data) => {
        setUserData(data);
        dispatch(setUsername(data.username));
      })
      .catch((error) => {
        console.error('Error fetching user data:', error);
      });
  }, [dispatch]);

  return (
    <div>
      <h2>Welcome, {username}!</h2>
      {userData && (
        <div>
          <p>Name: {userData.name}</p>
          <p>Email: {userData.email}</p>
        </div>
      )}
    </div>
  );
};

export default UserProfile;
```

3. Update `App.js` to include the `UserProfile` component.

```jsx
// src/App.js
import React from 'react';
import { Provider } from 'react-redux';
import store from './redux/store';
import Header from './components/Header';
import UserProfile from './components/UserProfile';

const App = () => {
  return (
    <Provider store={store}>
      <div>
        <Header />
        <main>
          <UserProfile />
        </main>
      </div>
    </Provider>
  );
};

export default App;
```

## 5. Implementing Routing

1. Create a few more components: `src/components/Home.js` and `src/components/NotFound.js`

```jsx
// src/components/Home.js
import React from 'react';

const Home = () => {
  return <div>Welcome to our E2E React App!</div>;
};

export default Home;
```

```jsx
// src/components/NotFound.js
import React from 'react';

const NotFound = () => {
  return <div>Page not found.</div>;
};

export default NotFound;
```

2. Set up routing in `App.js`.

```jsx
// src/App.js
import React from 'react';
import { Provider } from 'react-redux';
import { BrowserRouter as Router, Switch, Route } from 'react-router-dom';
import store from './redux/store';
import Header from './components/Header';
import Home from './components/Home';
import UserProfile from './components/UserProfile';
import NotFound from './components/NotFound';

const App = () => {
  return (
    <Provider store={store}>
      <Router>
        <div>
          <Header />
          <main>
            <Switch>
              <Route exact path="/" component={Home} />
              <Route path="/profile" component={UserProfile} />
              <Route component={NotFound} />
            </Switch>
          </main>
        </div>
      </Router>
    </Provider>
  );
```jsx
export default App;
```

## 6. Styling with CSS and CSS Modules

1. Create a `styles` directory inside the `src` folder.
2. Add a basic CSS file: `src/styles/main.css`

```css
/* src/styles/main.css */
body {
  font-family: Arial, sans-serif;
}

header {
  background-color: #333;
  color: #fff;
  padding: 1rem;
}

main {
  padding: 2rem;
}
```

3. Configure CSS Modules. Rename `main.css` to `main.module.css`.

```css
/* src/styles/main.module.css */
body {
  font-family: Arial, sans-serif;
}

/* ... other styles ... */
```

4. Update components to use CSS Modules.

```jsx
// src/components/Header.js
import React from 'react';
import styles from '../styles/main.module.css';

const Header = () => {
  return <header className={styles.header}>My E2E React App</header>;
};

export default Header;
```

## 7. Building and Deploying the Application

1. Build your application for production.

```bash
npm run build
```

2. Deploy your application to a hosting service of your choice (e.g., Netlify, Vercel, GitHub Pages).

## Conclusion

Congratulations! You've successfully built an End-to-End React application that incorporates various concepts, including component creation, state management with Redux, API integration, routing, and styling with CSS Modules. This tutorial has provided you with a foundation to expand your knowledge and create even more complex and feature-rich applications using React.

Remember, this tutorial is just the beginning. There's so much more you can explore and learn within the realm of web development and React. Happy coding!