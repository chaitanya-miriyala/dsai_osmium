# Contributing Guide

Thank you for your interest in contributing to **DSAI Osmium** 🎉
This repository uses a **monorepo structure** with a frontend-first setup. Please follow the guidelines below to ensure smooth collaboration and CI stability.

---

## 📁 Repository Structure

```
apps/
├── web/        # Frontend (Vite + React + TypeScript)
├── api/        # Backend (reserved)
└── mobile/     # Mobile app (reserved)

packages/       # Shared packages (future)
infra/          # Infrastructure & DevOps (future)
scripts/        # Automation scripts (future)
```

---

## 🧰 Prerequisites

Before contributing, make sure you have:

* **Node.js 20+** (recommended)
* **npm 9+**
* Git
* A Unix-like environment (Linux / macOS / WSL)

Optional but recommended:

* `nvm` (for managing Node versions)

---

## 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone <repo-url>
cd dsai-osmium
```

---

### 2️⃣ Install dependencies (workspace-aware)

From the repository root:

```bash
npm install
```

---

## ▶️ Running the Frontend

### Option A: Run from monorepo root (recommended)

```bash
npm run dev:web
```

### Option B: Run from app directory

```bash
cd apps/web
npm run dev
```

---

## 🌱 Environment Variables

Environment variables are **app-specific**.

For the frontend:

```bash
apps/web/.env.example
```

Create a local `.env` file if needed:

```bash
cp apps/web/.env.example apps/web/.env
```

⚠️ Do NOT commit `.env` files.

---

## ✅ Required Checks Before Commit

All contributions **must pass the following checks locally**:

### 1️⃣ Lint (mandatory)

```bash
cd apps/web
npm run lint
```

* Warnings are allowed
* Errors are NOT allowed

---

### 2️⃣ Build (mandatory)

```bash
cd apps/web
npm run build
```

This ensures the app is production-ready.

---

### 3️⃣ Git status check

Before committing:

```bash
git status
```

Ensure you are **not committing**:

* `node_modules/`
* `dist/`
* `.env`

---

## 🔄 Commit Guidelines

* Use clear, descriptive commit messages
* Prefer conventional prefixes:

```
feat: add new homepage section
fix: resolve navbar alignment issue
chore: update lint configuration
ci: adjust frontend workflow
```

---

## 🔍 Continuous Integration (CI)

This repository uses **GitHub Actions**.

### Frontend CI includes:

* Dependency installation
* ESLint checks
* Production build

CI runs automatically on:

* Pull Requests to `main`
* Pushes to `main`

❌ Pull requests will not be merged if CI fails.

---

## 🌿 Branching Strategy

* `main` → stable, production-ready
* Create feature branches:

```bash
git checkout -b feature/your-feature-name
```

---

## 📌 Notes

* Do NOT restructure the monorepo without discussion
* Do NOT add global dependencies
* App-specific changes must stay inside their respective folders

---

## 🤝 Need Help?

If you’re unsure about anything:

* Open an issue
* Start a discussion
* Ask before making large structural changes

---

Happy contributing 🚀