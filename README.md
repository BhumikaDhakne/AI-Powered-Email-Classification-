# 📂 Project Title: AI-Powered Email Classification & Spam Detection (Gmail + Make)

## 📌 Overview
I built this project to automatically classify emails in my Gmail using **AI** and **Make.com**. It’s designed to detect LinkedIn job emails, check if the job is relevant to my profile, and also filter out spam using an HTTP-based AI classifier.

---

## 🛠 Tech Stack I Used

- **Gmail (via Make)**
- **Make.com** – for building the full scenario with routers, filters, HTTP, and JSON parsers
- **Custom AI API** – to check for spam and job relevance
- **JSON Parsing**
- **Labeling & Filtering logic**
- **Mermaid** – to show a clean flowchart of the process

---

## 🧠 Real Use Case

> 🤔 “Why make this when Gmail already has a spam filter?”

Good question! But this goes a step further:
- Detects **LinkedIn job emails**
- Checks if the job **matches my skills** using AI
- Filters and labels emails more smartly than Gmail's basic spam logic

This project was my way of mixing productivity with AI automation for something I actually needed.

---

## 🔄 How the Flow Works

1. A new email arrives in Gmail (Make triggers the scenario).
2. First router checks if it’s a **LinkedIn** email.
3. If yes → another API call checks if the job **matches my profile**.
   - If yes → label it `Profile Matched`
   - If no → move it to spam
4. If it’s **not a LinkedIn email**, then:
   - Another API checks if it’s **spam**
   - If spam → move to spam
   - If not → label it `Spam Checked`

---

## 🧭 Flowchart (Simplified)

<details>
<summary>Click to Expand Mermaid Flowchart</summary>

flowchart TD
    A[Trigger: New Gmail Email] --> B{Router: LinkedIn Email?}
    B -- Yes --> C[HTTP API: LinkedIn Check]
    C --> D[JSON Parser: Is LinkedIn?]
    D -- Yes --> E{Router: Profile Match?}
    E -- Yes --> F[Label: Profile Matched]
    E -- No --> G[Move to Spam]
    D -- No --> H[HTTP API: Spam Check]
    H --> I[JSON Parser: Is Spam?]
    I -- Yes --> J[Move to Spam]
    I -- No --> K[Label: Spam Checked] 
</details>
---
##🧩 Screenshots from My Scenario

Here are the parts of my Make scenario that I’ll be adding screenshots for:

- Gmail trigger
- Router setup
- HTTP API and filters
- JSON parsing
- Gmail labeling module
---

## 📈 Future Improvements

- Replace mock API with **LLM model deployed via Replit / FastAPI**
- Log each classification to **Google Sheets or Notion**
- Add Telegram/Slack alert for profile-matched jobs
---
##📈 What I Plan to Improve

- Replace current AI API with something I host myself (maybe on Replit or FastAPI)  
- Log all results in Google Sheets or Notion for tracking  
- Add alerts on Telegram for matched job emails
---
##🎥 Optional Demo

I might add a Loom video or upload screenshots folder later for a quick walkthrough.
---
