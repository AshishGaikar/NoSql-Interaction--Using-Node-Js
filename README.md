# NoSQL Web Application with Node.js

A complete web application that interacts with MongoDB (NoSQL database) using Node.js, Express, and EJS templates.

## Features

### 🌐 Web Interface
- **Modern responsive design** with gradient backgrounds
- **User-friendly forms** for creating and editing users
- **Interactive user cards** with hover effects
- **Real-time CRUD operations** through web interface

### 🔧 API Endpoints
- **GET /api/users** - Get all users (JSON)
- **GET /api/users/:id** - Get user by ID (JSON)
- **POST /api/users** - Create new user (JSON)
- **PUT /api/users/:id** - Update user (JSON)
- **DELETE /api/users/:id** - Delete user (JSON)

### 📱 Web Routes
- **GET /** - Homepage with all users
- **GET /add** - Add new user form
- **POST /users** - Create user (form submission)
- **GET /edit/:id** - Edit user form
- **POST /users/:id** - Update user (form submission)
- **POST /delete/:id** - Delete user (form submission)

## Technology Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (NoSQL)
- **Frontend**: EJS Templates, CSS3
- **Styling**: Modern gradients, glassmorphism effects
- **Deployment**: Render/Railway compatible

## Database Schema

```javascript
{
  name: { type: String, required: true },
  email: { type: String, required: true, unique: true },
  age: { type: Number, required: true },
  city: { type: String, required: true },
  createdAt: Date,
  updatedAt: Date
}
```

## Installation & Setup

```bash
cd Assignment7
npm install
npm start
```

Visit: `http://localhost:3000`

## Usage

### Web Interface
1. **View Users**: Visit homepage to see all users
2. **Add User**: Click "Add New User" button
3. **Edit User**: Click "Edit" on any user card
4. **Delete User**: Click "Delete" with confirmation

### API Testing
- Use the existing Postman collection
- All API endpoints remain functional
- Web interface and API work simultaneously

## Deployment

The application is ready for deployment on:
- **Render** (recommended)
- **Railway**
- **Heroku**
- Any Node.js hosting platform

### Environment Variables
```
PORT=3000
MONGODB_URI=your_mongodb_connection_string
```

## Project Structure

```
Assignment7/
├── server.js              # Main application file
├── package.json           # Dependencies
├── views/                 # EJS templates
│   ├── index.ejs         # Homepage
│   ├── add.ejs           # Add user form
│   └── edit.ejs          # Edit user form
├── public/               # Static files
│   └── style.css         # Styling
└── README.md             # Documentation
```

## Key Features

✅ **Full CRUD Operations** via web interface  
✅ **RESTful API** for programmatic access  
✅ **MongoDB Integration** with Mongoose ODM  
✅ **Responsive Design** for all devices  
✅ **Modern UI/UX** with animations  
✅ **Form Validation** and error handling  
✅ **Deployment Ready** configuration