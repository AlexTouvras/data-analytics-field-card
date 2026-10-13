# Architecture

Standalone one-page field card. Public artifact is `index.html`. Maintenance notes live in `docs/` and `.state/`.

## Page

The card is a decision scene, not a reference table.

1. Hero: the headline and trust question sit on a scene of streams, a standing figure, and a decision screen (`assets/hero.jpg`). Stage marks are `assets/icon-ask.png`, `icon-grain.png`, `icon-truth.png`, and `icon-use.png`.
2. Four connected layers — ASK, GRAIN, TRUTH, USE — each with a failure mode.
3. Reconciliation gate: two illustrative ECL ratios, a gate, a published result. Always on sits beside it.
4. Ownership cycle: bottleneck, departure, delete, then the exit — build the metric once, with a named owner. An assistant that drafts the metric is not the owner.
5. Credit-risk case walking question, grain, truth, and decision.
6. Bottom row: architecture plates, tool groups, anti-patterns, maturity ladder, then the kill switch.

Accent is ice blue and green on a near-black navy sheet. Amber marks the disagreeing report. Motion is a few sparks on the hero stream; it stops for `prefers-reduced-motion`. Print flattens to a light sheet.

## Automation

Weekly judgment is described in `.state/AUTOMATION_CONTRACT.md` and `docs/weekly-refresh-prompt.md`. Discovery reads tool names out of `index.html`. The version stamp element id is `version-stamp`. The Changed line is `<p class="changed"><b>Changed</b> …`.

Primary verify when HTML or URLs change: `node scripts/check-links.mjs` exits 0.
