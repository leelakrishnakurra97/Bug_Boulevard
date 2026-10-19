# Bug Boulevard

Bug Boulevard is a multiplayer debugging game where players solve code challenges and compete in game rooms.

## Stack

- React, TypeScript, and Vite
- Express, TypeScript, and Socket.IO
- MongoDB with Mongoose (optional for local development)

## Requirements

- Node.js and npm
- MongoDB only if you want persistent database-backed data

## Setup

Install frontend dependencies from the project root:

```sh
npm install
```

Install backend dependencies:

```sh
cd server
npm install
```

The backend can run without a database connection. To use MongoDB, create `server/.env` from `server/.env.example` and set `MONGODB_URI` to your own connection string. Never commit `.env` files or credentials.

## Run locally

Start the backend in one terminal:

```sh
cd server
npm run dev
```

Start the frontend in another terminal, from the project root:

```sh
npm run dev
```

Open the local URL printed by Vite (usually `http://localhost:5173`). The backend listens on port `4000` by default.

## Checks

From the project root:

```sh
npm run lint
npm run build
```

From `server`:

```sh
npm run typecheck
npm run build
```

## Backend routes

- `GET /api/health`
- `POST /api/auth/register`
- `POST /api/auth/login`
- `GET /api/leaderboard`
- `POST /api/games`
- `GET /api/games/:id`
- `GET /api/lobby`
- `POST /api/lobby/join`
- `POST /api/lobby/leave`
