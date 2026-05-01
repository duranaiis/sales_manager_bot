# AI Sales Assistant — Telegram Bot

> Deployed in 3 weeks. Reduced manual support load for a sales team of 10+ managers.

An internal knowledge-base bot for sales managers, powered by RAG (Retrieval-Augmented Generation). 
Built and shipped end-to-end as part of the GulnurGV product ecosystem.

## My role
- Gathered requirements from the sales team through structured interviews
- Scoped the project and defined the knowledge base architecture
- Coordinated technical implementation and managed delivery timeline
- Validated bot responses against real sales scenarios before launch

## How it works

**`bot_config.json`** — Main Telegram bot workflow:
- Handles incoming messages from sales managers
- Retrieves answers from RAG knowledge base (Google Drive embeddings)
- Falls back to admin alert if the bot lacks information
- Logs all interactions to Supabase for quality review

**`google_drive_loader.json`** — Automated sync pipeline:
- Watches a Google Drive folder for new/updated documents
- Converts Docs, Sheets, Slides → chunks → embeddings
- Uploads to Supabase vector store automatically

## Tech stack
n8n · OpenAI GPT-4o · Supabase (PostgreSQL + Vector) · Telegram API · LangChain · Google Drive API

## Result
Deployed in 3 weeks from requirements gathering to production. 
Sales managers can now get instant answers from internal docs without waiting for a human response.

---
⚠️ All API keys and sensitive IDs are masked. Available for educational and research use (MIT).
