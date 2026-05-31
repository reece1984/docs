---
title: "Managing Actions"
sidebarTitle: "Actions"
description: "Track remediation work from discovery to completion -- turn assessment findings into assignable, trackable actions with owners, deadlines, and audit trails."
---

## Before you start
- At least one assessment must have findings that have been reviewed.
- You need **Reviewer** or **Admin** role to create and manage actions.
- Actions are created from the finding detail page, not from the actions page itself.

## Steps

### Creating an action

1. Navigate to a finding that represents a genuine gap (see [SOP 07 -- Finding Detail](/sops/07-finding-detail)).

2. From the finding detail page, click **Create Action**. This links the new action back to its source finding so you always know why the action exists.

3. Fill in the action details:
   - **Title** -- a clear, actionable description (e.g., "Update flood risk assessment to include 2080 climate scenarios").
   - **Owner** -- the person responsible for completing the action.
   - **Deadline** -- target completion date.
   - **Priority** -- Low, Medium, High, or Critical.

4. Click **Save**. The action is created with status **Not Started**.

### Managing actions

5. Open **Actions** from the sidebar to see all actions across the workspace.
   [screenshot: 11-actions.png]

6. Toggle between **List view** and **Board view** using the control at the top right:
   - **List view** -- sortable table with all action details visible.
   - **Board view** -- kanban-style columns grouped by status.

7. Use **filters** to narrow the list:
   - **Owner** -- see only actions assigned to a specific person.
   - **Status** -- filter by Not Started, In Progress, Completed, or Blocked.
   - **Due date** -- find overdue or upcoming actions.

### Updating action status

8. Click an action to open its detail panel.

9. Update the **status** as work progresses:
   - **Not Started** -- action has been logged but work has not begun.
   - **In Progress** -- work is underway.
   - **Completed** -- the gap has been addressed.
   - **Blocked** -- work cannot proceed; add a comment explaining why.

10. Add **comments** to the action for context, updates, or decisions. Every comment is timestamped and attributed, creating an audit trail.

11. Click the **source finding link** to jump back to the original finding that triggered this action.

## What happens next
- Completed actions demonstrate remediation progress and feed into the executive summary narrative.
- When you re-run an assessment after addressing actions, compare versions to see whether the finding has been resolved (see [SOP 15 -- Comparing Assessment Versions](/sops/15-compare-versions)).
- Outstanding actions appear in dashboard summaries (see [SOP 01 -- Workspace Dashboard](/sops/01-workspace-dashboard)).

## Common questions

**Q: Can I create an action without linking it to a finding?**
A: Actions are designed to trace back to findings for accountability. The creation flow starts from the finding detail page to enforce this link.

**Q: What is the difference between Blocked and In Progress?**
A: Use **Blocked** when external dependencies prevent progress -- for example, waiting for a third-party document or a decision from a steering group. This signals to the team that the action needs intervention, not just time.

**Q: Who can see and edit actions?**
A: All workspace members can view actions. Reviewers and Admins can create, edit, and update status. The action owner receives notifications when comments are added.
