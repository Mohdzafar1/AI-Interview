# 🤖 InterviewAI — AI-Powered Interview Platform

A full-stack MERN application where an **AI avatar speaks questions aloud**, listens to your answers via **speech recognition**, and gives you **instant AI-powered scoring and feedback**.

---

## ✨ Features

| Feature | Details |
|---|---|
| 🤖 AI Avatar | Animated face with mouth movement while speaking |
| 🔊 Text-to-Speech | Questions spoken aloud using browser Web Speech API |
| 🎙️ Speech Recognition | Real-time voice-to-text for your answers |
| ⌨️ Manual Input | Type answers if mic not available |
| 📊 AI Scoring | GPT-3.5 evaluates each answer 0–10 with feedback |
| ⏱️ Timer | Per-question countdown + total session timer |
| 📈 Results Page | Circular score, per-question breakdown |
| 📋 History | All past sessions with score trend chart |
| 🔒 Auth | JWT-based register/login |

---

## 🛠️ Tech Stack

**Frontend:** React 18, Ant Design 5, Framer Motion, React Router 6, React Speech Recognition, React Circular Progressbar

**Backend:** Node.js, Express, MongoDB (Mongoose), JWT Auth, OpenAI API

---

## 🚀 Quick Start

### Prerequisites
- Node.js v16+
- MongoDB running locally OR MongoDB Atlas URI
- (Optional) OpenAI API key for AI scoring

### 1. Clone & Setup
```bash
# Run the setup script
chmod +x setup.sh
./setup.sh
```

Or manually:
```bash
# Backend
cd backend
npm install
cp .env.example .env   # Edit this file!

# Frontend
cd frontend
npm install
```

### 2. Configure Environment
Edit `backend/.env`:
```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/ai-interview
JWT_SECRET=your_secret_key_here
OPENAI_API_KEY=sk-...   # Optional but recommended
```

### 3. Start the App
```bash
# Terminal 1 - Backend
cd backend
npm run dev

# Terminal 2 - Frontend
cd frontend
npm start
```

Open **http://localhost:3000**

---

## 📱 How to Use

1. **Register** a new account
2. On Dashboard → click **"Load Sample Interviews"** (first time only)
3. Choose an interview category
4. **AI avatar speaks the question**
5. Click mic button → **speak your answer**
6. Click **"Submit & Next"** to move forward
7. After all questions → view your **Results page**

---

## 📁 Project Structure

```
ai-interview-platform/
├── backend/
│   ├── models/
│   │   ├── User.js
│   │   ├── Interview.js
│   │   ├── Question.js
│   │   └── Session.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── interviews.js
│   │   ├── questions.js
│   │   └── sessions.js
│   ├── middleware/auth.js
│   ├── server.js
│   └── .env.example
│
└── frontend/
    └── src/
        ├── pages/
        │   ├── LoginPage.js
        │   ├── RegisterPage.js
        │   ├── DashboardPage.js
        │   ├── InterviewPage.js   ← Main interview room
        │   ├── ResultPage.js
        │   └── HistoryPage.js
        ├── components/
        │   └── MainLayout.js
        ├── context/
        │   └── AuthContext.js
        ├── App.js
        └── index.css
```

---

## 🔑 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register user |
| POST | `/api/auth/login` | Login user |
| GET | `/api/interviews` | Get all interviews |
| POST | `/api/interviews/seed` | Seed sample data |
| POST | `/api/sessions/start` | Start interview session |
| POST | `/api/sessions/:id/answer` | Submit answer with AI eval |
| POST | `/api/sessions/:id/complete` | Complete session |
| GET | `/api/sessions/history` | Get user's history |
| GET | `/api/sessions/:id` | Get session result |

---

## 🤝 Without OpenAI Key?

The app works fine without an OpenAI key:
- Answers are still recorded
- Basic scoring based on answer length
- All other features work normally

Add the key later anytime in `backend/.env`.