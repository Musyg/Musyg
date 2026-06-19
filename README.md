# Gilles

Security researcher, developer, and AI systems engineer. Based in Switzerland.
I work at Inaricom, where I cover security, and software engineering.

Three distinct practices — each stands on its own below.

---

## 🔒 Security

**Security Researcher & Auditor @ Inaricom**

I find and prove vulnerabilities in smart contracts.
Every finding ships with a reproducible proof of concept. If it isn't reproducible, it isn't a finding.

**Focus**
- Smart contracts — Solidity / Vyper, Foundry fork PoCs, formal verification
- ZK & applied cryptography — circuits, verifiers, proof systems

**Proof of work**
- [stvault-audit](https://github.com/Musyg/stvault-audit) — a deliberately vulnerable lending vault reviewed end to end: every finding proven with a passing Foundry PoC, plus a full PDF report.
- _More reviews coming — one repo per vulnerability class (oracle manipulation, cross-id reentrancy, ERC-4626 donation, governance executors)._

**Competition profiles**
- Cantina — [@GilMu](https://cantina.xyz/u/GilMu)
- Code4rena — [@GiMu84](https://code4rena.com/@GiMu84)

---

## 💻 Development

**Backend & infrastructure engineer**

Resilient, async-first Python services and the infrastructure primitives that keep them up.

- [async-api-client](https://github.com/Musyg/async-api-client) — resilient async REST client: rate limiting, retries, pagination.
- [agent-resilience](https://github.com/Musyg/agent-resilience) — circuit breaker, Redis-backed DLQ, offline MQTT buffer.

_Engagement: backend APIs, integrations, observability, CI._

---

## 🤖 AI & Agentic Systems

**Applied AI & Agentic Systems Engineer**

I design and build autonomous multi-agent systems that run real operations end to end and improve their own code over time. Mostly local models, orchestrated across a small fleet of machines.

- [talos](https://github.com/Musyg/talos) — distributed agentic platform: ~55 agents and 85+ services across a four-node fleet, four-part memory, real-time voice and chat assistant, self-improving build pipelines.
- [multi-agent-orchestrator](https://github.com/Musyg/multi-agent-orchestrator) — capability-based task routing template.

**Stack** — Python (async-first) · local LLM ops (llama.cpp / GGUF, model routing, VRAM-aware hot-swap) · multi-agent orchestration · graph-RAG memory · vector search · MQTT event bus · real-time voice · Prometheus / VictoriaMetrics · systemd · CI (ruff, pytest, pre-commit).

---

## How I work

- Evidence over claims. If it isn't reproducible, it isn't done.
- Metrics-driven — every change is measured.
- Execution-verified over single-shot.

## Also

- [inaricom.com](https://inaricom.com) — designed and built the company site.
