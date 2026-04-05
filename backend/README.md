# Backend - Social Media App

A robust Node.js backend for a full-stack social media platform, handling authentication, content management, real-time messaging, and more.

[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white)](https://socket.io/)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)

---

## 📌 Overview

This backend provides RESTful APIs and real-time capabilities for a social media application. It manages user authentication, posts, stories, loops (short videos), messaging, notifications, and more. Built with scalability and security in mind, using JWT for authentication and Socket.IO for real-time features.

---

## ✨ Features

- **Authentication**: JWT-based auth with OTP verification and password reset.
- **User Management**: Profiles, following/followers, search.
- **Content Management**: Posts, stories, loops with media uploads.
- **Messaging**: Real-time chat with text and images.
- **Notifications**: Alerts for interactions.
- **File Uploads**: Cloudinary integration for media storage.
- **Real-Time Events**: Socket.IO for live updates.

---

## 🛠 Tech Stack

- **Node.js**: Server runtime
- **Express.js**: Web framework
- **MongoDB**: Database with Mongoose
- **Socket.IO**: Real-time communication
- **JWT**: Token-based auth
- **bcryptjs**: Password encryption
- **Cloudinary**: Media hosting
- **Multer**: File handling
- **Nodemailer**: Email services

---

## 📂 Project Structure

```
backend/
├── config/          # Configurations (DB, Cloudinary, Mail, Token)
├── controllers/     # Route handlers (auth, posts, messages, etc.)
├── middlewares/     # Auth and upload middlewares
├── models/          # MongoDB schemas
├── routes/          # API routes
├── public/          # Static files
├── socket.js        # Socket.IO setup
├── index.js         # Server entry point
└── package.json     # Dependencies
```

---

## ⚙️ Installation & Setup

1. Navigate to backend directory:
   ```bash
   cd backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create `.env` file:
   ```env
   PORT=8000
   MONGO_URI=your_mongodb_uri
   JWT_SECRET=your_secret
   CLOUDINARY_CLOUD_NAME=your_name
   CLOUDINARY_API_KEY=your_key
   CLOUDINARY_API_SECRET=your_secret
   EMAIL_USER=your_email
   EMAIL_PASS=your_password
   ```

4. Run the server:
   ```bash
   npm run dev
   ```

---

## 🔌 API Endpoints

See the main README for full API documentation.

---

## 💬 Real-Time Features

- **Online Users**: Track user presence.
- **Messages**: Instant message delivery.
- **Notifications**: Live alerts.

---

## 🌍 Deployment

Deploy to Heroku, Railway, or similar. Set environment variables.

---

## 🤝 Contributing

Follow the main project's contribution guidelines.

---

## 📄 License

ISC License.