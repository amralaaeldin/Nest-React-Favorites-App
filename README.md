# Nest.js/ React.js Fullstack App

This is a fullstack application built with Nest.js and React.js. It is a simple favorites app that allows users to add and remove their favorite items. The app uses PostgreSQL as the database and Redis for caching.

The main data source of the app is [OMDb API]('https://www.omdbapi.com/').

## Features

- **Favorites**: Add, update, load and remove favorite items.

- **Caching**: Cache favorite items using Redis.

- **Pagination**: Paginate favorite items.

- **Search**: Search for favorite items.

- **Authentication**: Signup, login, logout, and Refresh Tokens.

## Requirements

- Node.js
- npm
- React.js
- Nest.js
- PostgreSQL
- Redis
- Docker (optional)

## Installation

### Without Docker

#### Step 1: Clone the Repository & Install Dependencies

Clone the repository to your local machine:

```bash
git clone --recurse-submodules https://github.com/amralaaeldin/Nest-React-Favorites-App
cd Nest-React-Favorites-App

cd server
npm install

cd ../client
npm install
```

#### Step 2: Define Environment Variables

- Create a `.env` file in the `server` directory and define the environment variables in .env.example file.

- - Set the DB_URL to your postgres database url.

```bash
PORT=3000
DB_URL=postgresql://postgres:password@127.0.0.1:5432/movies_db?schema=public
JWT_SECRET=your_jwt_secret_key
SALT_ROUNDS=10
REDIS_URL=redis://localhost:6379
OMDB_API_KEY=81e71765
```

- Create a `.env` file in the `client` directory and define the environment variables in .env.example file.

```bash
VITE_SERVER_URI=http://localhost:3000
```

#### Step 3: Start the Development Server

You can start the development server using the following command:

```bash
cd server
npm run migtate
npm run start:dev
```

```bash
cd client
npm run dev
```

You can access the application at `http://localhost:5173`.

### With Docker

#### Step 1: Clone the Repository

Clone the repository to your local machine:

```bash
git clone --recurse-submodules https://github.com/amralaaeldin/Nest-React-Favorites-App
cd Nest-React-Favorites-App
```

#### Step 2: Build the Docker Image using Docker Compose

Build the Docker image using the following command:

```bash
docker-compose up --build
```

#### Step 3: Start the Development Server

You can access the application at `http://localhost:5173`.

## Troubleshooting

If you run into issues:

- Ensure Docker is running if you're using Docker.
- Make sure you have the correct file permissions if you're running on a local system.
- Check your .env file for any configuration mistakes (like the wrong database credentials).
