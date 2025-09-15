# User Management API - Starter Code

⚠️ **EDUCATIONAL PURPOSE**: This code contains intentional security vulnerabilities for learning. Do NOT use in production!

## Overview
Basic Flask API for user management. Your assignment is to transform this into a secure, professionally configured repository.

## Current Features
- User registration
- User login
- Basic user listing
- Health check endpoint

## Known Issues (Your Assignment)
This code has multiple security vulnerabilities you need to identify and fix:
- Hardcoded secrets
- SQL injection vulnerabilities
- Weak password hashing
- Missing input validation
- Insecure logging

## Setup Instructions

```bash
# Install dependencies
pip install -r requirements.txt

# Run the application
python app.py
```

## API Endpoints

### Health Check
```bash
GET /health
```

### Create User
```bash
POST /users
{
    "username": "john_doe",
    "password": "password123"
}
```

### Login
```bash
POST /login
{
    "username": "john_doe",
    "password": "password123"
}
```

### List Users
```bash
GET /users
```

## Your Mission
Transform this basic code into a professional, secure repository by:
1. Setting up proper branch protection and workflows
2. Implementing security scanning and pre-commit hooks
3. Fixing all security vulnerabilities
4. Adding professional documentation
5. Creating automated CI/CD pipeline