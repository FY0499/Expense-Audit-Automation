# Expense Audit Automation

I built this n8n workflow to review submitted expenses, detect possible duplicate or unusual amounts, and use AI to check the expense category and prepare a short audit note.

<img width="792" height="213" alt="image" src="https://github.com/user-attachments/assets/f3fc479d-1c8c-4c2d-9c0e-666ce43c5404" />

## How it works

1. An employee submits a new expense through a form, including the store or supplier, amount, category, and date.
2. The workflow retrieves previous expense records from Google Sheets.
3. JavaScript checks whether the same store, amount, and date already exist, calculates the average historical expense, and flags amounts that are more than three times the average.
4. Google Gemini reviews the expense category and returns an audit note with a suggested category when needed.
5. The result is saved to Google Sheets, and suspicious expenses trigger a Telegram notification.

## Main features

- Expense submission form.
- Duplicate expense detection.
- Unusual amount detection based on historical average.
- AI-assisted category review.
- Audit notes and Telegram alerts.
- Google Sheets expense tracking.

## Technologies

n8n, Google Sheets, Google Gemini, JavaScript, AI Agent, Telegram, and n8n Forms.

## Setup

Import [workflow.json](./workflow.json) into n8n, configure your Google Sheets, Gemini, and Telegram credentials, then connect your expense history sheet and test the workflow with sample expenses.
