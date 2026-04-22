# 🤖 InterviewAI – Smart AI Interview Platform

InterviewAI is a full-stack MERN application that simulates real interview experiences using AI-driven questions and evaluation. It helps candidates practice interviews and enables admins to manage questions, interviews, and candidates efficiently.

---

## 📸 Screenshots (Optional)
#Login Screen
<img width="1920" height="980" alt="image" src="https://github.com/user-attachments/assets/4d65382b-5190-41ab-bec7-3fccd9fd0151" />
#Candiate Dashboard Screen
<img width="1920" height="981" alt="image" src="https://github.com/user-attachments/assets/ec7a665c-7bcd-4221-a4f6-40abf1572b7b" />
#Interview Screen with Ai
<img width="1920" height="987" alt="image" src="https://github.com/user-attachments/assets/9810bad5-f613-4abd-9cd7-c23b00a6cf66" />





---

## 🚀 Features

### 👨‍💻 Candidate Side

* Register & login securely
* Select multiple interview roles (Frontend, Backend, HR, etc.)
* Attend AI-based interviews
* Get real-time performance analysis
* View interview history & results

### 🛠 Admin Panel

* Manage interview questions (Create, Update, Delete)
* Create & manage interviews
* Assign questions to interviews
* Manage candidates
* Assign interviews to candidates
* Filter & organize data easily

---

## 🧠 Core Functionalities

* 🎯 Role-based access (Admin / Candidate)
* 📊 Performance tracking system
* 🧾 Interview session management
* 🔍 Advanced filtering (category, difficulty, user)
* ✅ Multi-select & bulk operations
* 🔗 Relationship handling (User ↔ Interview ↔ Questions)

---

## 🏗 Tech Stack

### Frontend

* React.js
* Ant Design (UI)
* Framer Motion (animations)
* React Router

### Backend

* Node.js
* Express.js
* MongoDB (Mongoose)

### Other

* JWT Authentication
* REST APIs

---

## 📂 Project Structure

```
/client   → React frontend
/server   → Node.js backend
/models   → Mongoose schemas
/routes   → API routes
/controllers → Business logic
```

---

## 🔐 Authentication & Authorization

* JWT-based authentication
* Role-based access control:

  * Admin → Full access
  * Candidate → Limited access

---

## ⚙️ Installation

### 1. Clone Repository

```
git clone https://github.com/your-username/interview-ai.git
cd interview-ai
```

### 2. Install Dependencies

```
npm install
cd client
npm install
```

### 3. Setup Environment Variables

Create `.env` file in server:

```
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_secret_key
```

### 4. Run Project

```
# Backend
npm run server

# Frontend
cd client
npm start
```

---


## 🚀 Future Enhancements

* AI voice-based interview
* Resume analysis
* Video interview support
* Real-time feedback using ML
* Company-level dashboards

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Mohd Zafar**
Frontend Developer | MERN Stack Developer
