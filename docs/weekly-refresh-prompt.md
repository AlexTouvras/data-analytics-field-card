# Weekly Data Analytics field card — Cursor Automation

Each Friday the automation **judges whether the public card should change**, applies updates when earned, and leaves the weekly PR open. A separate **review** agent publishes or keeps the previous card. Do not assume CI left ready-to-merge HTML on main.

Discovery alone is not enough. Every run must end with an explicit **update** or **no HTML change** decision.

## Slack

Do **not** post Approve links from this run. The review agent is the gate. If that agent misses, Monday watchdog posts a FYI in #orbit — finish by re-running the 18:00 review (or `Apply review`), not Slack Approve.

## Scope (keep this card honest)

This is **not** a Power BI / Fabric product card. The stable spine is:

- **ASK → GRAIN → TRUTH → USE** as the picture (four chambers), not a problem table
- Verb line under the H1 (`Ask → name → define → consume`) — do not drop
- The question the card answers: can we trust this number enough to act on it?
- One illustrative credit case walking those four layers. The reconciliation diagram uses teaching figures, not a portfolio result. A disagreement blocks publish.
- **Always on** beside the gate (Security, Governance, Observability, Evals, Human Approve) — not picker items
- Architecture, tool groups, anti-patterns, and the maturity ladder
- Named practices grouped by constraint. A new brand is an example inside a group, not a new layer.
- Hero and stage images use the GitHub Pages `assets/` URLs. The site copy transfers `index.html` only, so relative `assets/` paths do not show on alextouvras.com.

Churn zone: practice links, concrete nouns in the case, doc URLs, version stamp. Do **not** restore the old problem table. Do **not** redesign the four layers for a renamed vendor feature.

## Steps

1. Check out `AlexTouvras/data-analytics-field-card`. Prefer open branch `chore/weekly-refresh-YYYY-Www` for this ISO week; otherwise create/update it from `main`.
2. Run `npm run discover` (GitHub access via `gh` in the Cloud Agent). Read `data/discovery-report.md` and the current `index.html`.
3. **Decide (required):**
   - **Update card** if a practice swap, docs URL fix, or new *job* in the case is earned.
   - **No HTML change** if candidates are noise, picker is full with better incumbents, or nothing new belongs on a one-pager.
   - Write the decision in the PR `## Summary` either way. Never skip this step.
4. If updating `index.html`:
   - Named practices ≤ 7; swap by constraint (transforms, local-sql, volume, consume, definitions, lineage, orchestration…) — not hype or star count alone.
   - Do not invent docs URLs; use discovery report, watchlist, or existing card links.
   - A new *job* changes the case or a chamber’s failure, not the four layer names (new brand ≠ new layer).
   - Keep practice labels short; nuance in the case.
   - No editor notes on the public HTML.
   - Prefer broad analytics language (SQL, Python, metrics, grain, lineage). Avoid making Fabric/Power BI the whole card.
   - Update the footer **Changed** line; bump version with `npm run bump:version` when the card content changed.
5. If **no HTML change**: leave the chambers and named practices alone. Keep the weekly stamp CI (or you) already bumped. Stamp-only still ships — the review agent **approves** it. Still commit discovery artifacts if you re-ran discover on this branch.
6. Run `node scripts/check-links.mjs` and fix failures on any URLs you touched.
7. Update `data/watchlist.json` for tools you confirm for ongoing tracking (`onCard` true/false).
8. Commit and push to the weekly PR. Do not merge. Do not force-push `main`.
9. Rewrite the PR body to include at least:
   - `## Summary` — 3–6 bullets: what changed on the card **or** why nothing changed; what was deferred.
   - `## Card preview` — one line: the review agent will compare this HTML to live.
10. Stop. Do not notify Slack. Do not merge. The Friday 18:00 review agent publishes (including stamp-only). It declines only when the PR would make the live card worse.

## Done when

- Discovery ran this session
- Explicit update **or** no-change decision is in `## Summary`
- Link check exits 0 (if HTML or links changed)
- PR left open for the review agent
