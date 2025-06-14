# n8n Executive Order Agent – README

This repository contains a production-grade **n8n workflow** for automated, AI-powered analysis and newsletter generation of U.S. Executive Orders (EOs). It connects scraping, enrichment, LLM-driven policy analysis, and HTML email briefing into a single agentic pipeline—built for GovCon, federal strategy, and public-sector intelligence use cases.



## 1. Overview

**Workflow Name:** Executive Order Intelligence Agent  
**Core Technologies:** n8n, LangChain, Anthropic Claude, OpenAI, Perplexity, Postgres  
**Purpose:**

* Scrape, deduplicate, and enrich EO data from [whitehouse.gov](https://www.whitehouse.gov/presidential-actions/)
* Run policy-grade analysis with LLMs (including web search)
* Generate executive-ready newsletter briefings for senior government and industry stakeholders

### Why use this workflow?

- Automates tedious manual work by scraping and processing new Executive Orders continuously  
- Produces structured, actionable policy insights tailored for senior decision makers  
- Generates clean, mobile-friendly newsletter emails ready for distribution  
- Centralizes data and metadata for audit, reporting, and extended analytics  



## 2. Features

* **End-to-end EO pipeline:** From web scraping to analysis to publishing, fully automated  
* **LLM Policy Analysis:** Structured prompts deliver concise, actionable outputs for SES, Flag Officer, and C-level audiences  
* **Newsletter Generation:** Responsive, skimmable HTML briefs with mobile/dark mode support, formatted for Gmail/Outlook  
* **Deduplication & Update Logic:** Only processes and publishes new, high-impact EOs  
* **Database Integration:** All data, summaries, and metadata are persisted in Postgres for query, audit, and reporting  



## 3. Installation & Setup

### Prerequisites

- Node.js (latest LTS recommended)  
- n8n version tested: 1.97.1  
- Postgres database up and running  

### Steps

1. **Clone this repository and navigate to it:**

   ```bash
   git clone https://github.com/aporb/ipn-startup-resources.git
   cd ipn-startup-resources
   ```

2. **Install n8n (if not already):**

   ```bash
   npm install -g n8n
   ```

3. **Start n8n:**

   ```bash
   n8n start
   ```

4. **Import the workflow JSON (`n8n-ExecutiveOrder-agent-example.json`) via the n8n UI.**

5. **Configure all required credentials in n8n:**

   * Postgres database  
   * Anthropic (Claude), OpenAI, Perplexity API keys  
   * Gmail/OAuth2 (for newsletter delivery)  

> **Security:** Store all sensitive keys using n8n’s credential manager. Never commit or hard-code secrets in workflows.



## 4. Configuration

| Node / Section       | Configuration Required                                                                          |
| -------------------- | ----------------------------------------------------------------------------------------------- |
| **Scraper**          | Set base URL to `https://www.whitehouse.gov/presidential-actions/`.                             |
| **Postgres**         | Point to your target database and create the `executive_orders` table per included schema.      |
| **AI Agent**         | Update system prompts and model keys (Claude, OpenAI). Adjust temperature, maxTokens as needed. |
| **Perplexity**       | Insert Perplexity API credentials for real-time web search enrichment.                          |
| **Newsletter Email** | Set recipient, sender, and optional BCC addresses.                                              |
| **Triggers**         | Choose between manual, scheduled (cron), or external trigger for workflow execution.            |



## 5. Workflow Breakdown

| Node Name                             | Purpose                                                                                           |
| ------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Set Initial URL**                   | Initializes scraping from the official EO listing page.                                           |
| **Fetch EO Page/Extract Articles**    | Downloads and parses the list of EOs.                                                             |
| **Extract EO Links**                  | Pulls out titles, links, dates, tags for each EO found.                                           |
| **Check if Exists / If**              | Deduplication: checks if the EO is already present in Postgres.                                   |
| **Insert New Record**                 | Adds new EO metadata into Postgres with scrape timestamp.                                         |
| **Find Unprocessed**                  | Retrieves EOs lacking summary/content for enrichment.                                             |
| **Fetch EO HTML/Extract EO Content**  | Downloads full EO HTML, extracts and cleans content.                                              |
| **Clean Content**                     | Strips HTML, normalizes for LLM prompt.                                                           |
| **Create Prompt**                     | Builds a role-specific policy analysis prompt with full EO context.                               |
| **AI Agent (LangChain)**              | Calls LLM (Claude/OpenAI) for structured policy analysis (JSON output).                           |
| **Perplexity Search**                 | Optional web search to enrich analysis with real-world developments/context.                      |
| **Update Record**                     | Writes LLM outputs (summary, policy impact, keywords) into Postgres.                              |
| **Find Processed/Combine/Newsletter** | Pulls the top 3–5 most relevant EOs, batches for newsletter formatting.                           |
| **Build Newsletter**                  | Converts JSON batch into a responsive, inline-styled HTML newsletter per strict formatting rules. |
| **Gmail**                             | Sends out the EO Intelligence Brief to designated recipients.                                     |
| **Logging/Status**                    | Marks EOs as published in newsletter, avoids re-publishing.                                       |



## 6. Database Schema

Minimal required schema for `executive_orders`:

| Field                         | Type      | Description                          |
| ----------------------------- | --------- | ------------------------------------ |
| id                            | serial    | Primary key                          |
| title                         | text      | EO title                             |
| url                           | text      | EO URL                               |
| date_posted_et                | timestamp | Publication date (Eastern Time)      |
| tags                          | text[]    | EO tags                              |
| scraped_at                   | timestamp | Scrape timestamp                     |
| source                        | text      | Always "whitehouse.gov"              |
| summary                       | text      | Executive summary (AI generated)     |
| policy_intent                | text      | Policy intent (AI generated)         |
| agency_impact                | text      | Agency-level impact                  |
| contractor_implications      | text      | Implications for contractors/vendors |
| budgetary_signals            | text      | Budget/funding signals               |
| watchpoints                   | text[]    | Key risks/ambiguities                |
| notes                         | text[]    | Analyst notes                        |
| relevance_score              | integer   | 1–5, subjective impact               |
| strategic_keywords           | text[]    | Major themes/keywords                |
| is_vectorized                | boolean   | Reserved for future vectorization    |
| is_summarized                | boolean   | True when summary is available       |
| is_published                 | boolean   | True when included in a newsletter   |
| is_published_in_newsletter | boolean   | Newsletter tracking                  |
| published_in_newsletter_at | timestamp | Publish timestamp                    |
| content                       | text      | Cleaned EO content                   |



## 7. Usage

1. **Run the workflow manually, on schedule, or via an API trigger.**

2. The pipeline will:

   * Scrape and ingest new EOs  
   * Enrich and analyze unprocessed EOs with LLM and web context  
   * Write structured policy insights into Postgres  
   * Batch the top relevant EOs for briefing  
   * Send an HTML EO Intelligence Brief via Gmail  

3. **View results:**

   * All data is in your Postgres `executive_orders` table  
   * Email briefings are sent per configuration  
   * Extend or reuse workflow logic for Slack/Teams, web dashboards, or other channels as needed  



## 8. Customization & Extensibility

* **Modify prompts:** Tune policy focus, agency/sector priorities, or output format for your audience  
* **Switch models:** Plug in any LangChain-compatible LLM or web search API (Claude, Gemini, Llama, etc)  
* **Add integrations:** Push to Slack, Teams, or webhooks; trigger actions based on EO content or scores  
* **Expand analysis:** Layer on risk scoring, bill tracking, policy trend detection, or custom watchlists  



## 9. Troubleshooting & FAQ

If you encounter issues:

* Verify API credentials and limits (Anthropic, OpenAI, Perplexity)  
* Check Postgres connectivity and permissions  
* Monitor n8n logs for workflow errors  
* Make sure the scraper URL is up to date if scraping fails  
* Confirm Gmail/OAuth2 is correctly configured to send emails  

For help, open a GitHub issue or DM via LinkedIn.



## 10. Contributing

Open issues or pull requests for enhancements, integrations, or prompt improvements.  
This workflow is designed to serve as a foundation for advanced AI-powered GovCon and public-sector analytics.



## 11. Attribution

Built and maintained by [Amyn Porbanderwala](https://www.porbanderwala.com)  
AI-powered situational awareness for the GovCon and public-sector policy community.



## 12. License

Open-source, MIT or Apache 2.0 (confirm per repo standard).



**For questions or demo requests, DM via LinkedIn or open a GitHub issue.**

> *Let’s raise the bar for public-sector intelligence. Remix, extend, and deploy it for your mission.*
