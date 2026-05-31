---
title: "Creating a New Assessment"
description: "Walk through the new assessment wizard to set up a framework, connect documents, and configure assessment preferences."
---

## Before you start
- You are logged in to Programme Insights (see [SOP 00](/sops/00-getting-started)).
- You have Reviewer or Admin permissions on the workspace.
- You know which framework you want to assess against (browse the library first if unsure -- see [SOP 03](/sops/03-frameworks-library)).
- Your documents are accessible via SharePoint or ready for manual upload (see [SOP 02](/sops/02-documents)).

## Steps

### Opening the wizard

1. Click **New Assessment** from the dashboard, the assessments index page, or the sidebar. The new assessment wizard opens.

[screenshot: 05-new-assessment-wizard.png]

### Filling in the required fields

The wizard is deliberately short. There are **three required fields** and one optional field.

2. **Assessment Name** -- give the assessment a descriptive name (e.g. "HS2 Phase 2b -- Gateway 3 Review, May 2026"). This name appears throughout the platform and in reports.

3. **Framework** -- select the criteria framework this assessment will use. Start typing to search, or browse the full list. Each assessment uses exactly one framework. See [SOP 03](/sops/03-frameworks-library) for details on what frameworks are available.

4. **Document Source** -- choose how to connect your documents:
   - **SharePoint folder** -- provide the SharePoint site URL and folder path. The platform discovers all files in the folder and subfolders.
   - **Manual upload** -- drag and drop files or browse to select.

   See [SOP 02](/sops/02-documents) for full details on document connection.

### Adding the optional field

5. **Programme / Initiative tag** (optional) -- assign this assessment to a programme or initiative for cross-assessment grouping. Initiatives let you track multiple assessments (e.g. different gateway stages for the same project) as a cohesive portfolio. See SOP 14 -- Initiatives (forthcoming) for more.

### Configuring assessment preferences

6. After the core fields, you can optionally configure:
   - **Categories to include** -- by default all categories in the chosen framework are assessed. Deselect any categories you want to exclude from this run.
   - **Document scope** -- if your connected folder contains documents not relevant to this assessment, you can exclude specific files.

### Reviewing and creating

7. Review your selections on the confirmation screen. Check:
   - Assessment name is correct.
   - The right framework is selected.
   - Document source shows the expected file count.
   - Categories and document scope match your intent.

8. Click **Create Assessment**. The assessment is created in **draft** state.

9. To start the assessment pipeline, click **Run Assessment** from the assessment summary page. See [SOP 05](/sops/05-running-assessments) for what happens next.

## What happens next
- Understand the assessment pipeline: [SOP 05 -- Running & Monitoring Assessments](/sops/05-running-assessments)
- Browse frameworks before choosing one: [SOP 03 -- Browsing the Frameworks Library](/sops/03-frameworks-library)
- Connect documents in advance: [SOP 02 -- Connecting & Managing Documents](/sops/02-documents)

## Common questions

**Q: Can I edit an assessment after creating it?**
Yes, while the assessment is in draft state you can change the name, document source, and category selection. Once the pipeline has started running, the framework and document source are locked for that run.

**Q: How many documents can an assessment handle?**
There is no hard limit. Typical assessments work with 10-100 documents. Very large document sets (500+) may increase processing time but are supported.

**Q: Can I duplicate an existing assessment?**
Not directly from the wizard, but you can create a new assessment with the same framework and document source. The platform does not copy findings or review decisions between assessments.
