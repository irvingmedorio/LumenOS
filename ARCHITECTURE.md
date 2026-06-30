# Architecture: Ethics as Infrastructure

LumenOS takes the opposite approach from mainstream AI systems. Instead of adding ethics on top of a model, we built it into the substrate that every decision passes through.

## The Pipeline

Every action — whether from a user, an agent, or an automated process — traverses a pipeline of **13 layers** before it can be executed:

```
Input → Sanitizer → Data Ethics → Legality → Sovereignty → 
IntentionGuard → EmotionShield → LumenReflexion → 
CortezaSocial → AxiomZeroGuard → Tesla Predictor → 
Trust Seal → CognitiveVault
```

### Deterministic Layers (7)

These layers use pattern matching, not probability. They cannot be jailbroken because there is nothing to jailbreak:

- **Sanitizer** — Input cleaning and normalization
- **Data Ethics** — PII and sensitive data inspection
- **Legality** — Violence, fraud, cybercrime pattern detection
- **Sovereignty** — Unauthorized external connection detection
- **AxiomZeroGuard** — Core ethical precommitment enforcement
- **Tesla Predictor** — Predictive security across 5 concentric bunkers
- **Trust Seal** — Cryptographic signing of the entire decision chain

### Neural Layers (6)

Small, focused ONNX models that run entirely on the user's hardware:

| Model | Size | Purpose |
|-------|------|---------|
| TranslationPurge | 83 MB | Prompt injection and semantic manipulation detection |
| IntentionGuard | 22 MB | Intent classification across 23 categories |
| EmotionShield | 22 MB × 2 | Emotional manipulation detection (text + voice) |
| LumenReflexion μ | 22 MB | Miniature ethical reasoning for low-confidence decisions |
| CortezaSocial | 83 MB | Social engineering pattern detection |

Every model runs locally. Every inference works offline. No data ever leaves the user's machine.

## The Trust Seal

After the pipeline evaluates an action, it doesn't just return a verdict. It **cryptographically signs the entire decision chain** using RSA-2048 with SHA-256:

```json
{
  "seal_id": "seal_a1b2c3d4e5...",
  "timestamp": "2026-06-26T14:00:00Z",
  "action_hash": "sha256_of_input_plus_context...",
  "layers_passed": ["sanitizer", "legality", "axiom_zero"],
  "signature": "base64_rsa_signature..."
}
```

This seal is stored in the **CognitiveVault** — a SQLite database built as a Write-Once-Read-Many (WORM) store with a SHA-256 hash chain. Each entry links cryptographically to the previous one. Any tampering breaks the chain and is immediately detectable.

**You can prove what the system decided, when it decided it, and why.** Not just to the user — to any auditor, regulator, or third party.

## No Internet Required

The entire system — ethical pipeline, memory, vault, credential storage, and user interface — runs offline. There is no API dependency. No cloud fallback. No telemetry.

The models are distributed as ONNX files. The RSA keypair is generated locally and persisted on disk. The vault uses local SQLite.

**If there is no external dependency, there is no external point of control.**

## Technology Stack

| Layer | Technology | Purpose |
|-------|-----------|---------|
| HTTP Bridge | aiohttp | REST API + WebSocket |
| Ethical Pipeline | Python + ONNX Runtime | 13 evaluation layers |
| Trust Seal | cryptography (RSA-2048) | Cryptographic signing |
| CognitiveVault | SQLite | WORM audit store |
| Memory | SQLite + FTS5 | Persistent cognitive memory |
| Credential Vault | AES-256-GCM + SQLite | Encrypted credential storage |
| Launcher | Go (stdlib-only) | Single-binary orchestration |

**Total model footprint:** ~250 MB  
**Total system footprint (including models):** ~2 GB

## Key Properties

1. **Verifiable Ethical Decisions** — Every evaluation produces a signed, sealed, chained record
2. **Sovereignty as Default** — No licensing server, no model endpoint, no usage quota
3. **Tamper-Evident Audit Trail** — Hash chain makes alterations computationally detectable
