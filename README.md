# 🤖 RUNBOOK AGENT
[![Watch the Demo Explanation Video](https://img.shields.io/badge/Watch-Demo%20Video-red?style=for-the-badge&logo=googledrive)](https://drive.google.com/drive/folders/1BX5-v6IP2rZ9mvcntu_ihYKvY_68ao-P?usp=sharing)

**Autonomous Incident Resolution Engine powered by Llama 3**

RUNBOOK AGENT is a real-time autonomous operator that monitors infrastructure, detects failures, and executes recovery runbooks. It leverages the Model Context Protocol (MCP) to bridge AI reasoning with system execution.

---

## 🚀 Key Features
- **Deterministic Autonomy**: Executes markdown-based runbooks sequentially.
- **AI Classification**: Uses local Llama 3 to distinguish between SAFE and RISKY steps.
- **Human-in-the-Loop**: Automatically pauses for user confirmation on critical system changes.
- **MCP Security**: Integrated ShellExecutor with a strict command allowlist.
- **Modern Dashboard**: Real-time terminal feed and infrastructure health monitoring.
- **Discord Alerts**: Instant incident notifications via webhooks.

## 🏗️ Intelligence Stack
1. **Detection**: Monitoring layer triggers incidents based on health status.
2. **Analysis**: Llama 3 analyzes command risk and blast radius.
3. **Execution**: MCP Tool executes validated commands in a simulated environment.

## 📁 Project Structure
- `backend/`: FastAPI server and Agent Control Loop.
- `frontend/`: Single-page interactive dashboard.
- `runbooks/`: Operational instruction sets (Markdown).
- `.env.example`: Template for configuration settings.

## 🚀 Quick Start

### 1. Requirements
- Python 3.11+
- [Ollama](https://ollama.com/) (with `llama3` model)

### 2. Setup
```powershell
# Install dependencies
pip install -r requirements.txt

# Configure environment
cp .env.example .env
```

### 3. Execution
```powershell
# Start the FastAPI server
python -m uvicorn backend.main:app --reload --port 8000
```
Then visit: **http://localhost:8000**

---
