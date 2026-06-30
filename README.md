# LumenOS — Sovereign AI Operating System

**Ethics as infrastructure. Sovereignty as default. Zero cloud dependencies.**

LumenOS is a sovereign AI operating system built on a radical premise: that artificial intelligence can be designed to serve the individual instead of the corporation. Every action — whether from a user, an agent, or an automated process — traverses a pipeline of 13 ethical layers before it can be executed. Every decision is cryptographically signed with RSA-2048 and stored in a tamper-evident vault with SHA-256 hash chaining.

**It runs on a laptop today. No internet required.**

---

## The Philosophy

| Principle | Meaning |
|-----------|---------|
| **Sovereignty as Default** | No licensing server, no model endpoint, no usage quota. Runs on your hardware, with your models, on your data. |
| **Ethics as Infrastructure** | Not a content filter on top — 13 layers built into the substrate every decision passes through. |
| **Privacy by Architecture** | RSA-signed Trust Seals. Tamper-evident CognitiveVault. Zero telemetry. Zero data collection. |
| **Transparency, not dopamine** | The system tells the truth, even when it hurts. No fake empathy, no engagement tricks. |

---

## Core System

```
Input → Sanitizer → Data Ethics → Legality → Sovereignty → 
IntentionGuard → EmotionShield → LumenReflexion → 
CortezaSocial → AxiomZeroGuard → Tesla Predictor → 
Trust Seal → CognitiveVault
```

- **13 evaluation layers** — 7 deterministic, 6 local ONNX models
- **Trust Seal** — RSA-2048 cryptographic signature on every decision
- **CognitiveVault** — Write-Once-Read-Many SQLite with SHA-256 hash chain
- **100% offline** — No API dependency, no cloud fallback, no telemetry

---

## Architecture Overview

| Layer | Technology | Purpose |
|-------|-----------|---------|
| HTTP Bridge | aiohttp | REST API + WebSocket |
| Ethical Pipeline | Python + ONNX Runtime | 13 evaluation layers |
| Trust Seal | cryptography (RSA-2048) | Cryptographic signing |
| CognitiveVault | SQLite | WORM audit store |
| Memory | SQLite + FTS5 | Persistent cognitive memory |
| Credential Vault | AES-256-GCM + SQLite | Encrypted credential storage |
| Launcher | Go (stdlib-only) | Single-binary orchestration |

**Total system footprint** (including models): ~2 GB

---

## Read the Full Article

📖 **Medium** — [Empire of AI: How LumenLUX Builds the Ethical Alternative That Hao Demands](https://medium.com/p/21776daebc00)

---

## Documentation

| File | What it covers |
|------|----------------|
| [MANIFESTO.md](./MANIFESTO.md) | The 3 immutable laws: Crystal Transparency, Time Economy, Symmetry of Respect |
| [MANIFIESTO_DE_SOBERANIA.md](./MANIFIESTO_DE_SOBERANIA.md) | Privacy policy: zero data collection, no advertising, anonymous learning |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Technical architecture: pipeline, Trust Seal, CognitiveVault |
| [ROADMAP.md](./ROADMAP.md) | Current status, next phases, and future vision |
| [article.md](./article.md) | Full article: "Empire of AI: How LumenLUX Builds the Ethical Alternative That Hao Demands" (English) |
| [articulo.md](./articulo.md) | Artículo completo en español |

---

## The Code

LumenOS is a living system. The source code lives in a separate repository:

👉 **[irvingmedorio/LumenPowerMain](https://github.com/irvingmedorio/LumenPowerMain)** — Python + ONNX + Go implementation

---

## Why This Matters

> *"The question Hao raised was about the kind of AI we want to exist. This is one answer: an AI that cannot lie about what it decided, cannot be remotely controlled, and does not need to sell your attention to function."*

LumenOS is not a product. It is a proof that the alternative is buildable.

---

📖 Read on **[Medium](https://medium.com/p/21776daebc00)**

**Created by [Irving Díaz Medorio](https://github.com/irvingmedorio)** — June 2026  
Part of the LumenOS ecosystem.
