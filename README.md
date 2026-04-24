# 🚀 JobSync – AI-Powered Job Application Tracker

**Track • Analyze • Optimize – Your job search, supercharged with AI.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-15-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-98.9%25-blue)](https://www.typescriptlang.org/)
[![Prisma](https://img.shields.io/badge/Prisma-ORM-2D3748)](https://www.prisma.io/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED)](https://www.docker.com/)

**JobSync** is a **self-hosted, open‑source** job search companion that combines a full‑featured application tracker with an **AI‑powered career assistant**. Keep complete control over your data while getting intelligent resume reviews, job matching, and actionable analytics.

![Dashboard Preview](screenshots/dashboard.png)

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| 📋 **Application Tracker** | Centralized log of all jobs, statuses, notes, and deadlines |
| 📊 **Analytics Dashboard** | Interactive charts for success rates, trends, and task progress |
| 🤖 **AI Resume Review** | Instant, actionable feedback on your resume (local or cloud AI) |
| 🎯 **AI Job Matching** | Semantic similarity scoring between your resume and job descriptions |
| 📝 **Resume Management** | Version control, multiple resumes, and ATS compatibility checker |
| ✅ **Task Logging** | Time‑tracked activities, follow‑up reminders, and productivity insights |
| 🔐 **Privacy‑First** | Self‑hosted, local data storage, optional offline AI with Ollama |

---

## 🧠 AI Providers – You Choose

JobSync works with **any AI model** that supports structured output – switch providers anytime in the **Settings** page.

| Provider | Type | Privacy | Cost |
|----------|------|---------|------|
| **Ollama** (local) | Local LLM | 🔒 Highest – data never leaves your machine | Free |
| **OpenAI** (GPT‑4, GPT‑3.5) | Cloud API | 🔓 Standard | Pay‑as‑you‑go |
| **DeepSeek** | Cloud API | 🔓 Standard | Very low |
| **Google Gemini** | Cloud API | 🔓 Standard | Free tier available |
| **OpenRouter** | Aggregator | 🔓 Varies | Provider‑dependent |

> 💡 **Recommended**: Start with **Ollama** for complete privacy and zero cost.

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| **Frontend** | Next.js 15, React, Shadcn UI, Tailwind CSS, Tiptap Editor |
| **Backend** | Next.js API Routes, NextAuth.js (authentication) |
| **Database** | SQLite + Prisma ORM (type‑safe, easy migration to PostgreSQL) |
| **AI** | Ollama, OpenAI, DeepSeek, Gemini, OpenRouter |
| **Visualization** | Nivo Charts, D3.js |
| **Deployment** | Docker, Docker Compose |
| **Language** | TypeScript (98.9% of codebase) |

---

## 📦 Quick Start (Docker)

**Prerequisites:** Docker and Docker Compose installed.

```bash
# 1. Clone the repository
git clone https://github.com/kirankumarrout/jobsync.git
cd jobsync

# 2. Start the application
docker compose up -d

# 3. Open your browser and visit
http://localhost:3737



# Install dependencies
npm install

# Configure environment
cp .env.example .env
# Edit .env with your database and auth settings

# Setup database
npx prisma generate
npx prisma db push

# Run development server
npm run dev

⚙️ Configuration
Environment variables are set in docker-compose.yml or .env.

Variable	Description	Required
DATABASE_URL	SQLite database path (e.g., file:./prisma/dev.db)	Yes
NEXTAUTH_URL	Your app’s base URL (e.g., http://localhost:3737)	Yes
NEXTAUTH_SECRET	Secret for auth tokens – generate with openssl rand -base64 32	Yes
ENCRYPTION_KEY	For encrypting API keys – use same 32‑byte random	Only if using cloud AI
TZ	Your timezone (e.g., Asia/Kolkata, America/New_York)	Recommended



