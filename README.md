<img width="1200" height="543" alt="(o_O)7" src="https://github.com/user-attachments/assets/b7c39009-756b-4ca8-afea-a9ffd57a7255" />

I build AI systems for production, from the retrieval and agent layer to the queues, billing, storage and cloud infrastructure that keep them running. The model is only one part of the system, so I care about what happens when a provider fails or a worker restarts.

I came into AI engineering through backend and cloud work. I spent two years at Agenta, an open-source LLMOps platform, building the evaluation and model registry layer. After that I was the sole product and infrastructure engineer on an AI film production platform, where I took a single-user prototype to a multi-tenant product that serves thousands of enterprise customers, and built the orchestration layer across 12+ generative providers.

That background shapes how I build. I care about durable execution, retries that separate transient failures from permanent ones, evaluations that catch regressions, and guardrails that keep an agent inside its permissions. An agent is not ready for production until it can recover from a crash, explain what it did, and be tested before it ships.

## Current Work

- Building agents, retrieval and evaluations for an AI bid management platform.
- Building Dailies, an agent that turns a brief into a narrated video.
- Building Assay, a financial planner that shows its working.
- Building Waypoint and Provenance, open-source tools for crash recovery and guarded agent actions.

## Projects

- **dailies**: Turns a brief into a narrated video. It plans the shots, generates them on serverless GPUs, and adds narration. A vision model checks every shot and regenerates the ones that fail. The whole job runs inside a fixed cost budget.
- **[assay](https://github.com/aybruhm/assay)**: A financial planner that shows its working. It answers personal finance questions for the UK and Nigeria, and every figure comes from a tested calculator rather than the model. A validator checks each number before the answer is shown.
- **[waypoint](https://github.com/aybruhm/waypoint)**: Crash recovery for agent workflows. It saves the input and output of every step, so a workflow that dies can restart from the last good step instead of running everything again. Completed steps return their saved result, so you do not pay twice for the same LLM call.
- **[provenance](https://github.com/aybruhm/provenance)**: Guardrails and approvals for agent actions. Before an agent pays, sends a message or changes infrastructure, it asks Provenance. A policy for each customer decides whether the action is allowed, blocked or sent to a person, and every decision is written to a tamper-evident log.
- **[safe-agentic-payment-system](https://github.com/aybruhm/safe-agentic-payment-system)**: Payments within limits the agent cannot change. It makes payments on its own, but the limits are set in policy and it cannot raise them.
- **[ai-video-generation-poc-with-temporal](https://github.com/aybruhm/ai-video-generation-poc-with-temporal)**: A video generation pipeline built with Temporal and FastAPI. Generation, upload, token deduction and the database write each run as a separate step, so a failure can resume instead of starting over.
- **[folio](https://github.com/aybruhm/folio)**: An investment tracker you can host yourself. It follows your holdings, compares their performance against a benchmark, and keeps your financial goals in one place. It runs on your own hardware, so your data stays with you.

## Technical Focus

### AI Engineering
- Agents and agentic workflows (LangGraph, LangChain, PydanticAI, smolagents)
- Retrieval and search (RAG, Qdrant, Elasticsearch)
- Evaluation (code-based evaluators, LLM-as-judge, RAGAS)
- Durable execution and event sourcing (Temporal)
- Guardrails, human-in-the-loop approval and audit logging
- Multi-provider model integration (12+ image, video, audio and text providers in production)

### Backend
- Languages: Python, TypeScript
- Frameworks: FastAPI, Django, Node.js
- Data: PostgreSQL, Aurora, Redis, MongoDB, DocumentDB
- Queues: Celery, RabbitMQ, Kafka, AWS SQS

### Infrastructure
- Cloud: AWS (ECS, Fargate, Lambda, Aurora, S3, SQS, CloudFront)
- Observability: Prometheus, Grafana, CloudWatch, Sentry
- Tooling: Pulumi, Docker, NGINX, GitHub Actions

### Frontend
- React, Svelte
