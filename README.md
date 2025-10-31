# CodeQuest  
**AI-Powered Coding Challenge Platform**  
*Create, Solve, and Assess with Real-Time Feedback*  

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)  
![React](https://img.shields.io/badge/React-18.2.0-blue?logo=react)  
![Express](https://img.shields.io/badge/Express-4.18.2-lightgrey?logo=express)  
![MongoDB](https://img.shields.io/badge/MongoDB-7.0-green?logo=mongodb)  
![Vite](https://img.shields.io/badge/Vite-5.0-yellow?logo=vite)  

---

## Project Overview

**CodeQuest** is a modern, full-stack platform for **creating, solving, and evaluating** coding challenges with **AI-generated test cases** and **real-time feedback**.

Whether you're a **coding enthusiast** practicing for interviews, an **educator** building assessments, or a **company** screening candidates — CodeQuest delivers a seamless, customizable experience.

### Key Features
| Feature | Description |
|-------|-----------|
| **Custom Challenge Creation** | Define problems, constraints, input/output formats |
| **AI Test Case Generation** | Automatically generate edge cases using third-party AI |
| **Real-Time Code Execution** | Instant feedback with detailed test results |
| **Role-Based Workflows** | Tailored for enthusiasts, educators, and recruiters |
| **Responsive UI** | Built with Vite + React + Monaco Editor |

---

## Tech Stack

| Layer | Technology |
|------|------------|
| **Frontend** | Vite, React 18, React Router, Monaco Editor |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (via Mongoose) |
| **AI Integration** | Third-party API (`https://ai-api.com/generate-test-cases`) |
| **Deployment** | Docker, Heroku/AWS-ready |
| **Testing** | Jest, React Testing Library, Cypress (planned) |

---

## Project Structure

```bash
code-quest/
├── backend/                # Express.js server
│   ├── models/
│   ├── routes/
│   ├── services/
│   └── server.js
├── frontend/               # Vite + React app
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.jsx
│   └── vite.config.js
├── docs/                   # Documentation
│   ├── PRD.md              # Product Requirements
│   ├── TASKS.md            # Development breakdown
│   ├── API-DOCS.md         # Full API spec
│   └── CODE-SNIPPETS.md    # Ready-to-use code
├── .env.example
├── docker-compose.yml
└── README.md
```

---

## Quick Start (Development)

### Prerequisites
- [Node.js](https://nodejs.org/) ≥ 18
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- [Git](https://git-scm.com/)

### 1. Clone & Install

```bash
git clone https://github.com/decagondev/code-quest.git
cd code-quest
```

### 2. Set Up Environment

```bash
cp .env.example .env
```

Edit `.env`:
```env
MONGODB_URI=mongodb://localhost:27017/codequest
PORT=5000
AI_API_KEY=your_ai_api_key_here
NODE_ENV=development
```

### 3. Install Dependencies

```bash
# Backend
cd backend
npm install

# Frontend (in another terminal)
cd ../frontend
npm install
```

### 4. Run the App

```bash
# From root: Start both servers
npm run dev
```

> Backend: http://localhost:5000  
> Frontend: http://localhost:5173

---

## Available Scripts

| Script | Description |
|-------|-------------|
| `npm run dev` | Run backend + frontend in parallel |
| `npm run backend` | Start Express server (`nodemon`) |
| `npm run frontend` | Start Vite dev server |
| `npm run build` | Build frontend for production |
| `npm run preview` | Preview production build |

---

## Documentation

All project documentation lives in [`/docs`](./docs/):

| File | Purpose |
|------|--------|
| [`PRD.md`](./docs/PRD.md) | Full product vision, user stories, architecture |
| [`TASKS.md`](./docs/TASKS.md) | Epic → PR → Commit breakdown for developers |
| [`API-DOCS.md`](./docs/API-DOCS.md) | Complete REST API spec + OpenAPI YAML |
| [`CODE-SNIPPETS.md`](./docs/CODE-SNIPPETS.md) | Copy-paste ready code for all features |

---

## API Endpoints

See full API docs: [API-DOCS.md](./docs/API-DOCS.md)

**Base URL**: `http://localhost:5000/api`

| Method | Endpoint | Description |
|-------|----------|-----------|
| `POST` | `/challenges` | Create challenge + AI test cases |
| `GET` | `/challenges/:id` | Get challenge (with hidden tests if owner) |
| `POST` | `/submit` | Run code against test cases |

---

## Deployment

### Docker (Recommended)

```bash
docker-compose up --build
```

### Manual (Heroku, Render, etc.)

1. Build frontend: `npm run build` (in `/frontend`)
2. Set `NODE_ENV=production`
3. Deploy backend with `server.js` as entrypoint

---

## Contributing

We follow a **PR-based workflow** with granular commits (see [TASKS.md](./docs/TASKS.md)).

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/your-task`
3. Follow commit structure from `TASKS.md`
4. Open a PR with clear description

---

## Roadmap

| Milestone | Features |
|---------|----------|
| **v1.0 (MVP)** | Challenge CRUD, AI test cases, real-time feedback |
| **v1.1** | User auth (JWT), private challenges |
| **v1.2** | Multi-language support (Python, Java) |
| **v2.0** | Leaderboards, analytics dashboard |

---

## License

[MIT License](./LICENSE) – Free to use, modify, and distribute.

---

## Made with Love by Decagon

> **CodeQuest** — Level up your coding, one challenge at a time.

[GitHub](https://github.com/decagondev/code-quest) • [Docs](./docs) • [Report Bug](https://github.com/decagondev/code-quest/issues)

---

*Built for developers, educators, and innovators.*
