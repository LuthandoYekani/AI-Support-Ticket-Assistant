# 🔧 Troubleshooting Guide

This guide covers common issues encountered when setting up or running the AI Support Ticket Assistant workflow.

---

# Google Gemini Authentication Error

## Symptoms

- Authentication failed
- Invalid API Key
- Permission denied

## Solution

1. Verify the API key in Google AI Studio.
2. Ensure the key has not been deleted.
3. Confirm the key is pasted correctly into the n8n credential.
4. Save the credential and re-run the workflow.

---

# No AI Response

## Symptoms

- Workflow executes successfully
- LLM node returns no output

## Solution

- Verify the Google Gemini Chat Model is connected to the Basic LLM Chain.
- Confirm the model is selected.
- Check internet connectivity.
- Re-execute the workflow.

---

# Prompt Variables Not Working

## Symptoms

Variables appear as:

```
{{$json.customerName}}
```

instead of actual values.

## Solution

- Ensure the field names in the Edit Fields node exactly match the variables in the prompt.
- Verify the workflow execution passes data into the Basic LLM Chain.

---

# n8n Workflow Stops

## Symptoms

Execution stops before reaching the AI node.

## Solution

- Execute each node individually.
- Inspect node outputs.
- Verify connections between nodes.
- Check execution logs.

---

# Poor AI Responses

## Possible Causes

- Prompt lacks detail.
- Customer information is incomplete.
- Issue description is too short.

## Recommended Fix

Provide:

- Customer name
- Subject
- Detailed issue description
- Relevant troubleshooting already performed

---

# API Rate Limits

Google Gemini may temporarily reject requests if API usage limits are exceeded.

### Solution

- Wait a few minutes.
- Retry the workflow.
- Monitor API usage in Google AI Studio.

---

# Future Integrations

When Gmail, Jira, ServiceNow, or Microsoft Teams integrations are added, additional troubleshooting documentation will be included in future releases.
