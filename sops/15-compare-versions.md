# Comparing Assessment Versions
> View the diff between assessment runs to track what changed -- findings added, findings resolved, rating movements, and reviewer decisions over time.

## Before you start
- The assessment must have been run at least **twice** to have two versions to compare.
- Any workspace member can view version comparisons; no special role is required.
- Each assessment run creates a new version automatically. You do not need to do anything special to enable versioning.

## Steps

1. Open the assessment you want to compare and navigate to **Compare Versions** (accessible from the assessment header or sidebar).
   [screenshot: 18-compare-versions.png]

2. Select the two versions you want to compare using the version selectors. Typically this is the most recent run versus the previous run, but you can compare any two versions.

3. The comparison view shows a structured diff organised into sections:

   - **Findings Added** -- new findings that appeared in the later version but were not present in the earlier one. These may indicate newly identified gaps or newly uploaded documents triggering additional criteria matches.

   - **Findings Resolved** -- findings present in the earlier version that no longer appear. These represent gaps that have been addressed, often as a result of remediation actions.

   - **DCA Movements** -- changes in Delivery Confidence Assessment ratings (e.g., Red to Amber, Amber to Green). Each movement shows the before and after rating with the criteria involved.

   - **Reviewer Decisions** -- human review actions taken between the two versions, showing which findings were accepted, challenged, or re-rated.

4. Use the **diff toggle** to switch between a side-by-side view and an inline view, depending on your preference.

5. Click any finding in the comparison to open its detail page for full context (see [SOP 07 -- Finding Detail](/sops/07-finding-detail)).

### Telling the story of improvement

6. Use version comparison when preparing for gateway reviews or programme board meetings. The diff answers the question: "What has changed since the last assessment?"

7. Track progress over multiple runs by comparing non-adjacent versions (e.g., version 1 vs version 5) to show the full improvement trajectory.

8. Pair version comparison with the summary page (see [SOP 09 -- Summary](/sops/09-summary-page)) to provide both the current state and the change narrative in a single briefing.

## What happens next
- Version comparison data supports the executive summary narrative, showing evidence of continuous improvement.
- If the comparison reveals new findings, investigate them via the results page (see [SOP 06 -- Results & Findings Overview](/sops/06-results)).
- Resolved findings linked to actions demonstrate that remediation work is having the intended effect (see [SOP 13 -- Managing Actions](/sops/13-actions)).

## Common questions

**Q: How many versions does the platform retain?**
A: Every assessment run is retained as a version. There is no automatic pruning. You can compare any two versions regardless of how many runs have occurred.

**Q: Does the comparison show changes to documents as well as findings?**
A: The comparison focuses on findings, ratings, and reviewer decisions. Document-level changes (new uploads, replacements) are reflected indirectly through the findings they produce.

**Q: Can I share a version comparison with someone outside the platform?**
A: Version comparison data feeds into the PDF executive report. Generate a report from the summary page to share externally (see [SOP 09 -- Summary](/sops/09-summary-page)).
