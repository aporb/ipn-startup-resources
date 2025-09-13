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
- [Developer Tools](#-developer-tools)
- [Educational Resources](#-educational-resources)
- [Who This Is For](#-who-this-is-for)
- [Quickstart](#-quickstart)
- [Usage Examples](#-usage-examples)
- [How to Use This](#-how-to-use-this)
- [Roadmap](#-roadmap)
- [Contributing](#-want-to-contribute)
- [Contributors](#-contributors)
- [Contact](#-contact)
- [Bigger Picture](#-bigger-picture)

---

## 🧰 What You'll Find Here

This repo is a growing collection of:

- Ready-to-run automations (like n8n workflows)
- Developer tools and extensions for AI coding platforms
- Agent prompt templates and decision frameworks
- Lightweight stack ideas for bootstrapping
- Curated open-source tools to help you move fast without burning capital

Featured resources include the **Executive Order Intelligence Agent** — a production-grade, end-to-end AI-powered pipeline built in n8n — and the **Claude Code Subagent Manager** — providing access to 126+ specialized AI subagents for developers.

Start with what clicks for you. No need to understand it all at once.

---

## 📁 Repository Structure

```
ipn-startup-resources/
├── workflows/                 # Ready-to-deploy automation workflows
│   ├── n8n-telegram-ai-agent/       # Telegram AI bot with LangChain
│   └── n8n-executive-order-agent/   # Government EO intelligence agent
├── prompts/                   # AI prompt templates and frameworks
│   └── meeting-transcript-analysis.md
├── automations/              # Standalone automation scripts (coming soon)  
├── frameworks/               # Reusable system architectures (coming soon)
├── docs/                     # Educational resources and reports
│   ├── claude-code-subagent-manager.md
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

## 🛠️ Developer Tools

### Claude Code Subagent Manager
*By [Akbar Aziz](https://github.com/akbaraziz) - Solutions Architect @ Palo Alto Networks*

Interactive installer for Claude Code subagents from the awesome-claude-code-subagents community repository. Access 126+ specialized AI subagents across 10 categories with both CLI and cross-platform GUI interfaces.

**Key Features:**
- **126+ Subagents** across Core Development, Language Specialists, Infrastructure, Quality & Security, Data & AI, and more
- **Cross-Platform GUI** for Windows, macOS, and Linux
- **Command-Line Interface** for automation and power users
- **GitHub Token Support** for enhanced API rate limits (5,000 vs 60 requests/hour)
- **Smart Installation** with conflict management and validation

**Quick Start:**
```bash
# Install globally
npm install -g claude-code-subagent-manager

# Interactive CLI installer
claude-subagents

# Launch GUI interface
claude-subagents --gui
```

📖 **Full Documentation:** [`docs/claude-code-subagent-manager.md`](./docs/claude-code-subagent-manager.md)  
📦 **NPM Package:** [claude-code-subagent-manager](https://www.npmjs.com/package/claude-code-subagent-manager)

---

## 📚 Educational Resources

### DoD SBIR/STTR 101 Webinar Report

Comprehensive analysis and insights from the Department of Defense Small Business Innovation Research / Small Business Technology Transfer program webinar. This report covers eligibility requirements, funding phases, proposal strategies, and practical guidance for small businesses looking to engage with DoD innovation programs.

Full report: [`docs/DoD-SBIR-STTR-101-Webinar-Report.md`](./docs/DoD-SBIR-STTR-101-Webinar-Report.md)

---

## 👥 Who This Is For

### 🎯 Primary Audience
- **IPN Network Members** - Ismaili professionals building businesses and careers
- **Startup Founders** - Early-stage entrepreneurs needing automation and AI tools
- **Solo Entrepreneurs** - Building lean, efficient operations from day one
- **Small Business Owners** - Looking to compete with larger players through smart automation

### 🏢 Secondary Audience  
- **GovCon Professionals** - Federal contractors needing intelligence and analysis tools
- **Consultants & Agencies** - White-labeling solutions for clients
- **Technical Leaders** - CIOs, CTOs seeking practical AI implementations
- **Students & Learners** - Understanding real-world AI/automation applications

### 💡 What You Get
- **Working Solutions** - Not just theory, but deployable tools
- **Learning by Example** - Study how problems are solved, then adapt
- **Community Support** - Connect with like-minded builders
- **Cost-Effective Growth** - Scale without burning capital on custom development

---

## 🚀 Quickstart

```bash
git clone https://github.com/aporb/ipn-startup-resources.git
cd ipn-startup-resources
```

### Choose Your Path:
1. **Start with Telegram AI Agent** → `cd workflows/n8n-telegram-ai-agent` → Follow the README
2. **Explore Government Intelligence** → `cd workflows/n8n-executive-order-agent` → Follow the README  
3. **Browse Educational Content** → `ls docs/` → Pick a topic that interests you

### Verify Your Setup:
```bash
# Check Node.js version
node --version

# Install n8n globally
npm install -g n8n

# Start n8n (opens http://localhost:5678)
n8n start
```

---

## 💡 Usage Examples

### Example 1: Personal AI Assistant
> *"I needed a Telegram bot to manage my daily tasks, send emails, and track weather for my commute. The Telegram AI Agent workflow gave me a production-ready solution in 30 minutes."*

**What you get:** A personal AI assistant accessible via Telegram that can integrate with Gmail, weather APIs, URL shorteners, and more.

### Example 2: Government Contract Intelligence  
> *"As a GovCon consultant, I needed to track Executive Orders that could impact my clients. The EO Intelligence Agent now sends me weekly briefings with policy analysis."*

**What you get:** Automated monitoring and analysis of government policy changes with executive-ready summaries.

### Example 3: Learning AI Implementation
> *"I'm a CTO evaluating AI tools for our company. These workflows showed me exactly how to architect production AI systems with real-world examples."*

**What you get:** Reference implementations for AI agents, data pipelines, and automated analysis systems.

---

## 🧠 How to Use This

* Don't copy everything — study how it solves a problem, then tailor it.
* Store your credentials securely using n8n's built-in tools.
* Run workflows locally first, then move to Docker or cloud deployment when ready.
* Want a demo? DM me in the IPN group or drop a question.

---

## 🗺️ Roadmap

### Coming Soon
- **Prompts Library** (`prompts/`) - Curated AI prompt templates for business use cases
  - Customer service prompts
  - Marketing copy generation
  - Technical documentation
  - Meeting summaries and action items

- **Automation Scripts** (`automations/`) - Standalone Python/Node.js scripts
  - Social media schedulers  
  - Data backup automations
  - Report generators
  - API integrations

- **System Frameworks** (`frameworks/`) - Complete architectural patterns
  - Multi-tenant SaaS boilerplate
  - Serverless API frameworks
  - Dashboard templates
  - Authentication systems

### Future Additions
- Video tutorials and walkthroughs
- Community showcase of adaptations
- Integration templates for popular SaaS tools
- Mobile app automation examples

---

## 📞 Contact

### Get Help & Connect
- **GitHub Issues** - For bugs, feature requests, or technical questions
- **LinkedIn** - Connect with [Amyn Porbanderwala](https://www.linkedin.com/in/amynporb) for collaboration
- **IPN Network** - Ask questions in the IPN Telegram group
- **Email** - For partnership inquiries: [contact info in profile]

### Want to Discuss?
- **Consulting** - Need help implementing these solutions? Let's talk.
- **Speaking** - Available for tech talks and workshops on AI automation
- **Partnerships** - Interested in building solutions together? Reach out.

---

## 🤝 Want to Contribute?

### Ways to Contribute
- **Share Your Adaptations** - Built something cool using these workflows? Let's showcase it!
- **Add New Resources** - Have automation scripts, prompts, or frameworks others could use?
- **Improve Documentation** - Found gaps or ways to make instructions clearer?
- **Report Issues** - Found bugs or have suggestions for improvements?

### How to Contribute
1. **Fork this repository** and create a feature branch
2. **Follow the folder structure** - place new content in the appropriate directory
3. **Include documentation** - READMEs, setup instructions, and usage examples
4. **Test your contributions** - ensure everything works as documented
5. **Submit a pull request** with a clear description

### Contribution Guidelines
- Keep it practical and deployable
- Include proper attribution and licensing
- No proprietary/closed-source dependencies
- Follow existing documentation patterns
- Test with real data when possible

**Too complex?** Just DM me and I'll help you add it in!

---

## 🤝 Contributors

### Community Contributors

#### Akbar Aziz ([@akbaraziz](https://github.com/akbaraziz))
**Solutions Architect @ Palo Alto Networks**

**Contribution:** [Claude Code Subagent Manager](./docs/claude-code-subagent-manager.md) - Interactive installer for 126+ Claude Code subagents. Published September 10, 2025.

**Connect:** [LinkedIn](https://www.linkedin.com/in/akbaraziz/) | [GitHub](https://github.com/akbaraziz) | [NPM](https://www.npmjs.com/~akbaraziz)

---

## 🌍 Bigger Picture

I built this for the people I wish I had on the journey.

### The Mission
Too many great ideas die not from lack of vision, but from lack of practical, working tools. This repository bridges that gap by providing real, deployable solutions you can adapt and scale.

### The Community
Whether you're part of the Ismaili Professional Network or any community looking to build meaningful solutions, this is for builders who believe that smart automation and AI can level the playing field.

### The Impact
Every workflow, prompt, and framework here has been battle-tested in real businesses. Take what works, adapt it to your context, and build something that matters.

---

## 🙏 Show Your Support

If this repository helps you build something meaningful:

* ⭐ **Star the repo** - helps others discover these resources
* 🔄 **Share it** - with someone in the IPN group or your network  
* 🛠️ **Remix it** - improve it, extend it, make it yours
* 💬 **Tell us** - what you built with it (we love success stories!)

---

**Let's raise the bar for what's possible — and who gets to build it.**

*Built with ❤️ for builders everywhere*
