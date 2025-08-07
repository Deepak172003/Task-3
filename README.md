# Book API

A simple RESTful API for managing a collection of books, built with Express.js.

## Features

- List all books
- Add a new book
- Update an existing book
- Delete a book
  

### Running the Server


node book-api/index.js

The server will start at [http://localhost:3000](http://localhost:3000).

## API Endpoints

### Get all books


GET /books

**Response:**
json
[
  {
    "id": 1,
    "title": "The Alchemist",
    "author": "Paulo Coelho"
  }
]


### Add a new book


POST /books


**Request Body:**
json
{
  "title": "Book Title",
  "author": "Author Name"
}


**Response:**
json
{
  "id": 3,
  "title": "Book Title",
  "author": "Author Name"
}


### Update a book

PUT /books/:id

**Request Body:** (any or both fields)
json
{
  "title": "Updated Title",
  "author": "Updated Author"
}

**Response:**  
Returns the updated book object.

### Delete a book

DELETE /books/:id

**Response:**
json
{
  "message": "Book deleted successfully"
}

## License

This project is licensed under the ISC License.
