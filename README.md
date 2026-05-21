# Todo App (MERN)

A modern, responsive Todo application built with the MERN stack.

## Features
- Create, read, update, and delete todos
- Responsive UI with a modern blue theme
- Loading states and error handling
- RESTful API with Express & MongoDB (Mongoose)
- Environment‑based configuration

## Project Structure

root/
├─ backend/
│  ├─ package.json
│  ├─ server.js
│  └─ .env.example
├─ frontend/
│  ├─ package.json
│  ├─ index.html
│  ├─ src/
│  │  ├─ main.jsx
│  │  ├─ App.jsx
│  │  └─ App.css
└─ README.md


## Prerequisites
- Node.js (v20 or later)
- npm or yarn
- MongoDB instance (local or Atlas)

## Setup Instructions
### 1. Clone the repository
bash
git clone <repo-url>
cd <repo-folder>

### 2. Backend
bash
cd backend
npm install   # or yarn
cp .env.example .env
# Edit .env if needed (MongoDB URI, PORT)
npm run dev   # starts server with nodemon

The API will be available at `http://localhost:5000/api/todos`.

### 3. Frontend
bash
cd ../frontend
npm install   # or yarn
# Create a .env file for Vite (optional)
# VITE_API_URL=http://localhost:5000
npm run dev   # starts Vite dev server

Open `http://localhost:5173` (default Vite port) in your browser.

### 4. Production Build
#### Backend
bash
npm run start   # after setting proper PORT and MONGO_URI

#### Frontend
bash
npm run build
# Serve the `dist` folder with any static server (e.g., serve, nginx)


## API Endpoints
| Method | Endpoint            | Description                     |
|--------|---------------------|---------------------------------|
| GET    | `/api/todos`        | Get all todos                   |
| POST   | `/api/todos`        | Create a new todo (`{text}`)    |
| PUT    | `/api/todos/:id`    | Update a todo (e.g., toggle `completed`) |
| DELETE | `/api/todos/:id`    | Delete a todo                   |

## Environment Variables
- **Backend** (`.env`)
  - `PORT` – Port for Express server (default 5000)
  - `MONGO_URI` – MongoDB connection string
- **Frontend** (`.env` for Vite)
  - `VITE_API_URL` – Base URL of the backend API (default `http://localhost:5000`)

## License
MIT
