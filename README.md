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
2. **Configure File URL**:
In the Set Variables node, replace the predefined file URL with the location of your resume (e.g., a link from Supabase or Dropbox).

3. **Provide Job Description**:
Update the Set Variables node with the relevant job description that you want to match against the resume.

4. **OpenAI Credentials**:
Make sure you have an OpenAI API key and set it up in N8N under the OpenAI API credentials.

5. **Run the Workflow**:
Trigger the workflow manually by using the Test Workflow node in N8N to start the process.

---

**Use Case**
This workflow is ideal for recruitment professionals who want to automate the process of evaluating resumes based on a specific job description. The workflow provides a match percentage, a summary of candidate suitability, and detailed insights into why a candidate is suitable (or not) for the role.

