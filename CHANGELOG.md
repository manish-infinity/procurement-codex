# The Procurement Codex — Method Validation Changelog

A running record of the core-logic improvements made on each autonomous run. Fairness and accuracy compound with every pass. Corrections welcome via PR.

## 2026-08-03 — Episode 02 (Spend Analysis & Category Strategy)

Published `episodes/ep02-spend-analysis-and-category-strategy.html`.

**Rubric refinement:** Added an explicit *Data enrichment* scoring criterion to the L1 comparison. Episode 01's intake rubric had no enrichment axis, but enrichment quality (external data, supplier parent-child normalization, price references) is a primary differentiator for spend analytics — so it now scores on its own 1–5 axis.

**Roster expansion:** Extended the platform set for analytics-heavy steps to include **Sievo** (best-of-breed spend analytics) and **Zycus** (Merlin AI auto-classification), scored on the same shared rubric as the S2P suites, each with an explicit *best* AND *watch-out*.

**Stack Builder:** Confirmed the permutation engine is step-agnostic; adapted its columns to the spend/category context (ERP/AP, Spend Analytics, Taxonomy, Process Mining, AI, Ownership) while reusing the same `summary()` / `seamNote()` logic that powers every episode.

**Fix:** Corrected an HTML-entity artifact in the L6 layer title so it renders "People & roles" cleanly.

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.
