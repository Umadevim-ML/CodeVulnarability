# Backend - Code Vulnerability Scanner

The backend service for the Code Vulnerability Scanner application. Built with Node.js and Express, it provides APIs for code analysis, user authentication, and vulnerability scanning using AI.

## Features

- **User Authentication**: Secure login and signup with JWT tokens
- **Code Scanning**: Analyze code for vulnerabilities using AI
- **Rule-based Analysis**: Custom scanning rules for different code patterns
- **Gemini AI Integration**: Leverage Google Gemini AI for intelligent code analysis

## Technologies

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose
- **AI Service**: Google Gemini API
- **Authentication**: JWT

## Project Structure

```
backend/
├── server.js          # Main server entry point
├── scanner.js         # Core scanning logic
├── rules.js           # Vulnerability scanning rules
├── package.json       # Dependencies
├── AUTH_SETUP.md      # Authentication setup guide
├── ai/
│   └── gemini.js      # Gemini AI integration
├── models/
│   └── User.js        # User database model
└── routes/
    └── auth.js        # Authentication endpoints
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB instance
- Google Gemini API key

### Installation

1. Navigate to the backend directory:

   ```bash
   cd backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Configure environment variables (see [AUTH_SETUP.md](AUTH_SETUP.md))

### Running the Server

```bash
npm start
```

The server will start on the configured port (default: 5000).

## API Endpoints

### Authentication

- `POST /api/auth/signup` - Register a new user
- `POST /api/auth/login` - Authenticate user

### Scanning

- `POST /api/scan` - Submit code for vulnerability scanning
- `GET /api/results/:id` - Retrieve scan results

## Environment Variables

Required environment variables (see AUTH_SETUP.md for detailed setup):

- `PORT` - Server port
- `MONGODB_URI` - MongoDB connection string
- `JWT_SECRET` - JWT secret key
- `GEMINI_API_KEY` - Google Gemini API key

## Development

For more details on authentication setup, refer to [AUTH_SETUP.md](AUTH_SETUP.md).

## License

MIT
