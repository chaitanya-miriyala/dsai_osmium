# DSAI Osmium – Monorepo

This repository follows a **monorepo architecture**, where multiple applications live inside a single Git repository.

Currently, the project contains a **frontend web application**. Backend and mobile applications can be added later without changing the structure.

---

## 📁 Folder Structure

```
dsai-osmium/
│
├── apps/
│   ├── web/              # Frontend (Vite + React + TypeScript)
│   │   ├── src/
│   │   ├── public/
│   │   ├── index.html
│   │   ├── package.json
│   │   ├── tsconfig.json
│   │   └── vite.config.ts
│   │
│   ├── api/              # (Reserved) Backend app – not added yet
│   └── mobile/           # (Reserved) Mobile app – not added yet
│
├── packages/             # (Reserved) Shared code (utils, types, UI)
├── infra/                # (Reserved) Infrastructure / DevOps
├── scripts/              # (Reserved) Automation scripts
│
├── package.json          # Root workspace configuration
├── .gitignore
└── README.md
```

---

## 🧠 Monorepo Overview

- All applications live inside the `apps/` directory
- The repository uses **npm workspaces**
- Each app is isolated but managed from a single repo
- Structure is scalable and industry-standard

---

## 🚀 Running the Web Application

There are **two supported ways** to run the frontend.

### Option 1: Run from Monorepo Root (Recommended)

```
npm run dev:web
```

This uses the root workspace configuration and runs the web app inside `apps/web`.

---

### Option 2: Run from Web App Directory

```
cd apps/web
npm install
npm run dev
```

This runs the frontend as a standalone project.

---

## 📦 Installing Dependencies

### Install from repository root (recommended)

```
npm install
```

This installs dependencies for all workspace applications.

---

### Install only for web app

```
cd apps/web
npm install
```

---

## 🛠 Web Tech Stack

- Vite
- React
- TypeScript
- Tailwind CSS
- npm Workspaces

---

## 🔮 Future Expansion

- Backend service in `apps/api`
- Mobile application in `apps/mobile`
- Shared code in `packages/`
- CI/CD and Docker support

---

## 📌 Developer Notes

- Prefer running commands from the **repo root**
- Do not use global instal