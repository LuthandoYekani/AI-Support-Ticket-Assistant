# System Architecture

## Overview

The AI Support Ticket Assistant is an intelligent workflow built using n8n and Google Gemini.

It automates the first stage of technical support by analysing incoming customer support requests and generating a structured technical assessment.

---

## Architecture

```mermaid
flowchart LR

A[Manual Trigger] --> B[Edit Fields]

B --> C[Google Gemini LLM]

C --> D[Technical Analysis]

D --> E[Issue Summary]

D --> F[Priority]

D --> G[Troubleshooting]

D --> H[Customer Response]

H -. Future .-> I[Gmail]

H -. Future .-> J[Jira]

H -. Future .-> K[ServiceNow]

H -. Future .-> L[Microsoft Teams]
```
---

## Technologies

- n8n
- Google Gemini
- JSON
- REST APIs
- AI Prompt Engineering

---

## Future Enhancements

- Automatic Gmail monitoring
- Jira ticket creation
- ServiceNow incident creation
- Microsoft Teams notifications
- Knowledge Base integration
- Customer sentiment analysis
