**Assignment: Responsive URL Shortener using ReactJS and Redux**

**Objective:**
Create a responsive URL shortener web application using ReactJS and manage state using Redux. This assignment focuses on designing a user-friendly interface and implementing functionality to shorten URLs. You will also deploy the application using Vercel, Netlify, or GitHub Pages and use an open-source URL shortening API.

**Requirements:**

1. **Setup:**
   - Set up a new React application using Create React App or your preferred React configuration.
   - Set up Redux for state management.

2. **User Interface:**
   - Design a clean, responsive, and user-friendly user interface for the URL shortener.
   - Create an input field for users to enter a long URL.
   - Implement a "Shorten" button for generating a short URL.
   - Display the short URL and allow users to copy it to the clipboard.

3. **Functionality:**
   - Use React components and Redux for managing state to interact with an open-source URL shortening API.
   - When the user enters a long URL and clicks "Shorten," fetch and display the corresponding short URL.
   - Handle cases where the short URL is not generated successfully or the API request fails gracefully, providing clear feedback to the user.

4. **Responsive Design:**
   - Ensure the application is responsive and works well on different screen sizes (desktop, tablet, mobile).

5. **Styling:**
   - Apply CSS or use a styling framework like Material-UI to make the application visually appealing.
   - Use appropriate fonts, colors, and layout techniques for a polished look.

6. **Redux State Management:**
   - Implement Redux for managing the state of the URL shortener. Define actions, reducers, and selectors for relevant data.

7. **Deployment:**
   - Deploy the application on one of the following platforms: Vercel, Netlify, or GitHub Pages.

8. **Documentation:**
   - Create a simple user guide or README explaining how to use the URL shortener.

**Extra Credit (Optional):**

- Implement a feature to allow users to customize the short URL slug.
- Include a history feature to keep a record of previously shortened URLs.
- Add a dark mode or theme switcher for the app.

**Submission:**

1. Create a new GitHub repository for your project.
2. Commit your React application, Redux code, and any CSS files to the repository.
3. Create a `README.md` file with a brief description of the project, instructions on usage, and a link to the live deployment.
4. Deploy the project on Vercel, Netlify, or GitHub Pages and provide the live URL in the README.

**Grading Criteria:**

Your assignment will be evaluated based on the following criteria:
- Functionality (40%)
- User Interface and Responsiveness (25%)
- Validation and Error Handling (15%)
- Styling and Presentation (10%)
- Redux State Management (10%)

**Open Source URL Shortening APIs:**

Here are some open-source URL shortening APIs that you can use for your project:

1. **Rebrandly API**:
   - API Documentation: [Rebrandly API](https://developers.rebrandly.com/docs)

2. **Bitly API**:
   - API Documentation: [Bitly API](https://dev.bitly.com/docs/getting-started/intro)

3. **TinyURL API**:
   - API Documentation: [TinyURL API](https://tinyurl.com/api)

4. **Cuttly API**:
   - API Documentation: [Cuttly API](https://cutt.ly/docs)

Please review the terms and conditions, rate limits, and usage policies of the chosen API before integrating it into your project. Some of these APIs may have usage limitations for free access.