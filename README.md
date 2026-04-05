# Social Media App

A modern full-stack social media platform built with real-time messaging, interactive posts, stories, and video loops.

[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socketdotio&logoColor=white)](https://socket.io/)
[![License: ISC](https://img.shields.io/badge/License-ISC-blue.svg)](https://opensource.org/licenses/ISC)

---

## 📌 Overview

This social media application provides a comprehensive platform for users to connect, share content, and communicate in real-time. It addresses the need for a feature-rich social networking experience with seamless interactions, including posts, stories, short video loops, messaging, and notifications. Ideal for developers looking to build scalable social platforms or for users seeking an engaging online community.

---

## ✨ Features

- **User Authentication**: Secure signup, login, OTP verification, and password reset with JWT tokens.
- **Posts & Media**: Upload images/videos, like, comment, and save posts.
- **Stories**: Share temporary photo/video stories with view tracking.
- **Loops**: Short video content (reels) with likes and comments.
- **Real-Time Messaging**: Instant text and image messaging with online status.
- **Notifications**: Real-time alerts for likes, comments, follows, and messages.
- **User Profiles**: Edit profiles, follow/unfollow users, and view suggested connections.
- **Search**: Find users and content across the platform.
- **Responsive Design**: Mobile-friendly UI built with React and Tailwind CSS.

---

## 🛠 Tech Stack

### Backend
- **Node.js**: Runtime environment
- **Express.js**: Web framework
- **MongoDB**: NoSQL database with Mongoose ODM
- **Socket.IO**: Real-time communication
- **JWT**: Authentication tokens
- **bcryptjs**: Password hashing
- **Cloudinary**: Media storage and optimization
- **Multer**: File upload handling
- **Nodemailer**: Email services for OTP

### Frontend
- **React**: UI library with Vite for fast development
- **Redux Toolkit**: State management
- **Tailwind CSS**: Utility-first CSS framework
- **Axios**: HTTP client for API calls
- **React Router**: Client-side routing
- **Socket.IO Client**: Real-time frontend integration

---

## 📂 Project Structure

```
social-media-app/
├── backend/
│   ├── config/          # Database, Cloudinary, Mail, Token configs
│   ├── controllers/     # Business logic for auth, posts, messages, etc.
│   ├── middlewares/     # Authentication and file upload middlewares
│   ├── models/          # MongoDB schemas for users, posts, messages
│   ├── routes/          # API route definitions
│   ├── public/          # Static assets
│   ├── socket.js        # Socket.IO server setup
│   ├── index.js         # Main server entry point
│   └── package.json     # Backend dependencies
├── frontend/
│   ├── public/          # Static assets
│   ├── src/
│   │   ├── components/  # Reusable UI components
│   │   ├── pages/       # Main application pages
│   │   ├── hooks/       # Custom React hooks for data fetching
│   │   ├── redux/       # State slices and store
│   │   ├── App.jsx      # Main app component
│   │   └── main.jsx     # Entry point
│   ├── vite.config.js   # Vite configuration
│   └── package.json     # Frontend dependencies
└── README.md
```

---

## ⚙️ Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- Cloudinary account for media storage

### Backend Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/social-media-app.git
   cd social-media-app/backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory:
   ```env
   PORT=8000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   CLOUDINARY_CLOUD_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_email_app_password
   ```

4. Start the backend server:
   ```bash
   npm run dev
   ```

### Frontend Setup
1. Navigate to frontend directory:
   ```bash
   cd ../frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

The application will be available at `http://localhost:5173` for frontend and `http://localhost:8000` for backend.

---

## 🚀 Usage

1. **Register**: Create an account with email verification via OTP.
2. **Login**: Authenticate and access the dashboard.
3. **Explore Feed**: View posts, stories, and loops from followed users.
4. **Create Content**: Upload posts, stories, or loops with media.
5. **Interact**: Like, comment, and save content.
6. **Connect**: Follow users and send messages in real-time.
7. **Notifications**: Stay updated with real-time alerts.

Example flow: Sign up → Verify email → Login → Upload a post → Follow users → Send a message.

---

## 🔌 API Documentation

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/signup` | User registration |
| POST | `/api/auth/signin` | User login |
| POST | `/api/auth/sendOtp` | Send OTP for verification |
| POST | `/api/auth/verifyOtp` | Verify OTP |
| POST | `/api/auth/resetPassword` | Reset password |
| GET | `/api/auth/signout` | Logout user |
| POST | `/api/posts/upload` | Upload a new post |
| GET | `/api/posts/getAll` | Get all posts |
| GET | `/api/posts/like/:postId` | Like/unlike a post |
| GET | `/api/posts/saved/:postId` | Save/unsave a post |
| POST | `/api/posts/comment/:postId` | Add comment to post |
| POST | `/api/messages/send/:receiverId` | Send message |
| GET | `/api/messages/getAll/:receiverId` | Get conversation messages |
| GET | `/api/messages/prevChats` | Get previous chat users |
| GET | `/api/users/current` | Get current user profile |
| GET | `/api/users/suggested` | Get suggested users |
| GET | `/api/users/getProfile/:userName` | Get user profile |
| GET | `/api/users/follow/:targetUserId` | Follow/unfollow user |
| GET | `/api/users/followingList` | Get following list |
| GET | `/api/users/search` | Search users |
| GET | `/api/users/getAllNotifications` | Get notifications |
| POST | `/api/users/markAsRead` | Mark notifications as read |
| POST | `/api/users/editProfile` | Edit user profile |
| POST | `/api/stories/upload` | Upload story |
| GET | `/api/stories/getAll` | Get all stories |
| GET | `/api/stories/getByUserName/:userName` | Get stories by user |
| GET | `/api/stories/view/:storyId` | View story |
| POST | `/api/loops/upload` | Upload loop (video) |
| GET | `/api/loops/getAll` | Get all loops |
| GET | `/api/loops/like/:loopId` | Like loop |
| POST | `/api/loops/comment/:loopId` | Comment on loop |

---

## 💬 Real-Time Features

Powered by Socket.IO for seamless real-time interactions:

- **Online Users**: Track online status of connected users.
- **New Messages**: Instant delivery of text and image messages.
- **Notifications**: Real-time alerts for social interactions (likes, comments, follows).
- **Connection Management**: Automatic handling of user connections and disconnections.

Events include:
- `newMessage`: Emitted when a new message is sent.
- `getOnlineUsers`: Broadcasts list of online users.

---

## 📸 Screenshots / Demo

*Add screenshots here to showcase the UI and features.*

- Home Feed
- Messaging Interface
- Profile Page
- Story Viewer

*(Placeholder: Include images like `screenshots/home.png`, `screenshots/messages.png`, etc.)*

---

## 🌍 Deployment

### Backend Deployment
- Deploy to platforms like Heroku, Railway, or Vercel.
- Ensure environment variables are set in production.
- Use MongoDB Atlas for database hosting.

### Frontend Deployment
- Build the app: `npm run build`
- Deploy to Netlify, Vercel, or GitHub Pages.

*(Note: Configure CORS and environment variables for production.)*

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Commit changes: `git commit -m 'Add your feature'`.
4. Push to branch: `git push origin feature/your-feature`.
5. Open a Pull Request.

Please ensure code follows ESLint rules and includes tests where applicable.

---

## 📄 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

- Built with modern web technologies for educational and portfolio purposes.
- Inspired by popular social media platforms.
- Special thanks to the open-source community for the amazing tools and libraries.