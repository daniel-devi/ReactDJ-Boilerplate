### **API.md Content**

```markdown
# API Documentation

This document provides details about the API endpoints available in the ReactDJ Boilerplate backend.

---

## 🛠️ **Authentication Endpoints**

### **1. User Registration**
- **URL**: `/api/auth/register/`
- **Method**: POST
- **Request Payload**:
  ```json
  {
    "username": "username",
    "email": "youremail@example.com",  # Required
    "password": "yourpassword",       # Required
  }

  ```
- **Response**:
  ```json
  {
    "message": "User registered successfully",
    "user": {
      "id": 1,
      "first_name": "first name",
      "last_name": "last name",
      "username": "yourusername",
      "email": "youremail@example.com"
      ... other fields in the User Model
    }
  }
  ```
- **Notes**: 
  - Ensure that the email is unique.
  - Passwords should meet the minimum security requirements, in the frontend - No validation is done in the Backend.

---

### **2. User Login**
- **URL**: `/api/auth/login/`
- **Method**: POST
- **Request Payload**:
  ```json
  {
    "username": "yourusername",
    "password": "yourpassword"
  }
  ```
- **Response**:
  ```json
  {
    "access": "your_access_token",
    "refresh": "your_refresh_token"
  }
  ```
- **Notes**: 
  - Returns JWT tokens upon successful login.
  - Store the `access` token for API authentication.
  - Store the `refresh` token to refresh the `access` token.

---

### **3. JWT Token Refresh**
- **URL**: `/api/token/refresh/`
- **Method**: POST
- **Request Payload**:
  ```json
  {
    "refresh": "your_refresh_token"
  }
  ```
- **Response**:
  ```json
  {
    "access": "new_access_token"
  }
  ```
- **Notes**: 
  - Use the `refresh` token to obtain a new `access` token when it expires.

---

## 📋 **User Endpoints**

### **4. Retrieve User Profile**
- **URL**: `/api/auth/profile/`
- **Method**: GET
- **Headers**:
  ```json
  {
    "Authorization": "Bearer your_access_token"
  }
  ```
- **Response**:
  ```json
  {
    "id": 1,
    "username": "yourusername",
    "email": "youremail@example.com",
    "date_joined": "2023-11-30T10:00:00Z"
    .... other User fields
  }
  ```
- **Notes**: 
  - Requires authentication via JWT token.

---

## ⚙️ **Custom Endpoints**
Add more API endpoints here as you expand your project. Document each with a clear structure like above.

---

## 🔒 **Authentication**
- **Token Handling**: Use the `access` token in the `Authorization` header for protected routes.
- **Example**:
  ```bash
  curl -H "Authorization: Bearer your_access_token" http://localhost:8000/api/auth/profile/
  ```

---

For any additional questions or support, refer to the project’s [README](../readme.md) or contact me.
```

---
