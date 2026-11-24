# Secure Connect and Communication Platform

Lab 4 - Web Dev III

## Setup

1. Install dependencies
   ```bash
   npm install
   ```
2. Create a `.env` file (see `.env.example`)
   ```
   PORT=5000
   MONGO_URI=mongodb://127.0.0.1:27017/secure_connect
   JWT_SECRET=your_secret_here
   JWT_EXPIRES_IN=1h
   ADMIN_EMAIL=admin@example.com
   ```
3. Start MongoDB, then run the server
   ```bash
   node server.js
   ```
   Server runs at `http://localhost:5000`.

## API Endpoints

| Method | Route | Access | Description |
|---|---|---|---|
| POST | /api/auth/signup | Public | Register a user |
| POST | /api/auth/login | Public | Login and get JWT |
| GET | /api/notes | JWT | Get my notes |
| POST | /api/notes | JWT | Create a note |
| GET | /api/notes/:id | JWT | Get a note |
| PUT | /api/notes/:id | JWT | Update a note |
| DELETE | /api/notes/:id | JWT | Delete a note |
| GET | /api/admin/users | Admin | List all users |

Requests without a token return `403 No token provided`.

## Real-Time Chat

Open `http://localhost:5000` in two browser windows, log in with different users, and chat in the `general` room.

## Screenshots

### Signup and Login


### Notes API


### Real-Time Chat
