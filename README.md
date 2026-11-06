
# Workflow Automation

A hands-on project focused on workflow automation using **n8n, Zapier, FastAPI, and LLM APIs**.

This repository contains the implementation and documentation of a CV Screening Automation Pipeline, a Smart Extractor integration, and a comparison of n8n and Zapier.

## 🚀 Projects Overview

### 1. CV Screening Automation Pipeline

An automated workflow that receives CVs from Google Drive and Gmail, extracts candidate information, evaluates candidates using an LLM, validates the results, and stores the screening outcomes in Google Sheets.

**Workflow:**

1. Receive CVs through Google Drive or Gmail.
2. Extract text from PDF files.
3. Send extracted text to an LLM using OpenRouter.
4. Generate structured candidate information in JSON format.
5. Validate the extracted information.
6. Check for duplicate candidates using Source ID.
7. Evaluate candidates based on their screening score.
8. Store shortlisted candidates in Google Sheets.
9. Send email notifications for shortlisted candidates.
10. Route invalid or low-quality results to Manual Review.
11. Handle workflow errors through a separate Error Handler workflow.

### 2. Smart Extractor – FastAPI Integration

Integrated an existing FastAPI-based Smart Extractor with n8n using Webhooks and HTTP Requests.

**Workflow:**

1. Receive text through an n8n Webhook.
2. Forward the text to the FastAPI `/extract` endpoint.
3. Process the text using the LLM-powered extraction service.
4. Return structured JSON containing:
   - Title
   - Summary
   - Keywords
   - Category

### 3. Zapier Automation

Created a mini automation using Google Sheets and Gmail.

- Trigger: New Spreadsheet Row in Google Sheets.
- Action: Automatically send an email through Gmail.
- Tested successfully with sample candidate data.

## 🛠️ Technologies Used

- **n8n** – Workflow automation
- **Zapier** – No-code automation
- **Python** – Backend development
- **FastAPI** – API integration
- **OpenRouter API** – LLM integration
- **GPT-4o-mini** – CV screening and information extraction
- **Google Drive** – CV file input
- **Gmail** – Email input and notifications
- **Google Sheets** – Candidate data storage
- **Docker Desktop** – Local n8n environment
- **Webhooks & HTTP Requests** – Communication between services
- **JavaScript** – Data validation and transformation

## 📂 Repository Structure

```text
Workflow-Automation/
│
├── Automation Workflow ScreenShots.docx
├── CV Screening.json
├── CV Screening Error Handler.json
├── Smart Extractor - FastAPI Integration.json
├── CV Screening Pipeline - Prompt Documentation.docx
├── CV Screening Pipeline -Workflow diagram.png
├── n8n vs Zapier - Recommendation Memo.docx
└── README.md
```

## ⚙️ Running the Workflows

### Requirements

- Docker Desktop
- n8n
- Python 3.11+
- FastAPI Smart Extractor project
- OpenRouter API key
- Google Drive, Gmail, and Google Sheets credentials

### Setup

1. Start Docker Desktop.
2. Run your local n8n instance.
3. Open `http://localhost:5678`.
4. Import the required workflow JSON files.
5. Configure your Google Drive, Gmail, Google Sheets, and OpenRouter credentials.
6. Start the FastAPI application on port `8000`.
7. Configure the required webhook and API endpoints.
8. Test the workflows using sample CVs.

**Note:** Credentials and API keys must be configured separately. Never upload API keys, passwords, access tokens, or `.env` files to GitHub.

## 📚 Documentation

This repository also includes:

- Workflow screenshots and implementation details.
- CV Screening Pipeline architecture diagram.
- LLM prompt documentation.
- n8n vs Zapier comparison and recommendation memo.
- Exported n8n workflow JSON files.

## 🎯 Learning Outcomes

Through this project, I gained practical experience with:

- Building end-to-end automation workflows.
- Working with triggers, nodes, and conditional logic.
- Integrating REST APIs using HTTP Requests.
- Connecting FastAPI with n8n through Webhooks.
- Integrating LLM APIs into automation workflows.
- Extracting and validating structured JSON data.
- Implementing error handling and retry mechanisms.
- Preventing duplicate processing.
- Automating email notifications.
- Working with Docker-based local environments.
- Comparing n8n and Zapier for workflow automation.

---

**Author:** Shoaib Asghar

**GitHub:** https://github.com/shoaib980-make
