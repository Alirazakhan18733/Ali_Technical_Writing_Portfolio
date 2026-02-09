# REST API Overview

## Purpose
The REST API enables developers to integrate external applications
with the platform programmatically.

## Base URL
https://api.example.com/v1

## Supported HTTP Methods
- GET
- POST
- PUT
- DELETE

## Data Format
- Requests and responses use JSON.
- UTF‑8 encoding is supported.

## Versioning
- API versions are specified in the URL.
- Backward‑compatible changes are introduced in minor versions.

## Rate Limiting
- Requests are limited per API key.
- Exceeding limits returns HTTP 429 (Too Many Requests).

## Common Use Cases
- User management
- Message retrieval
- Automation workflows
