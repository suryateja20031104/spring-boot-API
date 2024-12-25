
# Goodreads Application

## Overview

The Goodreads application is a simple Java-based project built using the Spring Framework. It demonstrates a CRUD (Create, Read, Update, Delete) operation for managing books. The project uses an H2 database to store book information.

---

## Project Structure

```
src/main/java/com/example/goodreads
├── controller
│   ├── BookController.java
├── model
│   ├── Book.java
│   ├── BookRowMapper.java
├── repository
│   ├── BookRepository.java
├── service
│   ├── BookH2Service.java
├── GoodreadsApplication.java
```

### Explanation

- **controller**: Contains `BookController` which handles HTTP requests and maps them to appropriate services.
- **model**: Contains the `Book` class which represents the Book entity and `BookRowMapper` for mapping SQL results to objects.
- **repository**: Contains `BookRepository` which is responsible for interacting with the database.
- **service**: Contains `BookH2Service` which implements the business logic of the application.
- **GoodreadsApplication**: The entry point of the Spring Boot application.

---

## Features

1. **Book Management**: Add, update, retrieve, and delete books.
2. **H2 Database Integration**: Persistent storage for books using an H2 database.
3. **REST API**: A RESTful API to interact with the application.

---

## Book Model

The `Book` model consists of the following attributes:

- **id**: Unique identifier for the book.
- **name**: Name of the book.
- **imageUrl**: URL to the book's image.

### Example JSON Representation

```json
{
  "id": 1,
  "name": "The Great Gatsby",
  "imageUrl": "https://example.com/images/great-gatsby.jpg"
}
```

---

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repository.git
   ```

2. **Build the Project**:
   Ensure you have Java and Maven installed. Navigate to the project directory and run:
   ```bash
   mvn clean install
   ```

3. **Run the Application**:
   Use the following command to start the application:
   ```bash
   mvn spring-boot:run
   ```

4. **Access the Application**:
   The application will run on [http://localhost:8080](http://localhost:8080).

---

## Endpoints

### Base URL: `/api/books`

| Method | Endpoint       | Description            |
|--------|----------------|------------------------|
| GET    | `/`            | Retrieve all books    |
| GET    | `/{id}`        | Retrieve a book by ID |
| POST   | `/`            | Add a new book        |
| PUT    | `/{id}`        | Update an existing book |
| DELETE | `/{id}`        | Delete a book         |

---

## Example Usage

### Add a Book

```bash
POST /api/books
Content-Type: application/json

{
  "name": "The Great Gatsby",
  "imageUrl": "https://example.com/images/great-gatsby.jpg"
}
```

### Get All Books

```bash
GET /api/books
```

---

## Technologies Used

- **Java**
- **Spring Boot**
- **H2 Database**
- **Maven**

---


