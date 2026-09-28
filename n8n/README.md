# Real Estate Growth — n8n Automation

This folder contains the automation blueprint for the app.

## Flow

Lead Capture Webhook → Validate/Normalize → Score Lead → Google Sheets/CRM → Follow-up Queue

## Required environment/credentials

- N8N webhook URL
- Google Sheets credential (optional)
- CRM destination (optional)

## Lead payload

{
  "name": "نام مشتری",
  "phone": "09...",
  "need": "خرید آپارتمان",
  "budget": "..."
}

## Scoring

- phone present: +30
- need present: +25
- budget present: +25
- name present: +20

80–100 = hot
50–79 = warm
0–49 = cold

Do not send unsolicited messages. The workflow is designed to process leads who submit their information or otherwise provide contact permission.
