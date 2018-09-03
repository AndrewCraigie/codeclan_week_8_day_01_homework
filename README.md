# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using no frameworks, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?
  *The routes are defined in the create_router.js file using express methods*
2. What are the the responsibilities of server.js?
  *server.js imports the required modules for express, the app and the MongoClient.
   It defines the path to be used for public files, configures express, establishes
   the database connection and sets the port to listen on*
3. What are the responsibilities of the `gamesRouter`?
  *The gamesRouter is an instance of an express Router. It defines the routes for
   the server using router methods - get, post, delete and put. The code within these
   methods receives requests and sent body objects, performs actions actions on the
   collection object and sends responses to the client*
4. What process does the the client (front-end) use to communicate with the server?
  *The client uses http GET, POST, DELETE and PUT methods to communicate to the server
   including, where appropriate JSON strings in the body of the requests and receiving  
   JSON strings in the responses, where appropriate*
5. Which of the games API routes does the front-end application consume (i.e. make requests to)?
  *GET - get '/', POST post '/', DELETE delete /:id*

## Extensions

1. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?
  *The MongoDB Driver acts an an interface between the server-side javascript code and the
   MongoDB database application*
2. Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?
 *The ObjectId provides and unique ID to retrieve a specified record, update it or to delete it.*
