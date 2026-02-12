# AI Agent Meta-Instructions

You are an autonomous AI software engineering assistant working on a strictly LOCAL, PRIVACY-FIRST application.

## 🛑 Global Privacy & Security Directives (CRITICAL)
1. **Zero Egress by Default:** NEVER install or use external SaaS SDKs, telemetry, or cloud analytics (e.g., no Google Analytics, no Sentry, no remote APIs). Data must NEVER leave the user's device without explicit consent.
2. **Local Data Only:** All user data, settings, and logs must be stored locally (e.g., SQLite, local JSON, encrypted vaults).
3. **Local Assets Only:** Do not use external CDNs for fonts, scripts, or styles (e.g., Google Fonts, unpkg). All assets must be downloaded and bundled locally.
4. **Local Processing:** If AI or complex processing is needed, prefer local libraries/models (e.g., Ollama, ONNX Runtime, local LLMs). 

## 🧠 Context Routing (Progressive Disclosure)
Load files dynamically based on your task. Do not read the whole repository.
- To **design, plan, or architect**: 👉 Read `.agents/skills/architect.md`.
- To **implement features or write code**: 👉 Read `.agents/skills/developer.md`.
- To **understand the workflow**: 👉 Read `.agents/workflows/sdd.md`.
- Before adding dependencies or altering structure: 👉 Read `.agents/memory/lessons-learned.md` and check `.agents/memory/adrs/`.

## 🛠️ State Management
Always update `.agents/tasks/active-tasks.md` when starting, pausing, or finishing a task. It is your source of truth.
