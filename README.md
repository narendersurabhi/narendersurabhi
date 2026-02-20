# Narender Rao Surabhi

**ML Engineer | AI Solutions Architect | GenAI (RAG + Agents) | MLOps Platform | AWS (SageMaker/Bedrock)**

I design and ship **production-grade ML and LLM systems** with a focus on:
- **Release governance** (evaluation gates, policy checks, controlled promotion)
- **Observability by default** (metrics, traces, structured logs)
- **Local-first workflows** that map cleanly to cloud/Kubernetes production patterns

> All public repositories use educational, synthetic, or non-sensitive data only.

## What I’m best aligned for
- Senior/Staff ML Platform Engineer
- AI Platform Engineer
- Applied AI Engineer (RAG + agentic systems)

## Featured repositories

### 1) Goal-Driven Agentic Workflow Engine (AWE)
A production-style multi-agent workflow platform with hierarchical **Planner → Worker → Critic/Policy** orchestration, typed DAG execution, MCP tool-calling, retry/DLQ recovery on Redis Streams, and schema-validated tool contracts.

**Highlights:**
- Kubernetes-ready scaling patterns (HPA/KEDA)
- Artifact/document handling with filesystem + optional S3 fallback
- Full observability via OpenTelemetry, Prometheus, Grafana, Loki, and Jaeger

Repo: <https://github.com/narendersurabhi/planner-executer-agentic-platform>

Quick start:
```bash
cp .env.example .env && make up
make test && make lint && make typecheck
```

### 2) MLOps Release Gate Agent
A Kubernetes-first release governance demo showing plan/execute workflows, policy gating, MLflow integration, and observability with Prometheus + OpenTelemetry + Jaeger.

Repo: <https://github.com/narendersurabhi/mlops-release-gate-agent>

Quick start:
```bash
make kind-up && make docker-build && make kind-load && make helm-install
make smoke
```

### 3) ML Platform Release Gates
Reference implementation for model governance and promotion:
**train/evaluate/promote → registry/artifact flow → FastAPI serving → Prometheus/Grafana**.

Repo: <https://github.com/narendersurabhi/ml-platform-release-gates>

Quick start:
```bash
make setup && make pipeline && make run
# or
cp .env.example .env && make compose-up
```

### 4) MCP Control Plane
Production-grade MCP server with stdio + HTTP transport, OpenTelemetry + Prometheus, and scope-based bearer auth policy controls.

Repo: <https://github.com/narendersurabhi/mcp-control-plane>

Quick start:
```bash
make install && make run-stdio
# HTTP mode
export MCP_MODE=http MCP_BEARER_TOKEN=devtoken
python -m mcp_cp.server
```

### 5) LangChain Production Starter
FastAPI + RAG + tool-using agent starter with testable chain patterns, FAISS retrieval, offline deterministic `LLM_PROVIDER=fake` mode, and `/metrics`/`/healthz`/`/readyz` endpoints.

Repo: <https://github.com/narendersurabhi/langchain-prod-starter>

Quick start:
```bash
cp .env.example .env && make setup && make run
```

### 6) LLM Customization Ops
End-to-end LLM customization repo covering LoRA/QLoRA SFT, DPO preference tuning, evaluation gates, and production API/observability patterns.

Repo: <https://github.com/narendersurabhi/llm-customization-ops>

Quick start:
```bash
make setup && make lint && make type && make test
make train-sft && make train-qlora && make train-dpo && make eval && make serve
```

### Bonus: AWS MLOps Starter
Template pipeline for train → test → containerize → FastAPI on Lambda container, with CI and basic drift checks.

Repo: <https://github.com/narendersurabhi/mlops-starter-aws>

## Engineering approach
- **Contracts-first design** for predictable component boundaries
- **Evidence-based promotion** using measurable release criteria
- **Operability as a requirement** (not an afterthought)
- **Reproducibility in CI** through fixtures and deterministic modes

## Core stack
- **Platform/API:** Python, FastAPI, Docker, Kubernetes (kind/Helm), MLflow
- **Observability:** OpenTelemetry, Prometheus, Grafana, Jaeger
- **LLM systems:** RAG patterns, tool-calling agents, FAISS-based retrieval
- **Data/ML:** PySpark, XGBoost, PyTorch, classic ML pipelines

## Connect
- LinkedIn: <https://www.linkedin.com/in/narendersurabhi>
- GitHub: <https://github.com/narendersurabhi>
- Location: Okemos, MI
