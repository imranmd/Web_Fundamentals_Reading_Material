# Step-by-Step Tutorial: Building a Responsive Portfolio App using HTML and CSS

In this tutorial, we'll create a responsive portfolio app with five sections: Header banner, Education, Projects, Experience, and Contact. We'll use media queries to ensure the app looks great on various devices. Let's get started!

## Step 1: Setup the Basic HTML Structure

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>

<body>
  <header>
    <nav>
      <ul>
        <li><a href="#banner">Home</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <!-- Sections will be added in subsequent steps -->
  </main>
</body>

</html>
```

## Step 2: Add the Header Banner Section

```html
<section id="banner">
  <div class="banner-content">
    <h1>Your Name</h1>
    <p>Web Developer</p>
    <p>Welcome to my portfolio!</p>
  </div>
</section>
```

## Step 3: Style the Header Banner Section

Create `styles.css` file and add the following CSS rules:

```css
/* Global Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* Header Styles */
header {
  background-color: #333;
  color: #fff;
  padding: 10px;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

nav ul li {
  display: inline;
  margin-right: 20px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

/* Header Banner Styles */
#banner {
  background-image: url('placeholder_banner.jpg');
  background-size: cover;
  background-position: center;
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.banner-content {
  text-align: center;
}

.banner-content h1 {
  font-size: 48px;
  margin: 0;
}

.banner-content p {
  font-size: 24px;
  margin: 5px 0;
}
```

## Step 4: Add the Education Section

```html
<section id="education">
  <h2>Education</h2>
  <ul>
    <li>
      <h3>University Name</h3>
      <p>Degree, Major</p>
      <p>Year of Graduation</p>
    </li>
    <!-- Add more education entries here -->
  </ul>
</section>
```

## Step 5: Style the Education Section

```css
/* Education Section Styles */
#education {
  background-color: #f0f0f0;
  padding: 30px;
}

#education h2 {
  text-align: center;
}

#education ul {
  list-style: none;
  padding: 0;
}

#education li {
  border-bottom: 1px solid #ccc;
  padding: 10px 0;
}

#education h3 {
  margin: 0;
}

#education p {
  margin: 5px 0;
}
```

## Step 6: Add the Projects Section

```html
<section id="projects">
  <h2>Projects</h2>
  <ul>
    <li>
      <h3>Project Title</h3>
      <p>Project Description</p>
    </li>
    <!-- Add more project entries here -->
  </ul>
</section>
```

## Step 7: Style the Projects Section

```css
/* Projects Section Styles */
#projects {
  background-color: #fff;
  padding: 30px;
}

#projects h2 {
  text-align: center;
}

#projects ul {
  list-style: none;
  padding: 0;
}

#projects li {
  padding: 10px 0;
}

#projects h3 {
  margin: 0;
}

#projects p {
  margin: 5px 0;
}
```

## Step 8: Add the Experience Section

```html
<section id="experience">
  <h2>Experience</h2>
  <ul>
    <li>
      <h3>Job Title</h3>
      <p>Company Name</p>
      <p>Duration</p>
      <p>Job Description</p>
    </li>
    <!-- Add more experience entries here -->
  </ul>
</section>
```

## Step 9: Style the Experience Section

```css
/* Experience Section Styles */
#experience {
  background-color: #f0f0f0;
  padding: 30px;
}

#experience h2 {
  text-align: center;
}

#experience ul {
  list-style: none;
  padding: 0;
}

#experience li {
  border-bottom: 1px solid #ccc;
  padding: 10px 0;
}

#experience h3 {
  margin: 0;
}

#experience p {
  margin: 5px 0;
}
```

## Step 10: Add the Contact Section

```html
<section id="contact">
  <h2>Contact</h2>
  <form>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" required></textarea>
    <button type="submit">Send</button>
  </form>
</section>
```

## Step 11: Style the Contact Section

```css
/* Contact Section Styles */
#contact {
  background-color: #fff;
  padding: 30px;
}

#contact h2 {
  text-align: center;
}

#contact form {
  display: flex;
  flex-direction: column;
  max-width: 400px;
  margin: 0 auto;
}

#contact label {
  margin-top: 10px;
}

#contact input,
#contact textarea {
  margin-bottom: 10px;
  padding: 5px;
}

#contact button {
  background-color: #333;
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
}
```

## Step 12: Add Media Queries for Responsiveness

Add the following media queries to adjust the layout for different screen sizes:

```css
/* Media Queries */
@media screen and (max-width: 768px) {
  .banner-content h1 {
    font-size: 36px;
  }
  
  .banner-content p {
    font-size: 18px;
  }
  
  #education,
  #projects,
  #experience,
  #contact {
    padding: 20px;
  }
  
  #contact form {
    max-width: 100%;
  }
}
```

In this media query, we adjusted the font sizes in the header banner to make them smaller on smaller screens. We also reduced the padding in the education, projects, experience, and contact sections to save space. For the contact form, we made it wider to ensure it fits well on smaller screens.

With these media queries, our portfolio app should now be responsive and adapt well to various screen sizes.

## Summary

Congratulations! You have successfully created a responsive portfolio app using HTML and CSS. In this tutorial, you learned how to build a multi-section portfolio with a header banner, education, projects, experience, and contact sections. We also added media queries to ensure that the app looks great on different devices.

Remember that you can further customize the app and add more content and styling to make it truly unique to your needs. Additionally, consider incorporating JavaScript to add interactivity and further enhance the user experience. Keep learning and experimenting to continue improving your web development skills. Happy coding!