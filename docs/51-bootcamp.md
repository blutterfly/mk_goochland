# Bootcamp

## Outcome

After the crash course attendees  will be able to:

1. Spin up a local or cloud LLM stack from template in < 30 min.
2. Index a new corpus into the RAG pipeline and validate search quality.
3. Extend the chat UI or add a new channel with minimal boilerplate.
4. Instrument, monitor, and troubleshoot latency, cost, and hallucination metrics.
5. Ship improvements via CI pipeline with policy‑as‑code checks.

That’s the skill foundation required to deliver a production‑grade conversational interface in **≤90 days**—and to iterate confidently afterwards.

## Minimum Skill Prerequisites for Attendees

| Area        | Baseline Skill                                    |
| ----------- | ------------------------------------------------- |
| Python      | Loops, functions, virtual env, `requests`         |
| Linux CLI   | SSH, `tmux`, package manager, basic networking    |
| Git         | Clone, branch, merge/pull‑request                 |
| HTML/CSS/JS | Enough to tweak React component props             |
| SQL basics  | `SELECT`, joins, indexes                          |
| Cloud login | Ability to navigate chosen cloud portal/dashboard |

*(Those missing prerequisites receive pre‑work videos and a “zero‑to‑Git” half‑day primer.)*

## Crash‑Course Competency Matrix

*Everything your delivery team needs to master—in one fire‑hose boot‑camp.*

| #      | Competency Cluster                       | Why It Matters                                                         | Core Know‑How & Hands‑On Labs                                                                                                                                                                                                                                                   |
| ------ | ---------------------------------------- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1**  | **Python Dev Workstation**               | All bot logic, data pipelines, and infra scripts will be Python‑first. | *Tools:* VS Code + Remote Containers, Pyenv/Conda, Poetry or pip‑tools, Git + GitHub Desktop/CLI. <br>*Lab:* Provision a laptop from bare metal → push “Hello LLM” repo with pre‑commit hooks and CI lint.                                                                      |
| **2**  | **Version Control & CI/CD**              | Repeatable builds; automate lint, test, Docker image, deploy.          | GitFlow vs. trunk‑based; GitHub Actions (or GitLab CI) secrets, caching, matrix builds. <br>*Lab:* Add unit tests + GitHub Action that publishes an image to GHCR on tag.                                                                                                       |
| **3**  | **Container & Data Runtime**             | Ensure dev = prod; isolate GPU drivers, libraries, and vector DBs.     | Docker / Podman basics, Docker Compose, Volume management, BuildKit, OCI image scanning. <br>*Lab:* Compose file that spins up FastAPI, Qdrant, and a Jupyter notebook in one command.                                                                                          |
| **4**  | **AI Workstation / GPU PoC**             | Local hosting & latency testing for on‑prem LLMs.                      | Hardware sizing (RTX 4090 vs. A100), NVIDIA drivers + CUDA, nvidia‑docker, llama‑cpp‑python, HF transformers. <br>*Lab:* Quantize Llama‑3 8B to 4‑bit GGUF and serve via llama.cpp; benchmark tokens/s.                                                                         |
| **5**  | **LLM Orchestration Frameworks**         | Glue between prompts, RAG, and tool‑calling.                           | LangChain, LlamaIndex, Guardrails‑AI; prompt templates, memory stores, function‑calling schemas. <br>*Lab:* Build a chain that answers from two docs + triggers a “create‑ticket” function.                                                                                     |
| **6**  | **Retrieval‑Augmented Generation (RAG)** | Ground answers in corporate manuals & SOPs.                            | Embedding models (instructor‑xl, text‑embedding‑3‑small), chunking strategies, metadata filtering, similarity vs. hybrid search, vector DBs (Qdrant, Pinecone, pgvector). <br>*Lab:* Index a 100‑page PDF; query with source‑citation and metadata filter (department = “Ops”). |
| **7**  | **Data Engineering & ETL**               | Keep knowledge fresh and trustworthy.                                  | Airflow/Dagster basics, incremental ingest, OCR/PDF parsing, schema evolution, checksum‑based change detection. <br>*Lab:* Nightly DAG that ingests Confluence export → vector DB delta update.                                                                                 |
| **8**  | **Security, Compliance & IAM**           | Bots must not leak PII or violate policy.                              | OAuth2/OIDC, SAML, SCIM provisioning, RBAC, PII redaction regex vs. ASR, audit logging, secrets rotation. <br>*Lab:* Protect FastAPI endpoint with Azure AD login; prove token propagation to LangChain.                                                                        |
| **9**  | **Front‑End & UX**                       | Users interact via browser, Slack, or Teams.                           | React / Next.js, WebSockets / SSE, Tailwind UI, conversation transcript components, accessibility ARIA roles. <br>*Lab:* Build a chat widget that streams tokens, supports slash‑commands, and shows citations inline.                                                          |
| **10** | **MLOps & Observability**                | Monitor cost, quality, drift, and user feedback.                       | Prometheus + Grafana dashboards, LangSmith traces, Evidently & DeepChecks for hallucination metrics, MLflow for model registry. <br>*Lab:* Capture thumbs‑up/down; pipe events into Evidently dashboard with hourly refresh.                                                    |
| **11** | **Prompt Engineering & Evaluation**      | Reduce hallucination, improve tone and accuracy.                       | System vs. user vs. context roles, chain‑of‑thought vs. succinct mode; synthetic eval sets, tolerance tests. <br>*Lab:* A/B test three prompt templates; measure answer‑quality via rubric scoring script.                                                                      |
| **12** | **Project Boilerplates**                 | Start fast, stay organized.                                            | Cookiecutter templates: `fastapi-rag-stack`, `react-chat-widget`, Terra‑ form IaC skeleton. <br>*Lab:* Generate repo from template, push to org, run “make deploy‑local”.                                                                                                       |
| **13** | **Cloud & Edge Deployment**              | Choose right home for each workload.                                   | Azure OpenAI provisioning, AWS Bedrock endpoints, GCP TPU shots; edge K8s with K3s; auto‑scaling & cost guards. <br>*Lab:* Blue/green deploy of GPT‑4o proxy; switch traffic with <2 s downtime.                                                                                |
| **14** | **Domain & Knowledge SME Pairing**       | Technical staff must map jargon to model.                              | Embedding taxonomy workshops, glossary curation, doc hygiene. <br>*Exercise:* Engineers shadow Ops SME; extract 50 real FAQs to seed evaluation set.                                                                                                                            |

---

#### Boot‑Camp Delivery Plan (2 Weeks, 60% Hands‑On)

| Day | Morning (Theory)         | Afternoon (Lab)                        |
| --- | ------------------------ | -------------------------------------- |
| 1   | Python env, Git, CI      | Set up dev laptop, push sample repo    |
| 2   | Containers 101           | Compose full RAG stack                 |
| 3   | LLM basics & quant       | Serve Llama‑cpp; load test             |
| 4   | Vector DB & embeddings   | Ingest sample manuals                  |
| 5   | Secure APIs & Auth       | Lock down endpoints                    |
| 6   | Prompt design patterns   | Template A/B evaluation                |
| 7   | Front‑end streaming UX   | Build chat widget                      |
| 8   | Tool‑calling & workflows | Integrate “reset password” function    |
| 9   | Observability & cost     | Dashboards + alert rules               |
| 10  | Capstone hack‑day        | Build mini copilot; demo & peer review |

---


---

