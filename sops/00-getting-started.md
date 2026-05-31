---
title: "Getting Started with Programme Insights"
sidebarTitle: "Getting Started"
description: "Log in, orient yourself, and understand the core assessment workflow."
---

## Before you start
- You need a Microsoft Entra ID account provisioned by your organisation's admin.
- Your admin must have added you to the Programme Insights tenant with the appropriate role (Viewer, Reviewer, or Admin).
- Use a modern browser (Edge, Chrome, or Firefox).

## What is Programme Insights?

Programme Insights is an AI-assisted assurance platform for major infrastructure and government programmes. It takes a set of project documents, assesses them against a criteria framework (such as the IPA Gateway Review framework), and surfaces scored findings with citations back to the source material. Every finding can be reviewed, challenged, or accepted by a human reviewer before actions and reports are produced.

## The six-step assessment flow

The core workflow follows six stages:

1. **Pick a framework** -- choose the criteria template your documents will be assessed against (e.g. IPA Gateway 3, Green Book, CDM).
2. **Connect documents** -- bind a SharePoint folder or upload files so the platform can ingest and index them.
3. **Run the assessment** -- the agentic pipeline processes documents, matches content to criteria, and scores each finding.
4. **Review findings** -- walk through each scored finding, read the AI rationale and citations, then accept, challenge, or query.
5. **Act on gaps** -- create actions for findings that need remediation and assign owners.
6. **Produce a report** -- generate an executive summary, detailed report, or export for stakeholders.

### Core concept

An **assessment** is the atomic unit of work: one document set assessed against one framework. If you need to assess the same documents against two frameworks, you create two assessments. If you need to assess two document sets against the same framework, you also create two assessments.

## Steps

### Logging in

1. Navigate to your organisation's Programme Insights URL.
2. Click **Sign in with Microsoft**.
3. Authenticate via Microsoft Entra ID. If your organisation uses MFA, complete the second factor.
4. On first login you may be asked to consent to the application permissions -- accept to proceed.

### Navigating the workspace

5. After login you land on the **Workspace Dashboard**. This is your portfolio-level home page showing KPIs, running assessments, and upcoming deadlines.

[screenshot: 01-dashboard.png]

6. The **sidebar** is your primary navigation. It is split into two zones:

   **Workspace pages** (always visible):
   - Dashboard -- portfolio overview
   - Assessments -- list of all assessments
   - Initiatives -- cross-assessment programme groupings
   - Frameworks -- browse available criteria frameworks
   - Review Queue -- findings awaiting human review across all assessments

   **Assessment-scoped pages** (visible when you open an assessment):
   - Summary -- headline findings and coverage
   - Results -- scored criteria grouped by category
   - Findings -- individual finding cards
   - Documents -- connected document set
   - Actions -- remediation tasks
   - Reports -- generated outputs
   - Chat -- RAG-powered Q&A with citations

## What happens next
- Explore your dashboard: [Your Workspace Dashboard](/sops/01-workspace-dashboard)
- Create your first assessment: [Creating a New Assessment](/sops/04-creating-assessments)

## Common questions

**Q: Can I use a personal Microsoft account?**
No. Programme Insights requires a Microsoft Entra ID (formerly Azure AD) organisational account. Your admin provisions access.

**Q: I logged in but see an empty dashboard -- is something wrong?**
No. A new workspace has no assessments yet. Follow guide 04 to create your first one.

**Q: What browsers are supported?**
Edge, Chrome, and Firefox (latest two major versions). Safari works but is not officially tested.
