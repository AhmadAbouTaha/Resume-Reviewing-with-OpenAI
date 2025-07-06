Resume Evaluation Workflow with OpenAI
Overview
This workflow automates the resume evaluation process using N8N. It integrates multiple nodes to download a resume, extract the text from the document, analyze it using OpenAI, and store the results in a structured format.

It is particularly useful for recruitment agencies and HR professionals to streamline the hiring process by evaluating resumes based on a job description.

Workflow Steps
Trigger: The workflow starts when you manually trigger the action using N8N's Test Workflow feature.

Download File: Downloads the resume from a given URL. The file URL is predefined for demonstration purposes, but can be customized to work with other storage solutions (e.g., Supabase).

Extract Document PDF: The workflow extracts text from the downloaded PDF file using N8N’s PDF extraction node.

Analyze Resume with OpenAI: The extracted data (resume text) along with the job description is sent to OpenAI for analysis. OpenAI returns:

A match percentage score of the candidate’s suitability for the role.

A summary of why the candidate is a good fit or not for the position.

A detailed breakdown of reasons why the candidate is or isn't suitable.

Store Results: The results from OpenAI (including match score, suitability summary, and reasons) are parsed into a structured JSON format.

Results Visualization: Sticky notes are included for reminders and setup instructions within the workflow.

Key Nodes
Manual Trigger: Initiates the workflow manually for testing purposes.

Download File: Fetches the resume from a URL.

Extract Document PDF: Extracts text content from the PDF document.

OpenAI - Analyze Resume: Sends the extracted text and job description to OpenAI's API for analysis.

Set Variables: Defines the necessary variables such as file URL and job description.

Parsed JSON: Parses the JSON response from OpenAI for further use.

Setup
File URL: Set the URL where the resume is stored (e.g., Supabase or Dropbox).

Job Description: Provide the job description that will be used to match with the resume.

OpenAI Connection: Ensure that your OpenAI API credentials are set up correctly for analysis.

Use Case
This workflow is ideal for recruitment professionals who want to automate the evaluation of resumes based on a specific job description. It provides a match percentage, a summary, and insights into whether the candidate is suitable for the role.

Requirements
N8N instance running

OpenAI API credentials

A resume stored online (e.g., Supabase or Dropbox)
