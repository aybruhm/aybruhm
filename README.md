<img width="1200" height="543" alt="(o_O)7" src="https://github.com/user-attachments/assets/b7c39009-756b-4ca8-afea-a9ffd57a7255" />

I build production AI systems, including retrieval, agents and evaluations, along with the backend and cloud infrastructure they run on. I came into AI engineering from backend and cloud work, and that background shapes how I build. In my view, an agent is not ready for production until it can recover from a crash, explain what it did, and be tested before it ships.

---

## Current Work

- Building retrieval and agent systems for production AI products
- Building Assay, a durable financial planning agent on LangGraph
- Open-source tooling for running AI agents safely in production

---

## Projects

- **dailies**: Agent that turns a written brief into a narrated video on serverless GPUs. A vision critic reviews every shot and regenerates the ones that fail, all inside a hard cost budget per job.
- **[assay](https://github.com/aybruhm/assay)**: Durable conversational financial planning agent built on LangGraph. The model never does the arithmetic: every figure comes from a deterministic calculator, and a validator checks each displayed number against a calculator result before the response goes out.
- **[waypoint](https://github.com/aybruhm/waypoint)**: Lightweight Python SDK for fault-tolerant LLM agent workflows. After a crash, it replays execution from checkpoints without re-running LLM calls or tool invocations that already completed.
- **[provenance](https://github.com/aybruhm/provenance)**: Compliance and governance middleware for autonomous agents. Agents act within policy-defined guardrails, risky actions wait for human approval, and every decision is recorded in a cryptographic audit trail.
- **[safe-agentic-payment-system](https://github.com/aybruhm/safe-agentic-payment-system)**: Agent that initiates payments on its own, within policy limits it cannot override.
- **[ai-video-generation-poc-with-temporal](https://github.com/aybruhm/ai-video-generation-poc-with-temporal)**: Video generation pipeline built with Temporal and FastAPI. Generation, S3 upload, token deduction and the database write each run as a step in a Temporal workflow.
- **[folio](https://github.com/aybruhm/folio)**: Self-hostable investment tracker for portfolio management, performance analysis, benchmarking and financial goal tracking.

---

## Technical Focus

### AI Engineering
- Agents and agentic workflows (LangGraph, LangChain, PydanticAI, smolagents)
- Retrieval-augmented generation (RAG)
- LLM evaluation: code-based evaluators and LLM-as-judge
- Vector and hybrid search (Qdrant, Elasticsearch)
- Durable execution and event sourcing (Temporal)
- Task queues and background processing (Celery)
- Guardrails, human-in-the-loop approval and audit logging
- Multi-provider model integration (12+ image, video, audio and text providers in production)

### Backend
- Languages: Python, TypeScript
- Frameworks: FastAPI, Django, Node.js
- Data: PostgreSQL, Redis, MongoDB
- Queues: Celery, RabbitMQ, Kafka, AWS SQS

### Infrastructure
- Cloud: AWS
- Tooling: Pulumi, Docker, NGINX, GitHub Actions

### Frontend
- React, Svelte
