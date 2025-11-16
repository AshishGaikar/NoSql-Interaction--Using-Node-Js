# Deployment Guide

## Deploy to Render (Free Hosting)

### Step 1: Prepare Repository
1. Initialize git repository:
```bash
git init
git add .
git commit -m "Initial commit"
```

2. Push to GitHub:
```bash
git remote add origin https://github.com/yourusername/crud-api.git
git push -u origin main
```

### Step 2: Deploy on Render
1. Go to [render.com](https://render.com) and sign up
2. Click "New +" → "Web Service"
3. Connect your GitHub repository
4. Configure:
   - **Name**: crud-api-assignment6
   - **Environment**: Node
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Instance Type**: Free

### Step 3: Set Environment Variables
In Render dashboard, add:
- `NODE_ENV`: production
- `MONGODB_URI`: your MongoDB connection string

### Step 4: Test Deployment
Your API will be available at: `https://crud-api-assignment6.onrender.com`

## Alternative: Deploy to Railway

1. Go to [railway.app](https://railway.app)
2. Click "Deploy from GitHub repo"
3. Select your repository
4. Railway will auto-detect Node.js and deploy

## Testing the Deployed API

### Using Postman:
1. Import the `CRUD_API.postman_collection.json` file
2. Update the `baseUrl` variable to your deployed URL
3. Test all endpoints

### Manual Testing:
```bash
# Test API is running
curl https://your-app-url.onrender.com

# Create a user
curl -X POST https://your-app-url.onrender.com/api/users \
  -H "Content-Type: application/json" \
  -d '{"name":"Test User","email":"test@example.com","age":25,"city":"Test City"}'

# Get all users
curl https://your-app-url.onrender.com/api/users
```