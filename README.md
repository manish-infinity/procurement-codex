# The Procurement Codex

A free, interactive, self-publishing reference library that teaches every process in procurement as an ordered system. Each episode covers one step of the source-to-pay spine — first in plain concept, then across every major platform (fair A vs B vs C), then layered up with process mining, intelligence, orchestration and people, until it's clear why standalone tools are never enough.

**Live site:** `https://<username>.github.io/procurement-codex/` *(after first deploy)*
**Cadence:** two episodes per week (Tue & Fri), published autonomously.
**Cost:** $0 — every dependency is free/open source.

---

## Repo structure

```
procurement-codex/
├─ README.md
├─ package.json                 # Astro + Tailwind (all MIT)
├─ astro.config.mjs
├─ .github/
│  └─ workflows/
│     ├─ deploy.yml             # build + deploy to GitHub Pages on push
│     └─ publish-episode.yml    # cron (Tue/Fri) → build → self-check gate → LinkedIn
├─ src/
│  ├─ layouts/
│  │  └─ Episode.astro          # the fixed episode template (spine, layers, quiz…)
│  ├─ components/
│  │  ├─ SpineNav.astro
│  │  ├─ ComparisonTable.astro  # shared rubric engine
│  │  ├─ LayerPeeler.astro
│  │  ├─ StackBuilder.astro     # the permutation-matrix engine (build once)
│  │  ├─ CheatSheet.astro
│  │  └─ ScenarioQuiz.astro
│  ├─ data/
│  │  ├─ spine.json             # the 15 ordered steps
│  │  ├─ platforms.json         # the vendor roster + rubric scores
│  │  └─ episodes/
│  │     └─ ep01-intake.json    # per-episode content (concept, scores, layers, quiz)
│  └─ pages/
│     ├─ index.astro            # the Codex home / progress meter
│     └─ episodes/[slug].astro  # renders any episode from its JSON
├─ public/
│  └─ og/                       # social share images per episode
└─ scripts/
   ├─ generate-episode.mjs      # scaffolds the next spine step's JSON
   └─ self-check.mjs            # the publish gate (see below)
```

**Design intent:** content lives in JSON, the template and engines (comparison, layer peeler, stack builder) are built **once**. Producing a new episode = filling one JSON file. The single-file `ep01-intake-and-need.html` in this drop is the *reference implementation* — the proof the template works before we split it into components.

---

## The self-check gate (the one guardrail under full autonomy)

`scripts/self-check.mjs` runs after build, before any LinkedIn post. The post is blocked unless **all** pass:

- every comparison cell is filled (no empty / TODO)
- the page returns HTTP 200 and renders without JS errors
- all internal + external links resolve
- Mermaid / diagrams parse
- the cheat sheet and quiz are present and non-empty

On failure: **halt, do not post, notify Manish.** Worst case is a skipped episode — never a broken one under your name.

---

## Publishing pipeline (twice weekly)

1. **Generate** next spine step's JSON from the template
2. **Build** with Astro → static site
3. **Deploy** to GitHub Pages (canonical URL)
4. **Self-check gate** (above)
5. **Publish** to LinkedIn via the logged-in browser session: authoritative caption + link to the live episode
6. **Log** to the public episode index / progress meter

---

## Tech stack (all free / open source)

Astro · Tailwind CSS · Alpine.js · Mermaid.js · Chart.js · PM4Py / Apromore (process-mining demos) · GitHub Pages (hosting) · GitHub Actions (CI + cron).

---

## Roadmap — Season 1 (the spine)

| Ep | Step | Ep | Step |
|----|------|----|------|
| 01 | Intake & Need ✅ (reference build) | 09 | PO Management |
| 02 | Spend Analysis & Category Strategy | 10 | Goods & Service Receipt |
| 03 | Sourcing & RFx | 11 | Invoice & 3-way Match |
| 04 | Supplier Evaluation & Selection | 12 | Payment & Working Capital |
| 05 | Negotiation | 13 | Supplier Performance (SPM/SRM) |
| 06 | Contract Lifecycle (CLM) | 14 | Risk, Compliance & ESG |
| 07 | Supplier Onboarding & Master Data | 15 | Spend Intelligence & the Loop |
| 08 | Requisition & Guided Buying | 16 | Season 1 capstone: the full spine |

**Season 2 (composites):** for each step, a deep dive into a specific multi-vendor stack — proving the "value is in the seams" thesis repeatedly.

---

*Corrections welcome — fairness across vendors is the entire credibility model. Open a PR.*
