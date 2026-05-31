---
title: "Administration & Configuration"
sidebarTitle: "Administration"
description: "Configure every aspect of how Programme Insights works for your organisation -- from terminology and scoring schemes to AI prompts and report formats."
---

## Before you start
- You need **Admin** role for all operations described in this guide.
- Some configuration changes (e.g., vocabulary, scoring) affect all assessments in the workspace. Coordinate with your team before making changes.
- Config pack changes do not retroactively alter completed assessment runs. They apply to future runs only.

## Steps

### Admin Hub

1. Click **Admin** in the sidebar to open the Admin Hub -- the central landing page for all configuration areas.
   [screenshot: needed]

2. The Admin Hub provides links to:
   - Config Pack Management
   - Organisation Configuration (6 editors)
   - Organisation Management
   - Pack Endorsement
   - PII Anonymisation

---

### Config Pack Management

3. Navigate to **Admin > Config Packs** to browse available config packs. Config packs define the criteria framework used during assessments (e.g., IPA Gate Review, Green Book, NEC4).
   [screenshot: needed]

4. To create or edit a config pack, open the **Config Pack Builder** at **Admin > Config Packs > Builder**.
   [screenshot: needed]

5. In the Config Pack Builder, define:
   - **Criteria** -- the individual requirements the AI will assess documents against.
   - **Evidence requirements** -- what constitutes sufficient evidence for each criterion.
   - **Categories** -- how criteria are grouped (e.g., "Commercial", "Financial", "Deliverability").
   - **Scoring rubrics** -- what each rating level (Red, Amber, Green) means for each criterion.

6. Save the config pack. It becomes available for selection when creating new assessments (see [Creating an Assessment](/sops/04-creating-assessments)).

### Overlay Customisation

7. To make per-organisation modifications to a standard config pack without forking it, navigate to **Admin > Config Packs > [pack code] > Customise**.
   [screenshot: needed]

8. Overlays let you:
   - **Add criteria** specific to your organisation that are not in the standard pack.
   - **Remove criteria** that are not relevant to your context.
   - **Modify criteria** -- adjust wording, evidence requirements, or scoring for existing criteria.

9. Overlays are applied on top of the base pack. When the base pack is updated, your overlay modifications are preserved.

---

### Organisation Configuration (6 Editors)

All six editors are accessible from **Admin > Organisation > Configuration**.

#### 1. Vocabulary Editor (/vocabulary)

10. Open the **Vocabulary Editor** to override platform terminology for your organisation.
    [screenshot: needed]

11. Common overrides include:
    - "Finding" replaced with "Observation"
    - "Assessment" replaced with "Review"
    - "Initiative" replaced with "Programme Stream"

12. Changes apply across the entire UI for all users in your organisation.

#### 2. Scoring / RAG Editor (/scoring)

13. Open the **Scoring Editor** to customise what Red, Amber, and Green mean for your organisation.
    [screenshot: needed]

14. Define the threshold descriptions, confidence levels, and decision guidance for each rating level.

15. You can also configure additional rating levels beyond the standard three if your organisation uses a different scale.

#### 3. Prompts Editor (/prompts)

16. Open the **Prompts Editor** to view and edit the AI prompt templates used during assessment runs.
    [screenshot: needed]

17. Each prompt template controls how the AI evaluates evidence against a specific type of criterion. Edit prompts to:
    - Adjust the level of detail expected in AI explanations.
    - Add organisation-specific context the AI should consider.
    - Modify the instruction style for different assessment types.

18. Changes to prompts affect all future assessment runs. Test changes on a non-production assessment first.

#### 4. Reports Editor (/reports)

19. Open the **Reports Editor** to configure the output format of generated reports.
    [screenshot: needed]

20. Configure:
    - Which sections appear in the PDF executive report.
    - Section ordering and grouping.
    - Branding elements (logo, colour scheme, header/footer text).
    - Level of detail included per section.

#### 5. Strictness Editor (/strictness)

21. Open the **Strictness Editor** to adjust how conservative or liberal the AI scoring should be.
    [screenshot: needed]

22. Strictness controls the AI's tendency to:
    - Rate findings more conservatively (stricter = more Reds and Ambers).
    - Rate findings more liberally (looser = more Greens).

23. Adjust strictness per criteria category if different areas of your framework require different levels of rigour.

#### 6. Custom Fields Editor (/fields)

24. Open the **Custom Fields Editor** to add user-defined fields (UDFs) for organisation-specific metadata.
    [screenshot: needed]

25. UDFs allow you to capture data the platform does not track by default, such as:
    - Internal reference numbers.
    - Risk tier classifications.
    - Steering group owner.
    - Gate review cycle identifier.

26. Define the field name, type (text, number, date, dropdown), and where it appears (assessment, finding, or action level).

---

### Organisation Management

27. Navigate to **Admin > Organisation** to manage workspace membership and settings.
    [screenshot: needed]

28. From this page you can:
    - Invite new members and assign roles (Viewer, Reviewer, Admin).
    - Remove members or change their roles.
    - Update organisation display name and settings.

---

### Pack Endorsement

29. Navigate to **Admin > Pack Endorsement** to manage named expert endorsements for config packs.
    [screenshot: needed]

30. Endorsements record which domain experts have reviewed and approved a config pack, adding credibility for governance and audit purposes.

---

### PII Anonymisation

31. Navigate to **Admin > PII Anonymisation** to configure redaction of personally identifiable information.
    [screenshot: needed]

32. When enabled, PII (names, email addresses, phone numbers) is automatically redacted from assessment outputs, reports, and exported data.

## What happens next
- Config packs you create or customise become available when creating assessments (see [Creating an Assessment](/sops/04-creating-assessments)).
- Vocabulary and scoring changes take effect immediately across the UI for all workspace users.
- Frameworks configured here are browsable from the frameworks page (see [Frameworks](/sops/03-frameworks-library)).

## Common questions

**Q: If I change the vocabulary, does it affect existing reports and exports?**
A: Vocabulary changes apply to the UI and future exports. Previously generated PDF reports retain the terminology used at the time of generation.

**Q: Can I revert a config pack overlay to the base pack defaults?**
A: Yes. Each overlay modification can be individually removed, restoring the base pack criterion. You can also delete the entire overlay to return to the unmodified base pack.

**Q: What happens if I change strictness mid-programme?**
A: Strictness changes apply to future assessment runs only. Previous runs retain their original ratings. Use version comparison (see [Comparing Assessment Versions](/sops/15-compare-versions)) to see the effect of strictness changes across runs.
