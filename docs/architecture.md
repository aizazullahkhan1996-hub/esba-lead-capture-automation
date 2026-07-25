# ESBA Lead Capture Automation - Architecture

## Overview

This project automates the lead capture process for businesses using n8n. When a potential customer submits a form, the workflow automatically stores the information, creates or updates a CRM contact, and sends a confirmation email.

## Workflow

```
Website Contact Form
        │
        ▼
     Webhook
        │
        ▼
 Google Sheets
        │
        ▼
 HubSpot CRM
        │
        ▼
 Gmail
```

## Components

### 1. Webhook
- Receives lead data from the website form.
- Accepts JSON payloads via HTTP POST.

### 2. Google Sheets
- Stores every lead as a new record.
- Creates a simple lead database for reporting and backup.

### 3. HubSpot CRM
- Creates or updates a contact using the submitted email address.
- Prevents manual CRM entry.

### 4. Gmail
- Sends an automatic confirmation email to the lead.
- Improves customer communication and response time.

## Technologies Used

- n8n
- Webhooks
- Google Sheets API
- HubSpot CRM
- Gmail API

## Business Benefits

- Eliminates manual data entry.
- Centralizes lead management.
- Improves response time.
- Integrates CRM automatically.
- Creates a scalable workflow for SMEs.

## Future Enhancements

- AI lead qualification
- WhatsApp notifications
- Slack notifications
- Lead scoring
- Follow-up reminders
- Error handling and logging
