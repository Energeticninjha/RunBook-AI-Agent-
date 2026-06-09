# 🤖 RUNBOOK AGENT — Autonomous Runbook Execution Agent

RUNBOOK AGENT is a real-time, autonomous agent designed to detect, diagnose, and resolve infrastructure failures. It bridges the gap between AI reasoning and system execution using the Model Context Protocol (MCP) pattern.

## 🚀 Key Features
- **Autonomous Agent Loop**: Reads markdown runbooks and executes steps sequentially.
- **MCP Tool Execution**: Custom `ShellExecutorMCPTool` with a strict security allowlist and realistic Linux simulation.
- **Llama 3 Integration**: Uses local Ollama Llama3 to classify steps as SAFE or RISKY.
- **Human-in-the-Loop**: Automatically pauses and requests confirmation for risky operations (restarts, kills).
- **Real-time Dashboard**: Stunning dark theme UI with live feed, health monitoring, and resolution stats.
- **Discord Alerts**: Instant notifications for incident detection and step completion.

## 🛠️ Tech Stack
- **Backend**: Python 3.11, FastAPI, Uvicorn, SQLite
- **AI**: Ollama Llama3 (Local LLM)
- **Frontend**: Vanilla HTML5, CSS3 (Grid/Flexbox), JavaScript (Fetch API)
- **Notifications**: Discord Webhooks

## 📦 Project Structure
```text
runbook-agent/
├── backend/
│   ├── main.py              ← FastAPI app + Routes
│   ├── agent_runner.py      ← AI Agent Control Loop
│   ├── mcp_tool.py          ← Execution Layer (Simulated Linux)
│   ├── runbook_parser.py    ← Operational Knowledge Parser
│   └── database.py          ← SQLite Persistence
├── frontend/
│   └── index.html           ← Single-page Dashboard
├── runbooks/                ← Operational Intelligence
│   ├── nginx_down.md
│   ├── high_cpu.md
│   ├── database_failure.md
│   └── disk_full.md
├── requirements.txt
└── README.md
```

## 🛠️ Windows Setup
1. **Install Dependencies**:
   ```powershell
   pip install -r requirements.txt
   ```
2. **Setup AI**:
   - Install [Ollama](https://ollama.com/)
   - Pull the model: `ollama pull llama3`
3. **Configure Discord (Optional)**:
   - Edit `backend/agent_runner.py` and replace `DISCORD_WEBHOOK` with your URL.
4. **Run the App**:
   ```powershell
   python -m uvicorn backend.main:app --reload --port 8000
   ```
5. **Open Dashboard**:
   - `http://localhost:8000`

## 📊 Demo Script (5 Minutes)
1. **Minute 1**: Introduce the Dashboard and the concept of Autonomous AI Operations.
2. **Minute 2**: Trigger **"🔴 Nginx Server Down"**. Watch the card turn red and the Agent Activity terminal activate.
3. **Minute 3**: Observe the agent performing checks via the MCP tool. Check Discord for live step updates.
4. **Minute 4**: When "Step 4: Restart Nginx" appears, notice it's flagged as **RISKY**. Click **"✅ Confirm & Execute"** in the UI.
5. **Minute 5**: The agent resolves the issue. The status turns green. Show the History table and Execution stats.

---
*Built with ❤️ by Team AI Ops*
