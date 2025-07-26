# Newsletter Generation Workflow

This repository contains an n8n workflow for generating newsletters. The workflow is triggered by a form, and uses AI to generate content based on user-defined parameters.

## Workflow Overview

The workflow performs the following steps:

1.  **Form Trigger:** The workflow is initiated when a user submits a form with the following details:
    *   Date for the newsletter
    *   Specific topic (e.g., AI, ML, Security)
    *   Specific industry (e.g., Healthcare, Financial Services)
    *   Content timeline (how far back to look for content)
    *   Length of the email
    *   Special event coverage
    *   Previous month's newsletter (for context)

2.  **Content Generation:** The workflow uses a combination of AI tools to generate the newsletter content:
    *   **Brave Search, Brave News:** To gather relevant articles and information.
    *   **AWS Bedrock:** To generate embeddings for the content.
    *   **Qdrant Vector Store:** To store and retrieve vector embeddings, which helps in avoiding duplicate content from previous newsletters.

3.  **HTML Conversion:** The generated content is then converted into an HTML file, ready to be sent as a newsletter.

## SELF-HOSTED-AI-STARTER-KIT

The local n8n instance for this workflow is hosted on Docker Desktop using the [SELF-HOSTED-AI-STARTER-KIT](https://github.com/n8n-io/self-hosted-ai-starter-kit) by n8n.
