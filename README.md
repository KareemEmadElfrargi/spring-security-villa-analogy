# Spring Boot Security & JWT (Simplified) - Simple Task

> A simplified, real-world implementation of **Spring Security 6** with **JWT** using PostgreSQL.

## 📖 The Concept 
This project demystifies Spring Security by using a **"Villa & Bodyguards"** analogy:
* **The Villa:** Your Application.
* **The Bodyguard (Filter):** Intercepts visitors at the door.
* **The ID Card (JWT):** A token issued after verification, allowing stateless access.
* **The Security Manager:** Handles authentication logic.


## 🚀 Features
* **User Registration:** Create new accounts with encrypted passwords (BCrypt).
* **Authentication:** Login and receive a JWT token.
* **Authorization:** Role-based access control (Admin vs User).
* **Stateless:** No server-side sessions; fully token-based.
* **PostgreSQL:** Robust database integration.

## 🛠️ Tech Stack
* **Java 21**
* **Spring Boot 4.0.1
* **Spring Security 6**
* **PostgreSQL**
* **JWT** (JSON Web Token)
* **Lombok**
* **Spring Web**

##  Setup & Run

1.  **Clone the repository:**
    ```bash
    git clone  https://github.com/KareemEmadElfrargi/spring-security-villa-analogy.git
    ```
2.  **Configure Database:**
    * Create a PostgreSQL database named `security_db`.
    * Update `src/main/resources/application.properties` with your credentials.
3.  **Run the App:**
    ```bash
    mvn spring-boot:run
    ```

## API Endpoints

### 1. Register (Create User)
* **POST** `/api/auth/register`
* **Body:**
    ```json
    {
      "firstname": "Kareem",
      "lastname": "Emad",
      "email": "kareem@gmail.com",
      "password": "123"
    }
    ```

### 2. Authenticate (Login)
* **POST** `/api/auth/authenticate`
* **Body:**
    ```json
    {
      "email": "kareem@gmail.com",
      "password": "123"
    }
    ```
* **Response:** Returns `{ "token": "eyJhbGci..." }`

### 3. Access Protected Route
* **Header:** `Authorization: Bearer <YOUR_TOKEN>`

---
Created with ❤️ by **Kareem El-Farargi****
