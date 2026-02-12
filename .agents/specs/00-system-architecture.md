# System Architecture (Local-First Baseline)

*Note: Update this file with your actual chosen tech stack once decided.*

**Core Philosophy:** 100% Local, Offline-capable, Zero Telemetry, Privacy-respecting.

## Technology Stack (Example)
- **Frontend/UI:** Desktop application (e.g., Tauri, Electron, PySide) or local web UI (FastAPI/Flask + React/Vanilla JS).
- **Database:** Local SQLite (Use SQLCipher if encryption at rest is required) or local JSON for settings.
- **AI/Processing:** Local inference via `llama.cpp` / Ollama / ONNX Runtime. 
- **File System:** Application data must be stored strictly in the OS-designated local AppData/Config directories.

## Core Patterns
- All external HTTP requests are banned unless they strictly target `localhost` or `127.0.0.1`.
- Avoid pip/npm packages known for tracking. Always prefer minimal, open-source, local-only dependencies.
