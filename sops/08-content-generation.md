---
title: "Generating Content"
sidebarTitle: "Generate Content"
description: "Use AI-assisted content generation to draft remediation text for RED and AMBER findings."
---

## Before you start
- The finding must have a **RED** or **AMBER** rating -- content generation is not available for GREEN findings.
- You need **Reviewer** or **Admin** role on the assessment.
- Familiarise yourself with the finding's evidence gaps first via the Finding Detail view ([SOP 07](/sops/07-finding-detail)).

## Steps

1. **Open content generation.** From a finding's detail view, click **Generate Content**. The content generation workspace loads.
   [screenshot: 12-content-generation.png]

2. **Review the context assembly.** Before generating, the system assembles context from multiple sources:
   - **Finding details** -- the current RAG rating, evidence coverage percentage, and reviewer notes.
   - **Evidence gaps** -- the specific requirements where coverage is missing or insufficient.
   - **Criterion definition** -- the framework's formal description of what good evidence looks like.
   - **Framework terminology** -- the expected language conventions for the framework (e.g. IPA Green Book terms for HMT assessments).

3. **Configure tone and length.** Use the controls to adjust:
   - **Tone** -- formal, balanced, or concise.
   - **Length** -- short paragraph, standard section, or extended narrative.
   These settings influence how the AI drafts the remediation content.

4. **Generate the draft.** Click **Generate**. The AI drafts remediation content using the finding's cited evidence, the criterion definition, and the framework's expected language. Each field in the output shows a per-field confidence score indicating how well-supported the draft is by the source material.

5. **Review the output.** Read through the generated content carefully. The draft is structured to address the evidence gaps identified in the finding. Check that:
   - The language matches the framework's conventions.
   - The claims are supported by the cited evidence.
   - The remediation guidance is actionable.

6. **Choose your next action.** Three options are available:

   | Action | What it does |
   |--------|--------------|
   | **Revise** | Edit the draft directly in the editor. Make targeted changes while keeping the AI's structure. |
   | **Regenerate** | Discard the current draft and generate a fresh version. Useful if the tone or approach is wrong. |
   | **Accept** | Save the content back to the finding. The accepted text becomes part of the finding record. |

7. **Accept and save.** When satisfied, click **Accept**. The generated content is saved against the finding and appears in the finding detail view and in any reports that reference this criterion.

8. **Check generation analytics.** A generation analytics dashboard is available from the content generation workspace. It shows aggregate statistics across the assessment: how many findings have generated content, acceptance rates, and average confidence scores.

## What happens next
- Return to the finding to continue review: [SOP 07 -- Reviewing Findings](/sops/07-finding-detail).
- Continue working through results: [SOP 06 -- Understanding Results](/sops/06-results).
- See the reference diagram: `content-generation-flow.md`.

## Common questions

**Q: Can I generate content for a GREEN finding?**
A: No. Content generation targets remediation -- GREEN findings already have sufficient evidence and do not need remediation drafts.

**Q: Does accepting generated content change the finding's RAG rating?**
A: No. The RAG rating reflects the evidence in the assessed documents. Generated content is a remediation aid, not a substitute for submitting improved evidence. The rating updates only when a new assessment is run against updated documents.

**Q: What does the confidence score mean?**
A: Each field's confidence score (0--100%) indicates how much of the draft is grounded in cited evidence versus inferred by the AI. Higher scores mean stronger source backing. Review low-confidence fields with extra care.
