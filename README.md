# Mercury Intelligence

> A production-deployed AI sales intelligence system — built to demonstrate what modern AI engineering looks like in practice.

## What It Does

Mercury Intelligence researches any company and produces a structured MEDDPICC sales brief, routes it by deal score, and generates a multi-framework strategic recommendation — all triggered by a Slack slash command.

**Live demo available on request.**

---

## System Architecture

Five integrated layers, all production-deployed:

| Layer | Component | Role |
|---|---|---|
| 1 | User Interface | Slack `/intel` + `/counsel` slash commands, web frontend |
| 2 | Workflow Orchestration | n8n 8-node pipeline, scoring gate, Slack routing |
| 3 | AI Research Engine | Multi-layer agent architecture — web search, agentic loop, BM25 RAG, MEDDPICC brief |
| 4 | Decision Engine | 5 parallel agents + synthesizer, Charlie Munger mental models, deal health verdict |
| 5 | AI Security | DefenseClaw — prompt injection protection, rate limiting, Splunk audit trail |

→ [Interactive architecture diagram](https://mercury-intelligence.pages.dev/assets/architecture-diagram.html)

---

## Demo Outputs

Static showcase outputs for two fictional companies:

- **Zantova Financial Group** — wealth management (Singapore), score 8/10 (Hot Lead)
- **Vantelo Logistics** — 3PL / freight forwarding (Singapore), score 6/10 (Nurture)

→ [View demo site](https://mercury-intelligence.pages.dev/demo/index.html)

---

## Tech Stack

- **Claude Sonnet** — research agents (multi-layer agentic architecture)
- **Claude Opus** — decision synthesis (Block 3 Decision Engine)
- **n8n** — workflow orchestration (8-node pipeline, scoring gate, Slack routing)
- **Cloudflare Workers** — Block 3 Decision Engine (stateless, edge-deployed)
- **Flask / EC2** — AI research API layer (Layers 1–4)
- **Splunk** — AI security and audit (DefenseClaw)
- **Tavily** — live web search
- **Redis** — rate limiting across all API workers

---

## Repository Structure

```
mercury-intelligence/
├── demo/
│   └── index.html                  # Static showcase — 2 fictional companies, MEDDPICC brief + Decision Engine outputs
├── assets/
│   └── architecture-diagram.html  # Interactive 5-layer system architecture diagram
└── README.md
```

---

Built by [Yeo Zhi Yong](https://www.linkedin.com/in/zhiyongyeo/)
