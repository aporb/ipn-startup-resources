# IPN Startup Resources

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub last commit](https://img.shields.io/github/last-commit/aporb/ipn-startup-resources)](https://github.com/aporb/ipn-startup-resources/commits/main)
[![GitHub stars](https://img.shields.io/github/stars/aporb/ipn-startup-resources?style=social)](https://github.com/aporb/ipn-startup-resources/stargazers)

This repo is for anyone in the IPN network — or beyond — trying to build something real.

Whether you're just getting started or already deep in the game, my goal with this is simple: give you working, remixable tools you can deploy today. *Automations. Prompts. Agents. Frameworks. Systems.* Things I wish I had when I started my journey.

I'm sharing what I use, what works, and how it all connects.

## 📋 Table of Contents

- [What You'll Find Here](#-what-youll-find-here)
- [Repository Structure](#-repository-structure)  
- [Prerequisites](#-prerequisites)
- [Featured Workflows](#-featured-workflows)
- [Educational Resources](#-educational-resources)
- [Who This Is For](#-who-this-is-for)
- [Quickstart](#-quickstart)
- [Usage Examples](#-usage-examples)
- [How to Use This](#-how-to-use-this)
- [Roadmap](#-roadmap)
- [Contributing](#-want-to-contribute)
- [Contact](#-contact)
- [Bigger Picture](#-bigger-picture)

---

## 🧰 What You'll Find Here

This repo is a growing collection of:

- Ready-to-run automations (like n8n workflows)
- Agent prompt templates and decision frameworks
- Lightweight stack ideas for bootstrapping
- Curated open-source tools to help you move fast without burning capital

Among the featured workflows is the **Executive Order Intelligence Agent** — a production-grade, end-to-end AI-powered pipeline built in n8n to scrape, analyze, and generate executive newsletters on U.S. Executive Orders, leveraging LangChain, Claude, OpenAI, Perplexity, and Postgres.

Start with what clicks for you. No need to understand it all at once.

---

## 📁 Repository Structure

```
ipn-startup-resources/
├── workflows/                 # Ready-to-deploy automation workflows
│   ├── n8n-telegram-ai-agent/       # Telegram AI bot with LangChain
│   └── n8n-executive-order-agent/   # Government EO intelligence agent
├── prompts/                   # AI prompt templates and frameworks (coming soon)
├── automations/              # Standalone automation scripts (coming soon)  
├── frameworks/               # Reusable system architectures (coming soon)
├── docs/                     # Educational resources and reports
│   └── DoD-SBIR-STTR-101-Webinar-Report.md
├── LICENSE
└── README.md
```

---

## 🔧 Prerequisites

Before diving in, make sure you have:

### Required
- **Node.js** (LTS version recommended) - for running n8n and workflows
- **Git** - for cloning and contributing to the repository

### Workflow-Specific Requirements
- **n8n** - workflow automation platform (`npm install -g n8n`)
- **PostgreSQL** - for workflows that require data persistence
- **API Keys** - for AI services (OpenAI, Anthropic, Perplexity) as needed per workflow

### Optional but Recommended
- **Docker** - for containerized deployments
- **Postman/Insomnia** - for testing webhook integrations
- Basic familiarity with **JSON** and **REST APIs**

---

## ⚡ Featured Workflows

### 🤖 Telegram AI Agent (Built in n8n + LangChain)

A fully operational Telegram bot that connects to an AI agent using LangChain. It routes tool calls (Gmail, Bitly, Weather, etc), enriches prompts, and logs chat memory to Postgres.

**Tech Stack:** n8n, LangChain, OpenAI/Anthropic, PostgreSQL, Telegram Bot API  
**Use Cases:** Personal productivity bots, client service assistants, lightweight co-founders  
**Complexity:** Intermediate (requires API keys and database setup)

📖 **Setup:** [`workflows/n8n-telegram-ai-agent/README.md`](./workflows/n8n-telegram-ai-agent/README.md)  
💾 **Workflow:** [`workflows/n8n-telegram-ai-agent/workflow.json`](./workflows/n8n-telegram-ai-agent/workflow.json)

### 🏛️ Executive Order Intelligence Agent

An automated, AI-powered pipeline in n8n that:

- Scrapes, deduplicates, and enriches U.S. Executive Orders from the White House website
- Runs LLM-driven policy analysis with web search enrichment
- Generates executive-ready, mobile-friendly HTML newsletters for senior government and industry stakeholders
- Persists all data and metadata in Postgres

**Tech Stack:** n8n, LangChain, Claude, OpenAI, Perplexity, PostgreSQL, Gmail API  
**Use Cases:** GovCon intelligence, policy analysis, executive briefings, competitive intelligence  
**Complexity:** Advanced (production-grade with multiple integrations)

📖 **Setup:** [`workflows/n8n-executive-order-agent/README.md`](./workflows/n8n-executive-order-agent/README.md)  
💾 **Workflow:** [`workflows/n8n-executive-order-agent/workflow.json`](./workflows/n8n-executive-order-agent/workflow.json)

---

## 📚 Educational Resources

### DoD SBIR/STTR 101 Webinar Report

Comprehensive analysis and insights from the Department of Defense Small Business Innovation Research / Small Business Technology Transfer program webinar. This report covers eligibility requirements, funding phases, proposal strategies, and practical guidance for small businesses looking to engage with DoD innovation programs.

Full report: [`docs/DoD-SBIR-STTR-101-Webinar-Report.md`](./docs/DoD-SBIR-STTR-101-Webinar-Report.md)

---

## 🚀 Quickstart

```bash
git clone https://github.com/aporb/ipn-startup-resources.git
cd ipn-startup-resources
```

Then open the README for whichever workflow you want to test. Most are self-contained and portable.

---

## 🧠 How to Use This

* Don't copy everything — study how it solves a problem, then tailor it.
* Store your credentials securely using n8n's built-in tools.
* Run workflows locally first, then move to Docker or cloud deployment when ready.
* Want a demo? DM me in the IPN group or drop a question.

---

## 🤝 Want to Contribute?

If you've built something cool or have useful tools for others:

* Fork this repo and submit a pull request
* Or just DM me and I'll help you add them in

---

## 🌍 Bigger Picture

I built this for the people I wish I had on the journey.

If you're part of the Ismaili community or anyone looking to build smart, this repo is for you.
If this helps you:
* ⭐ Star the repo
* 📩 Share it with someone in the IPN group
* 🛠️ Remix it, improve it, make it yours

Let's raise the bar for what's possible — and who gets to build it.
