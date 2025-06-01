# 🔐 Dynamic JWT Authentication with Flask

A lightweight Flask app showcasing **dynamic JWT-based authentication** for securing API endpoints — with tokens generated uniquely every time the app runs.

> 🧠 Perfect for learning how to implement secure, stateless authentication for your own Python APIs.

---

## 🚀 Features

✅ Runtime-generated JWT token  
✅ Token-based protection for endpoints  
✅ Dynamic configuration via authenticated `/info`  
✅ Simple `/run` endpoint for demo processing  
✅ Educational `demo_script.py` included  
✅ `.env` support for secret management

---

## 📂 Project Structure

dynamic-jwt-authentication/
├── app.py # Flask app with JWT auth
├── demo_script.py # Script to demo usage of endpoints
├── .env.example # Template for environment variables
├── requirements.txt # Project dependencies
└── README.md # You're here :)

## 🧠 How It Works

- generate_runtime_token() creates a JWT at runtime using a UUID + timestamp.

- verify_jwt_token() checks the Authorization header and validates the token.

- Endpoints are protected and only respond to requests with a valid JWT.

## ⚙️ How to Use
### 🔐 Token Authentication
Copy the printed token from the console:
==================================================
NEW RUNTIME TOKEN GENERATED:
adfhghuqwertgjiuyyhnhuopoiyg...
==================================================

Copy the token and pass it at Headers of endpoints request body as:
==================================================
Header of /info endpoint:
Key                         Value
Authorization            Bearer adfhghuqwertgjiuyyhnhuopoiyg...
==================================================

## 🧬 How JWT Token Generation Works
### 🔐 Algorithm Details:

Algorithm: HS256 (HMAC + SHA-256)

Library: PyJWT

Secret: A secure key defined in your .env file (via JWT_SECRET_KEY)

### 🔑 Why HS256?

Symmetric: Uses the same secret for signing and verifying

Fast & Lightweight: Ideal for internal or lightweight API authentication

Secure: As long as the secret is strong and kept private
