QA Assessment – Task 2

n8n API Integration Workflow

Name: Tripti

 Objective
This workflow demonstrates API integration, data transformation, API enrichment, conditional filtering, error handling, and Discord output using n8n.

 Workflow
Schedule Trigger → GitHub API Request → Code – Select Top 5 Repositories → GitHub README API Request → IF – Stars > 1000 → Code – Prepare Output → Discord Webhook

 APIs Used
- GitHub REST API – repository search
- GitHub README API – repository enrichment
- Discord Webhook – final output

 Transformation
The workflow selects the top 5 repositories and extracts repository name, URL, owner, description, star count, and README URL.

 Conditional Logic
Repositories are checked using **Stars > 1000**.

Error Handling
HTTP Request nodes use **On Error → Continue** so the workflow can continue if an API request encounters an error.

 Credentials
Credentials are stored using n8n's credential system. No webhook secrets or API credentials are hard-coded.

 Test Result
The workflow executed successfully and sent 5 repository results to Discord with their actual star counts.

### Files
- `My workflow 2.json` – exported n8n workflow
- Screenshots – workflow and successful execution evidence
