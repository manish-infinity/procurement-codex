# The Procurement Codex — Method Validation Changelog

A running record of the core-logic improvements made on each autonomous run. Fairness and accuracy compound with every pass. Corrections welcome via PR.

## 2026-08-19 — Episode 07 (Supplier Onboarding & Master Data)

Published `episodes/ep07-supplier-onboarding-and-master-data.html`.

**Rubric refinement (the core-logic improvement this cycle):** Re-based the L1 comparison onto onboarding/master-data-specific axes — self-service registration, data validation & enrichment, master data governance & dedup, workflow & approvals, risk/compliance screening, and integration & orchestration. Crucially, *master data governance & dedup* and *risk/compliance screening* are now scored as their own 1–5 dimensions rather than folded into a generic "integration" or "AI" column. This is the honest way to compare this step: the biggest onboarding failures — duplicate vendors, unverified/fraudulent bank details, unscreened sanctioned parties, ownerless records — are governance and screening failures, not registration-UX failures. Isolating them keeps registration-first suites from scoring high on capabilities they do not truly own.

**Roster expansion:** Added a dedicated, vendor-neutral **supplier master data management (MDM)** layer and a **data-integrity/fraud-controls** specialist to the platform set — **HICX** (vendor-neutral supplier MDM: golden record, dedup and sync across many ERPs/P2P suites), **SAP MDG-S** (authoritative supplier master governance inside SAP), and **Apex Analytix** (bank-account validation, OFAC/fraud screening, duplicate/overpayment prevention) — scored on the same six axes alongside SAP Ariba SLP, Ivalua Supplier 360, Coupa Supplier Management, GEP SMART, Jaggaer and Oracle Supplier Management, each with an explicit *best* AND *watch-out*. Prior rosters had no MDM layer or data-integrity specialist at all, which structurally understated where onboarding value and risk actually live; HICX and MDG-S deliberately score low on supplier-facing registration UX and high on governance/dedup, while suite portals score the reverse — reinforcing that no one tool does it all.

**Layer-model tightening:** Promoted external validation & enrichment (Dun & Bradstreet, Apex Analytix) and the supplier MDM golden record to first-class parts of the L4 (Intelligence/AI) layer and the L7 composite, and framed *segregation of duties on bank-detail changes* as the key L2/L6 control against payment-diversion fraud (the single most expensive, most common onboarding failure). This sharpens the recurring thesis for this step: no single tool registers, validates every bank account, fuzzy-matches to kill duplicates, governs the golden record AND syncs it across a heterogeneous ERP estate — the value is in the seams between a self-service portal, external validation, a supplier MDM layer, fraud/sanctions screening and ERP/P2P sync.

**Method note (carried forward):** Applied the standing entity-rendering rule from Ep03/Ep04/Ep06 — raw characters ("and" / "&") inside Alpine `x-text` JS-bound strings, HTML entities (`&amp;`) reserved for literal body markup, and plain words (e.g. "D and B") inside `<pre class="mermaid">` node labels to avoid Mermaid parse issues. Verified on the live GitHub Pages URL that the L1 table, Layer Peeler metrics, L7 Mermaid diagram, Stack Builder and Scenario Check all render correctly before posting.

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.

## 2026-08-18 — Episode 06 (Contract Lifecycle Management / CLM)

Published `episodes/ep06-contract-lifecycle-management.html`.

**Rubric refinement (the core-logic improvement this cycle):** Introduced an explicit *Obligation & milestone management* scoring criterion to the L1 comparison for the CLM step, and re-based the whole rubric onto CLM-specific axes: authoring & clause library, redlining & collaboration, repository & AI search, obligation & milestone management, risk/compliance analytics, and integration & orchestration. Earlier steps had no axis that isolated *post-signature* management — obligations, milestones, renewals — even though that is precisely where most contract value leaks (missed rebates, silent auto-renewals, unclaimed service credits). Scoring it on its own 1–5 dimension keeps the comparison honest: obligation-first platforms (Icertis, Sirion, Agiloft) now score high on the capability that actually protects value, while authoring/e-signature-first tools (Ironclad, DocuSign CLM) sit honestly lower on it despite strong authoring UX — and S2P-native contract modules (SAP Ariba Contracts, Coupa CLM) score high only on integration, not on standalone CLM depth.

**Roster expansion:** Added dedicated CLM specialists to the platform set — **Icertis**, **Sirion**, **DocuSign CLM**, **Ironclad**, **SAP Ariba Contracts**, **Coupa CLM(S)**, **Ivalua**, **Conga CLM** and **Agiloft** — each scored on the same six axes with an explicit *best* AND *watch-out*. Conga CLM and Agiloft were added specifically because the base roster under-represented the no-code/configurable and Salesforce-native segments; including them prevents the comparison from implying that enterprise obligation suites are the only credible option.

**Layer-model tightening:** Made AI *clause + obligation extraction* a first-class part of the L4 layer and the L7 composite (Sirion, Icertis DiscoverAI), framed as the mechanism that turns a large legacy-contract back-catalogue into a searchable, risk-scored asset. This sharpens the recurring thesis for this step: no single tool authors, digitises legacy paper, tracks every obligation AND closes the loop to buying — so the value is in the seams between authoring, e-signature, extraction, an obligation engine and P2P/ERP integration.

**Method note (carried forward):** Applied the standing entity-rendering rule from Ep03/Ep04 — raw characters ("and" / "&") inside Alpine `x-text` JS-bound strings, HTML entities (`&amp;`) reserved for literal body markup and `<pre class="mermaid">` content. Verified on the live page that the L1 table, Layer Peeler metrics, L7 Mermaid diagram, Stack Builder and Scenario Check all render correctly before posting.

*Method note:* Scores remain directional teaching aids based on typical deployments, not vendor benchmarks. No paid placements or endorsements.

## 2026-08-11 — Episode 05 (Negotiation)

Published `episodes/ep05-negotiation.html`.

**Rubric refinement (the core-logic improvement this cycle):** Added **Pactum** to the platform roster and introduced an explicit *AI / autonomous negotiation* scoring criterion to the L1 comparison for the negotiation step, alongside auction-event breadth, expressive/optimization bidding, should-cost modeling, non-price terms & value, and auditability. Prior rubrics had no column that isolated autonomous negotiation — it was implicitly folded into generic "AI" or omitted — which understated both tail-automation specialists (Pactum) and optimization / auction-bot specialists (Keelvar), while overstating full suites on a capability they do not truly own. Scoring autonomous long-tail negotiation as its own dimension keeps the comparison fair: the full suites (Ariba, Coupa, Jaggaer, Ivalua, GEP) now sit honestly mid-pack on it, specialists score high on their niche and low where they are not full negotiation/terms suites, and the L7 "value is in the seams" thesis is reinforced — no single tool models should-cost, optimizes a constrained multi-lot award, and negotiates thousands of tail deals.

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
