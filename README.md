# Team Task Manager

A full-stack team and project task management application built with the MERN stack.

## Features

- User signup and login with JWT authentication
- Password hashing with bcrypt
- Role-based user roles (Admin, Manager, and Team Member)
- Project creation and management
- Task assignment, status tracking, and due dates
- Dashboard for viewing project and task information
- REST API built with Express and MongoDB/Mongoose

## Tech Stack

**Frontend:** React, Vite, React Router, Axios, CSS  
**Backend:** Node.js, Express, JWT, bcrypt  
**Database:** MongoDB, Mongoose

## Project Structure

```text
team-task-manager/
├── client/          # React frontend
├── server/          # Express REST API
├── Screenshots/     # Application screenshots
├── render.yaml      # Render frontend deployment configuration
└── README.md
```

## Local Setup

### Requirements
- Node.js and npm
- A MongoDB database (local MongoDB or MongoDB Atlas)

### 1. Configure the backend

```bash
cd server
npm install
```

Create a `server/.env` file locally with your own values:

```dotenv
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=replace_with_a_long_random_secret
```

Do not commit `.env` or share its values publicly.

Start the API:

```bash
npm run dev
```

The server starts on port `5000` by default.

### 2. Configure the frontend

In a second terminal:

```bash
cd client
npm install
npm run dev
```

The Vite development server will print the local URL in the terminal.

The frontend currently uses the deployed API URL configured in `client/src/api/axios.js`. To use a local backend, change the `baseURL` to `http://localhost:5000/api`.

## Screenshots

Screenshots of the dashboard, login, project creation, and task creation are available in the `Screenshots/` directory.

## Notes

This repository is a portfolio project. Review and test authorization rules before using it with real users or sensitive data.
