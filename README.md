# IPN Startup Resources

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub last commit](https://img.shields.io/github/last-commit/aporb/ipn-startup-resources)](https://github.com/aporb/ipn-startup-resources/commits/main)
[![GitHub stars](https://img.shields.io/github/stars/aporb/ipn-startup-resources?style=social)](https://github.com/aporb/ipn-startup-resources/stargazers)

This repo is for anyone in the IPN network — and the global Ismaili community — trying to build something meaningful.

Whether you're just getting started or already deep in the game, our goal is simple: share knowledge and tools that help each other succeed. In the spirit of our 1,400-year tradition of seeking knowledge for the betterment of ourselves and our communities, we're building a collection of practical resources that anyone can use and improve upon.

We believe in pluralism — embracing different approaches while finding common ground. We believe in self-reliance through shared knowledge. Most importantly, we believe in lifting each other up.

## 📋 Table of Contents

- [What You'll Find Here](#-what-youll-find-here)
- [Featured Resource](#-featured-resource)
- [Educational Resources](#-educational-resources)
- [Getting Started](#-getting-started)
- [Who This Is For & Usage Examples](#-who-this-is-for--usage-examples)
- [Community & Contributing](#-community--contributing)
- [Our Mission](#-our-mission)

---

## 🧰 What You'll Find Here

This repo is a growing collection of tools and resources for the global Ismaili community:

- **Claude Code Subagent Manager** - Access 126+ specialized AI subagents for developers
- **Educational insights** - Real-world reports and analysis from community experiences
- **Automation workflows** - Practical n8n-based solutions you can deploy
- **Curated prompts** - Templates tested in real scenarios

Our featured resource is the **Claude Code Subagent Manager** by Akbar Aziz — providing instant access to specialized AI subagents across 10 categories for every aspect of development and business.

Start with what resonates with you. No need to understand it all at once.

---

## 🛠️ Featured Resource

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
 **NPM Package:** [claude-code-subagent-manager](https://www.npmjs.com/package/claude-code-subagent-manager)

---

## 📚 Educational Resources

### DoD SBIR/STTR 101 Webinar Report

Comprehensive analysis and insights from the Department of Defense Small Business Innovation Research / Small Business Technology Transfer program webinar. This report covers eligibility requirements, funding phases, proposal strategies, and practical guidance for small businesses looking to engage with DoD innovation programs.

Full report: [`docs/DoD-SBIR-STTR-101-Webinar-Report.md`](./docs/DoD-SBIR-STTR-101-Webinar-Report.md)

---

## 🚀 Getting Started

```bash
git clone https://github.com/aporb/ipn-startup-resources.git
cd ipn-startup-resources
```

### Your Next Steps:
1. **Try Claude Code Subagent Manager** → `npm install -g claude-code-subagent-manager` → Run `claude-subagents`
2. **Browse Educational Content** → Check out `docs/` for insights and reports
3. **Explore Other Resources** → Look through `workflows/` and `prompts/` for additional tools

### How to Approach This:
* Don't copy everything — study how it solves a problem, then tailor it to your needs
* Start with what interests you most, no need to understand it all at once
* Want a demo? Reach out in the IPN group or drop us a question

---

## 👥 Who This Is For & Usage Examples

This is for builders in the global Ismaili community and beyond who believe that knowledge should be shared, that we grow stronger together, and that technology can be a force for improving quality of life.

Whether you're an IPN member in Toronto, a startup founder in Karachi, a developer in London, or an entrepreneur in Nairobi — if you're trying to build something that matters, you'll find value here. We welcome everyone who shares our ethic of collaboration, pluralism, and mutual support.

### 💡 What You Get
- **Knowledge Sharing** - Learn from what others have built and tested
- **Community Support** - Connect with builders who want to help each other succeed  
- **Self-Reliance Tools** - Resources that help you become independent and capable
- **Meaningful Impact** - Solutions focused on improving quality of life, not just profit

### Usage Examples

### Example 1: Personal AI Assistant
> *"I needed a Telegram bot to manage my daily tasks, send emails, and track weather for my commute. The Telegram AI Agent workflow gave me a production-ready solution in 30 minutes."*

**What you get:** A personal AI assistant accessible via Telegram that can integrate with Gmail, weather APIs, URL shorteners, and more.

### Example 2: Government Contract Intelligence  
> *"As a GovCon consultant, I needed to track Executive Orders that could impact my clients. The EO Intelligence Agent now sends me weekly briefings with policy analysis."*

**What you get:** Automated monitoring and analysis of government policy changes with executive-ready summaries.

### Example 3: Learning AI Implementation
> *"I'm a CTO evaluating AI tools for our company. These workflows showed me exactly how to architect production AI systems with real-world examples."*

**What you get:** Reference implementations for AI agents, data pipelines, and automated analysis systems.

### Example 4: Specialized AI Coding Assistance
> *"As a startup founder, I needed different AI expertise across our entire tech stack - backend APIs, React frontend, DevOps deployment, security testing, and data analysis. The Claude Code Subagent Manager gave me instant access to specialized subagents for every aspect of our business without switching tools or losing context."*

**What you get:** Access to 126+ specialized AI subagents across 10 categories that cover every aspect of startup development - from core engineering and infrastructure to business analysis and product management - all integrated seamlessly into your Claude Code workflow.

---

## 🤝 Community & Contributing

### Our Contributors

#### Amyn Porbanderwala ([@aporb](https://github.com/aporb))
**Repository Creator & Maintainer**

**Contributions:** 
- [Telegram AI Agent](./workflows/n8n-telegram-ai-agent/README.md) - AI-powered Telegram bot with LangChain integration for personal productivity and automation
- [Executive Order Intelligence Agent](./workflows/n8n-executive-order-agent/README.md) - Automated policy analysis and newsletter generation pipeline for GovCon intelligence

**Connect:** [LinkedIn](https://linkedin.com/in/aporbanderwala) | [GitHub](https://github.com/aporb)

#### Akbar Aziz ([@akbaraziz](https://github.com/akbaraziz))
**Solutions Architect @ Palo Alto Networks**

**Contribution:** [Claude Code Subagent Manager](./docs/claude-code-subagent-manager.md) - Interactive installer for 126+ Claude Code subagents. Published September 10, 2025.

**Connect:** [LinkedIn](https://www.linkedin.com/in/akbaraziz/) | [GitHub](https://github.com/akbaraziz) | [NPM](https://www.npmjs.com/~akbaraziz)

### Join Our Community
- **Share Your Work** - Built something useful? We'd love to feature it!
- **Improve Documentation** - Found gaps or ways to make things clearer?
- **Report Issues** - Bugs or suggestions for improvements?

**How to Contribute:**
1. Fork this repository and create a feature branch
2. Follow our community values: keep it practical, include proper attribution
3. Test your contributions and submit a pull request

**Too complex?** Just reach out and we'll help you add it!

---

## 🌍 Our Mission

We built this for the global Ismaili community and all builders who share our values.

True to our tradition of pooling knowledge and resources, this repository grows through community contributions. In the spirit of our tradition of seeking knowledge for betterment, we're creating a space where practical tools and wisdom can be shared freely.

Whether you're part of the Ismaili Professional Network, the broader global Ismaili community, or any group committed to pluralism and mutual support — this is for builders who believe that sharing knowledge and lifting each other up creates opportunities for everyone.

Every tool and resource here reflects our commitment to improving quality of life through technology and collaboration. We take what works, share it openly, and help each other build something meaningful.

---

## 🙏 Show Your Support

If this repository helps you build something meaningful:

* ⭐ **Star the repo** - helps others discover these resources
* 🔄 **Share it** - with someone in the IPN group or your network  
* 🛠️ **Remix it** - improve it, extend it, make it yours
* 💬 **Tell us** - what you built with it (we love success stories!)

---

**Together, let's raise the bar for what's possible — and who gets to build it.**

*Built with ❤️ for the global Ismaili community and builders everywhere*

**Contact:** [GitHub Issues](https://github.com/aporb/ipn-startup-resources/issues) | [IPN LinkedIn Group](https://www.linkedin.com/groups/1218897/) | [IPN Startup WhatsApp Group](https://ipn.link/startups)
