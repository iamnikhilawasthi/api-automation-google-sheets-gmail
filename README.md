# api-automation-google-sheets-gmail
Automated API testing workflow built using n8n. Integrates Google Sheets for test logging and Gmail for real-time pass/fail email alerts. Validates API responses with conditional logic, enabling efficient QA automation with minimal coding. Ideal for developers/testing teams seeking scalable, no-code API validation and alerting.

Automated API Testing & Alerts with n8n
Overview
This project demonstrates a real-world QA automation workflow using n8n.
It performs API testing, logs results in Google Sheets, and sends real-time email notifications for test pass/fail events.

Features
API testing via HTTP Request node (sample: GitHub User API)

Response validation with IF node (login/data match check)

Result logging in Google Sheets for audit trail and reporting

Automated email notification to stakeholders using dynamic message fields

Branching for success/failure including error/failure details

Tech Stack
n8n (No Code Workflow Automation)

Google Sheets (QA results log)

Gmail (notification)

REST API (sample: GitHub)

Usage Instructions
Export/Import Workflow:

Export the provided JSON workflow from n8n editor

Import it into your n8n instance

Setup Credentials:

Configure Google Sheets and Gmail integrations in n8n

Configure API Endpoint & IF Condition:

Update HTTP Request node (endpoint/sample payload if needed)

Set expected value (e.g., login == octocat) in IF node

Run the Workflow:

Click Execute — verify logs in Google Sheets, receive mail on pass/fail

Timestamp         |  API_URL                               |  Username  |  TestResult  |  Details/Error         
------------------+----------------------------------------+------------+--------------+------------------------
2025-10-18 14:30  |  https://api.github.com/users/octocat  |  octocat   |  Pass        |                        
2025-10-18 14:32  |  https://api.github.com/users/octocat  |  abc       |  Fail        |  User validation failed


Email Alert Example:

Subject: API Test Alert - Pass/Fail

API Test Alert!

Timestamp: 2025-10-18T14:32:00Z
Username: octocat
Test Result: Pass/Fail
API: https://api.github.com/users/octocat
Details/Error: User validation failed

This email was sent automatically by n8n.

![Workflow Editor](Screenshot%20(67).png)
![Sheet Log](Screenshot%20(68).png)
![Email Notification](Screenshot%20(69).png)


