# AI-Powered E-commerce Email Automation Agent

An end-to-end automated customer support agent built with **n8n**, **Groq AI**, and **Gmail API**. It monitors incoming e-commerce customer emails, classifies their intent, and automatically generates and sends context-aware responses in real time.

## Workflow Architecture

![n8n Workflow Architecture](./workflow.png)

## How It Works

1. **Email Trigger (Gmail):** Listens for incoming customer support emails in real time.
2. **Intent & Context Processing (Groq AI):** Analyzes the email content using low-latency LLM inference and structured prompt engineering to determine the inquiry type (e.g., order status, return policy, general FAQ).
3. **Conditional Routing:**
   - **Standard Inquiries:** Automatically drafts and sends a polite, brand-aligned reply within seconds.
   - **Complex / Urgent Issues:** Flags and escalates the email for human review to ensure accuracy.

## Sample Input & Output

**Incoming Customer Email:**
> *"Hi, I placed an order yesterday (Order #1042) and wanted to check when it will be shipped. Thanks!"*

**AI Generated Response (Sent in less than 10 seconds):**
> *"Hello! Thank you for reaching out. Your order (#1042) is currently being processed and will be shipped within 24 hours. You will receive a tracking link via email as soon as it dispatches. Let us know if you need any further assistance!"*

## Tech Stack
- **Automation Engine:** n8n (Cloud)
- **AI / LLM:** Groq AI
- **Integration:** Gmail API
- **Core Skill:** Prompt Engineering & Conditional Logic

## How to Use This Workflow
1. Download the `workflow.json` file from this repository.
2. Open your **n8n** workspace (Cloud or Self-Hosted) and create a new workflow.
3. Click the top-right menu (`...`) ➔ **Import from File** and select `workflow.json`.
4. Connect your own **Gmail** and **Groq API** credentials to activate.
