# Roadmap

## ✅ Current Status (June 2026)

The following are implemented and operational:

- [x] **13-layer ethical pipeline** — 7 deterministic + 6 local ONNX models
- [x] **Trust Seal** — RSA-2048 cryptographic signing of every decision
- [x] **CognitiveVault** — WORM SQLite with SHA-256 hash chain
- [x] **Credential Vault** — AES-256-GCM encrypted storage
- [x] **Full offline operation** — Zero cloud dependencies
- [x] **Engram memory system** — SQLite + FTS5 persistent memory with tiered storage
- [x] **HTTP Bridge** — aiohttp REST API + WebSocket (~65 routes)
- [x] **Go Launcher** — Single-binary subprocess orchestration (stdlib only)
- [x] **Whisper STT** — Local speech-to-text via faster-whisper
- [x] **WebSocket streaming** — Real-time ethical status broadcasting
- [x] **File upload** — POST /api/files/upload with sovereign path restrictions

## 🔄 In Progress

- [ ] **Self-contained Windows installer** — Embed Python + models + dependencies via Inno Setup
- [ ] **llama-cpp-python** — In-process GGUF inference (remove Ollama dependency)
- [ ] **agent.py decomposition** — Separate skills, reflexion, and core into focused modules

## 🔮 Next Phase

### NESI — Sovereign Browser
A browser that routes all web traffic through the ethical pipeline. Every page load, every form submission, every download is evaluated by the 13 layers before execution.

### CCM — Central Command Dashboard
Multi-agent orchestration dashboard for monitoring, routing, and coordinating multiple LumenOS instances within a local network.

### Peer Attestation
Cross-system verification of Trust Seals between independent LumenOS instances. Enables a network of mutually trusting sovereign agents without a central authority.

### CriptoLUX Marketplace
Decentralized marketplace for sovereign AI services, powered by local proof-of-work validation.

---

## The Long View

LumenOS is not a product. It is a proof that the alternative is buildable.

The goal is not to compete with GPT-4 on breadth of knowledge — it's to compete on **trust**. For a growing class of use cases, trust matters more than trivia.

> *"If someone like me — without a degree, without funding, without a team — could get this far, then the alternative isn't just buildable. It must be built."*
