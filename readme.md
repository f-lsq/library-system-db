Documentation Reference: https://github.com/nadialefebvre/library

# Library System Database

This project was built as a means to learn ExpressJS in conjunction with Mongo Atlas (10 March 2023).

## Overview
This simple Javascript server acts as a basic library managemement system, allowing users to manage a collection of books. Users will be able to perform CRUD (Create, Delete, Update, Delete) operations on the books through a set of RESTFUL API endpoints. This application was built using the ExpressJS framework and utilises a Mongo Database for database interactions.

Here is a simple entity relationship diagram of the library system
![alt text](assets/library-erd.png)

## Getting Started

To run the Library System server,

1. Install the following packages from Node.JS (Express, CORS, DotEnv and MondoDB)
```
npm install express cors dotenv mongodb
```

2. Install Node Monitor
```
npm install -g nodemon
```

3. Start the server using Node Monitor
```
nodemon
```

The server will start and the API endpoints may be reached using tools such as Advanced REST Client (ARC), Postman or Insomnia

## API Endpoints
The following API endpoints are available to perform the CRUD operations.

### Books
* `GET /books` : Retrieve information of all books
* `POST /books` : Create a new book
* `PUT /books/{bookid}` : Update details of an existing book
* `DELETE /books/{bookid}` : Delete an existing book

### Users
* `POST /user` : Create a new user
* `POST /login` : Generate JSONWebToken via user login (expires in 3 days)
* `POST /profile` : Access protected route via valid JSONWebToken

## Example Usage
Here are some examples of how you can interact with the API and how it will be logged in MongoDB.

### Books 
* Retreve information of all books
```
GET http://localhost:3001/books
```
Example of successful retrival of book information in ARC
![alt text](assets/create-books.png)

Example of book information stored in MongoDB
![alt text](assets/create-books-db.png)

* Create a new book
* Update details of an existing book
* Delete an existing book

### Users
* Create a new user
* Generate JSONWebToken via user login (expires in 3 days)
* Access protected route via valid JSONWebToken

## Technological Stacks Used
* JavaScript
* NPM Packages (Express, CORS, DotEnv)
* Mongo Atlas Database