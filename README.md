# Go REST API

A simple RESTful CRUD API built with **Go**, **Gin**, and **MongoDB**. The project demonstrates how to structure a basic Go backend with routes, controllers, models, and database operations.

## Tech Stack

- Go
- Gin
- MongoDB
- MongoDB Go Driver

## Features

- Create a book
- Get all books
- Get a book by ID
- Update a book
- Delete a book
- RESTful API architecture
- MongoDB database integration

## Project Structure

```text
.
├── controllers/
│   └── book_controller.go
├── models/
│   └── book.go
├── routes/
│   └── book_routes.go
├── main.go
├── go.mod
└── go.sum
```

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | `/books` | Get all books |
| GET | `/books/:id` | Get a book by ID |
| POST | `/books` | Create a new book |
| PUT | `/books/:id` | Update a book |
| DELETE | `/books/:id` | Delete a book |

## Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd go-rest-api
```

Install dependencies:

```bash
go mod download
```

## MongoDB Configuration

Make sure MongoDB is running locally or use a MongoDB Atlas cluster.

Configure your MongoDB connection string in the application according to your environment.

Example:

```text
mongodb://localhost:27017
```

## Run the Application

```bash
go run .
```

The server will start on:

```text
http://localhost:8000
```

## Example Request

### Create a Book

```http
POST /books
Content-Type: application/json
```

```json
{
  "title": "The Go Programming Language",
  "author": "Alan Donovan",
  "description": "A book about programming in Go"
}
```

### Get All Books

```http
GET /books
```

### Update a Book

```http
PUT /books/{id}
Content-Type: application/json
```

```json
{
  "title": "Updated Book",
  "author": "Updated Author",
  "description": "Updated description"
}
```

### Delete a Book

```http
DELETE /books/{id}
```

## Learning Goals

This project is intended to practice:

- Go project structure
- HTTP servers in Go
- REST API development
- Gin routing
- Request and response handling
- MongoDB integration
- CRUD operations
- JSON serialization
- Backend error handling

## License

This project is for learning and educational purposes.
