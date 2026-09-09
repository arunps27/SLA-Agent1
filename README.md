# SLA-Agent
Capstone case study
Note: SLA Analizer_Draft.ipynb is a draft version. I will fine tune and update final if possible

PROMPT TO GENERATE THE COMPLETE COLAB APPLICATION

Build a production-style AI Operations, Governance & Support Studio in Google Colab using Python + Streamlit + Azure OpenAI.

The final deliverable must be a single Google Colab notebook script that can be copied and executed directly in Colab without modifications.

The application should look and behave like a production operations portal, not a simple chatbot.

Objective

Create a complete AI Operations Studio that demonstrates:

AI Operations Operating Model
Incident Classification
SLA Risk Analysis
Runbooks & Playbooks
Governance & Guardrails
ServiceNow Support Copilot
Azure OpenAI Integration
Monitoring Dashboard

The UI should resemble an enterprise operations platform with multiple tabs and a professional design.

Technology Stack

Use:

Python
1
streamlit
2
azure-openai
3
pandas
4
plotly
5
python-dotenv
6
pyngrok or cloudflared
Show more lines

The application must run entirely from Google Colab.

Environment Variables

Use only three secrets:

Python
1
AOAI_ENDPOINT
2
AOAI_API_KEY
3
AOAI_DEPLOYMENT
Show more lines

The application must automatically verify the connection during startup.

Display:

Plain Text
1
✅ Connected to Azure OpenAI
Show more lines

or

Plain Text
1
❌ Connection Failed
Show more lines
Main Application Layout

Create the title:

Plain Text
1
AI Ops, Governance & Support Studio
Show more lines

Description:

Plain Text
1
AI Operations operating model, runbooks, governance, SLA monitoring, capstone incident simulation, and a ServiceNow support copilot in one application.
Show more lines

Create the following tabs:

Plain Text
1
1. AI Ops Operating Model
2
2. Runbooks & Playbooks
3
3. Governance Controls
4
4. Incident Simulator
5
5. SLA Analyzer
6
6. ServiceNow Support Agent
7
7. Admin Dashboard
Show more lines
TAB 1
AI Ops Operating Model

Display a Severity Matrix.

Use the following definitions:

Python
1
SEV1
2
Critical outage
3
Customer impact
4
Security incident
5
Data loss risk
6
Response SLA: 15 minutes
7
 
8
SEV2
9
Major incident
10
Multiple users affected
11
Response SLA: 30 minutes
12
 
13
SEV3
14
Minor issue
15
Workaround available
16
Response SLA: 4 hours
17
 
18
SEV4
19
Low impact
20
Informational
21
Response SLA: Next business day
Show more lines

Render these as professional cards.

TAB 2
Runbooks & Playbooks

Create a runbook repository.

Example runbooks:

Python
1
Azure OpenAI Outage
2
 
3
API Version Error
4
 
5
Authentication Failure
6
 
7
ServiceNow Integration Failure
8
 
9
Deployment Not Found
10
 
11
High Latency Incident
12
 
13
Prompt Injection Detected
Show more lines

Each runbook should display:

Plain Text
1
Overview
2
 
3
Root Cause
4
 
5
Business Impact
6
 
7
Immediate Actions
8
 
9
Escalation Path
10
 
11
Validation Steps
12
 
13
Recovery Criteria
Show more lines

Use expanders.

TAB 3
Governance Controls

Create a Governance Dashboard showing:

Safety Controls
Plain Text
1
Content Filtering Enabled
2
Prompt Injection Detection Enabled
3
Jailbreak Detection Enabled
4
PII Protection Enabled
5
Audit Logging Enabled
6
Human Approval Workflow Enabled
Show more lines

Display green status indicators.

Model Settings

Display current settings:

Python
1
temperature = 0.2
2
 
3
top_p = 0.95
4
 
5
max_completion_tokens = 350
6
 
7
frequency_penalty = 0
8
 
9
presence_penalty = 0
Show more lines
TAB 4
Incident Simulator

Create a textbox:

