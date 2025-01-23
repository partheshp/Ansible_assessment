# Markdown to Google Docs Parser

This project provides a Python script that converts Markdown content into a formatted Google Docs document using the Google Docs API. The script supports various Markdown features, such as headings, bullet points, and checkboxes, while adding specific styles in the Google Doc.

## Features

- Converts Markdown headings (`#`, `##`, `###`) into corresponding Google Docs heading styles.
- Supports bullet points (`*`) and checkboxes (`- [ ]`), including task assignments.
- Italicizes and styles special footer lines like "Meeting recorded by:" or "Duration:".
- Batch updates Google Docs for efficient processing.

## Setup Instructions

### Prerequisites

1. **Google Cloud Project**:
   - Create a Google Cloud project.
   - Enable the **Google Docs API** and **Google Drive API**.

2. **Service Account or OAuth2 Credentials**:
   - Authenticate with Google Colab using OAuth2 (the script uses `google.colab.auth.authenticate_user()`).

### Required Dependencies

Install the required Python libraries:

```bash
pip install google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client
```

### Colab Setup:

If running on Google Colab, the script automatically uses Colab's built-in authentication (google.colab.auth).

### How to Run the Script in Google Colab:

1. **Authenticate Google Account:**
  - The script will prompt for authentication when executed. Follow the steps to authenticate.

2. **Initialize the APIs:**
  - The ```initialize_api()``` function sets up Google Docs and Drive API services.

3. **Create a Google Doc:**
  - Use the ```create_google_doc(title)``` function to create a new Google Document and retrieve its ID.
    
4. **Convert Markdown to Google Docs:**
  - Use ```parse_markdown_to_google_docs(markdown_content, doc_id)``` to process and upload Markdown content to the created Google Doc.

### Example Notebook:

To test the script in Colab:

1. Open Google Colab.
2. Copy and paste the script into a new notebook.
3. Replace markdown_content with your Markdown text.
4. Run the notebook to generate a formatted Google Doc.

### Expected Output:

The above Markdown content will be converted into a styled Google Doc with headings, bullet points, checkboxes, and footer styles.
