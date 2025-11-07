# TaskMapr

[![Backed by MIT Sandbox](https://img.shields.io/badge/Backed_by-MIT_Sandbox-A31F34.svg)](https://innovation.mit.edu/entrepreneurship-2/mit-sandbox-innovation-fund/)

**Cursor-style AI assistants for your web applications**

TaskMapr provides React components and AI agent integration tools that bring Cursor-like experiences to websites and web apps.

## Projects

### [@taskmapr/ui-overlay](https://github.com/taskmapr/ui-overlay)
React overlay component with built-in chat, UI highlighting, and guided walkthroughs.

```bash
npm install @taskmapr/ui-overlay
```

**Features:**
- Self-contained chat overlay
- Element highlighting by ID or keywords
- Interactive guided walkthroughs
- AI agent integration (OpenAI Agents SDK, Swarm, custom backends)
- Expanded chat composer with smarter autosizing
- Full TypeScript support
- Beautiful dark theme UI

### [taskmapr/orchestrator](https://github.com/taskmapr/orchestrator)
FastAPI backend for AI agent orchestration with OpenAI Agents SDK, Supabase persistence, and rich contextual awareness.

**Features:**
- OpenAI Agents SDK integration with reasoning and tool use
- Rich context from DOM elements, page state, and navigation
- Built-in knowledge tools that expose curated markdown briefs
- SSE streaming with real-time typed events
- Supabase integration for persistent conversation history
- MCP tools for extensible domain-specific workflows
- JWT authentication via Supabase token verification

## Architecture at a Glance

```mermaid
flowchart LR
    A[TaskMapr UI Overlay<br/>@taskmapr/ui-overlay] -->|Actions & Context| B(TaskMapr Orchestrator<br/>FastAPI)
    B -->|Streaming Responses| A
    B -->|Persistence| C[(Supabase)]
    B -->|Tool Calls| D[(MCP / External Systems)]
```

## Tech Stack

- **Frontend:** React, TypeScript, Tailwind CSS
- **Backend:** FastAPI, Python, Supabase
- **AI Integration:** OpenAI Agents SDK, Swarm
- **Build:** Vite, Rollup

## Quick Start

```bash
# 1. Install the overlay package for your React app
npm install @taskmapr/ui-overlay

# 2. Clone & run the orchestrator backend
git clone https://github.com/taskmapr/orchestrator.git
cd orchestrator
pip install -r requirements.txt
uvicorn app.server:app --reload --port 8000
```

That’s the high-level flow—refer to each project’s README for environment variables, auth configuration, and deeper setup instructions.

## License

All TaskMapr projects are MIT licensed unless otherwise specified.

---

**Built with ❤️ for developers who want to add AI assistance to their apps**
