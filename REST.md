# Introduction to REST

REST (Representational State Transfer) is an architectural style widely used for building APIs, enabling communication between systems over the web. It focuses on resources, represented by URLs, and uses HTTP methods to perform actions.

## Key Concepts

### 1. **Resources**
In REST, everything is considered a **resource**. Resources can be any entity in the system, such as users, products, or orders. Each resource is identified by a **unique URL**.

- Example URL for a user resource:
  ```
  https://api.example.com/users/1
  ```

### 2. **HTTP Verbs**
HTTP verbs define the actions to be taken on the resources.

- **GET**: Retrieves data from a resource.
- **POST**: Creates a new resource.
- **PUT**: Updates an existing resource.
- **DELETE**: Removes a resource.
- **PATCH**: Partially updates a resource.

#### Example:
- **GET** `/users/1`: Returns details of the user with ID 1.
- **POST** `/users`: Creates a new user.
- **PUT** `/users/1`: Updates the user with ID 1.
- **DELETE** `/users/1`: Deletes the user with ID 1.

### 3. **Structure of a REST URL**
A REST API URL follows a clear structure that represents the resource.

- **Endpoint**: `https://api.example.com/users`
- **Specific Resource**: `https://api.example.com/users/1`

### 4. **Data Format**
Most REST APIs return data in **JSON** format, which is lightweight and easy to parse.

- Example of a JSON response:
  ```json
  {
    "id": 1,
    "name": "John Doe",
    "email": "john.doe@example.com"
  }
  ```

### 5. **HTTP Status Codes**
REST APIs use HTTP status codes to indicate the outcome of requests:

- **200 OK**: Request successful.
- **201 Created**: Resource created successfully.
- **204 No Content**: Request processed, no content returned (used after a DELETE).
- **400 Bad Request**: Invalid request (e.g., invalid data).
- **401 Unauthorized**: Authentication required or invalid.
- **404 Not Found**: Resource not found.
- **500 Internal Server Error**: Server encountered an error.

### 6. **Authentication**
Many REST APIs require some form of authentication to ensure that only authorized users can access certain endpoints.

- **Bearer Token** (JWT): A token is sent in the request header.
  ```http
  GET /users HTTP/1.1
  Host: api.example.com
  Authorization: Bearer <token>
  ```

## Practical Example of Routes

### 1. List Users
- **GET** `/users`
- Response:
  ```json
  [
    {"id": 1, "name": "John"},
    {"id": 2, "name": "Jane"}
  ]
  ```

### 2. Create a New User
- **POST** `/users`
- Request Body:
  ```json
  {
    "name": "New User",
    "email": "new@example.com"
  }
  ```
- Response:
  ```json
  {
    "id": 3,
    "name": "New User",
    "email": "new@example.com"
  }
  ```

### 3. Update an Existing User
- **PUT** `/users/1`
- Request Body:
  ```json
  {
    "name": "John Updated",
    "email": "john.updated@example.com"
  }
  ```
- Response:
  ```json
  {
    "id": 1,
    "name": "John Updated",
    "email": "john.updated@example.com"
  }
  ```

### 4. Delete a User
- **DELETE** `/users/1`
- Response:
  ```json
  {
    "message": "User deleted successfully"
  }
  ```

---

This is a basic introduction to REST, a crucial concept for building modern APIs.
