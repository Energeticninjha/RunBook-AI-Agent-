<div align="center">
  <br />
  <img src="https://img.icons8.com/isometric/512/robot.png" width="120" />
  <h1>🚀 RUNBOOK AGENT</h1>
  <h3>Autonomous Incident Resolution Engine</h3>
  <p><i>The Bridge Between AI Reasoning and Infrastructure Recovery</i></p>

  <p>
    <img src="https://img.shields.io/badge/Status-Active-brightgreen" />
    <img src="https://img.shields.io/badge/AI-Llama_3-blue" />
    <img src="https://img.shields.io/badge/Backend-FastAPI-009688" />
    <img src="https://img.shields.io/badge/Automation-MCP-orange" />
  </p>
  <br />
</div>

---

### 🛡️ What is RUNBOOK AGENT?
An enterprise-grade autonomous IT operations agent that detects, classifies, and resolves infrastructure failures in real-time. By combining the **Model Context Protocol (MCP)** with **Llama 3 reasoning**, it executes operational runbooks with safety-first precision.

---

## 🏛️ Intelligence Architecture
```mermaid
graph TD
    A[Infrastructure Monitor] -->|Critical Alert| B(Incident Detected)
    B --> C{Layer 1: Parser}
    C -->|Extract Steps| D[Layer 2: AI Classifier]
    D -->|Safe Check| E{AI Analysis}
    E -->|Safe| F[Layer 3: Execution Engine]
    E -->|Risky| G[Human-in-the-Loop]
    G -->|Confirmed| F
    F -->|Recovery| H[Discord Notification]
```

---

## 🏛️ Three-Layer Autonomy Stack
1.  **Layer 1 · Intelligent Parser**: Transforms Markdown instructions into structured executable JSON pipelines.
2.  **Layer 2 · AI Classifier (LLM)**: Uses Llama 3 to analyze the "Blast Radius" of every command to distinguish between `SAFE` (Reads) and `RISKY` (Restarts/Kills).
3.  **Layer 3 · MCP Execution Engine**: A secure shell executor with a strict security allowlist to prevent unauthorized system modification.

---

## 💬 Incident Resolution Flow
> **[09:00] MONITOR** → 🔴 High CPU Usage Detected (>95%)
>
> **[09:01] AGENT**   → 🔍 Triggered `high_cpu.md`
>
> **[09:01] AGENT**   → 🧠 AI Logic: "Finding top processes is SAFE. Killing PID 1234 is RISKY."
>
> **[09:02] AGENT**   → ⚠️ Paused for human confirmation.
>
> **[09:02] USER**    → ✅ Confirmed.
>
> **[09:03] AGENT**   → 🟢 Resolved. CPU load normalized to 15%.

---

## 📁 Project Structure
*   **`backend/`**: FastAPI logic, Agent Control Loop, and MCP Tooling.
*   **`frontend/`**: Real-time Glassmorphism Dashboard.
*   **`runbooks/`**: Standard markdown operational intelligence.
*   **`.env`**: Centralized configuration management.

---

## 🚀 Quick Start
1.  **Clone**: `git clone <repo-url> && cd opsbot-ai`
2.  **Config**: `cp .env.example .env` (Add your Discord Webhook)
3.  **AI**: `ollama pull llama3`
4.  **Run**: `python -m uvicorn backend.main:app --reload --port 8000`

---
<div align="center">
  Built with ❤️ by Team AI Ops
</div>
