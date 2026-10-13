# Architecture

Standalone one-page field card. Public artifact is `index.html`. Maintenance notes live in `docs/` and `.state/`.

## Page

The card is a decision scene, not a reference table.

1. Headline and the question: can we trust this number enough to act on it?
2. Four chambers — ASK, GRAIN, TRUTH, USE — with one illustrative credit case. Truth shows two measures and a blocked publish.
3. Judgement: three lines, definition vs report, kill switch.
4. Named practices, at most seven, chosen by constraint.
5. Always on: Security, Governance, Observability, Evals, Human Approve.

Accent is ice blue on a near-black navy sheet, with amber only for the unexplained gap. Motion is a particle stream; it stops for `prefers-reduced-motion`. Print flattens to a light sheet and shows every layer.

## Automation

Weekly judgment is described in `.state/AUTOMATION_CONTRACT.md` and `docs/weekly-refresh-prompt.md`. Discovery reads tool names out of `index.html`. The version stamp element id is `version-stamp`. The Changed line is `<p class="changed"><b>Changed</b> …`.

Primary verify when HTML or URLs change: `node scripts/check-links.mjs` exits 0.
