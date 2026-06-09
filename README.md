# RUNBOOK AGENT
```
██████╗ ██╗   ██╗███╗   ██╗██████╗  ██████╗  ██████╗ ██╗  ██╗     █████╗  ██████╗ ███████╗███╗   ██╗████████╗
██╔══██╗██║   ██║████╗  ██║██╔══██╗██╔═══██╗██╔═══██╗██║ ██╔╝    ██╔══██╗██╔════╝ ██╔════╝████╗  ██║╚══██╔══╝
██████╔╝██║   ██║██╔██╗ ██║██████╔╝██║   ██║██║   ██║█████╔╝     ███████║██║  ███╗█████╗  ██╔██╗ ██║   ██║   
██╔══██╗██║   ██║██║╚██╗██║██╔══██╗██║   ██║██║   ██║██╔═██╗     ██╔══██║██║   ██║██╔══╝  ██║╚██╗██║   ██║   
██║  ██║╚██████╔╝██║ ╚████║██████╔╝╚██████╔╝╚██████╔╝██║  ██╗    ██║  ██║╚██████╔╝███████╗██║ ╚████║   ██║   
╚═╝  ╚═╝ ╚═════╝ ╚═╝  ╚═══╝╚═════╝  ╚═════╝  ╚═════╝ ╚═╝  ╚═╝    ╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚═╝  ╚═══╝   ╚═╝   
```

Autonomous · Incident-Aware · Safety-First
RUNBOOK AGENT is an enterprise-grade autonomous IT operations agent that processes infrastructure failures through a three-layer intelligence stack — resolving downtime with AI precision.

## 🏛️ Three-Layer Autonomy Stack
```
┌──────────────────────────────────────┐
│       INFRASTRUCTURE MONITOR         │
│  (Nginx / CPU / DB / Disk Metrics)   │
└──────────────────┬───────────────────┘
                   │
         🚀 INCIDENT TRIGGERED 
                   │
╔══════════════════▼════════════════════╗
║    LAYER 1 · INTELLIGENT PARSER      ║
║                                      ║
║  Markdown Runbooks ──► JSON steps    ║
║  SAFE vs RISKY Tagging               ║
╚══════════════╤═══════════════════════╝
               │
╔══════════════▼═══════════════════════╝
║    LAYER 2 · AI CLASSIFIER (LLM)     ║
║                                      ║
║  Llama 3 Reasoning Engine            ║
║  Auto-Execute / Confirm Logic        ║
╚══════════════╤═══════════════════════╝
               │
╔══════════════▼═══════════════════════╝
║    LAYER 3 · MCP EXECUTION ENGINE    ║
║                                      ║
║  ShellExecutor (Simulated Linux)     ║
║  Security Allowlist Verification     ║
╚══════════════════════════════════════╝
```

## 💬 Full Incident Walkthrough
```
[09:00] MONITOR → 🔴 [ALARM] Nginx Service Down (Port 80 Refused)
[09:00] AGENT   → 🔍 IDENTIFIED: nginx_down.md selected.
[09:01] AGENT   → 🧠 CLASSIFYING: Step 1 (Check status) -> [SAFE: Read-only]
[09:01] AGENT   → ⚡ EXECUTING: systemctl status nginx...
[09:02] AGENT   → 🧠 CLASSIFYING: Step 4 (Restart Nginx) -> [RISKY: Service State Change]
[09:02] AGENT   → ⚠️ AWAITING CONFIRMATION: Dashboard alert triggered.
[09:02] USER    → ✅ [CONFIRMED via Dashboard]
[09:02] AGENT   → ⚡ EXECUTING: systemctl restart nginx...
[09:03] AGENT   → 🟢 RESOLVED: Nginx healthy. Recovery notification sent to Discord.
```

## 📁 Project Structure
```
runbook-agent/
├── backend/
│   ├── main.py              Application bootstrap · FastAPI Routing
│   ├── agent_runner.py      Autonomous Control Loop · Llama 3 Client
│   ├── mcp_tool.py          MCP ShellExecutor · Safety Allowlist
│   ├── runbook_parser.py    Markdown Intelligence · Step Extraction
│   └── database.py          SQLite Persistence · Incident History
│
├── frontend/
│   └── index.html           Real-time Dashboard · Terminal Feed · Health UI
│
├── runbooks/                Static Operational Intelligence
│   ├── nginx_down.md        Web Service Recovery
│   ├── high_cpu.md          Performance Optimization
│   ├── database_failure.md  Connection Recovery
│   └── disk_full.md         Storage Cleanup
│
├── .env.example             Environment Variable Template
├── requirements.txt         FastAPI · OpenAI · Requests · PyYAML
└── README.md                Enterprise Documentation
```

## 🚀 Quick Start
1 · Clone & Configure
```powershell
git clone <repo-url> && cd opsbot-ai
cp .env.example .env # Edit .env with your DISCORD_WEBHOOK_URL
```

2 · Setup AI
Install [Ollama](https://ollama.com/) and run:
```powershell
ollama pull llama3
```

3 · Run Locally
```powershell
pip install -r requirements.txt
python -m uvicorn backend.main:app --reload --port 8000
```

## ⚙️ Configuration
| Variable | Default | Description |
|----------|---------|-------------|
| `OLLAMA_URL` | `http://localhost:11434/v1` | Local LLM Server |
| `DISCORD_WEBHOOK_URL` | `None` | Notification endpoint |
| `PORT` | `8000` | Dashboard listener |

---
*Built with ❤️ by Team AI Ops*
