# Applied AI & Agentic Systems Engineer

I design and build autonomous multi-agent systems that run real operations end to
end - commerce, sales, trading, and creative work - and that improve their own code
and capabilities over time. Mostly local models, orchestrated across a small fleet
of machines.

Fribourg, Switzerland.

## Talos - my agentic platform

A distributed "agentic operating system": around 55 agents and 85+ services across a
four-node fleet, a four-part memory, a real-time voice and chat assistant, and
self-improving audit / build / architect pipelines. Commerce, autonomous sales (with
self-hosted eIDAS-grade e-signature), trading research, content generation, and
app/site builders run with little to no human input.

→ [github.com/Musyg/talos](https://github.com/Musyg/talos)

## Open-source components

Extracted and generalized from Talos, released under MIT:

- [agent-resilience](https://github.com/Musyg/agent-resilience) - circuit breaker, Redis-backed DLQ, offline MQTT buffer.
- [async-api-client](https://github.com/Musyg/async-api-client) - resilient async REST client: rate limiting, retries, pagination.
- [multi-agent-orchestrator](https://github.com/Musyg/multi-agent-orchestrator) - capability-based task routing template.

## How I work

- Execution-verified generation (Best-of-N with compile and test oracles) over single-shot prompting.
- Constrained decoding for schema-valid model output; ensemble judges to kill false positives.
- Metrics-driven - every change is measured. One self-audit pipeline went from 218s to 75s per run (-65%) while eliminating a class of silent failures.
- Evidence over claims. If it isn't reproducible, it isn't done.

## Stack

Python (async-first) · local LLM ops (llama.cpp / GGUF, model routing, VRAM-aware
hot-swap) · multi-agent orchestration · graph-RAG memory · vector search · MQTT event
bus · real-time voice (streaming STT/TTS, speaker ID) · Prometheus / VictoriaMetrics
observability · systemd · CI with ruff, pytest, and pre-commit.

## Also

- [inaricom.com](https://inaricom.com) - designed and built the company site.
- Background in security and applied cryptography research.
