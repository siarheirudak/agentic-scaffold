# System Architecture (Local-First Baseline)

_Note: Update this file with your actual chosen tech stack once decided._

**Core Philosophy:** 100% Local, Offline-capable, Zero Telemetry, Privacy-respecting.

## Technology Stack (Example)

- **Frontend/UI:** Desktop application (e.g., Tauri, Electron, PySide) or local web UI (FastAPI/Flask + React/Vanilla JS).
- **Database:** Local SQLite (Use SQLCipher if encryption at rest is required) or local JSON for settings.
  10: - **AI/Processing:** Local inference via `llama.cpp` / Ollama / ONNX Runtime. **Fallback:** Remote LLM APIs (e.g., OpenAI, Anthropic) if local is insufficient.
  11: - **File System:** Application data must be stored strictly in the OS-designated local AppData/Config directories.
  12:
  13: ## Core Patterns
  14: - All external HTTP requests are banned unless they strictly target `localhost`, `127.0.0.1`, or an approved Remote LLM provider.
- Avoid pip/npm packages known for tracking. Always prefer minimal, open-source, local-only dependencies.
