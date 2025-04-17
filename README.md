# 🔧 LLM-based Automation Agent

> **Automate plain-English tasks using a GPT-4o-Mini powered agent**  
> Built for DataWorks Solutions (TDS 2025 Project 1)

---

## 📜 Project Overview

This project is an intelligent automation agent designed to handle operational and business tasks described in natural language. It uses a Large Language Model (LLM) — via AI Proxy's GPT-4o-Mini — to interpret task instructions and perform multi-step actions within a controlled environment.

---

## 🧠 How It Works

This agent exposes two REST API endpoints:

- `POST /run?task=<task description>`  
  → Executes a plain-English task by parsing it, determining its intent, and running appropriate actions.

- `GET /read?path=<file path>`  
  → Returns the contents of a file for verification purposes.

---

## ✅ Supported Tasks

### 📁 Phase A – Operational Tasks
- Run external Python data scripts
- Format files using `prettier`
- Date counting (e.g., count Wednesdays in a file)
- Sort JSON arrays
- Extract log entries
- Parse Markdown headings
- Use LLM to extract structured data (e.g. email, card number)
- Use embeddings to find comment similarity
- Run SQL queries on SQLite files

### 🧩 Phase B – Business + Security Tasks
- Enforce sandboxed `/data`-only access (no deletion, no exfiltration)
- API fetching and saving
- Git repo cloning and commits
- SQL on SQLite / DuckDB
- Web scraping
- Image compression/resizing
- Audio transcription
- Markdown-to-HTML conversion
- CSV filtering via API

---

## 🚀 Getting Started

### 🧪 Run via Docker

> Make sure you have [Podman](https://podman.io/) or Docker installed.

```bash
podman run --rm \
  -e AIPROXY_TOKEN=$AIPROXY_TOKEN \
  -p 8000:8000 \
  your-dockerhub-username/your-repo-name
