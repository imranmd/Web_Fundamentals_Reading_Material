# Tutorial: Introduction to Next.js and Deploying React Applications

## Table of Contents

1. Introduction to Next.js
   - What is Next.js?
   - Key Features
   - Why use Next.js?

2. Setting Up Your Development Environment
   - Prerequisites
   - Installation
   - Creating a New Next.js Project

3. Creating a Basic Next.js App
   - Project Structure
   - Pages and Routing
   - Creating Components
   - Styling with CSS Modules

4. Deploying a Next.js App
   - Preparing for Deployment
   - Hosting Options
   - Deploying to Vercel

## 1. Introduction to Next.js

### What is Next.js?

Next.js is a popular React framework that helps you build modern web applications with ease. It provides a set of tools and conventions for building fast, scalable, and SEO-friendly applications using React. Next.js takes care of many configuration details, allowing developers to focus on building great user experiences.

### Key Features

- Server-side rendering (SSR) and static site generation (SSG) for optimal performance and SEO.
- Automatic code splitting for efficient loading of JavaScript assets.
- Built-in routing system for creating pages and handling navigation.
- CSS Modules for scoped and modular styling.
- API routes for creating serverless functions within your app.
- Fast refresh for instant feedback during development.
- Excellent developer experience and community support.

### Why use Next.js?

Next.js offers several advantages for building React applications:

- Improved performance: Server-side rendering and automatic code splitting result in faster page loads and better user experiences.
- SEO optimization: Server-side rendering and static site generation improve search engine visibility and ranking.
- Simplified routing: Next.js provides a simple and intuitive routing system, making it easy to create complex applications with multiple pages.
- Developer experience: Fast refresh, CSS Modules, and other built-in features enhance the development process and reduce boilerplate code.
- Serverless functions: You can create API routes directly within your app, enabling serverless backend functionality.

## 2. Setting Up Your Development Environment

### Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v14.0.0 or higher)
- npm (v6.0.0 or higher) or yarn (v1.22.0 or higher)

### Installation

Open your terminal and run the following command to install the Next.js CLI globally:

```bash
npm install -g create-next-app
```

### Creating a New Next.js Project

To create a new Next.js project, navigate to your desired directory and run:

```bash
npx create-next-app my-next-app
```

This will set up a new Next.js project named "my-next-app" in a folder of the same name.

## 3. Creating a Basic Next.js App

### Project Structure

Next.js projects have a predefined structure:

```plaintext
my-next-app/
├── node_modules/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── styles/
│   └── ...
├── .gitignore
├── next.config.js
├── package.json
└── ...
```

- `public/`: Static assets like images and fonts.
- `src/`: Source code directory.
  - `components/`: Reusable React components.
  - `pages/`: Application pages and routing.
  - `styles/`: CSS styles.

### Pages and Routing

1. Navigate to the `src/pages/` directory.
2. Create a new file named `index.js`:

```jsx
import React from 'react';

function HomePage() {
  return <div>Welcome to Next.js!</div>;
}

export default HomePage;
```

3. Open your browser and navigate to `http://localhost:3000` to see the result.

### Creating Components

1. Navigate to the `src/components/` directory.
2. Create a new file named `Header.js`:

```jsx
import React from 'react';

function Header() {
  return <header>This is the header component</header>;
}

export default Header;
```

3. Use the `Header` component in your `src/pages/index.js`:

```jsx
import React from 'react';
import Header from '../components/Header';

function HomePage() {
  return (
    <div>
      <Header />
      <div>Welcome to Next.js!</div>
    </div>
  );
}

export default HomePage;
```

### Styling with CSS Modules

1. Navigate to the `src/styles/` directory.
2. Create a new file named `styles.module.css`:

```css
.header {
  background-color: #333;
  color: #fff;
  padding: 1rem;
}
```

3. Update `Header.js` to use the CSS module:

```jsx
import React from 'react';
import styles from '../styles/styles.module.css';

function Header() {
  return <header className={styles.header}>This is the header component</header>;
}

export default Header;
```

## 4. Deploying a Next.js App

### Preparing for Deployment

1. Make sure your Next.js app is fully functional and free of errors.
2. Review and optimize your application code for production.
3. Remove any sensitive information from your source code.

### Hosting Options

Next.js apps can be deployed to various hosting platforms. Some popular options include:

- [Vercel](https://vercel.com)
- [Netlify](https://www.netlify.com)
- [Heroku](https://www.heroku.com)
- [AWS Amplify](https://aws.amazon.com/amplify)
- [DigitalOcean](https://www.digitalocean.com)

### Deploying to Vercel

Vercel offers an easy way to deploy Next.js apps:

1. Install the Vercel CLI:

```bash
npm install -g vercel
```

2. Navigate to your project's root directory.

3. Run the following command and follow the prompts:

```bash
vercel
```

4. Once the deployment is complete, you'll receive a URL for your deployed app.

Congratulations! You've successfully created a basic Next.js app and deployed it to a hosting platform.

## Conclusion

In this tutorial, you've learned the basics of Next.js, including creating a simple app, adding components, and styling with CSS Modules. You've also learned how to prepare your app for deployment and deploy it to a hosting platform like Vercel. This is just the beginning of what Next.js can offer, and you're encouraged to explore more advanced features and build more complex applications using this powerful framework. Happy coding!