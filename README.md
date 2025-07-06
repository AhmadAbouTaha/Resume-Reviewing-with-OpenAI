# Resume Evaluation Workflow with OpenAI

## Overview

This repository contains a workflow for automating the **resume evaluation** process using N8N. It integrates multiple nodes to download a resume, extract text from the document, analyze it with OpenAI, and store the results in a structured format.

The workflow is particularly useful for recruitment agencies and HR professionals to streamline the hiring process by evaluating resumes based on job descriptions.

---

## Workflow Steps

1. **Trigger**: The workflow starts when you manually trigger the action using N8N's *Test Workflow* feature.
   
2. **Download File**: Downloads the resume from a given URL. The file URL is predefined for demonstration purposes, but it can be customized to work with other storage solutions (e.g., Supabase).

3. **Extract Document PDF**: The workflow extracts text from the downloaded PDF file using N8N’s PDF extraction node.

4. **Analyze Resume with OpenAI**: The extracted data (resume text) along with the job description is sent to OpenAI for analysis. OpenAI returns:
   - A match percentage score of the candidate’s suitability for the role.
   - A summary of why the candidate is a good fit or not for the position.
   - A detailed breakdown of reasons why the candidate is or isn't suitable.

5. **Store Results**: The results from OpenAI (including match score, suitability summary, and reasons) are parsed into a structured JSON format.

6. **Results Visualization**: Sticky notes are included for reminders and setup instructions within the workflow.

---

## Key Nodes

- **Manual Trigger**: Initiates the workflow manually for testing purposes.
- **Download File**: Fetches the resume from a URL.
- **Extract Document PDF**: Extracts text content from the PDF document.
- **OpenAI - Analyze Resume**: Sends the extracted text and job description to OpenAI's API for analysis.
- **Set Variables**: Defines the necessary variables such as file URL and job description.
- **Parsed JSON**: Parses the JSON response from OpenAI for further use.

---

## Setup Instructions

To set up and use this workflow, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/resume-evaluation-workflow.git
   cd resume-evaluation-workflow
