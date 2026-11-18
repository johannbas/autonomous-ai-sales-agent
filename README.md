# autonomous-ai-sales-agent
Autonomous AI Sales SDR workflow in n8n. Uses Gemini 2.5 Pro Live Search Grounding to research B2B leads and draft hyper-personalized cold emails in Gmail.

# 🤖 Autonomous AI Sales SDR (Lead Research & Outreach Pipeline)

[![n8n](https://img.shields.io/badge/n8n-Cloud-FF6C37?style=flat-square&logo=n8n)](https://n8n.io/)
[![Google Gemini](https://img.shields.io/badge/Gemini_2.5_Pro-Live_Search-4285F4?style=flat-square&logo=google)](https://ai.google.dev/)
[![Gmail API](https://img.shields.io/badge/Gmail-Drafting-EA4335?style=flat-square&logo=gmail)](https://developers.google.com/gmail/api)

A 100% cloud-native, autonomous Sales Development Representative (SDR) workflow. This pipeline autonomously researches B2B leads via live web search and drafts hyper-personalized outreach emails, turning cold outreach into warm, contextual conversations at scale.

## 🚀 The Business Problem It Solves
Generic B2B cold emails have a near-zero conversion rate. True personalization requires a human SDR to spend 15-20 minutes researching a prospect's recent company news, funding rounds, or product launches before writing a single email. 

This project automates that 20-minute research and writing process down to **3 seconds per lead**, operating 24/7 without fatigue.

## ⚙️ Architecture & Tech Stack
* **Orchestration:** n8n Cloud (Serverless, automated queue management, and crash recovery).
* **Live Research & Reasoning:** Google Gemini 2.5 Pro with **Google Search Grounding** enabled. The LLM actively browses the web for the prospect's company to find real-time, relevant hooks.
* **Database / CRM:** Google Sheets (acts as the lead queue and state tracker).
* **Delivery:** Gmail API (creates ready-to-send Drafts for human-in-the-loop review, or can be set to auto-send).

## 🧠 Workflow Logic
1. **Queue Ingestion:** The 15-minute watchdog reads a Google Sheet for new leads (Name, Company, Website).
2. **State Locking:** The row is locked (`IN_PROGRESS`) to prevent duplicate processing.
3. **Live AI Research:** Gemini is prompted to search the target company's recent news and extract a highly specific personalization hook.
4. **Copywriting:** Gemini synthesizes the research into a 4-sentence, high-converting cold email bridging the prospect's recent initiative with our automation services.
5. **Draft Creation:** The email is generated as a Draft in Gmail.
6. **Checkpointing:** The Google Sheet updates to `DRAFT_READY`, logging the timestamp.

## 🤝 Let's Collaborate
I engineer autonomous systems that eliminate manual bottlenecks and drive direct revenue. I am actively seeking collaborations with B2B tech companies, agencies, and founders looking to scale their outbound sales engines.

**Let’s connect!** Reach out to me directly via LinkedIn (link in GitHub bio) to discuss how we can implement AI agents into your sales pipeline.

---
**Tags & Keywords:** `n8n workflow` `AI SDR` `Sales Automation` `Gemini Search Grounding` `B2B Lead Generation` `Cold Email Automation` `Autonomous Agents` `Business Automation`

