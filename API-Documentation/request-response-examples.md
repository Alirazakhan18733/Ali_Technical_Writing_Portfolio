# Request and Response Examples

This document provides sample API requests and responses
to help developers understand how to interact with the API.

---

## Create User

### Request
```http
POST /users HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john.doe@example.com"
}
```
### Response

HTTP/1.1 201 Created
Content-Type: application/json
```
{
  "id": "u12345",
  "name": "John Doe",
  "email": "john.doe@example.com",
  "status": "active"
}
```

## Get User by ID

Retrieve details for a specific user using a unique identifier.

### Request
```http
GET /users/u12345 HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
```
### Response

HTTP/1.1 200 OK
Content-Type: application/json
```
{
  "id": "u12345",
  "name": "John Doe",
  "email": "john.doe@example.com",
  "status": "active"
}
```
## Delete User

### Request
```http
DELETE /users/u12345 HTTP/1.1
Host: api.example.com
Authorization: Bearer <access_token>
```
### Response

HTTP/1.1 204 No Conten
















