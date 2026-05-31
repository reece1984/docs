---
title: "Understanding Results"
sidebarTitle: "Understanding Results"
description: "Navigate the Results page to triage, filter, and prioritise every finding surfaced by the AI assessment."
---

## Before you start
- At least one assessment must have completed (status: **Complete** or **Reviewing**).
- You need **Reviewer** or **Admin** role on the assessment.
- Familiarise yourself with RAG ratings: **RED** (significant gap), **AMBER** (partial coverage), **GREEN** (sufficient evidence).

## Steps

1. **Open the Results page.** From the sidebar, click **Results**. The page loads all findings for the current assessment.
   [screenshot: 08-results.png]

2. **Choose your view tab.** Three tabs sit above the findings list, each with a live count:
   - **Assigned to me** -- findings where you are the named reviewer.
   - **My team** -- findings assigned to anyone in your team.
   - **All findings** -- the full unfiltered set.

3. **Apply filters.** Use the filter bar to narrow results by:
   - **Category** -- the framework section (e.g. Strategic Case, Management Case).
   - **DCA rating** -- RED, AMBER, or GREEN.
   - **Review status** -- Pending, Accepted, Challenged, Queried.
   - **Reviewer** -- a specific team member.
   - **Deadline** -- findings with upcoming or overdue deadlines.

4. **Sort the list.** Click the sort control to reorder by:
   - **Deadline proximity** -- most urgent first.
   - **Severity** -- RED before AMBER before GREEN.
   - **Last updated** -- most recently changed first.

5. **Read the Category cards.** Above the findings list, each category displays a RAG distribution bar showing the proportion of RED, AMBER, and GREEN findings at a glance.

6. **Check the Gate Readiness card.** This summary card shows whether the assessment meets the sign-off threshold. It aggregates outstanding decisions and flags blockers preventing gate clearance.

7. **Navigate with keyboard shortcuts.** For power users:
   - **J / K** -- move down / up through the findings list.
   - **Enter** -- open the selected finding in detail view.
   - **/** -- focus the filter bar.

8. **Open a finding.** Click any finding row (or press Enter) to enter the Finding Detail view for full evidence review.

## What happens next
- Drill into individual findings: [Reviewing Findings](/sops/07-finding-detail).
- Work through the review queue systematically: [Review Queue](/sops/11-review-queue).
- See the reference diagram: `review-workflow.md`.

## Common questions

**Q: Why do the tab counts not add up to the total?**
A: A single finding can appear under both "Assigned to me" and "My team" if you belong to the assigned team. "All findings" is the deduplicated total.

**Q: Can I save a filter combination for reuse?**
A: Not yet -- filters reset when you leave the page. Use the URL query string as a bookmark workaround; filter state is encoded there.

**Q: What does the Gate Readiness card measure?**
A: It checks whether every criterion in the framework has a reviewer decision (Accept or Challenge). Findings still in Pending or Queried status block gate clearance.
