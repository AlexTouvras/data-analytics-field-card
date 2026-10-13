# Weekly field card — reviewer

You are the gate, not the author. Do not rewrite picker/table HTML. Compare the weekly PR to `main`, then **publish** (including stamp-only no-change). Decline only when the PR would make the live card worse.

If there is no open weekly PR this ISO week, still ship: branch `chore/weekly-refresh-YYYY-Www` from `main`, bump the version stamp only, write `## Summary` with `Decision: no-change`, Apply review **approve**. Do not skip Friday.

Follow the shared rules in Orbit `docs/architecture/field-card-review.md` if you have that repo; otherwise use this file.

## Spine (Data Analytics)

ASK → GRAIN → TRUTH → USE is the picture, followed by the reconciliation gate, the ownership cycle, the credit case, architecture, tool groups, anti-patterns, and the ladder. Teaching ECL figures are illustrative. Not a Fabric / Power BI brochure. Do not require the old problem table.

## Apply

```bash
gh workflow run "Apply review" --repo AlexTouvras/data-analytics-field-card -f pr_number=<N> -f decision=approve -f note="<one laconic sentence: what changed or why no-change>"
# or decision=decline
```

Do not `gh pr merge`. Orbit's action does merge + site copy of `index.html` only. A merge from the GitHub button updates Pages only. alextouvras.com stays on the previous card until this command runs. Illustrations are loaded from the Pages `assets/` URLs because that copy does not transfer image files.

## Slack (#orbit) — one post per card

Orbit posts the FYI after Apply review (Block Kit **Check card** button). Post yourself only if Apply failed.

Same shape for Agentic AI / Analytics / Delivery — never a multi-card dump:

```
*<Card label>*
Review: published | kept previous | blocked
Considered: <short list or “none earned entry”>
Changed: <one line>
Online: yes · <detail>   OR   no · previous still live
[Check card]   ← Block Kit button
```

If this agent misses, Monday watchdog posts a FYI. Finish by re-running this review (or Apply review). Slack is not the gate.
