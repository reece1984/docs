---
title: "Browsing the Frameworks Library"
description: "Explore available criteria frameworks, drill into individual criteria, and understand how frameworks drive assessments."
---

## Before you start
- You are logged in to Programme Insights (see [SOP 00](/sops/00-getting-started)).
- You have at least Viewer permissions on the workspace.

## What is a framework?

A **framework** is a structured criteria template that the platform assesses your documents against. Each framework contains categories, and each category contains individual criteria -- the specific questions or requirements the AI evaluates. Frameworks represent established assurance standards, governance checklists, or bespoke evaluation schemes.

Programme Insights ships with **23 pre-built config packs** covering major UK infrastructure and government standards.

## Steps

### Browsing the library

1. Click **Frameworks** in the sidebar to open the frameworks library.

[screenshot: 04-frameworks-library.png]

2. The library lists all available frameworks grouped by category. Common categories include:

   | Category | Example frameworks |
   |----------|--------------------|
   | **IPA Gateway** | Gateway 0 (Strategic Assessment), Gateway 1 (Business Justification), Gateway 2 (Delivery Strategy), Gateway 3 (Investment Decision), Gateway 4 (Readiness for Service), Gateway 5 (Operations Review) |
   | **Green Book** | HM Treasury Green Book Appraisal |
   | **NEC** | NEC4 Contract Compliance |
   | **CDM** | Construction Design & Management Regulations |
   | **Nuclear** | Nuclear Baseline, ONR Licence Conditions |
   | **Social Value** | Social Value Act, TOMs Framework |

3. Use the search bar or category filters to narrow the list.

### Drilling into a framework

4. Click any framework name to open its full-page criteria browser at `/frameworks/:slug`.

[screenshot: 06-framework-configuration.png]

5. The criteria browser shows:
   - **Framework overview** -- description, source standard, total criteria count.
   - **Categories** -- the top-level groupings within the framework.
   - **Individual criteria** -- click any category to expand and see each criterion with its reference code, title, and description.

6. You can drill down to read the full text of any individual criterion. This is the exact wording the AI will evaluate your documents against.

### Admin configuration

7. Users with Admin permissions can:
   - Edit framework metadata (name, description).
   - Enable or disable individual categories within a framework.
   - Adjust scoring parameters via config packs.
   - Import custom frameworks.

8. Config packs define the module-level settings for each framework, including which categories are active, scoring weights, and assessment preferences. There are 23 pre-built config packs that can be used as-is or customised.

## What happens next
- Use a framework to create an assessment: [SOP 04 -- Creating a New Assessment](/sops/04-creating-assessments)
- Manage framework configuration as an admin: SOP 16 -- Admin Hub (forthcoming)

## Common questions

**Q: Can I create a completely custom framework?**
Yes, if you have Admin permissions. You can define categories and criteria from scratch, or import them from a structured template.

**Q: What happens if a framework is updated after I have run an assessment?**
Existing assessments are not affected. They retain the framework version that was active when the assessment was created. New assessments will use the updated framework.

**Q: Can I combine criteria from multiple frameworks into one assessment?**
No. Each assessment uses exactly one framework. If you need to assess against multiple frameworks, create one assessment per framework against the same document set.
