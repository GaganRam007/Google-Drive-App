# Google Drive Clone – Backend

A production-grade backend service for a cloud storage application built with **Node.js, Express, MongoDB Atlas, and AWS S3**.

---

## 🚀 Quick Start

### Prerequisites
- Node.js (v16+)
- MongoDB Atlas account
- AWS S3 bucket setup
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/GaganRam007/Google-Drive-App.git
cd backend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with your credentials

# Start server
npm start
```

### Environment Variables

Create a `.env` file in the backend directory:

```env
# Server
PORT=5000
NODE_ENV=development

# Database
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/db-name

# JWT
JWT_SECRET=your_jwt_secret_key
JWT_EXPIRE=7d

# Email Service
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
SMTP_SERVICE=gmail

# AWS S3
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-east-1
AWS_S3_BUCKET=your-bucket-name

# Frontend URL
FRONTEND_URL=http://localhost:3000
```

---

## 📂 Project Structure

```
backend/
├── models/
│   ├── User.js           # User schema
│   ├── File.js           # File metadata schema
│   └── Folder.js         # Folder schema
├── routes/
│   ├── auth.js           # Authentication endpoints
│   ├── files.js          # File management endpoints
│   └── folders.js        # Folder management endpoints
├── controllers/
│   ├── authController.js
│   ├── fileController.js
│   └── folderController.js
├── middleware/
│   ├── auth.js           # JWT verification
│   ├── errorHandler.js   # Error handling
│   └── validation.js     # Input validation
├── services/
│   ├── s3Service.js      # AWS S3 operations
│   └── emailService.js   # Email notifications
├── config/
│   ├── database.js       # MongoDB connection
│   └── aws.js            # AWS S3 configuration
├── .env.example
├── server.js
└── package.json
```

---

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `POST /api/auth/forgot-password` - Request password reset
- `POST /api/auth/reset-password/:token` - Reset password
- `GET /api/auth/verify-email/:token` - Verify email

### Files
- `POST /api/files/upload` - Upload file to S3
- `GET /api/files` - List user's files
- `GET /api/files/:id/download` - Download file
- `DELETE /api/files/:id` - Delete file
- `PATCH /api/files/:id` - Update file metadata

### Folders
- `POST /api/folders` - Create folder
- `GET /api/folders` - List folders
- `GET /api/folders/:id/contents` - Get folder contents
- `DELETE /api/folders/:id` - Delete folder
- `PATCH /api/folders/:id` - Update folder

---

## 🔐 Security Features

- **JWT Authentication** - Secure token-based authentication
- **Password Encryption** - bcrypt hashing with salt rounds
- **CORS Protection** - Restricted cross-origin requests
- **Rate Limiting** - Prevent API abuse
- **Input Validation** - Server-side validation of all inputs
- **AWS S3 Security** - Signed URLs, private bucket, server-side encryption
- **Secure Headers** - Helmet.js for HTTP security headers
- **Environment Variables** - Sensitive data protection

---

## 🛠 Tech Stack

| Component | Technology |
|-----------|-----------|
| Runtime | Node.js |
| Framework | Express.js |
| Database | MongoDB Atlas |
| Cloud Storage | AWS S3 |
| Authentication | JWT |
| Password Hashing | bcrypt |
| Email Service | Nodemailer |
| Validation | Joi |

---

## 📦 Dependencies

```json
{
  "express": "^4.18.2",
  "mongoose": "^7.0.0",
  "jsonwebtoken": "^9.0.0",
  "bcryptjs": "^2.4.3",
  "aws-sdk": "^2.1400.0",
  "nodemailer": "^6.9.1",
  "cors": "^2.8.5",
  "dotenv": "^16.0.3",
  "joi": "^17.9.2",
  "helmet": "^7.0.0",
  "express-rate-limit": "^6.7.0"
}
```

---

## 🚀 Deployment

### Render

1. Connect GitHub repository to Render
2. Set environment variables in Render dashboard
3. Deploy with auto-redeploy on push

### Railway

1. Import repository from GitHub
2. Configure environment variables
3. Deploy and monitor from Railway dashboard

### AWS EC2

1. Launch Ubuntu instance
2. Install Node.js and dependencies
3. Configure security groups
4. Deploy using PM2 for process management

---

## 📝 Notes

- Ensure MongoDB Atlas IP whitelist includes your server
- AWS S3 bucket must be private with appropriate CORS settings
- Use environment-specific configurations for development and production
- Regular backups recommended for MongoDB data
- Monitor AWS S3 costs for large file uploads

---

## 🐛 Troubleshooting

**MongoDB Connection Error**
- Verify connection string in .env
- Check IP whitelist in MongoDB Atlas

**AWS S3 Upload Fails**
- Confirm AWS credentials
- Verify bucket exists and permissions are set
- Check bucket CORS configuration

**Email Not Sending**
- Enable 2FA and generate app password (Gmail)
- Verify SMTP credentials in .env
- Check email service status
