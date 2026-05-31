---
title: "Reviewing Findings"
sidebarTitle: "Reviewing Findings"
description: "Use the two-pane reviewer workspace to evaluate AI-surfaced evidence, make decisions, and drive remediation."
---

## Before you start
- You must be assigned as a **Reviewer** on the finding, or hold **Admin** role on the assessment.
- The assessment must be in **Reviewing** status.
- Open the finding from the Results page ([SOP 06](/sops/06-results)) or the Review Queue.

## Steps

1. **Open the Finding Detail view.** Click any finding row on the Results page. The workspace loads in a two-pane layout:
   - **Left pane** -- evidence requirements, criterion definition, and reviewer actions.
   - **Right pane** -- the source document with every citation highlighted in context.
   [screenshot: 10-finding-detail.png]

2. **Read the evidence requirements.** The left pane lists each evidence requirement for this criterion. Each requirement shows the AI's assessment of whether the document set provides sufficient evidence, along with the specific passages cited.

3. **Follow citations in the document.** Click any citation reference in the left pane. The right pane scrolls to the highlighted passage in the source document, letting you verify the AI's read against the original text.

4. **Make a decision on each evidence requirement.** Four actions are available per requirement:

   | Action | When to use | What happens |
   |--------|-------------|--------------|
   | **Accept** | The AI's assessment is correct. | Requirement marked as reviewed; no further action needed. |
   | **Challenge** | The AI is wrong -- you disagree with the rating or interpretation. | You record a rationale. The finding is flagged for re-assessment in the next run. |
   | **Query AI** | You need clarification before deciding. | Opens a finding-scoped chat where you can ask follow-up questions about the evidence. |
   | **Create Action** | There is a genuine gap that needs remediation. | Creates a task with owner and deadline, linked back to this finding. |

5. **Record challenge rationale.** When challenging, a text field appears. Write a clear explanation of why the AI's assessment is incorrect -- this rationale is stored against the finding for audit and fed into the next assessment run.

6. **Use the finding-scoped chat (Query AI).** The chat panel opens alongside the finding. Questions are answered in the context of this specific criterion, its evidence, and the source documents. Close the chat to return to the decision view.

7. **Create remediation actions.** When clicking **Create Action**, fill in:
   - **Action title** -- a concise description of what needs doing.
   - **Owner** -- the person responsible.
   - **Deadline** -- target completion date.
   The action appears on the Actions page ([SOP 13](/sops/13-actions)) and links back to this finding.

8. **Complete sign-off.** The sign-off button activates only when every evidence requirement on the finding has a decision (Accept, Challenge, or Create Action). Queried requirements must be resolved first. Click **Sign Off** to lock your review.

9. **Navigate between findings.** Use keyboard shortcuts for speed:
   - **J / K** -- move to the next / previous finding without returning to Results.
   - **A** -- accept the current requirement.
   - **C** -- challenge the current requirement.
   - **?** -- show the full keyboard shortcuts overlay.
   - **Esc** -- close the finding detail and return to Results.

## What happens next
- Return to the results list to continue triage: [SOP 06 -- Understanding Results](/sops/06-results).
- Generate remediation content for RED/AMBER findings: [SOP 08 -- Generating Content](/sops/08-content-generation).
- Manage actions created during review: [SOP 13 -- Actions](/sops/13-actions).
- See the reference diagram: `review-workflow.md`.

## Common questions

**Q: What happens if I challenge a finding?**
A: The finding is flagged with your rationale. On the next assessment run, the AI incorporates your feedback. The challenge does not change the current rating -- it influences the next run.

**Q: Can I change my decision after sign-off?**
A: No. Once a finding is signed off, decisions are locked for audit integrity. If circumstances change, run a new assessment version and review the finding again.

**Q: Why is the Sign Off button greyed out?**
A: At least one evidence requirement still has no decision. Check for requirements in Pending or Queried status -- each must be resolved to Accept, Challenge, or Create Action before sign-off is permitted.
