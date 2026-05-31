---
title: "Initiatives & Grouping"
sidebarTitle: "Initiatives"
description: "Organise related assessments under programme-level initiatives for cross-assessment visibility and rollup reporting."
---

## Before you start
- You need **Admin** role to create and manage initiatives.
- At least one assessment must exist to tag it to an initiative, though you can create an empty initiative first.
- Initiatives are optional -- they add value for complex programmes but are not required for single assessments.

## Steps

### When to use initiatives

Initiatives are useful when a programme has multiple concurrent assessments. For example:
- **HS2** might run a Gate 3 OBC assessment, a Green Book FBC assessment, and an NEC4 contract review in parallel.
- **A large infrastructure programme** might have separate assessments per work package but need a unified programme-level view.

If you only have one or two assessments, you probably do not need initiatives.

### Creating an initiative

1. Navigate to **Initiatives** from the sidebar.
   [screenshot: 03-initiatives-index.png]

2. Click **New Initiative**.

3. Enter a name and optional description for the initiative (e.g., "HS2 Phase 2b -- Gate 3 Assurance").

4. Save the initiative. It appears in the initiatives list.

### Tagging assessments to an initiative

5. Open the initiative detail page by clicking its name.

6. Click **Add Assessment** and select one or more existing assessments to tag to this initiative.

7. Assessments can belong to multiple initiatives if needed (e.g., a shared document set used across programme streams).

### Using the initiative view

8. The initiative detail page shows **rollup metrics** aggregated across all tagged assessments:
   - Combined DCA (Delivery Confidence Assessment) status.
   - Activity summary showing recent review and assessment activity.
   - Assessment count and completion status.

9. Click any individual assessment within the initiative to drill down to its results, findings, or review queue.

10. Use the initiative view when reporting to programme boards -- it provides the cross-cutting view that individual assessments cannot.

## What happens next
- Initiative rollup data feeds into the dashboard (see [SOP 01 -- Workspace Dashboard](/sops/01-workspace-dashboard)).
- Individual assessments within an initiative follow the standard workflow: documents, assessment run, results, review (see [SOP 04 -- Creating an Assessment](/sops/04-creating-assessments)).

## Common questions

**Q: Do I have to use initiatives?**
A: No. Initiatives are entirely opt-in. Many workspaces run perfectly well with standalone assessments. Initiatives become valuable when you need cross-assessment reporting or programme-level oversight.

**Q: Can I remove an assessment from an initiative?**
A: Yes. Removing an assessment from an initiative only untags it -- the assessment itself and all its data remain intact.

**Q: What happens if I delete an initiative?**
A: Deleting an initiative removes the grouping only. All assessments, findings, and actions within those assessments are unaffected.
