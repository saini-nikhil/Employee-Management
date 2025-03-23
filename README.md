Full-Stack Employee Management System with Cloudinary Integration

Overview

This is a Full-Stack Employee Management System that allows users to perform CRUD operations on employee records and manage profile pictures using Cloudinary for image storage. The application consists of a Node.js + Express.js backend and a React.js (with Context API) frontend, using MongoDB as the database.

Features

Backend (Node.js + Express.js)

MongoDB Integration: Employee data is stored in a MongoDB database.

Mongoose Models: Schema modeling and database interactions using Mongoose.

Cloudinary File Storage: Employee profile pictures are stored on Cloudinary.

Multer Middleware: Handles image uploads.

JWT Authentication: API endpoints are secured using JWT.

CRUD Operations: Employees can be created, read, updated, and deleted.

Search & Pagination: Supports filtering and paginating employee records.

API Security: Implements security best practices.

Frontend (React.js + Context API)

React Router: Enables navigation between pages (e.g., list, add, edit employees).

Context API for State Management: Replaces Redux for managing global state.

Axios for API Calls: Handles communication with the backend.

File Upload Handling: Supports profile picture uploads and Cloudinary integration.

Responsive UI: A modern, mobile-friendly user interface.

Installation & Setup

Prerequisites

Ensure you have the following installed:

Node.js (v16 or later)

MongoDB

Cloudinary account (for image uploads)

Backend Setup

Clone the repository:

git clone https://github.com/yourusername/employee-management.git
cd employee-management/backend

Install dependencies:

npm install

Create a .env file in the backend folder and add:

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

Start the backend server:

npm start

Frontend Setup

Navigate to the frontend folder:

cd ../frontend

Install dependencies:

npm install

Create a .env file in the frontend folder and add:

REACT_APP_API_BASE_URL=http://localhost:5000

Start the frontend server:

npm start

API Endpoints

Authentication

POST /api/auth/register – Register a new user

POST /api/auth/login – Login and receive a JWT token

Employee CRUD Operations

POST /api/employees – Create an employee (Authenticated)

GET /api/employees – Fetch all employees (supports pagination & search)

GET /api/employees/:id – Fetch an employee by ID

PUT /api/employees/:id – Update an employee (Authenticated)

DELETE /api/employees/:id – Delete an employee (Authenticated)

Image Upload

POST /api/upload – Upload employee profile picture to Cloudinary

Folder Structure

employee-management/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── config/
│   ├── server.js
│   ├── .env
│   ├── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── App.js
│   │   ├── index.js
│   ├── .env
│   ├── package.json
│
└── README.md

Deployment

Backend Deployment

Use Render, Heroku, or Vercel for deploying the Node.js backend.

Ensure environment variables are set in the hosting provider.

Frontend Deployment

Deploy using Vercel or Netlify.

Update REACT_APP_API_BASE_URL in .env to point to the deployed backend URL.

Security & Best Practices

JWT-based authentication for secure API access.

CORS enabled to allow frontend-backend communication.

Environment variables for sensitive information.

Multer & Cloudinary for secure image uploads.

Future Enhancements

Role-based authentication (Admin/User permissions).

Dashboard with employee statistics.

Export employee data as CSV/PDF.

Author

Nikhil
