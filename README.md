<div align="center">
  <div>
    <img src="https://img.shields.io/badge/-Node.js-black?style=for-the-badge&logoColor=white&logo=nodedotjs&color=339933" alt="nodejs" />
    <img src="https://img.shields.io/badge/-Express.js-black?style=for-the-badge&logoColor=white&logo=express&color=000000" alt="expressjs" />
    <img src="https://img.shields.io/badge/-MongoDB-black?style=for-the-badge&logoColor=white&logo=mongodb&color=47A248" alt="mongodb" />
    <img src="https://img.shields.io/badge/-React_JS-black?style=for-the-badge&logoColor=white&logo=react&color=61DAFB" alt="reactjs" />
  </div>

  <h1 align="center">JobHunt</h1>
  <h3 align="center">A Full Stack Job Portal Application</h3>
</div>

## 📋 Table of Contents

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🏗️ [Project Structure](#project-structure)
6. 📝 [API Endpoints](#api-endpoints)

## <a name="introduction">🤖 Introduction</a>

JobHunt is a comprehensive job portal platform that connects job seekers with employers. The application allows users to create profiles, search for jobs, apply to positions, and for employers to post job listings and manage applicants.

## <a name="tech-stack">⚙️ Tech Stack</a>

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT Authentication
- Multer for file uploads
- Cloudinary for image storage

### Frontend
- React.js
- Context API for state management
- Axios for API requests
- React Router for navigation

## <a name="features">🔋 Features</a>

👉 **User Authentication**: Secure registration and login for both job seekers and employers

👉 **Profile Management**: Users can create and update detailed profiles with skills, bio, and resume uploads

👉 **Job Listings**: Employers can post, edit, and manage job listings

👉 **Job Applications**: Job seekers can browse and apply to positions with their profile

👉 **File Uploads**: Support for profile photos and resume uploads via Cloudinary

👉 **Role-Based Access**: Different functionalities for job seekers and employers

👉 **Responsive Design**: Works seamlessly across all device sizes

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up the project locally on your machine.

**Prerequisites**

Make sure you have the following installed on your machine:

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)
- [MongoDB](https://www.mongodb.com/) (Local or Atlas)

**Cloning the Repository**

```bash
git clone https://github.com/Suhasgowda7104/JobHunt.git
cd jobhunt
```

**Backend Setup**

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Create .env file with the following variables
# MONGO_URL=your_mongodb_connection_string
# PORT=8000
# SECRET_KEY=your_jwt_secret_key
# CLOUDINARY_CLOUD_NAME=your_cloudinary_name
# CLOUDINARY_API_KEY=your_cloudinary_api_key
# CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# Start the server
npm start
```

**Frontend Setup**

```bash
# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Start the development server
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to view the project.

## <a name="project-structure">🏗️ Project Structure</a>

### Backend

```
backend/
├── controllers/        # Request handlers
├── middlewares/        # Express middlewares
├── models/             # Mongoose schemas
├── routes/             # API routes
├── utils/              # Utility functions
├── index.js            # Entry point
└── .env                # Environment variables
```

### Frontend

```
frontend/
├── public/             # Static files
├── src/
│   ├── assets/         # Images, fonts, etc.
│   ├── components/     # Reusable components
│   ├── context/        # React Context
│   ├── pages/          # Application pages
│   ├── services/       # API service functions
│   ├── App.jsx         # Main component
│   └── main.jsx        # Entry point
└── index.html          # HTML template
```

## <a name="api-endpoints">📝 API Endpoints</a>

### User Routes

- `POST /api/v1/user/register` - Register a new user
- `POST /api/v1/user/register-json` - Register without file upload
- `POST /api/v1/user/login` - Login user
- `GET /api/v1/user/logout` - Logout user
- `POST /api/v1/user/profile/update` - Update user profile

### Job Routes

- `POST /api/v1/job` - Create a new job listing
- `GET /api/v1/job` - Get all job listings
- `GET /api/v1/job/:id` - Get a specific job listing

### Application Routes

- `POST /api/v1/application` - Submit a job application
- `GET /api/v1/application` - Get user's applications 
