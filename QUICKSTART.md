# 🚀 Quick Start Guide

Get your Visitor Pass Management System up and running in 5 minutes!

## ⚡ Fast Setup (3 Commands)

### 1. Backend Setup
```bash
cd server
npm install
npm run dev
```

### 2. Frontend Setup (in a new terminal)
```bash
cd client
npm install
npm run dev
```

### 3. Access the Application
- Frontend: http://localhost:5173
- Backend: http://localhost:3000

## 🔑 First Time Setup

### Configure Backend Environment
Create `server/.env`:
```env
MONGO_URI=mongodb://localhost:27017/visitor-pass
JWT_SECRET=mysecretkey123
PORT=3000
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-password
```

### Configure Frontend (Optional)
Create `client/.env`:
```env
VITE_API_URL=http://localhost:3000/api
```

## 👤 Create Your First User

1. Open http://localhost:5173
2. Click "Sign up"
3. Fill in the form:
   - Name: Admin User
   - Email: admin@example.com
   - Password: admin123
   - Role: Admin
4. Click "Create Account"
5. Go back and login with your credentials

## 📊 Using the Dashboard

After login, you'll see:
- **Dashboard**: Statistics and charts
- **Visitors**: Add/manage visitors
- **Passes**: Generate QR passes
- **Scanner**: Scan QR codes
- **Check Logs**: View activity

## 🎯 Common Tasks

### Add a Visitor
1. Go to "Visitors" page
2. Click "+ Add Visitor"
3. Fill in visitor details
4. Submit

### Generate a Pass
1. Go to "Passes" page
2. Pass will be auto-generated for approved visitors
3. Download or scan QR code

### Check-in a Visitor
1. Go to "QR Scanner"
2. Start camera scanner
3. Scan visitor's QR code
4. Confirm check-in

## 🛠️ Troubleshooting

### Backend won't start
- Check if MongoDB is running
- Verify .env file exists
- Check port 3000 is not in use

### Frontend won't start
- Clear node_modules and reinstall
- Check port 5173 is not in use
- Verify backend is running

### Can't login
- Check backend console for errors
- Verify MongoDB connection
- Check JWT_SECRET is set

## 📱 Testing the App

### Test Credentials
After registration, use:
- Email: Your registered email
- Password: Your password

### Test Flow
1. Register → 2. Login → 3. Add Visitor → 4. Generate Pass → 5. Scan QR

## 🎨 Customization

### Change Colors
Edit `client/tailwind.config.js`:
```js
colors: {
  primary: {
    500: '#your-color',
    600: '#your-darker-color',
  }
}
```

### Change Port
Backend: Edit `server/.env`
Frontend: Edit `client/vite.config.js`

## 📦 Production Build

### Backend
```bash
cd server
npm start
```

### Frontend
```bash
cd client
npm run build
npm run preview
```

## 🚀 Deploy

### Vercel (Frontend)
```bash
cd client
vercel
```

### Render (Backend)
1. Push to GitHub
2. Connect Render to repo
3. Add environment variables
4. Deploy

## 💡 Tips

- Use different terminals for backend and frontend
- Keep backend running while using frontend
- Check browser console for errors
- MongoDB must be running before backend

## 📞 Need Help?

- Check logs in terminal
- Verify all dependencies installed
- Ensure MongoDB is running
- Check environment variables

---

You're all set! 🎉 Start managing visitors efficiently!
