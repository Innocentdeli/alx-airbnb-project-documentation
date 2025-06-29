# Backend Feature Requirements Specification

This document outlines the technical and functional requirements for three core backend features of the property booking platform: **User Authentication**, **Property Management**, and the **Booking System**.

---

## 1. 🔐 User Authentication

### Functional Requirements
- Users can register with email and password.
- Users can log in using valid credentials.
- JWT tokens will be issued upon successful login.
- Role-based access control (guest, host, admin).

### API Endpoints
- `POST /api/register`  
  Registers a new user.
  
- `POST /api/login`  
  Authenticates the user and returns a JWT token.

- `GET /api/profile`  
  Returns the current user's profile (authenticated route).

### Input Specification
**POST /api/register**
```json
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "john@example.com",
  "password": "securePassword123",
  "role": "guest"
}

