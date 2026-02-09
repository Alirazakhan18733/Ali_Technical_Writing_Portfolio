# API Endpoints

## Overview
This document describes the available REST API endpoints
and their supported operations.

---

## Users

### GET /users
Retrieve a list of users.

**Request**
- Method: GET
- Endpoint: `/users`

**Response**
- 200 OK: Returns a list of users

---

### POST /users
Create a new user.

**Request**
- Method: POST
- Endpoint: `/users`

**Request Body**

```json
{
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```
**Response**

- 201 Created — User successfully created


### PUT /users/{id}
Update an existing user.

**Request**
- Method: PUT
- Endpoint: `/users/{id}`

**Response**
- 200 OK — User updated successfully


### DELETE /users/{id}
Delete a user.

**Request**
- Method: DELETE
- Endpoint: `/users/{id}`

**Response**
- 204 No Content — User deleted

