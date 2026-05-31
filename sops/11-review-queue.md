# Review Queue & Analytics
> Monitor, filter, and act on findings awaiting human review across all assessments, and measure how well the review process is calibrated.

## Before you start
- At least one assessment must have completed with findings generated.
- You need **Reviewer** or **Admin** role to accept/challenge findings.
- Findings appear in the review queue only after the AI assessment run finishes.

## Steps

### Review Queue

1. From the sidebar, click **Review Queue**. The page loads all findings awaiting review across every assessment in the workspace.
   [screenshot: 09-review-queue.png]

2. Findings are grouped by **section** (the criteria category they belong to). Each section header shows a count of pending items.

3. Use the **filter bar** at the top to narrow the list:
   - **Category** -- show only findings from a specific criteria group.
   - **Status** -- filter by review state (e.g., Pending, Accepted, Challenged).
   - **Reviewer** -- see only findings assigned to a particular team member.

4. Each finding row displays a **status pill** indicating its current review state. Click a row to open the finding detail (see [SOP 07 -- Finding Detail](/sops/07-finding-detail)).

5. Work through findings one by one: **Accept** the AI rating if you agree, or **Challenge** it if you disagree. Challenged findings require a reason and a revised rating.

6. As you process findings, the status pills update in real time and the pending count decreases.

### Review Analytics

7. Navigate to **Review Analytics** from the sidebar (or the link within the review queue page). This is a separate page focused on process quality rather than individual findings.
   [screenshot: 14-review-analytics.png]

8. Review the **Calibration Heatmap**. This grid shows AI rating on one axis and human decision on the other. Cells on the diagonal mean agreement; off-diagonal cells highlight where the AI and reviewers diverge.

9. Check the **Rejection Causes** breakdown. This shows the most common reasons reviewers challenge AI findings -- useful for tuning prompts or retraining the model.

10. Examine the **Activity Timeline**. This chart tracks reviewer activity over time so you can see whether the review pace is keeping up with assessment output.

11. Drill into **Category-Level Analysis** to see which criteria categories have the highest disagreement rates. Categories with frequent challenges may need prompt refinement or clearer evidence requirements.

## What happens next
- Findings you accept are marked as reviewed and feed into the results page -- see [SOP 06 -- Results & Findings Overview](/sops/06-results).
- Challenged findings return to the assessment owner for re-evaluation.
- Use review analytics data to refine your config pack prompts and scoring thresholds (see [SOP 16 -- Administration & Configuration](/sops/16-admin)).

## Common questions

**Q: Does the review queue show findings from all assessments at once?**
A: Yes. It is a workspace-level aggregation. Use filters to focus on a single assessment, category, or reviewer if the list is long.

**Q: What does the calibration heatmap tell me that individual findings do not?**
A: The heatmap reveals systemic patterns -- for example, if the AI consistently rates findings as Amber but reviewers downgrade them to Green, that signals the AI scoring may be too conservative. Individual findings only show one-off decisions.

**Q: Can I export review analytics data?**
A: Analytics data feeds into the executive report. For raw data export, use the reports page (see [SOP 06 -- Results & Findings Overview](/sops/06-results)).
