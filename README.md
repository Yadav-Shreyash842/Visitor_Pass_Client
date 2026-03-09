# 🎫 Visitor Pass Management System

A complete full-stack MERN application for managing visitor passes with QR code generation and scanning.

## 📋 Overview

This system allows organizations to manage visitors, generate digital passes with QR codes, and track check-ins/check-outs efficiently. Perfect for corporate offices, events, and secure facilities.

## ✨ Features

### Backend (Node.js + Express + MongoDB)
- ✅ User authentication with JWT
- ✅ Role-based access control (Admin, Security, Employee)
- ✅ Visitor management
- ✅ Pass generation with QR codes
- ✅ Check-in/Check-out logging
- ✅ Email notifications
- ✅ RESTful API

### Frontend (React + Vite + Tailwind CSS)
- ✅ Modern glassmorphism UI
- ✅ Interactive dashboard with charts
- ✅ Real-time statistics
- ✅ QR code scanner
- ✅ Visitor and pass management
- ✅ Responsive design
- ✅ Protected routes

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Nodemailer** - Email service
- **QRCode** - QR generation
- **UUID** - Unique IDs

### Frontend
- **React 18** - UI library
- **Vite** - Build tool
- **Tailwind CSS** - Styling
- **React Router** - Navigation
- **Axios** - HTTP client
- **Recharts** - Charts
- **Lucide React** - Icons
- **html5-qrcode** - Scanner

## 📁 Project Structure

```
visiter_Pass-2/
├── server/                    # Backend
│   ├── config/
│   │   └── db.js             # MongoDB connection
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── checkLogController.js
│   │   ├── passController.js
│   │   └── visitorController.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── roleMiddleware.js
│   ├── Models/
│   │   ├── Appointment.js
│   │   ├── CheckLog.js
│   │   ├── Pass.js
│   │   ├── User.js
│   │   └── Visitor.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── checkRoutes.js
│   │   ├── passRoutes.js
│   │   └── visitorRoutes.js
│   ├── utils/
│   │   ├── email.js
│   │   └── generateQRCode.js
│   ├── .env
│   ├── package.json
│   └── server.js
│
└── client/                    # Frontend
    ├── src/
    │   ├── api/
    │   │   └── axios.js
    │   ├── components/
    │   │   ├── layout/
    │   │   │   ├── Layout.jsx
    │   │   │   ├── Sidebar.jsx
    │   │   │   └── Navbar.jsx
    │   │   └── ui/
    │   │       ├── StatsCard.jsx
    │   │       ├── DataTable.jsx
    │   │       └── Modal.jsx
    │   ├── context/
    │   │   └── AuthContext.jsx
    │   ├── pages/
    │   │   ├── Login.jsx
    │   │   ├── Register.jsx
    │   │   ├── Dashboard.jsx
    │   │   ├── Visitors.jsx
    │   │   ├── Passes.jsx
    │   │   ├── CheckLogs.jsx
    │   │   └── QRScanner.jsx
    │   ├── App.jsx
    │   ├── main.jsx
    │   └── index.css
    ├── index.html
    ├── package.json
    └── vite.config.js
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v16+)
- MongoDB (local or Atlas)
- npm or yarn

### Backend Setup

1. Navigate to server directory:
```bash
cd server
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file:
```env
MONGO_URI=mongodb://localhost:27017/visitor-pass
JWT_SECRET=your_super_secret_jwt_key_here
PORT=3000
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
```

4. Start the server:
```bash
npm run dev
```

Server runs on `http://localhost:3000`

### Frontend Setup

1. Navigate to client directory:
```bash
cd client
```

2. Install dependencies:
```bash
npm install
```

3. Create `.env` file (optional):
```env
VITE_API_URL=http://localhost:3000/api
```

4. Start the development server:
```bash
npm run dev
```

Frontend runs on `http://localhost:5173`

## 🔐 API Endpoints

### Authentication
```
POST /api/auth/register    - Register new user
POST /api/auth/login       - Login user
```

### Visitors
```
GET    /api/visitors       - Get all visitors (protected)
GET    /api/visitors/all   - Get all visitors
POST   /api/visitors/createVisitor - Create visitor
GET    /api/visitors/:id   - Get visitor by ID
PUT    /api/visitors/:id   - Update visitor
DELETE /api/visitors/:id   - Delete visitor
```

### Passes
```
POST /api/pass             - Generate pass
GET  /api/pass             - Get all passes
GET  /api/pass/verify/:passCode - Verify pass
```

### Check Logs
```
POST /api/checklog/checkin      - Check in visitor
PUT  /api/checklog/checkout/:id - Check out visitor
GET  /api/checklog              - Get all logs
```

## 👥 User Roles

### Admin
- Full system access
- User management
- All CRUD operations

### Security
- Check-in/out visitors
- Verify passes
- View logs

### Employee
- Create visitor entries
- View passes
- Limited access

## 🎨 UI Screenshots

### Login Page
- Glassmorphism design
- Gradient animated background
- Smooth animations

### Dashboard
- Real-time statistics
- Interactive charts
- Recent activity feed

### QR Scanner
- Live camera scanning
- Manual code entry
- Instant verification

## 📱 Responsive Design

The application is fully responsive and works on:
- 📱 Mobile devices
- 💻 Tablets
- 🖥️ Desktops

## 🔒 Security Features

- JWT authentication
- Password hashing with bcrypt
- Role-based access control
- Protected API routes
- Input validation

## 📦 Deployment

### Backend (Render/Railway)
1. Push code to GitHub
2. Connect to Render/Railway
3. Add environment variables
4. Deploy

### Frontend (Vercel/Netlify)
```bash
cd client
npm run build
vercel --prod
```

## 🧪 Testing

### Backend
```bash
cd server
npm test
```

### Frontend
```bash
cd client
npm test
```

## 📝 Environment Variables

### Backend (.env)
```env
MONGO_URI=mongodb://localhost:27017/visitor-pass
JWT_SECRET=your_jwt_secret
PORT=3000
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
```

### Frontend (.env)
```env
VITE_API_URL=http://localhost:3000/api
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 👤 Author

**Visitor Pass Management System**

## 🙏 Acknowledgments

- Stripe Dashboard (UI inspiration)
- Vercel Dashboard (UI inspiration)
- Notion (UI inspiration)

## 📞 Support

For support, email support@visitorpass.com or open an issue.

## 🎯 Roadmap

- [ ] Mobile app (React Native)
- [ ] SMS notifications
- [ ] Facial recognition
- [ ] Advanced analytics
- [ ] Multi-language support
- [ ] Dark mode

---

Made with ❤️ for efficient visitor management
