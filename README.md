# 📝 Todo REST API

> A full CRUD REST API for Todo management built with **Node.js**, **Express**, and **MongoDB**, tested with **Postman**, and containerized with **Docker**.

![Node](https://img.shields.io/badge/Node.js-18-green?style=flat-square&logo=node.js)
![Express](https://img.shields.io/badge/Express-4.x-black?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/MongoDB-6.x-47A248?style=flat-square&logo=mongodb)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=flat-square&logo=docker)
![Postman](https://img.shields.io/badge/Postman-Tested-FF6C37?style=flat-square&logo=postman)

---

## 📌 Project Overview

This project is a **RESTful API** that allows users to create, read, update, and delete todo tasks. It uses **MongoDB** as the database with **Mongoose** for schema modeling. All endpoints were tested using **Postman** and the app runs inside **Docker** containers.

### How it works

The Express server connects to a MongoDB database on startup. API requests hit the `/api/todos` routes, which interact with the `Todo` model via Mongoose. The Postman collection in the `postman/` folder lets you test all endpoints instantly.

---

## ✨ Features

- ✅ Full **CRUD** operations (Create, Read, Update, Delete)
- 🗄️ **MongoDB** database with Mongoose schemas
- 🐳 **Dockerized** — app + MongoDB run together via Docker Compose
- 📬 **Postman collection** included for easy API testing
- 🔐 **Environment variables** via `.env` for secure config
- ⚡ Clean folder structure with routes, models, and config separated

---

## 🗂️ Project Structure

```
todo-api/
├── config/
│   └── db.js               # MongoDB connection logic
├── models/
│   └── Todo.js             # Mongoose schema & model
├── routes/
│   └── todos.js            # All CRUD API routes
├── postman/
│   └── collection.json     # Postman API test collection
├── app.js                  # Express app entry point
├── package.json            # Node dependencies & scripts
├── Dockerfile              # Docker image config
├── docker-compose.yml      # App + MongoDB services
├── .env.example            # Sample environment variables
├── .gitignore              # Files excluded from Git
└── README.md               # Project documentation
```

---

## 🛠️ Tech Stack

| Layer        | Technology                  |
|--------------|-----------------------------|
| Runtime      | Node.js 18                  |
| Framework    | Express 4.x                 |
| Database     | MongoDB 6 + Mongoose        |
| API Testing  | Postman                     |
| Container    | Docker + Docker Compose     |
| Config       | dotenv                      |

---

## 🔌 API Endpoints

Base URL: `http://localhost:5000/api/todos`

| Method | Endpoint       | Description          | Body                              |
|--------|----------------|----------------------|-----------------------------------|
| GET    | `/`            | Get all todos        | —                                 |
| GET    | `/:id`         | Get a single todo    | —                                 |
| POST   | `/`            | Create a new todo    | `{ "title": "Task name" }`        |
| PUT    | `/:id`         | Update a todo        | `{ "title": "...", "completed": true }` |
| DELETE | `/:id`         | Delete a todo        | —                                 |

---

## 🚀 Getting Started

### Prerequisites
- [Docker](https://www.docker.com/get-started) (v20+)
- [Node.js](https://nodejs.org/) (v18+) — only for local run without Docker

### Option 1: Docker Compose ⭐ Recommended

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/todo-api.git
cd todo-api

# Start app + MongoDB together
docker-compose up --build
```

App runs at: **http://localhost:5000**

### Option 2: Run locally (without Docker)

```bash
# Install dependencies
npm install

# Create your .env file
cp .env.example .env
# Edit .env and add your MongoDB URI

# Start the server
npm run dev
```

---

## 📬 Testing with Postman

1. Open **Postman**
2. Click **Import** → select `postman/collection.json`
3. All 5 endpoints will be loaded and ready to test!

---

## 🤝 Contributing

1. Fork this repository
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add: your feature description"
   ```
4. Push and open a Pull Request:
   ```bash
   git push origin feature/your-feature-name
   ```

---

## 📤 Upload to GitHub

```bash
git init
git add .
git commit -m "Initial commit: Todo REST API with MongoDB + Docker"
git remote add origin https://github.com/YOUR_USERNAME/todo-api.git
git branch -M main
git push -u origin main
```

> ⚠️ Make sure your `.env` file is listed in `.gitignore` — never push secrets to GitHub!

---

## 📄 License

MIT License — free to use and modify.

---

## 👨‍💻 Author

Made with ❤️ using Node.js + MongoDB + Docker

> ⭐ Star this repo if you found it helpful!
