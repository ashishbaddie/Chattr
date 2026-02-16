# Chattr

A modern, real-time chat application built with React, Express, Socket.io, and Prisma. Chattr provides a seamless messaging experience with user authentication, online status tracking, and customizable themes.

## ✨ Features

- 🔐 **User Authentication** - Secure signup/login with JWT tokens
- 💬 **Real-time Messaging** - Instant message delivery using Socket.io
- 👤 **User Profiles** - Customizable profile pictures with Cloudinary integration
- 🟢 **Online Status** - See who's currently online
- 🎨 **Theme Customization** - Multiple themes to personalize your chat experience
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🔒 **Protected Routes** - Secure access control for authenticated users

## 🛠️ Tech Stack

### Frontend
- **React 19** - Modern UI framework
- **Vite** - Fast build tool and dev server
- **TailwindCSS** - Utility-first CSS framework
- **DaisyUI** - Component library for Tailwind
- **Zustand** - Lightweight state management
- **Socket.io Client** - Real-time bidirectional communication
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Lucide React** - Beautiful icon library
- **React Hot Toast** - Notifications

### Backend
- **Node.js** - JavaScript runtime
- **Express** - Web application framework
- **Socket.io** - Real-time communication
- **Prisma** - Modern ORM for PostgreSQL
- **PostgreSQL** - Relational database
- **JWT** - JSON Web Tokens for authentication
- **bcryptjs** - Password hashing
- **Cloudinary** - Image hosting and management
- **Cookie Parser** - Parse HTTP cookies

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v18 or higher)
- PostgreSQL database
- npm or yarn package manager

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/ashishbaddie/Chattr.git
cd Chattr
```

### 2. Backend Setup

```bash
cd backend
npm install
```

Create a `.env` file in the backend directory:

```env
PORT=5001
NODE_ENV=development

# Database
DATABASE_URL="postgresql://username:password@localhost:5432/chattr"

# JWT Secret
JWT_SECRET=your_jwt_secret_key_here

# Cloudinary Configuration
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Run Prisma migrations:

```bash
npm run prisma:generate
npm run prisma:deploy
```

### 3. Frontend Setup

```bash
cd frontend
npm install
```

### 4. Run the Application

**Development Mode:**

Backend:
```bash
cd backend
npm run dev
```

Frontend:
```bash
cd frontend
npm run dev
```

The frontend will be available at `http://localhost:5173`  
The backend will be available at `http://localhost:5001`

**Production Build:**

From the root directory:
```bash
npm run build
npm start
```

## 📁 Project Structure

```
Chattr/
├── backend/
│   ├── src/
│   │   ├── controllers/      # Route controllers
│   │   ├── lib/              # Utility libraries (socket.io setup)
│   │   ├── middleware/       # Authentication middleware
│   │   ├── routes/           # API routes
│   │   ├── seeds/            # Database seed files
│   │   └── index.js          # Entry point
│   ├── prisma/               # Prisma schema and migrations
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/       # React components
│   │   ├── pages/            # Page components
│   │   ├── store/            # Zustand state management
│   │   ├── lib/              # Utility functions
│   │   ├── App.jsx           # Main app component
│   │   └── main.jsx          # Entry point
│   └── package.json
└── package.json              # Root package.json for deployment
```

## 🔑 API Endpoints

### Authentication Routes (`/api/auth`)
- `POST /signup` - Register a new user
- `POST /login` - Login user
- `POST /logout` - Logout user
- `GET /check` - Check authentication status
- `PUT /update-profile` - Update user profile (protected)

### Message Routes (`/api/messages`)
- `GET /users` - Get all users for sidebar (protected)
- `GET /:id` - Get messages with a specific user (protected)
- `POST /send/:id` - Send a message to a user (protected)

## 🎨 Available Themes

Chattr comes with multiple themes powered by DaisyUI:
- Light
- Dark
- Cupcake
- Bumblebee
- Emerald
- Corporate
- Synthwave
- And many more!

## 🔒 Security Features

- Password hashing with bcryptjs
- JWT-based authentication
- HTTP-only cookies for token storage
- Protected API routes with middleware
- CORS configuration for secure cross-origin requests

## 📸 Screenshots

<!-- Add screenshots of your application here -->

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/ashishbaddie/Chattr/issues).

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the ISC License.

## 👤 Author

**Ashish**
- GitHub: [@ashishbaddie](https://github.com/ashishbaddie)

## 🙏 Acknowledgments

- Icons by [Lucide](https://lucide.dev/)
- UI components by [DaisyUI](https://daisyui.com/)
- Image hosting by [Cloudinary](https://cloudinary.com/)

---

⭐ Star this repo if you find it helpful!
