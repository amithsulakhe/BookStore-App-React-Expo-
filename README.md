# Bookstore Backend API

Backend server for the Bookstore application built with Node.js and Express.

## Prerequisites

- Node.js (v14 or higher)
- MongoDB database
- Cloudinary account (for image storage)

## Installation

1. Install dependencies:
```bash
npm install
```

## Environment Variables

Create a `.env` file in the root of the `backend` directory with the following variables:

```env
# Server Configuration
PORT=3000

# Database Configuration
MONGO_URI=your_mongodb_connection_string

# JWT Authentication
JWT_SECRET=your_jwt_secret_key

# Cloudinary Configuration
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# API URL (for cron job)
API_URL=your_backend_api_url
```

### Environment Variables Explained

- **PORT**: The port on which the server will run (default: 3000)
- **MONGO_URI**: MongoDB connection string (e.g., `mongodb://localhost:27017/bookstore` or MongoDB Atlas connection string)
- **JWT_SECRET**: Secret key used to sign and verify JSON Web Tokens for authentication
- **CLOUDINARY_CLOUD_NAME**: Your Cloudinary cloud name
- **CLOUDINARY_API_KEY**: Your Cloudinary API key
- **CLOUDINARY_API_SECRET**: Your Cloudinary API secret
- **API_URL**: Full URL of your deployed backend API (used by cron job to keep the server alive)

## Starting the Project

To start the development server:

```bash
npm run dev
```

The server will start on the port specified in your `.env` file (default: 3000).

The `dev` script runs the server with `--watch` flag, which automatically restarts the server when file changes are detected.

## API Endpoints

- **Authentication**: `/api/auth`
- **Books**: `/api/books`

## Features

- User authentication with JWT
- Book management
- Image upload using Cloudinary
- Cron job for server health checks
- MongoDB database integration

## Dependencies

- express - Web framework
- mongoose - MongoDB object modeling
- jsonwebtoken - JWT authentication
- bcryptjs - Password hashing
- cloudinary - Image storage and management
- cors - Cross-origin resource sharing
- dotenv - Environment variable management
- cron - Scheduled tasks

