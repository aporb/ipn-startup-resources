# Claude Code Subagent Manager – README

*Created by **Akbar Aziz** - Solutions Architect @ Palo Alto Networks*

Interactive installer for Claude Code subagents from the awesome-claude-code-subagents community repository. Published September 10, 2025, this tool provides access to 126+ specialized AI subagents across 10 categories with both CLI and cross-platform GUI interfaces.

## 1. Overview

**Tool Name:** Claude Code Subagent Manager  
**Core Technologies:** Node.js, Electron (GUI), GitHub API, Claude Code Integration  
**Author:** [Akbar Aziz](https://github.com/akbaraziz) - Solutions Architect @ Palo Alto Networks  
**Published:** September 10, 2025  
**NPM Package:** [claude-code-subagent-manager](https://www.npmjs.com/package/claude-code-subagent-manager)

### Purpose
- Browse and install 126+ specialized Claude Code subagents across 10 categories
- Provide both CLI and cross-platform GUI interfaces for easy management
- Enable enhanced GitHub API rate limits (5,000 vs 60 requests/hour)
- Smart conflict management and validation for subagent installations

## 2. Features

* **126+ Subagents:** Access to the entire community collection across 10 specialized categories
* **Cross-Platform GUI:** Electron-based interface for Windows, macOS, and Linux
* **Command-Line Interface:** Traditional CLI for power users and automation
* **GitHub Token Support:** Enhanced API rate limits (5,000 vs 60 requests/hour)
* **Interactive Selection:** Browse by category with checkbox-style selection
* **Smart Installation:** Handles conflicts, validates files, prompts for overwrites
* **Live Updates:** Fetches the latest subagents from the community repository

## 3. Installation & Setup

### Prerequisites
- Node.js 14.0.0 or higher
- Claude Code installed and configured

### Installation Options

```bash
# Install globally
npm install -g claude-code-subagent-manager

# Or use directly with npx
npx claude-code-subagent-manager
```

## 4. Usage

### Interactive CLI Installer
```bash
claude-subagents
```

### Launch GUI Interface
```bash
claude-subagents --gui
# or
claude-subagents -g
```

### Set GitHub Token (Recommended)
```bash
claude-subagents --token YOUR_GITHUB_TOKEN
```

### Browse Available Subagents
```bash
claude-subagents --demo
```

### Show Help
```bash
claude-subagents --help
```

## 5. Available Categories

| Category | Count | Description |
|----------|-------|-------------|
| Core Development | 12 | Backend, Frontend, Fullstack developers |
| Language Specialists | 24 | Python, JavaScript, TypeScript, etc. experts |
| Infrastructure | 13 | DevOps, Cloud, Containerization specialists |
| Quality & Security | 13 | Testing, Security, Code review experts |
| Data & AI | 13 | AI Engineers, Data Scientists, ML specialists |
| Developer Experience | 11 | Tooling and Productivity experts |
| Specialized Domains | 12 | Game Dev, Mobile, Embedded systems |
| Business & Product | 12 | Product Managers, Business analysts |
| Meta & Orchestration | 9 | Multi-agent coordination |
| Research & Analysis | 7 | Research and Analysis specialists |

## 6. GitHub Token Setup

For enhanced API rate limits (5,000 vs 60 requests/hour):

1. Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Give it a name like "Claude Subagent Manager"
4. Select "public_repo" scope (read access to public repositories)
5. Click "Generate token" and copy it
6. Use with: `claude-subagents --token YOUR_TOKEN`

## 7. How It Works

1. **Browse Available Subagents:** See all 126+ subagents organized by category
2. **Interactive Selection:** Choose individual agents or entire categories
3. **Automatic Installation:** Downloads and installs to your `.claude/agents/` directory
4. **Conflict Management:** Smart handling of existing agents with overwrite prompts

## 8. Author Attribution

**Akbar Aziz**
- **GitHub:** [@akbaraziz](https://github.com/akbaraziz)
- **LinkedIn:** [Akbar Aziz](https://www.linkedin.com/in/akbaraziz/)
- **NPM Profile:** [@akbaraziz](https://www.npmjs.com/~akbaraziz)
- **Professional Role:** Solutions Architect/Domain Consultant 2 @ Palo Alto Networks

## 9. Links

- **NPM Package:** [claude-code-subagent-manager](https://www.npmjs.com/package/claude-code-subagent-manager)
- **Claude Code:** [Official Documentation](https://claude.ai/code)
- **Awesome Claude Code Subagents:** [Community Repository](https://github.com/VoltAgent/awesome-claude-code-subagents)

## 10. License

MIT License
