# Excel Analytics Website

A professional, reactive, and colorful Excel analytics website built with the MERN stack (MongoDB, Express.js, React.js, Node.js) featuring JWT authentication, file upload, data visualization with Chart.js, and comprehensive Excel file management.

## Features

- 🔐 **JWT Authentication** - Secure user registration and login
- 📁 **File Upload** - Drag & drop Excel file upload with validation
- 📊 **Data Visualization** - Interactive charts (Bar, Pie, Line) with Chart.js
- 🔍 **File Management** - View, search, filter, and delete Excel files
- 📈 **Analytics** - Advanced data analysis and statistics
- 🎨 **Modern UI** - Beautiful, responsive design with animations
- 📱 **Mobile Friendly** - Optimized for all device sizes

## Tech Stack

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **Multer** for file uploads
- **XLSX** for Excel file parsing
- **Helmet** for security
- **CORS** for cross-origin requests

### Frontend
- **React.js** with hooks
- **React Router** for navigation
- **Styled Components** for styling
- **Framer Motion** for animations
- **Chart.js** for data visualization
- **Axios** for API calls
- **React Hot Toast** for notifications

## Quick Start

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd excel-analytics-website
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   ```

3. **Configure Environment Variables**
   - Copy `config.env.example` to `config.env`
   - Update the MongoDB URI and JWT secret:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   PORT=5000
   NODE_ENV=development
   ```

4. **Frontend Setup**
   ```bash
   cd frontend
   npm install
   ```

5. **Configure Frontend Environment**
   - The `.env` file should already be created with:
   ```env
   REACT_APP_API_URL=http://localhost:5000
   ```

### Running the Application

1. **Start Backend Server**
   ```bash
   cd backend
   npm start
   ```
   Server will run on `http://localhost:5000`

2. **Start Frontend Development Server**
   ```bash
   cd frontend
   npm start
   ```
   Frontend will run on `http://localhost:3000`

3. **Open your browser**
   Navigate to `http://localhost:3000`

## API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile` - Get user profile

### Excel Files
- `POST /api/excel/upload` - Upload Excel file
- `GET /api/excel/files` - Get user's files
- `GET /api/excel/:id/data` - Get file data
- `POST /api/excel/:id/analyze` - Analyze file data
- `GET /api/excel/:id/download` - Download file
- `DELETE /api/excel/files/:id` - Delete file

## File Upload Troubleshooting

If you encounter upload issues:

1. **Check API URL**: Ensure frontend is posting to the correct backend URL
2. **Authentication**: Verify JWT token is included in request headers
3. **File Format**: Only `.xlsx`, `.xls`, and `.csv` files are supported
4. **File Size**: Maximum file size is 10MB
5. **CORS**: Ensure backend CORS is properly configured

### Common Issues

**400 Bad Request Error:**
- Check if file field name is "file" in FormData
- Verify file type is supported
- Ensure all required fields are present

**401 Unauthorized Error:**
- Check if JWT token is valid
- Verify token is included in Authorization header
- Try logging in again

**CORS Errors:**
- Ensure backend CORS is configured for frontend URL
- Check if requests are going to correct backend port

## Deployment

### Backend (Render)
1. Connect your GitHub repository to Render
2. Set environment variables in Render dashboard
3. Deploy as a Node.js service

### Frontend (Vercel)
1. Connect your GitHub repository to Vercel
2. Set environment variables:
   - `REACT_APP_API_URL` = your backend URL
3. Deploy

## Project Structure

```
├── backend/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── uploads/
│   └── server.js
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── contexts/
│   │   └── App.js
│   └── public/
└── README.md
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support and questions, please open an issue in the repository. 