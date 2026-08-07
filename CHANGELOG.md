# The Procurement Codex — Method Validation Changelog

A running record of the core-logic improvements made on each autonomous run. Fairness and accuracy compound with every pass. Corrections welcome via PR.

## 2026-08-07 — Episode 04 (Supplier Evaluation & Selection)

Published `episodes/ep04-supplier-evaluation-and-selection.html`.

**Rubric refinement (the core-logic improvement this cycle):** Introduced an explicit *Due-diligence / risk fit* scoring criterion to the L1 comparison for the selection step, alongside weighted-scorecard flexibility, consensus/committee scoring, TCO/should-cost, award-scenario optimization and auditability. Prior episodes scored sourcing platforms only on how well they *run an event and score a proposal* — but selection is not only proposal scoring. Whether the winning supplier is financially solvent, ESG-compliant and low-risk is a distinct capability, and full suites diverge sharply on it (e.g. Ariba SLP/Risk and Ivalua Supplier 360 fold risk into the decision, while award-optimization specialists deliberately do not). It now scores on its own 1–5 axis, so the comparison stays honest for the decision step rather than rewarding raw scoring throughput.

**Layer-model tightening:** Promoted external risk/ESG intelligence to a first-class part of the L4 (Intelligence/AI) layer and the L7 composite — EcoVadis (ESG) and Dun & Bradstreet (financial health) now appear explicitly as a *due-diligence overlay* that qualifies finalists before award. This sharpens the recurring thesis for this step: a single evaluation suite can score proposals but cannot itself judge supplier viability or solve a constrained multi-lot award, so the value is in the seams between the suite, external DD/ESG data and a dedicated award optimizer.

**Roster consistency:** SAP Ariba, Coupa, Jaggaer, Ivalua, GEP SMART, Zycus and Keelvar are all scored on the same six axes, each with an explicit *best* AND *watch-out*; Keelvar is scored fairly high on award optimization and low on due-diligence to reflect that it is an optimization specialist, not a full evaluation/DD suite.

**Method note (carried forward):** Applied the standing entity-rendering rule from Ep03 — raw characters ("and" / "&") inside Alpine `x-text` JS-bound strings, HTML entities reserved for literal body markup and `<pre class="mermaid">` content (verified: the "D&amp;B" node renders as "D&B" on the live page).

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.

## 2026-08-04 — Episode 03 (Sourcing & RFx)

Published `episodes/ep03-sourcing-and-rfx.html`.

**Rubric refinement:** Introduced an explicit *Award optimization* scoring criterion to the L1 comparison for the sourcing step. Generic S2P scorecards collapse "sourcing" into a single column, but the ability to solve constrained, multi-lot award scenarios (volume tiers, lot splits, capacity limits) is a distinct capability where full suites and specialists diverge sharply — so it now scores on its own 1–5 axis, alongside RFx design flexibility, e-auction, supplier discovery, bid analysis and cycle time.

**Roster expansion:** Added **Keelvar** (autonomous sourcing bots + best-in-class award optimization) to the platform set, scored on the same shared rubric as the S2P suites, with an explicit *best* AND *watch-out* (optimization/auction specialist, not a full S2P suite). This keeps the comparison honest for complex direct and logistics categories, where a suite alone typically underperforms a dedicated optimizer. Ariba, Coupa, Jaggaer, Ivalua, GEP SMART and Zycus iSource are all scored on the same axes.

**Method fix (carries forward to all episodes):** Fixed an entity-rendering bug — literal HTML entities (e.g. `&amp;`) placed inside Alpine `x-text` JavaScript strings render verbatim, because `x-text` sets `textContent` and performs no entity decoding. Corrected the affected strings (Ivalua "best at" cell and the Stack Builder summary) to plain text, and adopted a standing rule: use raw characters ("and" / "&") inside JS-bound strings, and reserve HTML entities for literal HTML body markup only. Entities inside `<pre class="mermaid">` remain correct, since that content is HTML-parsed before Mermaid renders it.

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.

## 2026-08-03 — Episode 02 (Spend Analysis & Category Strategy)

Published `episodes/ep02-spend-analysis-and-category-strategy.html`.

**Rubric refinement:** Added an explicit *Data enrichment* scoring criterion to the L1 comparison. Episode 01's intake rubric had no enrichment axis, but enrichment quality (external data, supplier parent-child normalization, price references) is a primary differentiator for spend analytics — so it now scores on its own 1–5 axis.

**Roster expansion:** Extended the platform set for analytics-heavy steps to include **Sievo** (best-of-breed spend analytics) and **Zycus** (Merlin AI auto-classification), scored on the same shared rubric as the S2P suites, each with an explicit *best* AND *watch-out*.

**Stack Builder:** Confirmed the permutation engine is step-agnostic; adapted its columns to the spend/category context (ERP/AP, Spend Analytics, Taxonomy, Process Mining, AI, Ownership) while reusing the same `summary()` / `seamNote()` logic that powers every episode.

**Fix:** Corrected an HTML-entity artifact in the L6 layer title so it renders "People & roles" cleanly.

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.
