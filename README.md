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
| 4 | Decision Engine | 5 parallel Claude agents + synthesizer, Munger mental models, deal health verdict |
| 5 | Governance & Audit | DefenseClaw — prompt injection protection, rate limiting, Splunk audit trail |

---

## Demo Outputs

Static showcase outputs for three fictional companies:

- **Zantova Financial Group** — enterprise fintech, score 8/10 (Hot Lead)
- **Meridian Systems** — mid-market infrastructure, score 6/10 (Nurture)
- **Crestline Technologies** — growth-stage SaaS, score 7/10 (Hot Lead)

→ [View demo site](./demo/index.html)

---

## Tech Stack

- **Claude Sonnet** — research agents (Layers 1-4)
- **Claude Opus** — decision synthesis (Block 3)
- **n8n** — workflow orchestration
- **Cloudflare Workers** — Block 3 Decision Engine
- **Cloudflare Pages** — frontend
- **Flask / EC2** — API layer
- **Splunk** — governance and audit (DefenseClaw)
- **Tavily** — live web search
- **Redis** — rate limiting

---

## Repository Structure

```
mercury-intelligence/
├── demo/               # Static showcase site
├── n8n/                # Sanitised n8n workflow export
├── assets/             # Architecture diagrams, screenshots
└── README.md
```

---

Built by [Yeo Zhi Yong](https://www.linkedin.com/in/yeozhiyong)
