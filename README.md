# Security researcher · Developer · AI systems engineer

Based in Switzerland.
I work across security and software engineering.

Three distinct practices, each standing on its own below.

---

## 🔒 Security

**Security Researcher & Auditor**

I find and prove vulnerabilities in smart contracts.
Every finding ships with a reproducible proof of concept. If it isn't reproducible, it isn't a finding.

**Focus**
- Smart contracts: Solidity / Vyper, Foundry fork PoCs, formal verification
- ZK & applied cryptography: circuits, verifiers, proof systems

**Proof of work**
- [security-reviews](https://github.com/Musyg/security-reviews), a catalogue of reproducible reviews, one repo per vulnerability class. Each ships a vulnerable target, an exploit PoC, a remediated branch, and a report, all green under CI.
- [erc4626-inflation-audit](https://github.com/Musyg/erc4626-inflation-audit). ERC-4626 first-deposit share inflation.
- [eip712-signature-replay-audit](https://github.com/Musyg/eip712-signature-replay-audit). ECDSA signature malleability double-spend.
- [reward-accounting-drift-audit](https://github.com/Musyg/reward-accounting-drift-audit). MasterChef-style reward accounting drift.
- [stvault-audit](https://github.com/Musyg/stvault-audit). Lending vault: oracle staleness, cross-function reentrancy, fee rounding.
- [vyper-access-control-audit](https://github.com/Musyg/vyper-access-control-audit). Vyper vault: unguarded ownership transfer (access control).
- [circom-underconstrained-audit](https://github.com/Musyg/circom-underconstrained-audit). ZK: under-constrained Circom circuit, Groth16 soundness break.
- [formal-verification-overflow-audit](https://github.com/Musyg/formal-verification-overflow-audit). Formal verification: averaging overflow refuted then proved with Halmos.

**Competition profiles**
- Cantina: [@GilMu](https://cantina.xyz/u/GilMu)
- Code4rena: [@GiMu84](https://code4rena.com/@GiMu84)

---

## 💻 Development

**Backend & infrastructure engineer**

Resilient, async-first Python services and the infrastructure primitives that keep them up.

- [production-agent-template](https://github.com/Musyg/production-agent-template). Production FastAPI service template: lifespan, health, circuit breaker, self-healing, metrics, scaffolding.
- [agent-resilience](https://github.com/Musyg/agent-resilience). Circuit breaker, Redis-backed DLQ, offline MQTT buffer.
- [async-api-client](https://github.com/Musyg/async-api-client). Resilient async REST client: rate limiting, retries, pagination.
- [agent-self-healing](https://github.com/Musyg/agent-self-healing). Dependency health monitor with online/degraded/error states and auto-recovery.
- [agent-metrics](https://github.com/Musyg/agent-metrics). Dependency-free counters, gauges, histograms with Prometheus text exposition.
- [infra-reference](https://github.com/Musyg/infra-reference). Sanitised platform-engineering reference: multi-arch Ansible, hardened systemd, distroless builds, mesh and observability.

_Engagement: backend APIs, integrations, observability, CI._

---

## 🤖 AI & Agentic Systems

**Applied AI & Agentic Systems Engineer**

I design and build autonomous multi-agent systems with self-improving build and audit pipelines. Mostly local models, orchestrated across a small fleet of machines.

- [talos](https://github.com/Musyg/talos). Distributed agentic platform: ~55 agents and 85+ services across a four-node fleet, four-part memory, real-time voice and chat assistant, self-improving build pipelines.
- [multi-agent-orchestrator](https://github.com/Musyg/multi-agent-orchestrator). Capability-based task routing template.

**Stack**: Python (async-first) · local LLM ops (llama.cpp / GGUF, model routing, VRAM-aware hot-swap) · multi-agent orchestration · graph-RAG memory · vector search · MQTT event bus · real-time voice · Prometheus / VictoriaMetrics · systemd · CI (ruff, pytest, pre-commit).

---

## How I work

- Evidence over claims. If it isn't reproducible, it isn't done.
- Metrics-driven; every change is measured.
- Execution-verified over single-shot.

## Also

- [inaricom.com](https://inaricom.com): built the website and backend for them.
