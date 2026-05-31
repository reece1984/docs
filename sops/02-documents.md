---
title: "Connecting & Managing Documents"
sidebarTitle: "Documents"
description: "Connect a document source, monitor processing, and understand how documents feed into assessments."
---

## Before you start
- You are logged in to Programme Insights (see [guide 00](/sops/00-getting-started)).
- You have Reviewer or Admin permissions on the workspace.
- If using SharePoint as a source, the SharePoint site and folder must be accessible to the Programme Insights service principal (configured by your admin).

## Key concept: connect, don't upload

Programme Insights follows a **connect, don't upload** philosophy. Rather than copying files into the platform, you bind it to the location where your documents already live -- typically a SharePoint folder. This means:

- Documents stay in your organisation's existing document management system.
- Version control and access permissions are managed in SharePoint as usual.
- The platform reads from the source; it does not modify your originals.
- You can re-sync at any time to pick up new or updated files.

Manual upload is available as a fallback for documents not stored in SharePoint.

## Steps

### Viewing the documents page

1. Open an assessment and click **Documents** in the sidebar.

[screenshot: 13-documents.png]

### Connecting a document source

2. Click **Connect Source** and choose one of:

   | Source type | How it works |
   |-------------|--------------|
   | **SharePoint folder** | Provide the SharePoint site URL and folder path. The platform connects via Microsoft Graph API using your organisation's service principal. All files in the folder (and subfolders) are discovered. |
   | **Manual upload** | Drag and drop files or browse to select. Files are stored in the platform's own storage. Use this for documents outside SharePoint. |

3. Confirm the connection. The platform begins discovering and processing files.

### Understanding document states

4. Each document passes through a processing pipeline:

   | State | Meaning |
   |-------|---------|
   | **Uploaded** | File has been received or discovered but processing has not started. |
   | **Processing** | Text extraction and indexing are in progress. |
   | **Processed** | Document is fully indexed and ready for assessment. |
   | **Error** | Processing failed (e.g. corrupt file, unsupported format). Check the error message for details. |

### What happens during processing

5. Behind the scenes, each document goes through three stages:
   - **Text extraction** -- Azure AI Document Intelligence extracts text, tables, and structure from PDFs, Word documents, and other supported formats.
   - **Chunking** -- Extracted text is split into semantically meaningful chunks for retrieval.
   - **Embedding** -- Each chunk is vectorised and stored for similarity search during assessment.

### Re-syncing documents

6. If documents in your SharePoint folder have been added, updated, or removed, click **Re-sync** to refresh the connection. The platform will:
   - Discover new files and begin processing them.
   - Re-process files whose content has changed.
   - Mark removed files as unavailable (they will not be deleted from previous assessment results).

### Reviewing match status

7. Once an assessment has run, the documents page shows additional columns:
   - **Match Status** -- whether the document was matched to any criteria during the assessment.
   - **Criteria Coverage** -- how many criteria reference evidence from this document.

## What happens next
- Create an assessment that uses these documents: [Creating a New Assessment](/sops/04-creating-assessments)
- Run the assessment and watch it process: [Running & Monitoring Assessments](/sops/05-running-assessments)

## Common questions

**Q: What file formats are supported?**
PDF, DOCX, XLSX, PPTX, and plain text. Scanned PDFs are supported via OCR through Azure AI Document Intelligence.

**Q: How long does document processing take?**
Typically 1-3 minutes per document depending on size and format. Large PDFs with many pages may take longer.

**Q: Can I connect multiple SharePoint folders to one assessment?**
Currently each assessment connects to a single document source. If you need files from multiple locations, consolidate them into one SharePoint folder or use manual upload for the additional files.
