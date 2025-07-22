## Expanded Boot‑Camp Delivery Plan

*Two‑week, 10‑day immersion that turns engineers into self‑sufficient LLM/RAG builders*

---

### 0️⃣  Pre‑Work (1–2 days, async)

| Task                                              | Purpose                                                | Resources                            |
| ------------------------------------------------- | ------------------------------------------------------ | ------------------------------------ |
| Install VS Code, Docker Desktop / Podman, Git CLI | Ensure every laptop can run containers & Python venvs. | Setup video (15 min), wiki checklist |
| Clone **`bootcamp‑starter`** repo                 | Pull down reproducible dev container & datasets.       | GitHub link + token                  |
| Watch “LLM Crash Intro” (45 min)                  | Baseline concepts: transformers, embeddings, RAG.      | Recorded webinar                     |
| **Skill self‑survey** (Google Form)               | Let instructors calibrate depth & pace.                | —                                    |

---

## Week 1 — Foundations & Plumbing

| Day                            | 09:00–10:30 *(Theory)*                       | 10:45–12:30 *(Hands‑On Lab)*                            | 13:30–15:00 *(Deep Dive)*                                   | 15:15–17:00 *(Lab / Q\&A)*                        |
| ------------------------------ | -------------------------------------------- | ------------------------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------- |
| **1 – Dev Env & Git**          | Bootcamp kickoff, goals, repo tour.          | ✓ VS Code dev‑container opens repo; run unit tests.     | GitFlow vs. trunk; PR etiquette; pre‑commit hooks.          | Automate lint + tests with GitHub Actions.        |
| **2 – Containers 101**         | Docker layers, image tags, Compose networks. | Build & run **`hello‑fastapi`**; hot‑reload demo.       | GPU passthrough, nvidia‑docker, BuildKit cache tricks.      | Compose stack: FastAPI + Qdrant + Jupyter.        |
| **3 – LLM Serving**            | Quantization, GGUF, llama.cpp vs. vLLM.      | Download Llama‑3 8B, quantize to 4‑bit, serve REST.     | Benchmarks, batch size tuning, tokenizer pitfalls.          | JMeter script measuring tokens/sec & latency.     |
| **4 – Embeddings & Vector DB** | Chunking strategies, metadata, hybrids.      | Embed sample PDFs with Instructor XL; load into Qdrant. | ANN algorithms (HNSW, IVF‑PQ).                              | Search queries; discuss precision/recall results. |
| **5 – Secure APIs & Auth**     | OAuth2 flows, JWT anatomy, RBAC patterns.    | Protect FastAPI endpoints with Auth0 dev tenant.        | Secrets management (doppler, Vault); rate‑limit middleware. | Pen‑test: attempt unauthorized query; fix.        |

> **Daily Rituals** – 08:45 stand‑up, 12:30 recap, 17:00 Slack parking‑lot cleanup.

---

## Week 2 — Conversation, UX, Ops & Capstone

| Day                              | 09:00–10:30                                                    | 10:45–12:30                                       | 13:30–15:00                                             | 15:15–17:00                                       |
| -------------------------------- | -------------------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------- |
| **6 – Prompt Engineering**       | Role design, few‑shot vs. system templates, Guardrails intro.  | Build prompt templates with variables & Jinja2.   | Automated evals with LangChain Bench.                   | A/B test two prompts on eval set; chart scores.   |
| **7 – Front‑End Streaming UX**   | React + Vite starter, WebSockets vs. SSE.                      | Scaffold chat widget; connect to FastAPI stream.  | Message diffing, typing indicators, citation pop‑overs. | Style with Tailwind; run Lighthouse audit.        |
| **8 – Tool‑Calling & Workflows** | OpenAI function‑calling, LangGraph routers.                    | Implement “resetPassword” & “createTicket” tools. | Multi‑step tasks with async queue, retry, idempotency.  | Demo end‑to‑end ticket creation via chat.         |
| **9 – Observability & Cost**     | Tracing (LangSmith), metrics (Prometheus), alerting (Grafana). | Instrument token & latency logging.               | Cost controls: max‑tokens, early‑exit, model tiering.   | Create dashboard; set alert for >2 s p95 latency. |
| **10 – Capstone Hack‑Day**       | Teams pick mini‑copilot idea; sprint planning.                 | Build for 3 hrs.                                  | Peer demos & feedback.                                  | Instructor code review, cert criteria check.      |

---

### Capstone Deliverable (Day 10)

**“Mini Copilot” Requirements**

1. Uses local Llama‑3 (or chosen alt) via RAG on supplied policy docs.
2. Secure FastAPI backend with Auth0.
3. React chat UI streaming responses & citing sources.
4. Prometheus + Grafana dashboard showing live metrics.
5. Deployed via `docker‑compose up` (& optional GH Action push).

Teams present a **5‑minute demo** + **2‑page README** showing setup, architecture diagram, and lessons learned.

---

## Assessment & Certification

| Component                                   | Weight |
| ------------------------------------------- | ------ |
| Daily Labs (auto‑graded via GitHub Actions) | 40 %   |
| Capstone Functionality & Code Quality       | 45 %   |
| Quiz (20 MCQ) on concepts                   | 15 %   |

Score ≥ 80 % → **“Conversational AI Builder – Level 1”** certificate.

---

## Post‑Boot‑Camp Support

* **Office Hours** – Twice weekly for 1 month; Slack channel monitored.
* **Template Upgrades** – Receive updated boilerplates for 6 months.
* **Fast‑Track Coaching** – Optional 4‑week embed of senior engineer to help ship first production bot.

---

### Logistics & Resources

* **Venue:** Company training room or virtual (Zoom + codespaces).
* **Class Size:** 10–15 engineers per cohort.
* **Instructors:** 1 lead + 1 TA (floats during labs).
* **Hardware:** At least one machine with RTX 4090 or better for GPU labs (remote SSH okay).
* **Materials:** Slide deck PDFs, lab instructions Markdown, solution branch per lab, cheat‑sheet cards, glossary poster.

The expanded plan equips your staff with the *practical muscle memory* to stand up, secure, and ship conversational AI systems—confidently moving from “zero” to “pilot‑ready” in just **10 action‑packed days**.
