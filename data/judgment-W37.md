# W37 judgment (2026-09-11)

## Summary

- **Decision: no HTML content change** — tool picker stays at 7 constraint rows; no swap earned this week.
- Candidates reviewed (Spark, Tableau, Dagster, Airflow, GX, Evidence, Hex, Snowflake/BigQuery, Iceberg, lakekeeper, omnigraph, mprove): either duplicate an incumbent constraint (volume/consume/warehouse/notebooks/definitions) or are orchestration/quality/novel noise that does not belong on this one-pager.
- Fresh releases on incumbents (dbt, Databricks, MetricFlow, OpenLineage) do not earn a picker swap.
- **Deferred:** orchestration (Dagster/Airflow), quality (Great Expectations), code-BI (Evidence), table formats (Iceberg), novels (lakekeeper/omnigraph/mprove) — watchlist `onCard: false` unchanged.
- Hygiene: restored footer **Changed** from CI placeholder (`Weekly discovery ready…`) to `Verb lede, always-on foundation strip`; bumped stamp to **v2026.37** (CI did not open W37 — discovery is workflow_dispatch only). Link check: 20/20 OK.
- Stack unchanged: ASK → GRAIN → TRUTH → USE; verb lede + Always on strip intact.

## Card preview

Review agent will compare this HTML to live (stamp-only + Changed hygiene; picker unchanged).

## PR status

- Branch pushed: `chore/weekly-refresh-2026-W37` (`b04cb41`).
- **Could not open PR:** cloud token lacks `pull_requests: write`; Automation Tools MCP has no `open_git_pr` this run.
- Compare: https://github.com/AlexTouvras/data-analytics-field-card/compare/main...chore/weekly-refresh-2026-W37?expand=1
- 18:00 review agent: open PR (paste `## Summary` / `## Card preview` from this file) then Apply review, or follow weekly-review-prompt no-PR path.
