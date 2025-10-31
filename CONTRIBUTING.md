# CONTRIBUTING.md

---

# Contributing to **CodeQuest**

Thank you for your interest in contributing to **CodeQuest**!  
We welcome contributions from developers, designers, educators, and AI enthusiasts.

This guide will help you get started quickly, follow our standards, and make high-quality contributions.

---

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Development Setup](#development-setup)
- [Project Structure](#project-structure)
- [Branching Strategy](#branching-strategy)
- [Commit Convention](#commit-convention)
- [Pull Request Process](#pull-request-process)
- [Testing](#testing)
- [Documentation](#documentation)
- [Release Process](#release-process)
- [Need Help?](#need-help)

---

## How to Contribute

We accept the following types of contributions:

| Type | Examples |
|------|--------|
| **Features** | New challenge types, multi-language support |
| **Bug Fixes** | UI glitches, API errors |
| **Documentation** | Improve README, add examples |
| **Testing** | Add Jest/Cypress tests |
| **UI/UX** | Better forms, accessibility |
| **Performance** | Optimize test runner, caching |

---

## Development Setup

### Prerequisites
- **Node.js** ≥ 18
- **MongoDB** (local or [MongoDB Atlas](https://mongodb.com))
- **Git**

### 1. Fork & Clone
```bash
git clone https://github.com/<your-username>/code-quest.git
cd code-quest
```

### 2. Set Up Environment
```bash
cp .env.example .env
```
Edit `.env`:
```env
MONGODB_URI=mongodb://localhost:27017/codequest_dev
PORT=5000
AI_API_KEY=your_test_key_here
NODE_ENV=development
```

### 3. Install & Run
```bash
# Install root deps
npm install

# Start both servers
npm run dev
```

> Frontend: http://localhost:5173  
> Backend: http://localhost:5000

---

## Project Structure

```bash
code-quest/
├── backend/              # Express.js API
│   ├── models/           # Mongoose schemas
│   ├── routes/           # API endpoints
│   ├── services/         # AI, test runner
│   └── server.js
├── frontend/             # Vite + React
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.jsx
├── docs/                 # PRD, API, Tasks, Snippets
├── .github/
└── docker-compose.yml
```

---

## Branching Strategy

We use **feature branches** with **descriptive names**:

| Purpose | Branch Name |
|--------|-------------|
| New feature | `feature/challenge-analytics` |
| Bug fix | `fix/submit-button-loading` |
| Docs | `docs/update-readme` |
| Hotfix | `hotfix/mongo-connection-leak` |

```bash
git checkout -b feature/your-feature-name
```

---

## Commit Convention

We follow **[Conventional Commits](https://www.conventionalcommits.org/)**.

### Format
```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```

### Types
| Type | When to Use |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `test` | Adding or fixing tests |
| `refactor` | Code changes, no behavior change |
| `perf` | Performance improvement |
| `chore` | Tooling, config, CI |

### Examples
```bash
feat(challenge): add input/output format fields
fix(submit): prevent double submission
docs(api): update POST /submit example
test(backend): add challenge creation unit test
```

> Use **imperative mood** ("add", not "added").

---

## Pull Request Process

1. **Update your branch**
   ```bash
   git fetch origin
   git rebase origin/main
   ```

2. **Run tests & lint**
   ```bash
   npm run lint
   npm run test
   ```

3. **Open PR**
   - Title: Use conventional commit format
   - Description: Link to issue, explain changes
   - Assign reviewer (if team)

4. **PR Template** (auto-filled via `.github/pull_request_template.md`)

---

### PR Checklist
- [ ] Follows commit convention
- [ ] Passes all tests
- [ ] No lint errors
- [ ] Updates docs if needed
- [ ] Tested in browser

---

## Testing

We use:
- **Backend**: Jest + Supertest
- **Frontend**: React Testing Library
- **E2E**: Cypress (planned)

### Run Tests
```bash
# Backend
cd backend && npm test

# Frontend
cd frontend && npm test
```

---

## Documentation

All docs live in [`/docs`](./docs):

| File | Update When |
|------|-------------|
| `PRD.md` | Feature planning |
| `TASKS.md` | New epics/PRs |
| `API-DOCS.md` | New endpoints |
| `CODE-SNIPPETS.md` | New reusable code |

> **Always update docs** when changing behavior.

---

## Release Process

1. **Bump version** in `package.json` (follow [SemVer](https://semver.org))
2. **Create changelog** from commits
3. **Tag release**
   ```bash
   git tag -a v1.0.0 -m "MVP with AI test cases"
   git push origin v1.0.0
   ```
4. **GitHub Release** with auto-generated notes

---

## Need Help?

- **Open an issue** with clear title and steps
- **Join discussions** in GitHub Discussions
- **Ask in PR comments**

We respond within **24 hours**.

---

## Thank You!

Your contribution makes **CodeQuest** better for thousands of learners and educators.

Let’s build the future of coding practice — **together**.

---

**Decagon Dev Team**  
[https://github.com/decagondev](https://github.com/decagondev)  
*Open Source • Open Minds*
