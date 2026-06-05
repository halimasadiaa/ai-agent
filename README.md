# 🤖 AI Agent Workflow (n8n + RAG + Memory + Cache)

This project is an advanced **AI Support Agent system built in n8n**, designed for the TradingPapa platform. It combines **RAG (Retrieval-Augmented Generation)**, **chat memory, caching, and multi-model AI routing** to deliver fast, context-aware, and accurate responses.

---

## 🚀 Overview

The workflow acts as an intelligent support assistant that:

- Responds to user chat messages via webhook
- Checks cached responses (Redis) for speed
- Uses AI Agent (Gemini + OpenAI models)
- Retrieves knowledge from:
  - Pinecone RAG API
  - Google Docs Knowledge Base
  - Supabase (future expansion)
- Stores conversation memory in PostgreSQL
- Caches responses for 7 days (Redis)
- Returns final response via webhook

---

## 🧠 Core Features

### 1. Chat Trigger (Webhook)
- Receives user messages in real time
- Extracts `chatInput` and `sessionId`

---

### 2. Redis Cache Layer ⚡
- Checks if response already exists:
