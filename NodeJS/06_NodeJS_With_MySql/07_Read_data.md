# Retrieving and Filtering Data from a MySQL Table Using Express.js

In this tutorial, we will focus on retrieving and filtering data from an existing MySQL table using an Express.js application. Ensure you have a configured MySQL connection and an existing Express project set up before proceeding. We will not cover the basic setup of the Express.js application.

## Step 1: Install the Required Dependencies

Make sure you have the `mysql2` library already installed in your project. If not, you can install it using the following command:

```bash
npm install mysql2 --save
```

## Step 2: Create a Route to Retrieve Data

Now, let's create a route in your Express application that allows you to retrieve data from a MySQL table. Here's an example route that listens for a `GET` request to `/getdata`:

```javascript
const express = require('express');
const db = require('./db'); // Import the database connection

const app = express();
const port = 3000;

// Retrieve and filter data from a MySQL table
app.get('/getdata', async (req, res) => {
  try {
    // Optional query parameters for filtering (e.g., ?name=John&city=NewYork)
    const { name, city } = req.query;

    // Build the SQL query with optional filters and ordering (replace with your table name)
    let selectDataSQL = 'SELECT * FROM your_table_name';
    
    // Add WHERE clauses based on query parameters
    const whereClauses = [];
    const queryParams = [];
    
    if (name) {
      whereClauses.push('name = ?');
      queryParams.push(name);
    }
    
    if (city) {
      whereClauses.push('city = ?');
      queryParams.push(city);
    }
    
    if (whereClauses.length > 0) {
      selectDataSQL += ` WHERE ${whereClauses.join(' AND ')}`;
    }

    // Add ORDER BY clause
    selectDataSQL += ' ORDER BY id';

    // Query the MySQL server to retrieve and filter data from the table
    const [rows, fields] = await db.query(selectDataSQL, queryParams);

    res.status(200).json(rows);
  } catch (error) {
    console.error('Error retrieving data from the table:', error);
    res.status(500).json({ error: 'An error occurred while retrieving data' });
  }
});

app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
```

In this route, we use query parameters to filter the data based on specific criteria such as `name` and `city`. The `selectDataSQL` query is built dynamically, including the `WHERE` clauses for the specified filters and an `ORDER BY` clause to sort the results by the `id` column. Replace `your_table_name` with the actual name of your table and adjust the SQL query and route handlers as needed for your application.

## Step 3: Start Your Express Application

Start your Express application by running the following command:

```bash
node app.js
```

Replace `app.js` with the name of your main application file.

## Step 4: Retrieve and Filter Data

To retrieve and filter data from the table, make a `GET` request to the `/getdata` route using a tool like Postman or by sending an HTTP request from your application code. Include the desired query parameters in the URL to filter the results based on your criteria (e.g., `?name=John&city=NewYork`).

After successful execution, you should receive a JSON response with the filtered data from the MySQL table.

Your Express.js application is now set up to retrieve and filter data from your MySQL table. You can extend this setup to include more complex queries, additional filters, and pagination as needed for your application.