---
title: "Running & Monitoring Assessments"
sidebarTitle: "Run & Monitor"
description: "Start an assessment run, monitor the agentic pipeline in real time, and understand assessment states."
---

## Before you start
- You have created an assessment in draft state (see [guide 04](/sops/04-creating-assessments)).
- Documents are connected and in **Processed** state (see [guide 02](/sops/02-documents)).
- You have Reviewer or Admin permissions.

## Steps

### Starting the pipeline

1. Open the assessment you want to run. If it is in **draft** state, you will see a **Run Assessment** button on the summary page.

2. Click **Run Assessment**. The assessment state changes from **draft** to **in_progress** and the agentic pipeline begins.

### What happens during a run

3. The pipeline processes your documents through multiple stages automatically. A typical full assessment takes approximately **30 minutes**, depending on the number of documents and criteria.

[screenshot: 17-assessment-running.png]

4. The live progress display shows each pipeline stage and its status:

   | Stage | What it does |
   |-------|--------------|
   | **Ingestion** | Reads and normalises all connected documents. |
   | **Indexing** | Chunks document text and builds the vector index for retrieval. |
   | **Criterion Matching** | For each criterion in the framework, retrieves the most relevant document passages using semantic search. |
   | **Scoring** | The AI evaluates matched passages against each criterion and assigns a RAG (Red/Amber/Green) score with rationale and citations. |
   | **Finding Generation** | Individual findings are created for each scored criterion, including evidence references and confidence levels. |
   | **Quality Checks** | Cross-references findings for consistency, flags low-confidence scores, and validates citation integrity. |
   | **Aggregation** | Rolls up criterion-level scores into category summaries and overall assessment metrics. |
   | **Completion** | Finalises all results and transitions the assessment to completed state. |

### You can leave and come back

5. The pipeline runs server-side. You do not need to keep the browser open. Close the tab, log out, or work on other assessments -- nothing is lost. When you return, the progress view picks up where it left off.

### Understanding assessment states

6. Every assessment is in one of three states:

   | State | Meaning | What you can do |
   |-------|---------|-----------------|
   | **Draft** | Assessment is created but the pipeline has not started. | Edit configuration, connect documents, start the run. |
   | **In Progress** | The agentic pipeline is actively processing. | Monitor progress, but you cannot edit the assessment configuration. |
   | **Completed** | All criteria have been scored and findings are ready. | Review findings, create actions, generate reports. |
   | **Failed** | The pipeline encountered an unrecoverable error. | Investigate the error message, fix the issue, and retry. |

### Handling a completed assessment

7. When the pipeline finishes, the assessment moves to **completed** state. You will see:
   - A summary of total criteria assessed, RAG distribution, and coverage.
   - All findings are now available in the Results and Review Queue pages.
   - The assessment is ready for human review.

### Handling a failed assessment

8. If the pipeline fails:
   - Check the error message on the progress view for details (e.g. document processing failure, service timeout).
   - Common fixes: re-sync documents to resolve file errors, check SharePoint permissions, or contact your admin.
   - Click **Retry** to restart the pipeline from the failed stage.

## What happens next
- Review scored results: Understanding Results (forthcoming)
- Drill into individual findings: Finding Detail & Review (forthcoming)

## Common questions

**Q: Can I run multiple assessments at the same time?**
Yes. Each assessment runs its own independent pipeline. You can start several assessments and monitor them all from the dashboard's Running Assessments panel.

**Q: What if I add new documents while an assessment is running?**
Documents added during a run will not be included in the current assessment. Wait for the run to complete, re-sync your documents, then run the assessment again to include the new files.

**Q: How accurate is the "30 minutes" estimate?**
It depends on the document set size and the framework. Small assessments (5-10 documents, 30 criteria) may complete in 10-15 minutes. Large assessments (100+ documents, 200+ criteria) may take an hour or more. The live progress display shows real-time stage completion and estimated time remaining.
