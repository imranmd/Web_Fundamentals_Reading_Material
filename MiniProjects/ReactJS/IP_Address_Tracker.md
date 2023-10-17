**Assignment: Responsive IP Address Tracker using ReactJS and Redux**

**Objective:**
Create a responsive IP address tracker web application using ReactJS and manage state using Redux. This assignment focuses on designing a user-friendly interface and implementing functionality to retrieve information about IP addresses. You will also deploy the application using Vercel, Netlify, or GitHub Pages and use an open-source IP geolocation API.

**Requirements:**

1. **Setup:**
   - Set up a new React application using Create React App or your preferred React configuration.
   - Set up Redux for state management.

2. **User Interface:**
   - Design a clean, responsive, and user-friendly user interface for the IP address tracker.
   - Create an input field for users to enter an IP address.
   - Implement a "Track IP" button for initiating the IP address lookup.
   - Display information about the IP address, including its location, region, country, and ISP.

3. **Functionality:**
   - Use React components and Redux for managing state to interact with an open-source IP geolocation API.
   - When the user enters an IP address and clicks "Track IP," fetch and display the location-based information of the IP address, including country, region, and city.
   - Handle cases where the IP address is not found or the API request fails gracefully, providing clear feedback to the user.

4. **Responsive Design:**
   - Ensure the application is responsive and works well on different screen sizes (desktop, tablet, mobile).

5. **Styling:**
   - Apply CSS or use a styling framework like Material-UI to make the application visually appealing.
   - Use appropriate fonts, colors, and layout techniques for a polished look.

6. **Redux State Management:**
   - Implement Redux for managing the state of the IP address tracker. Define actions, reducers, and selectors for relevant data.

7. **Deployment:**
   - Deploy the application on one of the following platforms: Vercel, Netlify, or GitHub Pages.

8. **Documentation:**
   - Create a simple user guide or README explaining how to use the IP address tracker.

**Extra Credit (Optional):**

- Add a map displaying the approximate location of the IP address.
- Implement a dark mode or theme switcher for the app.
- Include a history feature to keep a record of previously tracked IP addresses.

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

**Open Source IP Geolocation APIs:**

Here are some open-source IP geolocation APIs that you can use for your project:

1. **ipinfo.io**:
   - API Documentation: [ipinfo.io](https://ipinfo.io/)

2. **ip-api.com**:
   - API Documentation: [ip-api.com](http://ip-api.com/docs/)

3. **ipgeolocation.io**:
   - API Documentation: [ipgeolocation.io](https://ipgeolocation.io/documentation/)

4. **extreme-ip-lookup.com**:
   - API Documentation: [extreme-ip-lookup.com](https://extreme-ip-lookup.com/static/api)

5. **freegeoip.app**:
   - API Documentation: [freegeoip.app](https://freegeoip.app/)

Please review the terms and conditions, rate limits, and usage policies of the chosen API before integrating it into your project. Some of these APIs may have usage limitations for free access.