# n8n Workflow Portfolio - Duru Victor Ikechukwu

A portfolio of n8n workflows showcasing my expertise in business automation, AI integration, and complex data orchestration.

---

## Overview

This repository contains five production-ready n8n workflows exported as JSON files, demonstrating my ability to design, implement, and maintain scalable automation solutions.

### Core Skills Demonstrated

* **Advanced Logic:** Error Handling, Looping, Conditional Branches (IF/Switch), and Data Transformation (Code/Function nodes).
* **AI/LLM Integration:** Utilizing the Gemini/LLM nodes for complex text analysis and content generation.
* **Data Management:** Integration with databases, CRMs, and APIs (e.g., Google Sheets, webhooks, Airtable).
* **Workflow Design:** Use of **Tags** and clear naming conventions for maintainability.

---

## Workflow Index

Below is a detailed breakdown of each workflow available in this repository.

### 1. AI-Powered Content Brainstormer (`ai-powered-content-brainstormer.json`)
* **Objective:** To automate the generation of content ideas based on a scheduled prompt, minimizing manual effort for content teams.
* **Process Summary:**
    1.  Uses a **Webhook** to recieve real time data from tally form.
    2.  Pulls a list of topics from a Google Sheet (or database).
    3.  Iterates through the topics, using the **AI/LLM node** to generate a unique short write up on the topic.
    4.  Stores the final structured output in a designated Google Sheet, categorized by topic.
* **Demonstrates:** Scheduled execution, Advanced LLM prompting, and Structured data output.

### 2. Intelligent Customer Feedback Loop (`intelligent-customer-feedback-routing.json`)
* **Objective:** Automatically analyze incoming customer feedback for sentiment and topic, then route it to the appropriate team for action.
* **Process Summary:**
    1.  Starts with a **Webhook Trigger** to receive feedback (from Tally form).
    2.  Uses an **IF Node** (which is used for condition logic) to filter the inquiry based on the subject of the complaint.
    3.  Uses a **Switch Node** to route negative sentiment/bug reports to Jira/Slack and positive feedback to a testimonial database.
* **Demonstrates:** Webhook handling, Multi-step AI analysis, and Complex conditional routing.

### 3. Automated Lead Capture and Notifications (`Automated-lead-capture-&-notification.json`)
* **Objective:** Instantly process, enrich, and notify stakeholders of high-priority leads from a website form.
* **Process Summary:**
    1.  Uses a **Webhook Trigger** to capture new form submissions.
    2.  Populates the new leads data on Airtable (which is a CRM software).
    3.  Send a message notification to the lead for him/her to know that the details has been successfully recieved.
    4.  Sends an immediate, customized **Slack/Email notification** only for "Hot" leads.
* **Demonstrates:** Real-time processing, Automating with CRM softwares and Targeted notifications.

### 4. Daily Sales Report Generator (`daily-sales-report.json`)
* **Objective:** Aggregate and format daily sales figures from a CRM, generating a summary email for management every morning.
* **Process Summary:**
    1.  Uses a **CRON Trigger** set for 10:00 PM daily.
    2.  Pulls all closed/won opportunities from the CRM for the current day via an **Google Sheet**.
    3.  Calculates totals and summarizes key metrics using a **Code Node**.
    4.  Sends a styled **HTML email** with the summary metrics to a management distribution list.
* **Demonstrates:** Time-based triggers, Data aggregation, Custom reporting logic, and Email content formatting.

### 5. Credit Report Pull and Risk Assessment (`credit report-pull-&-intital-risk-assessment.json`)
* **Objective:** To automate the multi-step process of integrating with a third-party financial service and applying a calculated risk rating.
* **Process Summary:**
    1.  Triggered by an internal system (via **Webhook**).
    2.  Uses an **HTTP Request Node** with custom headers/authentication to pull a credit report from an external API.
    3.  A **Code Node** processes the complex report JSON, extracting key data points (e.g., debt-to-income, score).
    4.  Applies a final risk score and updates an internal database record with the result.
* **Demonstrates:** Secure API authentication, Complex JSON parsing/manipulation, and Transactional automation.

---
*All files are exported n8n workflow JSON, ready for immediate import and testing.*
