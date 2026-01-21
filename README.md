# Daily Job Scraper & Email Notifier Using n8n

## Overview
This **n8n workflow** automates the daily scraping of job postings from Google Jobs via **SerpAPI** and sends a curated list directly to your email. It is designed for **Data Scientists, AI professionals, and automation enthusiasts** looking for jobs in Pakistan, Remote, or Worldwide.  

The workflow ensures you never miss relevant job opportunities and delivers them in a clean, formatted email every day.  

---

## Features
- **Automated Schedule**: Runs daily at 9 PM to collect the latest job postings.  
- **Job Scraping**: Fetches job data from Google Jobs using SerpAPI.  
- **Categorization**: Jobs are automatically grouped into:
  - **Data Science** (Data Scientist / Data Analyst)
  - **AI & Machine Learning** (AI, GenAI, LLM, Machine Learning)
  - **n8n & Automation** (Workflow Automation / n8n)
- **Duplicate Prevention**: Removes duplicate job postings based on title and company.  
- **Email Notifications**: Sends a beautifully formatted HTML email with job details and "Apply Now" links.  
- **Supports Remote & Local Jobs**: Can filter by Pakistan, Remote, or Worldwide locations.  

---

## Workflow Steps

1. **Schedule Trigger**  
   - Workflow runs automatically at 9 PM every day.

2. **HTTP Request (SerpAPI)**  
   - Sends a query to SerpAPI to fetch job listings based on keywords like `Data Scientist`, `GenAI`, `n8n`, `Python Automation`, and `Machine Learning`.  

3. **Code Node (JavaScript)**  
   - Processes the fetched jobs:
     - Removes duplicates.
     - Categorizes jobs into **Data Science**, **AI**, and **n8n/Automation**.
     - Limits each category to the top 10 jobs.

4. **Send Email (Gmail Node)**  
   - Sends a formatted email to the recipient with all jobs categorized and clickable "Apply Now" links.  
   - Includes date and automation bot info for clarity.  

---

## Tech Stack

| Component          | Purpose                                             |
|------------------|-----------------------------------------------------|
| **n8n**           | Workflow automation platform                         |
| **SerpAPI**       | Fetches jobs from Google Jobs                        |
| **JavaScript**    | Data cleaning, duplicate removal, and categorization|
| **Gmail / SMTP**  | Sends daily job summary email                        |
| **HTML**          | Formatted email output with job cards               |

---

## Setup Instructions

1. **Install n8n**  
   Follow the [n8n installation guide](https://docs.n8n.io/getting-started/installation/).

2. **Import Workflow**  
   - Import the workflow JSON into n8n.

3. **Configure Credentials**  
   - **SerpAPI Key**: Replace with your personal SerpAPI key.  
   - **Gmail OAuth2**: Configure Gmail OAuth2 credentials to send emails.  

4. **Adjust Parameters**  
   - Modify keywords, job location, or recipient email as needed.  

5. **Activate Workflow**  
   - Turn on the workflow in n8n to start daily scraping and emailing.  

---

## Example Email Output
