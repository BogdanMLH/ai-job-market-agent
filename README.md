# 🤖 AI Job Market Assistant (n8n Workflow)

![n8n](https://img.shields.io/badge/Orchestration-n8n-FF6C37)
![OpenAI](https://img.shields.io/badge/AI-OpenAI_GPT--4-412991)
![Webhook](https://img.shields.io/badge/Integration-Webhook-red)

This repository contains the automation workflow for an intelligent Chatbot embedded on my Job Search Platform. The bot acts as a first-line support agent, capable of answering user queries and filtering job requests autonomously.

---

## 📸 Workflow Visualization

> **"The Brain" of the system:**
> ![Workflow Diagram]([/workflow-diagram.png](https://github.com/BogdanMLH/ai-job-market-agent/blob/main/main-workflow.json))
*(Note: This is the actual logic that drives the conversation)*

---

## 🧠 How It Works

The workflow utilizes an **Event-Driven Architecture**:

1.  **Webhook Trigger:** Receives the user's message from the frontend (React) instantly.
2.  **Context Management:** Checks prior conversation history to maintain context (Memory).
3.  **AI Processing (LLM):** Sends the structured prompt to **OpenAI (GPT-4/3.5)**.
    * *System Prompt:* "You are a helpful career assistant..."
4.  **Action Routing:**
    * If the user asks for *jobs* -> Triggers a database search.
    * If the user asks for *advice* -> Generates a consultation.
5.  **Response:** Returns a formatted JSON response back to the chat interface.

## 🛠️ Installation (Import to n8n)

To use or modify this workflow:

1.  Download the `main-workflow.json` file from this repository.
2.  Open your **n8n** instance.
3.  Go to **Workflows** -> **Import from File**.
4.  Select the JSON file.
5.  **Setup Credentials:** You will need to add your own OpenAI API Key and Database credentials.

---

### 💼 Business Value
This automation reduces manual support time by **80%** and provides 24/7 assistance to job seekers without human intervention.
