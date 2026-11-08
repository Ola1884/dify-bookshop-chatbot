# Dify Bookshop Chatbot

An AI assistant for **Kawn Bookshop** (a fictional independent bookshop in Cairo), built using Dify. It uses a Knowledge Base (RAG) to answer customer questions accurately based on a custom FAQ document, without inventing information.

## 🚀 Live Dify App URL
**Link:** [https://udify.app/chat/wTih4KhI5n6w06PS]

## 🛠️ Tech Stack & Configuration
* **Platform:** Dify Cloud Sandbox (Free Tier)
* **App Type:** Chatbot
* **LLM Provider:** Groq API (model: gpt-oss-120b)
* **Knowledge Base:** Attached `faq.md` using Vector Search (High Quality indexing)

## 📁 Repository Contents
* `faq.md` — The FAQ document covering 8+ shop topics (hours, location, shipping, etc.).
* `system_prompt.md` — The exact system prompt used to define the bot's persona, scope, and fallback rules.
* `screenshots/` — Visual proof of the setup and the chatbot answering questions via the live public link.

## 🧠 How it works
1. **Persona & Scope:** The system prompt restricts the bot to only answer questions about the bookshop using the provided context. 
2. **Grounding:** If a user asks a question not covered in the `faq.md`, the bot politely declines and suggests contacting the shop directly, preventing hallucinations.
3. **Knowledge Retrieval:** Dify retrieves relevant chunks from `faq.md` to generate accurate, grounded answers.

## 🔄 How to recreate (15-minute setup)
1. Sign up for a free account at [cloud.dify.ai](https://cloud.dify.ai).
2. Connect a free LLM provider (e.g., Google Gemini, Groq, or Moonshot).
3. Create a new **Chatbot** app.
4. Copy the contents of `system_prompt.md` into the **Instructions** box.
5. Go to **Knowledge**, create a new knowledge base, and upload `faq.md`. Use High-Quality indexing.
6. Attach the knowledge base to the Chatbot under the **Knowledge** section.
7. Click **Publish** to generate a public web app link.

## 💰 Cost
Total spend: **$0.00**. Built entirely using free-tier LLM API keys and the Dify Cloud Sandbox.
