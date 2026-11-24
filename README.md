<img width="2522" height="1664" alt="4" src="https://github.com/user-attachments/assets/dc7fd3bf-2eb9-4adf-9c2d-f86a83a97569" /># Secure Connect and Communication Platform

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
<img width="2590" height="1664" alt="1" src="https://github.com/user-attachments/assets/b9da7f78-585f-491e-a583-4e0e5c986972" />

<img width="2574" height="1664" alt="2" src="https://github.com/user-attachments/assets/18b4556c-f986-4526-8508-bb54be3179cd" />


### Notes API
<img width="2528" height="1682" alt="3" src="https://github.com/user-attachments/assets/510826a4-150d-4c97-a23f-e0d89d77b77f" />

<img width="2522" height="1664" alt="4" src="https://github.com/user-attachments/assets/ca64883f-954a-48bb-b8d0-ae90998f8796" />

<img width="2580" height="1664" alt="5" src="https://github.com/user-attachments/assets/96519160-4859-4270-9e44-73b63028a251" />


### Real-Time Chat

<img width="2904" height="1472" alt="6" src="https://github.com/user-attachments/assets/fbba38b0-afd6-478a-9fd2-abbf75834fa2" />