Plain Text
1
Describe what is happening
Show more lines

Example:

Plain Text
1
Users are unable to access the support chatbot.
2
API requests are failing.
3
Ticket backlog is increasing.
Show more lines

Send the incident description to Azure OpenAI.

Use a structured prompt that returns:

JSON
1
{
2
"severity": "",
3
"confidence": "",
4
"impact": "",
5
"root_cause": "",
6
"recommended_actions": []
7
}
Show more lines

Display the result as a professional incident summary.

Color code severity:

Plain Text
1
SEV1 Red
2
SEV2 Orange
3
SEV3 Yellow
4
SEV4 Green
Show more lines
TAB 5
SLA Analyzer

Create inputs:

Plain Text
1
Ticket Age (hours)
2
 
3
SLA Target (hours)
4
 
5
Current Status
6
 
7
Pending Work
Show more lines

Calculate:

Python
1
Remaining Time
2
 
3
SLA Health
4
 
5
At Risk / Not At Risk
6
 
7
Probability of Breach
Show more lines

Display:

Plain Text
1
Current SLA Status
2
Risk %
3
Reason
4
Recommended Action
Show more lines

Visualize risk using:

Python
1
plotly gauge chart
Show more lines
TAB 6
ServiceNow Support Agent

Create a chat interface.

System Prompt:

"You are an AI Operations Support Agent.

You help with:

Incident triage ServiceNow tickets SLA analysis Runbook execution Root cause hypotheses

Always determine SLA risk.

Always recommend severity.

Never invent facts.

If information is missing, explicitly state that."


User enters ticket details.

Agent returns:

Ticket Summary

Severity

SLA Risk

Recommended Actions

Escalation Recommendation

Next Steps


Store session history.

TAB 7
Admin Dashboard

Display:

Azure Status
Plain Text
1
Connection Status
2
 
3
Deployment Name
4
 
5
Endpoint
Show more lines
Usage Metrics

Display:

Plain Text
1
Total Requests
2
Estimated Token Usage
3
Estimated Cost
4
Session Duration
Show more lines

Store metrics in streamlit session state.

Sidebar Controls

Create a production configuration panel:

Python
1
temperature
2
 
3
top_p
4
 
5
max_completion_tokens
6
 
7
frequency_penalty
8
 
9
presence_penalty
10
 
11
seed
Show more lines

Add:

Plain Text
1
Reset Conversation
2
 
3
Clear Session Data
Show more lines
Enterprise UI Requirements

Use:

Python
1
wide layout
2
 
3
custom CSS
4
 
5
professional cards
6
 
7
status badges
8
 
9
metric tiles
10
 
11
charts
12
 
13
expanders
14
 
15
tabs
Show more lines

The application should visually resemble an enterprise operations portal rather than a prototype chatbot.

Fault Tolerance

The application must:

Python
1
Handle connection failures
2
 
3
Handle unsupported parameters
4
 
5
Retry Azure OpenAI requests
6
 
7
Display meaningful error messages
8
 
9
Prevent application crashes
Show more lines
Startup Behavior

When the notebook runs:

Install all dependencies.
Generate app.py automatically.
Launch Streamlit.
Create a public URL.
Display:
Plain Text
1
Application Started Successfully
2
Open URL:
3
<generated URL>
Show more lines
Deliverable

Generate:

Complete Google Colab code.
Fully functional Streamlit application.
No placeholders.
No pseudocode.
Production-quality implementation.
Everything in one Colab notebook.
Ready to copy, paste, and execute.

This prompt will produce something very close to the enterprise-style screen you shared, with the AI Ops model, SLA engine, governance controls, incident simulator, and ServiceNow support agent integrated into a single production-style portal.

**Output**
<img width="1216" height="547" alt="image" src="https://github.com/user-attachments/assets/402599a6-bfcc-415f-8ccb-f5d456fdd81a" />
<img width="1205" height="522" alt="image" src="https://github.com/user-attachments/assets/8cbf2f2f-3414-4427-a88b-defa033b0200" />


