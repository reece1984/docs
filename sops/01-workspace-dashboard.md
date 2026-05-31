# Your Workspace Dashboard
> Understand the portfolio-level dashboard and use it to monitor assessments, deadlines, and review workload.

## Before you start
- You are logged in to Programme Insights (see [SOP 00](/sops/00-getting-started)).
- You have at least Viewer permissions on the workspace.

## Steps

### Opening the dashboard

1. Click **Dashboard** in the sidebar, or navigate to the root URL after login. The dashboard is the default landing page.

[screenshot: 01-dashboard.png]

### Reading the KPI tiles

2. At the top of the dashboard you will see four KPI tiles summarising your portfolio:

   | Tile | What it shows |
   |------|---------------|
   | **Total Assessments** | Count of all assessments in the workspace (draft, running, and completed). |
   | **Running Now** | Assessments whose agentic pipeline is currently in progress. |
   | **Awaiting Review** | Assessments with findings that have not yet been accepted or challenged by a reviewer. |
   | **Open Actions** | Total remediation actions that are not yet marked complete across all assessments. |

### Monitoring running assessments

3. Below the KPI tiles, the **Running Assessments** panel lists every assessment currently being processed. Each row shows:
   - Assessment name and framework
   - Pipeline stage (e.g. Ingestion, Indexing, Criterion Matching, Scoring)
   - Progress bar with percentage complete
   - Estimated time remaining

4. Click any running assessment row to jump into its live progress view (see [SOP 05](/sops/05-running-assessments)).

### Checking upcoming deadlines

5. The **Upcoming Deadlines** panel shows assessments with a target completion date within the next 14 days. Deadlines are set when creating or editing an assessment.

### Starting a new assessment

6. Click the **New Assessment** button (top-right of the dashboard or in the running assessments panel) to launch the creation wizard. See [SOP 04](/sops/04-creating-assessments) for the full walkthrough.

## What happens next
- Create a new assessment: [SOP 04 -- Creating a New Assessment](/sops/04-creating-assessments)
- Connect documents to an assessment: [SOP 02 -- Connecting & Managing Documents](/sops/02-documents)
- Understand what happens when an assessment runs: [SOP 05 -- Running & Monitoring Assessments](/sops/05-running-assessments)

## Common questions

**Q: Do KPI numbers update in real time?**
Yes. The dashboard polls for updates while you have the page open. Running assessment progress refreshes automatically.

**Q: Can I customise which KPIs are shown?**
Not currently. The four tiles are fixed. Future releases may add configurable widgets.

**Q: I see "Awaiting Review" but I am not a reviewer -- can I still see the findings?**
Yes, if you have Viewer or higher permissions. You can read findings but only Reviewers and Admins can accept or challenge them.
