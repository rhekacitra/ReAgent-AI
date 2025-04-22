# CRM Email Automation with n8n

This workflow reads customer data from a CRM (Google Sheets), checks for valid emails, sends emails using Gmail, and updates the CRM with the status.

---

## Setup Instructions

1. Import `ReAgent_AI.json` into your n8n instance by clicking "Import from File".
2. Configure the following:
   - Google Sheets credentials (ensure correct spreadsheet ID and sheet name)
   - Gmail node for sending emails
3. Schedule the workflow or run manually via the editor.
4. Optional: Set up an error trigger workflow for global error handling.

---

## CRM Used

- **Google Sheets** — Used as the CRM backend to store contacts and track email status.
- 
A sample file is included: `Sample_CRM.xlsx`
Use this to create your own Google Sheet and connect it to your workflow.
It contains mock data for testing, including valid and invalid emails for error handling validation.
---

## Features & Assumptions

- Filters for pending emails only.
- Marks emails as `sent` or `error` in the Google Sheet.
- Error handling path updates rows with failure reasons.
- Assumes Gmail API is authorized.

