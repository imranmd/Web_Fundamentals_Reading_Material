# Updating Documents in MongoDB Using Node.js

In this tutorial, we will guide you through the process of updating documents in a MongoDB collection using Node.js. We will use the `updateOne()` and `updateMany()` methods to modify documents based on specific criteria.

## Prerequisites

Before you begin, make sure you have the `mongodb` library installed in your Node.js project. You can install it using npm:

```bash
npm install mongodb --save
```

## Step 1: Import the MongoDB Client

In your Node.js application, import the MongoDB client:

```javascript
const { MongoClient } = require('mongodb');
```

## Step 2: Set Up a MongoDB Connection

Create a MongoDB connection using the `MongoClient` and specify the connection URL for your MongoDB server. Replace `'mongodb://localhost:27017'` with the actual MongoDB connection URL:

```javascript
const url = 'mongodb://localhost:27017';
const client = new MongoClient(url, { useUnifiedTopology: true });
```

## Step 3: Create a Function to Update Documents

Define a function to update documents in a MongoDB collection based on specific criteria. In this example, we'll use two functions: one for updating a single document (`updateOne()`), and one for updating multiple documents (`updateMany()`). Customize the collection name, update criteria, and update operations as needed:

### Update a Single Document:

```javascript
async function updateSingleDocument() {
  try {
    // Connect to the MongoDB server
    await client.connect();

    // Specify the database and collection name
    const dbName = 'mydatabase';
    const collectionName = 'users';

    // Get a reference to the database
    const db = client.db(dbName);

    // Get a reference to the collection
    const collection = db.collection(collectionName);

    // Define the update criteria (e.g., update a user with a specific name)
    const updateCriteria = { name: 'John' };

    // Define the update operation (e.g., set a new age value)
    const updateOperation = { $set: { age: 35 } };

    // Update a single document matching the criteria
    const result = await collection.updateOne(updateCriteria, updateOperation);

    console.log(`${result.modifiedCount} document updated.`);
  } catch (error) {
    console.error('Error updating single document:', error);
  } finally {
    // Close the MongoDB client
    await client.close();
  }
}
```

### Update Multiple Documents:

```javascript
async function updateMultipleDocuments() {
  try {
    // Connect to the MongoDB server
    await client.connect();

    // Specify the database and collection name
    const dbName = 'mydatabase';
    const collectionName = 'users';

    // Get a reference to the database
    const db = client.db(dbName);

    // Get a reference to the collection
    const collection = db.collection(collectionName);

    // Define the update criteria (e.g., update users older than 40)
    const updateCriteria = { age: { $gt: 40 } };

    // Define the update operation (e.g., set a new status)
    const updateOperation = { $set: { status: 'inactive' } };

    // Update multiple documents matching the criteria
    const result = await collection.updateMany(updateCriteria, updateOperation);

    console.log(`${result.modifiedCount} documents updated.`);
  } catch (error) {
    console.error('Error updating multiple documents:', error);
  } finally {
    // Close the MongoDB client
    await client.close();
  }
}
```

## Step 4: Call the Functions to Update Documents

Call the functions to update documents based on the specified criteria:

```javascript
updateSingleDocument();
updateMultipleDocuments();
```

## Step 5: Run Your Node.js Application

Run your Node.js application using the following command:

```bash
node app.js
```

Replace `app.js` with the name of your main application file.

## Step 6: Verify the Updates

After running your Node.js application, the documents that match the specified update criteria will be modified in the MongoDB collection. You can verify the updates using a MongoDB client or by running MongoDB commands.

Your Node.js application is now set up to update documents in a MongoDB collection based on specific criteria using the `updateOne()` and `updateMany()` methods. Customize the collection name, update criteria, update operations, and include additional options as required for your application.