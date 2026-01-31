# 👋 Narender Rao Surabhi

**ML Engineer · AI Solutions Architect · GenAI (RAG/Agentic) · MLOps/Platform · AWS (SageMaker/Bedrock) · MLflow · PySpark**

I build **production-oriented ML + LLM systems** with a strong bias toward:
- **release governance** (evaluation gates, promotion workflows, policy-based decisions)
- **observability-by-default** (metrics + traces + structured logs)
- **local-first demos that map to production** (Docker/Compose, and Kubernetes patterns)

> Public repos are educational and use synthetic/non-sensitive data. No employer code, data, or confidential material.

---

## 🎯 Best-fit roles
**Senior/Staff ML Platform Engineer (MLOps + GenAI)** · **AI Platform Engineer** · **Applied AI Engineer (RAG/Agents)**

---

## Portfolio

**If you only click one:** **MLOps Release Gate Agent** - planner/executor + policy gating + MLflow + Prometheus + Jaeger, deployed “EKS-style” using kind + Helm.  
(Everything is runnable locally.)

### 1) MLOps Release Gate Agent (Kubernetes-first “release governance” demo)
Local release-gating agent that mirrors production-style deployment using **kind + Helm**, with **planning/execution**, **policy engine**, **MLflow integration**, and **Prometheus + OpenTelemetry → Jaeger**.  
Repo: https://github.com/narendersurabhi/mlops-release-gate-agent  
Quick run:
- `make kind-up && make docker-build && make kind-load && make helm-install`
- `make smoke`

### 2) ML Platform Release Gates (model governance reference system)
Reference system for **model governance & promotion**: train/eval/promote → artifact store/registry → FastAPI serving → Prometheus/Grafana. Includes explicit gate logic and promotion states.  
Repo: https://github.com/narendersurabhi/ml-platform-release-gates  
Quick run:
- `make setup && make pipeline && make run`  
  or `cp .env.example .env && make compose-up`

### 3) MCP Control Plane (secure tool access for agents)
Production-grade **MCP server** with **stdio + HTTP transport**, **OpenTelemetry + Prometheus**, and **bearer auth + scope-based policy** (e.g., `X-MCP-Scope`). Includes Docker/Compose and Helm assets.  
Repo: https://github.com/narendersurabhi/mcp-control-plane  
Quick run:
- `make install && make run-stdio`
- HTTP: `export MCP_MODE=http MCP_BEARER_TOKEN=devtoken && python -m mcp_cp.server`

### 4) LangChain Production Starter (FastAPI + RAG + agent demo)
Production-ready **LangChain + FastAPI** starter with **testable chains**, FAISS-backed **RAG**, and a **tool-using agent**. Supports an offline deterministic `LLM_PROVIDER=fake` mode and exposes `/metrics`, `/healthz`, `/readyz`.  
Repo: https://github.com/narendersurabhi/langchain-prod-starter  
Quick run:
- `cp .env.example .env && make setup && make run`

### 5) LLM Customization Ops (LoRA/QLoRA + DPO + eval gates)
End-to-end LLM customization repo demonstrating **LoRA/QLoRA fine-tuning**, **DPO preference tuning**, optional distillation, plus production features: **FastAPI**, **OpenTelemetry**, **Prometheus**, CI gates, and offline fixtures for repeatable runs.  
Repo: https://github.com/narendersurabhi/llm-customization-ops  
Quick run:
- `make setup && make lint && make type && make test`
- `make train-sft && make train-qlora && make train-dpo && make eval && make serve`

### + Bonus: AWS MLOps Starter
Production-lean template: **train → test → containerize → FastAPI on Lambda (container) → basic drift monitor**, with GitHub Actions.  
Repo: https://github.com/narendersurabhi/mlops-starter-aws

---

## 🧠 How I build
- **Contracts first:** predictable inputs/outputs, explicit interfaces
- **Evidence-driven releases:** gates make decisions from measured signals
- **Operable systems:** metrics/traces/logs are part of the design, not an afterthought
- **Reproducible demos:** offline fixtures + deterministic modes so CI stays reliable

---

## 🧰 Tech I use
Python · FastAPI · MLflow · Docker · Kubernetes (kind/Helm patterns) · OpenTelemetry · Prometheus/Grafana · Jaeger  
LLM/RAG: LangChain-style orchestration · FAISS · tool-using agents  
Data/ML: PySpark · XGBoost · PyTorch / classic ML pipelines

---

## 📫 Connect
```text
LinkedIn: https://www.linkedin.com/in/narendersurabhi
GitHub:   https://github.com/narendersurabhi
Location: Okemos, MI
```
