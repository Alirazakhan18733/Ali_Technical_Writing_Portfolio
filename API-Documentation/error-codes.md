# Error Codes and Handling

This document describes common API error responses and how
clients should handle them.

---

## Error Response Format

All error responses follow a consistent JSON structure:

```json
{
  "error": {
    "code": "string",
    "message": "Human‑readable description"
  }
}
```

## Common Error Codes

### 400 Bad Request

The request is invalid or malformed.

**Possible causes**
- Missing required fields
- Invalid request body format
- Unsupported or incorrect parameter values

**Recommended action**
- Validate request parameters before retrying.
- Ensure the request body matches the documented schema.

---

### 401 Unauthorized

Authentication failed or the access token is missing.

**Possible causes**
- Invalid access token
- Expired access token
- Authorization header not provided

**Recommended action**
- Generate a new access token.
- Include a valid `Authorization` header in the request.

---

### 403 Forbidden

The client is authenticated but does not have permission to perform the action.

**Possible causes**
- Insufficient user privileges
- Access restricted to specific roles

**Recommended action**
- Verify user roles and permissions.
- Contact an administrator if access is required.

---

### 404 Not Found

The requested resource does not exist.

**Possible causes**
- Incorrect resource identifier
- Resource has been deleted or is unavailable

**Recommended action**
- Verify the resource ID.
- Confirm the resource exists before retrying.

---

### 409 Conflict

The request could not be completed due to a conflict with the current state.

**Possible causes**
- Duplicate resource creation
- Conflicting updates

**Recommended action**
- Resolve the conflict and retry the request.
- Fetch the latest resource state before updating.

---

### 429 Too Many Requests

The client has exceeded the allowed request rate.

**Possible causes**
- Too many requests sent in a short time period

**Recommended action**
- Implement request throttling.
- Retry the request using exponential backoff.


### 500 Internal Server Error

An unexpected error occurred on the server.

**Possible causes**
- Temporary service disruption
- Unhandled server-side exception

**Recommended action**
- Retry the request after a short delay.
- Contact support if the issue persists.


