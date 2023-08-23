## Use below sample code snippet to do collaborative coding.
- https://codesandbox.io/s/react-new?file=/src/App.js:0-198
- Tools
    -   https://collabedit.com/
    -   Codility

## Mentor Interview Guidelines:
- Use combination of Easy/Medium/Hard[1+2+1 or 4+3+0 or 3+1+1]
- For each question try to grind on writing the code snippet
- Nudge the candidate on Why and When part of concept

## Beginner Questions: \[10 Points\]

**1\. Create a React component named Header that renders an element with the text "Welcome to My App!"**

**2\. Define a React component named Button that renders a button element with the text "Click Me."**

**3\. Why choose the React Framework over other frameworks such as Angular or VueJS? What are the advantages?**

**4\. What is the difference between Virtual DOM and Shadow DOM?**

**5\. Difference between UseMemo and UseCallback?**

**6\. Difference between State and Prop?**

**7\. Build a functional component named UserCard that takes two props, name and email, and displays them inside a <div> element.**

**8\. Create a parent component called App that renders three instances of the UserCard with different data.**

**9\. Develop a component called Toggle that renders a button with the text "Toggle" and an initial state of true. When clicked, the button should toggle the state between true and false, and display the current state as text.**

**10\. Build a component with a text input field. Use the useState hook to store the input's value and update it as the user types.**

**11\. Develop a component that displays the current date and time. Update the display every second using the setInterval function inside the useEffect hook.**

**12\. What are Pure Components? When should we use Pure components? Write a sample code snippet for the same.**

**13\. What is the useEffect hook? When should we use it? Provide a couple of use cases along with one sample code snippet.**

**14\. What is the difference between Class Component and Function Component? Which one should be used?**


## Intermediate[20 Points]: 

Sure, here are your questions numbered:

**15. What is HOC (Higher Order Component)? Provide sample use cases and explain when it should be used. Include a code snippet for one use case.**

**16. How do you memoize a Component?**

**17. Explain Context API, with a couple of use cases and provide a sample code snippet.**

**18. Develop a class/functional component named Counter that initializes its state with a count of 0. Display the count in a <p> element and provide buttons to increment and decrement the count.**

**19. Use the useEffect hook to fetch data from an API endpoint (https://jsonplaceholder.typicode.com/todos) when a component mounts. Display the fetched data on the screen.**

**20. Define a component named Calculator that has two input fields for numbers and buttons for addition, subtraction, multiplication, and division. Display the result of the operation when a button is clicked.**

**Instructions:**
- Use hooks, that are applicable.
- Nudge the learner on the hooks that are being used.

**21. Explain UseMemo and UseCallback with an example.**

**22. Explain PropDrilling and write sample pseudo code or code for the same.**

**23. What are the ways of communicating between components? Which one should be preferred with sample use cases?**

**24. How do we improve the performance of a React App? What are the ways?**


## Advanced[50 Points]:

You are given with a heavy data intensive react web application like amazon, You are asked to increase the load time of the app, What is your strategy and How do you analyze and what are the tasks you will derive in a priority order?[Looking majorly on React performance concepts, Ask the sample code snippet for each action]

Implement a custom hook named useLocalStorage that allows you to store and retrieve data in/from the browser's local storage.


// Redux flow end to end 
Implement a Counter:

Description: Create a Counter component where users can increase and decrease a counter. Use Redux to write and read the counter value.

Subtasks:

Create Redux Store: Set up a Redux store with a counter state.
Implement Counter Component: Build a React component that displays the counter value and buttons to increment and decrement it.
Connect Component to Redux: Use the connect function or React Redux hooks to connect the Counter component to the Redux store. Dispatch actions to update the counter value.

Implement a Todo List:

Description: Create a Todo List component where users can add and remove tasks. Use Redux to manage the state of the tasks.

Subtasks:

Redux Store for Tasks: Set up a Redux store with an initial state for the tasks.
Create Todo List Component: Build a React component that displays the list of tasks, along with input fields to add new tasks.
Manage Tasks with Redux: Implement actions and reducers to handle adding and removing tasks. Connect the Todo List component to the Redux store to manage tasks' state.

Build a User Profile Page:

Description: Design a User Profile page with fields like name, email, and bio. Allow users to edit their profile information and save the changes using Redux.

Subtasks:

Redux Store for User Profile: Set up a Redux store with an initial state for the user profile.
Create Profile Edit Component: Build a React component that displays the user profile fields and allows users to edit them.
Update Profile with Redux: Implement actions and reducers to update the user profile. Connect the Profile Edit component to the Redux store to manage profile state.

Develop a Shopping Cart:

Description: Create a Shopping Cart component for an e-commerce site. Users should be able to add and remove items from the cart, and the cart's total price should be displayed using Redux.

Subtasks:

Redux Store for Cart: Set up a Redux store with an initial state for the shopping cart.
Create Cart Component: Build a React component that displays the items in the cart, along with buttons to add and remove items.
Calculate Total Price with Redux: Implement actions and reducers to manage the cart items and calculate the total price. Connect the Cart component to the Redux store to manage cart state.


Craft a Blog Post Editor:

Description: Build a Blog Post Editor where users can write, edit, and preview blog posts. Use Redux to manage the content and state of the editor.

Subtasks:

Redux Store for Post Content: Set up a Redux store with an initial state for the blog post content.
Create Editor Component: Build a React component that provides input fields for writing and editing blog post content.
Manage Content with Redux: Implement actions and reducers to manage the blog post content. Connect the Editor component to the Redux store to manage content state.

Create a Polling App:

Description: Design a Polling App where users can create and vote on polls. Use Redux to manage the poll data and user votes.

Subtasks:

Redux Store for Polls: Set up a Redux store with an initial state for poll data and user votes.
Create Poll List Component: Build a React component that displays a list of polls and provides options to vote.
Manage Poll Data and Votes with Redux: Implement actions and reducers to manage poll data and user votes. Connect the Poll List component to the Redux store to manage poll state.
