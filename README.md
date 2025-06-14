# IPN Startup Resources

This repo is for anyone in the IPN network — or beyond — trying to build something real.

Whether you're just getting started or already deep in the game, my goal with this is simple: give you working, remixable tools you can deploy today. *Automations. Prompts. Agents. Frameworks. Systems.* Things I wish I had when I started my journey.

I'm sharing what I use, what works, and how it all connects.

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

## ⚡ Featured Workflows
### Telegram AI Agent (Built in n8n + LangChain)

A fully operational Telegram bot that connects to an AI agent using LangChain. It routes tool calls (Gmail, Bitly, Weather, etc), enriches prompts, and logs chat memory to Postgres.

Setup instructions are in [`n8n-telegram-ai-agent-readme.md`](./n8n-telegram-ai-agent-readme.md)  
Workflow JSON here: [`n8n-telegram-ai-agent-example.json`](./n8n-telegram-ai-agent-example.json)

### Executive Order Intelligence Agent

An automated, AI-powered pipeline in n8n that:

- Scrapes, deduplicates, and enriches U.S. Executive Orders from the White House website
- Runs LLM-driven policy analysis with web search enrichment
- Generates executive-ready, mobile-friendly HTML newsletters for senior government and industry stakeholders
- Persists all data and metadata in Postgres

Setup and usage details are available in [`n8n-ExecutiveOrder-agent-readme.md`](./n8n-ExecutiveOrder-agent-readme.md)
Workflow JSON: `n8n-ExecutiveOrder-agent-example.json` (./n8n-ExecutiveOrder-agent-example.json)

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
