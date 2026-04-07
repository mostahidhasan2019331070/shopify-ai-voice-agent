

---

# 🗣️ Shopify AI Voice Agent (n8n + LLM)

An AI-powered **voice-enabled Shopify assistant** built using **n8n**, **LLMs**, and **Shopify APIs**.
This workflow allows an AI agent to fetch Shopify product data, generate friendly product descriptions, and respond via webhook for voice or conversational AI platforms (e.g., Vapi).

---

## 🚀 Features

* 🔗 **Webhook-based API endpoint** for voice or chat agents
* 🛍️ **Fetch all Shopify products** automatically
* 🤖 **AI-generated product descriptions**
* 🧠 **Conversation memory support**
* 🔁 **LLM-powered response generation**
* ⚡ **Real-time JSON response for tool calls**
* 🔊 Ready for **voice AI platforms** (Vapi, Voiceflow, custom agents)

---

## 🧱 Tech Stack

* **n8n** – Workflow orchestration
* **Shopify API** – Product data access
* **Google Gemini (PaLM)** – AI reasoning
* **OpenAI GPT-4.1 Mini** – Natural language generation
* **LangChain (n8n nodes)** – Agent, memory, tools
* **Webhook API** – External integration

---

## 🧩 Workflow Overview

### 1️⃣ Webhook Trigger

* Endpoint:

  ```
  POST /vapi-end-point
  ```
* Receives tool calls from voice or chat agents

---

### 2️⃣ Shopify – Get Products

* Fetches **all products** from the connected Shopify store
* Extracts:

  * Title
  * Variants
  * Price
  * Inventory
  * Tags
  * Product type
  * Description (HTML cleaned)

---

### 3️⃣ AI Agent (Product Understanding)

* Receives structured product data
* Generates:

  * Friendly
  * Detailed
  * Customer-ready descriptions
* Ensures:

  * No newlines
  * Clean JSON-safe output

---

### 4️⃣ LLM Models

* **Google Gemini** → reasoning & context
* **OpenAI GPT-4.1 Mini** → fluent, natural responses

---

### 5️⃣ Memory

* Session-based memory using:

  ```
  sessionKey: conversation
  ```
* Maintains context across interactions

---

### 6️⃣ Webhook Response

* Responds in **tool-call compatible JSON**
* Example response structure:

```json
{
  "results": [
    {
      "toolCallId": "tool_call_id_here",
      "result": "AI generated product details"
    }
  ]
}
```

---

## 🧪 Example Use Cases

* 📞 AI voice agent answering:

  * “Tell me about this product”
  * “What variants are available?”
  * “Is this item in stock?”
* 💬 AI chat assistant for Shopify stores
* 🛒 Automated product explanation bot
* 📊 Internal product knowledge agent

---

## 🔐 Requirements

* n8n (self-hosted or cloud)
* Shopify Admin Access Token
* OpenAI API key
* Google Gemini (PaLM) API key

---

## ⚙️ Setup Instructions

1. Import this workflow into **n8n**
2. Configure credentials:

   * Shopify Access Token
   * OpenAI API
   * Google Gemini API
3. Activate the workflow
4. Use the webhook URL in your voice/chat agent

---

## 🛠️ Customization Ideas

* Add **order tracking**
* Enable **product creation / updates**
* Connect **ElevenLabs / TTS**
* Add **RAG (vector search)** for large catalogs
* Multi-language support (EN / BN)

---



Just tell me 👍

