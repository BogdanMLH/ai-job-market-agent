# 🤖 AI-Powered Job Market Intelligence Agent

![Project Status](https://img.shields.io/badge/Status-Active-success)
![n8n](https://img.shields.io/badge/Automation-n8n-ff6c37)
![Supabase](https://img.shields.io/badge/Database-Supabase-3ecf8e)
![OpenAI](https://img.shields.io/badge/AI-OpenAI_GPT--4-412991)

An autonomous agent designed to automate the job search and analysis process. The system leverages **n8n** for orchestration, **OpenAI (GPT-4)** for semantic analysis, and **Supabase** for data persistence. Accessed via a Telegram interface.

---

## 🚀 Key Features

* **🔍 Autonomous Research:** The bot can perform real-time web scraping to find relevant job listings or company data based on natural language requests.
* **🧠 AI Analysis:** Automatically parses unstructured job descriptions into structured data (Salary, Tech Stack, Requirements) using LLMs.
* **📂 Data Persistence:** Stores organized data directly into **Supabase** (PostgreSQL) and mirrors reports to **Google Sheets** for easy access.
* **💬 Natural Interface:** Fully interactive Telegram Bot interface capable of maintaining context (Memory).

## 🛠️ Architecture & Tech Stack

The project follows a modern **Event-Driven Architecture**:

1.  **Frontend:** Telegram Client (User Interface).
2.  **Orchestrator:** n8n (Self-hosted/Cloud) handles webhooks and logic flow.
3.  **Intelligence Layer:** OpenAI API for RAG (Retrieval-Augmented Generation) and data extraction.
4.  **Storage:** Supabase (PostgreSQL) for user auth and vacancy database.

### Workflow Visualization
> *[Вставь сюда скриншот своего самого красивого сценария из n8n. Это ДОКАЗАТЕЛЬСТВО твоей работы. Назови файл workflow-screenshot.png и положи в папку docs]*
> `![n8n Workflow Graph](./docs/workflow-screenshot.png)`

---

## ⚙️ How It Works (The Logic)

1.  **User Input:** User sends a voice or text message to the Telegram Bot (e.g., *"Find Junior Java jobs in Warsaw"*).
2.  **Intent Recognition:** n8n sends the prompt to OpenAI to classify the intent (Search / Analyze / Save).
3.  **Execution:**
    * If *Search*: Triggers a custom scraping script/API call.
    * If *Analyze*: Passes the text through a specific prompt to extract JSON data.
4.  **Response:** The agent formats the findings and sends a summary back to Telegram + saves rows to Google Sheets.

## 💻 Installation / Setup

To replicate this workflow:

1.  **Import Workflows:**
    * Download the JSON files from the `/workflows` folder.
    * Import them into your n8n instance.
2.  **Credentials:**
    * Set up credentials for: Telegram Bot API, OpenAI API, Supabase, Google Sheets.
3.  **Database:**
    * Use the SQL script provided in `/docs/schema.sql` to set up Supabase tables.

---

## 👨‍💻 Author

**Bogdan Malanchenko**
* **Role:** AI Automation Engineer & Backend Developer
* **Focus:** Bridging the gap between complex code and efficient No-Code solutions.
* [LinkedIn Profile](https://www.linkedin.com/in/bogdan-malanchenko)
