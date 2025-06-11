# django-auth-service

Authentication microservice that provides JWT token generation and validation for the Django microservices ecosystem.

## Features

- JWT token generation and refresh endpoints
- User and group management APIs
- Protected endpoints requiring authentication
- Stateless JWT authentication

## Endpoints

- `POST /api/token/`: Get access and refresh tokens
- `POST /api/token/refresh/`: Refresh access token
- `POST /api/token/verify/`: Verify token validity
- `GET /users/`: List users (protected)
- `GET /groups/`: List groups (protected)

## Usage

Run the service:
```
python manage.py runserver 8001
```

Get a token:
```bash
curl -X POST http://localhost:8001/api/token/ \
  -H "Content-Type: application/json" \
  -d '{"username": "admin", "password": "password"}'
```