# SkillSwap - Full Stack Application

A complete skill swapping platform built with Spring Boot backend and React frontend.

##  Quick Start

### Prerequisites
- Java 17 or higher
- Node.js 18 or higher
- MongoDB (running locally or cloud instance)

### Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd odoo-complete-main/backend
   ```

2. Start the Spring Boot application:
   ```bash
   ./mvnw spring-boot:run
   ```
   
   The backend will start on: http://localhost:8080

### Frontend Setup
1. Open a new terminal and navigate to the frontend directory:
   ```bash
   cd odoo-complete-main/frontend
   ```

2. Install dependencies (if not already installed):
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```
   
   The frontend will start on: http://localhost:5173

## 📁 Project Structure

```
odoo-complete-main/
├── backend/                 # Spring Boot application
│   ├── src/main/java/
│   │   └── com/example/
│   │       ├── controller/  # REST controllers
│   │       ├── service/     # Business logic
│   │       ├── repository/  # Data access
│   │       ├── model/       # Entity models
│   │       ├── dto/         # Data transfer objects
│   │       ├── security/    # JWT authentication
│   │       └── config/      # Configuration classes
│   └── src/main/resources/
│       └── application.properties
└── frontend/               # React + TypeScript application
    ├── src/
    │   ├── components/     # React components
    │   ├── pages/          # Page components
    │   ├── services/       # API services
    │   ├── config/         # Configuration
    │   └── hooks/          # Custom hooks
    └── package.json
```

## 🔧 Configuration

### Backend Configuration
- **Port**: 8080
- **Database**: MongoDB
- **Authentication**: JWT
- **CORS**: Configured for frontend

### Frontend Configuration
- **Port**: 5173
- **API Base URL**: http://localhost:8080/api
- **Framework**: React + TypeScript + Vite
- **UI Library**: Radix UI + Tailwind CSS

## 🛠️ Available Scripts

### Backend
```bash
./mvnw clean compile    # Compile the project
./mvnw spring-boot:run  # Run the application
./mvnw test            # Run tests
```

### Frontend
```bash
npm run dev           # Start development server
npm run build         # Build for production
npm run preview       # Preview production build
npm run lint          # Run ESLint
```

## 🔐 Authentication

The application uses JWT authentication:
- Register: `POST /api/auth/register`
- Login: `POST /api/auth/login`
- Protected routes require valid JWT token

## 📊 Features

- **User Management**: Registration, login, profile management
- **Skill Swapping**: Offer and request skills
- **Real-time Chat**: WebSocket-based messaging
- **Admin Dashboard**: User management, platform messages
- **Rating System**: User feedback and ratings
- **Search & Filter**: Find users and skills

## 🐛 Troubleshooting

### Common Issues

1. **Backend won't start**:
   - Ensure MongoDB is running
   - Check port 8080 is available
   - Verify Java 17+ is installed

2. **Frontend won't start**:
   - Check port 5173 is available
   - Ensure Node.js 18+ is installed
   - Run `npm install` if dependencies are missing

3. **API connection errors**:
   - Verify backend is running on port 8080
   - Check CORS configuration
   - Ensure API_BASE_URL is correct in frontend config

4. **Database connection issues**:
   - Verify MongoDB is running
   - Check connection string in application.properties
   - Ensure database exists

### Error Codes
- **400**: Bad Request - Invalid data sent
- **401**: Unauthorized - Authentication required
- **404**: Not Found - Resource doesn't exist
- **500**: Internal Server Error - Backend issue

## 🚀 Deployment

### Backend Deployment
1. Build the JAR file:
   ```bash
   ./mvnw clean package
   ```

2. Run the JAR:
   ```bash
   java -jar target/skillswap-backend-1.0.0.jar
   ```

### Frontend Deployment
1. Build for production:
   ```bash
   npm run build
   ```

2. Serve the dist folder with a web server

## 📝 API Documentation

### Auth Endpoints
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login

### User Endpoints
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update user profile
- `GET /api/users/search` - Search users

### Swap Endpoints
- `POST /api/swaps` - Create swap request
- `GET /api/swaps` - Get swap requests
- `PUT /api/swaps/{id}/accept` - Accept swap
- `PUT /api/swaps/{id}/reject` - Reject swap

### Admin Endpoints
- `GET /api/admin/dashboard/stats` - Dashboard statistics
- `GET /api/admin/users` - Get all users
- `POST /api/admin/messages` - Send platform message

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

