# Go Fiber PostgreSQL Application

This project is a RESTful API built with [Go Fiber](https://gofiber.io/), a web framework inspired by Express, and PostgreSQL as the database. It demonstrates how to perform basic CRUD (Create, Read, Update, Delete) operations.

## Features

- **Fiber Framework**: Utilizes the Go Fiber framework for handling HTTP requests.
- **PostgreSQL Integration**: Connects to a PostgreSQL database to manage data persistence.
- **CRUD Operations**: Provides endpoints to create, read, update, and delete records.

## Prerequisites

Before running this application, ensure you have the following installed:

- [Go](https://golang.org/dl/) (version 1.20 or higher)
- [PostgreSQL](https://www.postgresql.org/download/)

## Getting Started

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/logoes0/go-fiber-postgres.git
   cd go-fiber-postgres
   ```

2. **Set Up the Database**:

   - Create a PostgreSQL database named `fiber_demo`.
   - Update the database connection settings in the `main.go` file:

     ```go
     const (
         host     = "localhost"
         port     = 5432
         user     = "postgres"
         password = "yourpassword"
         dbname   = "fiber_demo"
     )
     ```

3. **Install Dependencies**:

   ```bash
   go mod tidy
   ```


4. **Start the Application**:

   ```bash
   go run main.go
   ```

   The server will start on `http://localhost:3000`.

## API Endpoints

- **Get All Books**: `GET /books`
- **Add a New Book**: `POST /create_books`
- **Get Book by ID**: `GET /get_book/:id`
- **Delete an Book**: `DELETE /delete_book/:id`

## Project Structure

```
.
├── main.go        # Application entry point
├── go.mod         # Go module file
├── go.sum         # Go checksums
├── models/        # Contains database models
└── storage/       # Contains database connection and queries
```

## References

- [Fiber Documentation](https://docs.gofiber.io/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

