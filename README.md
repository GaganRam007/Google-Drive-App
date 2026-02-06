# Google Drive Clone – Full Stack Cloud Storage Application

A production-ready cloud storage web application inspired by **Google Drive**, built using **React, Node.js, Express, MongoDB Atlas, and AWS S3**.  
This application allows users to securely upload, organize, and access files and folders with private cloud storage and enterprise-level authentication.

---

## ✨ Features

### 🔐 Authentication & Security
- User registration with email activation  
- Secure login using JWT authentication  
- Encrypted passwords with bcrypt  
- Forgot/reset password via email  
- Protected routes & secure APIs  
- Private AWS S3 bucket storage  
- Signed URLs for secure file download  

### 📂 File Management
- Upload files to AWS S3  
- Drag & drop file upload  
- Secure file download  
- Delete files  
- View file details & timestamps  

### 📁 Folder Management
- Create folders  
- Nested folder structure  
- Organize files inside folders  
- Folder navigation system  

### 📊 Dashboard
- Modern Google Drive-style UI  
- View all files & folders  
- Upload & manage files  
- Responsive design with Tailwind CSS  

---

## 🛠 Tech Stack

**Frontend**
- React.js  
- Tailwind CSS  
- Axios  
- React Dropzone  

**Backend**
- Node.js  
- Express.js  
- MongoDB Atlas  
- JWT Authentication  
- Nodemailer  

**Cloud Services**
- AWS S3 (Private Bucket)  
- MongoDB Atlas  

**Deployment**
- Frontend: Vercel / Netlify  
- Backend: Render / Railway / AWS EC2  

---

## 📂 Project Structure
googledrive-project
│
├── backend
│   ├── src
│   │   ├── controllers
│   │   ├── models
│   │   ├── routes
│   │   ├── middleware
│   │   ├── config
│   │   └── server.js
│
└── frontend
├── src
│   ├── components
│   ├── pages
│   ├── context
│   └── App.jsx

Code

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository
```bash
git clone https://github.com/yourusername/googledrive-project.git
cd googledrive-project
2️⃣ Backend Setup
bash
cd backend
npm install
npm run dev
Create a .env file in the backend directory:

env
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret
AWS_ACCESS_KEY=your_key
AWS_SECRET_KEY=your_secret
AWS_BUCKET=your_bucket
AWS_REGION=ap-south-1
CLIENT_URL=http://localhost:5173
3️⃣ Frontend Setup
bash
cd frontend
npm install
npm run dev
☁️ AWS S3 Configuration
Create a private S3 bucket

Enable programmatic access

Add access key & secret in .env

🔒 Security Features
JWT Authentication

Password Encryption

Private AWS S3 storage

Signed download URLs

Protected API routes

📌 Use Cases
Cloud storage system

Google Drive clone

Full-stack cloud project

MERN stack portfolio project

AWS S3 integration project

👨‍💻 Author
Gagan Ram  
Software Developer
📧 Email: b.gaganram@gmail.com (gmail.com in Bing)
