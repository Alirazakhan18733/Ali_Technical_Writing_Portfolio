# Authentication

## Overview
The API uses token‑based authentication to ensure secure access
to protected resources.

## Authentication Method
- Bearer token authentication
- Tokens are issued by the authorization service

## Request Header
All API requests must include the following HTTP header:
Authorization: Bearer <access_token>
## Obtaining an Access Token
1. Register the application in the developer portal.
2. Generate an API token.
3. Store the token securely.

## Token Expiration
- Tokens have a limited validity period.
- Expired tokens must be regenerated.

## Security Best Practices
- Never expose tokens in client‑side code.
- Rotate tokens regularly.
- Revoke compromised tokens immediately.
