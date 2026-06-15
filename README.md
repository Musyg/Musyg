# Gilles — Applied AI & Agentic Systems Engineer

I build autonomous multi-agent systems that run real operations end to end: code that
audits and improves itself, e-commerce and marketing automation, autonomous sales agents,
and trading research — orchestrated across a small fleet of machines, mostly on local models.

Geneva, Switzerland.

## What I build

- **Self-improving dev pipelines** — agentic audit / build / architect loops that scan,
  generate, and refactor code and infrastructure, with execution verifiers, ensemble
  judges, and automatic rollback. Defense-in-depth, not a single prompt.
- **E-commerce & marketing automation** — async integrations (Shopify, WooCommerce,
  Stripe, Printful, dropshipping, TikTok Shop) plus ML engines for pricing, demand
  forecasting, recommendation, fraud detection, and content generation.
- **Autonomous sales agents** — prospection → qualification → negotiation → closing,
  with a deal ledger, a compliance guard, and self-hosted eIDAS-grade e-signature.
  Tested end to end.
- **Distributed agent infrastructure** — an MQTT event bus with circuit breakers and
  dead-letter queues, a service registry, centralized memory, health monitoring, and
  self-healing remediation.

## How it's built

Python (async-first) · local LLM ops (llama.cpp / GGUF, model routing, VRAM-aware
hot-swap) · multi-agent orchestration · Qdrant RAG · MQTT · Prometheus / VictoriaMetrics
observability · systemd · Tailscale · CI with ruff, pytest, and pre-commit.

## How I work

- Execution-verified generation (Best-of-N with compile and test oracles) over
  single-shot prompting.
- Constrained decoding for schema-valid model output; ensemble judges to kill
  false positives.
- Metrics-driven — every change is measured. One self-audit pipeline went from 218s to
  75s per run (-65%) while eliminating a class of silent failures.
- Evidence over claims. If it isn't reproducible, it isn't done.

## Selected work

- **inaricom.com** — designed and built the company site.

## Also

Background in security and applied cryptography research.

<!--
**Musyg/Musyg** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
