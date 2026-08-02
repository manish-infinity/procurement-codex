# The Procurement Codex — Master Blueprint

*Working document. Version 0.1 — for iteration.*

---

## 1. The one-sentence definition

**The Procurement Codex is a free, interactive, self-publishing reference library that teaches every process in procurement as an ordered system — showing each step first in plain concept, then across every major platform (fair A vs B vs C), then layered up with process mining, intelligence, orchestration, and people, until the learner sees why standalone tools are never enough and value lives in the seams between vendors.**

The thought-leadership outcome is a *byproduct*. We do not chase visibility. We build the single best resource that exists, publish it relentlessly on a schedule, and let it compound into authority. The goal state: when anyone on earth needs to understand a procurement process honestly and completely, this is the thing they open — and your name is on it.

---

## 2. The three structural layers of the whole project

Everything the project ever produces sits on three fixed ideas. Get these right and the rest is execution.

### 2.1 The Spine — the procurement lifecycle, in strict sequence

One ordered backbone. Every episode is a single step on it, published in order. This ordering *is* the differentiation — almost everyone teaches procurement as disconnected topics; we teach it as a system that runs start to finish.

The canonical source-to-pay spine, from its true starting point:

| # | Process step | Also called |
|---|---|---|
| 1 | Intake & need identification | Demand, request-to-buy, intake-to-procure |
| 2 | Spend analysis & category strategy | Spend cube, category management |
| 3 | Sourcing & RFx | RFI/RFP/RFQ, eSourcing, auctions |
| 4 | Supplier evaluation & selection | Bid analysis, scorecards, award |
| 5 | Negotiation | Should-cost, eAuction, award optimization |
| 6 | Contract lifecycle management (CLM) | Authoring, clause library, e-sign, obligations |
| 7 | Supplier onboarding & master data | Vendor master, registration, networks |
| 8 | Requisitioning & guided buying | Catalogs, punchout, guided procurement |
| 9 | Purchase order management | PO issue, change orders, flip |
| 10 | Goods & service receipt | GR, service entry sheets |
| 11 | Invoice management & 3-way match | AP automation, exceptions, tolerances |
| 12 | Payment & working capital | Terms, dynamic discounting, supply-chain finance |
| 13 | Supplier performance & relationship (SPM/SRM) | Scorecards, QBRs, development |
| 14 | Risk, compliance & ESG | Third-party risk, sanctions, sustainability |
| 15 | Spend intelligence & continuous improvement | Analytics, benchmarking, the loop back to #1 |

Twice a week = one full pass in roughly 7–8 weeks. Then the loop restarts as **Pass 2 (composites)** — deep dives into specific multi-vendor stacks for the same steps.

### 2.2 The Layer Stack — the signature reveal

For each spine step, the episode reveals it in stacking layers. The *act of stacking* is the teaching. This is what makes the audience feel they are watching someone who sees the whole board.

| Layer | Name | What it adds |
|---|---|---|
| L0 | **Concept** | What this step fundamentally is, why it exists, what "good" looks like |
| L1 | **Platform-native (A vs B vs C)** | How each major suite does this exact step, side by side, fairly |
| L2 | **Best practice** | Process design, controls, KPIs, common failure modes |
| L3 | **Process mining** | Overlay Celonis / Signavio / open-source PM4Py to expose the real bottleneck |
| L4 | **Intelligence / AI** | Predictive, GenAI copilots, agentic automation on top |
| L5 | **Orchestration** | Intake-to-procure / cross-system workflow that stitches tools together |
| L6 | **People, roles & skills** | RACI, competencies, who actually owns it, org design |
| L7 | **Synergy composite** | The best-of-breed, multi-vendor architecture — the core thesis |

L7 is the recurring punchline of the whole series: **standalone is never enough; the value is in the integration seams.**

### 2.3 The Permutation Matrix — combinatorial, not repetitive

You were right that we must not rebuild everything for every platform. We show a concrete example **once**, then express the rest as a matrix the learner can recombine themselves:

```
Composite = ERP {S/4HANA, Oracle, Workday, D365, NetSuite, Infor}
          × Suite {Ariba, Oracle, Coupa, GEP, Ivalua, Jaggaer, Zycus}
          × Process mining {Celonis, Signavio, PM4Py*, Apromore*, Power Automate}
          × Orchestration {Zip, ORO, Pivot, native}
          × Intelligence/AI {native copilots, Sievo, custom GenAI}
          × Framework {CIPS, category mgmt, Kraljic, SRM maturity}
          × People {CPO office, category mgr, buyer, AP, SRM lead}
   (* = open-source)
```

The web app renders this as an interactive "stack builder": pick one from each column, and the app assembles the composite architecture and its trade-offs. Build the engine once; every future episode plugs into it.

---

## 3. The platform roster (what "everything that exists" means, concretely)

We commit to fairness and completeness across these. Not every one appears in every episode, but the roster is fixed so coverage is honest.

- **Source-to-pay suites:** SAP Ariba, Oracle Fusion Procurement Cloud, Coupa, GEP SMART, Ivalua, Jaggaer, Zycus, Basware (P2P/AP), Tradeshift
- **CLM specialists:** Icertis, SirionLabs, DocuSign CLM, Ironclad
- **ERPs:** SAP S/4HANA, Oracle, Workday, Microsoft Dynamics 365, NetSuite, Infor
- **Intake & orchestration:** Zip, ORO Labs, Pivot, Levelpath
- **Supplier networks:** SAP Business Network, Coupa Supplier Portal, Oracle Supplier Network
- **Process mining:** Celonis, SAP Signavio, Microsoft Power Automate Process Mining, UiPath Process Mining, **Apromore (open source)**, **PM4Py (open source)**
- **Spend analytics / intelligence:** Sievo, native suite analytics, GenAI copilots (e.g., SAP Joule, Coupa AI)
- **Frameworks (vendor-neutral):** CIPS cycle, Kraljic matrix, category management, SRM maturity models, source-to-pay maturity curves

Fairness rule: every comparison uses the same scoring rubric and explicitly states what each platform is *best* and *worst* at. Credibility is the moat — one biased comparison and the authority is gone.

---

## 4. Anatomy of a single episode (the web app)

Every episode is one self-contained interactive page on the site. Fixed template so production is repeatable and the brand is unmistakable:

1. **Hook & placement** — where this step sits on the spine (animated spine with the current node lit)
2. **L0 Concept** — short, sharp explainer + the "what good looks like" bar
3. **A vs B vs C comparison** — interactive table with the shared rubric; toggle platforms; expand any cell
4. **Guided simulation** — a click-through of the actual process on 2–3 platforms (the "guided buying on SAP vs Oracle vs Coupa" style walk-through)
5. **Layer peeler** — a control that stacks L3→L7 onto the base process, visibly changing the architecture diagram (Mermaid) and the outcome metrics
6. **Stack builder** — the permutation matrix as an interactive picker
7. **Cheat sheet** — a dense, printable one-screen summary (downloadable)
8. **Gamified check** — a short scenario quiz ("your PO cycle time is 14 days, which layer fixes it fastest?") with scoring
9. **Cite & share** — canonical link, so it becomes referenceable

Every episode ends with the same structural payoff: *here is the plain thing; here is what it becomes when the layers and vendors combine.*

---

## 5. Visual & gamification system

- **Signature identity:** consistent color-coded layers (L0–L7 each own a color), a persistent spine navigator, one typographic system. Recognizable at a glance in a LinkedIn feed.
- **Gamification:** per-episode scenario quizzes, a "Codex completion" progress meter across the whole spine, unlockable "composite architect" badges as learners complete stack-builder challenges. All client-side, no accounts, no tracking needed for v1.
- **Accessibility & speed:** static site, works on mobile, loads instantly, no login wall. Friction kills reference tools.

---

## 6. Technology stack — 100% free / open source

| Concern | Choice | License / cost |
|---|---|---|
| Repo & hosting | GitHub + **GitHub Pages** | Free |
| Automation & schedule | **GitHub Actions** (cron) | Free tier |
| Site generator | **Astro** (islands for interactivity) | MIT / free |
| Interactivity | **Alpine.js** + vanilla JS | MIT / free |
| Styling | **Tailwind CSS** | MIT / free |
| Diagrams | **Mermaid.js** | MIT / free |
| Charts | **Chart.js** | MIT / free |
| Process-mining demos | **PM4Py**, **Apromore Community** | Open source |
| Content authoring | Markdown / MDX | Free |
| Publishing to LinkedIn | Browser automation of your logged-in session | Free |

No paid dependency anywhere in the pipeline. If we later need more (a new library, a diagram engine, an IDE), we add only free/open-source components.

---

## 7. The autonomous publishing pipeline

Runs twice a week as a scheduled task (proposed: **Tuesday & Friday, 9:00 AM your time**). One run = one episode.

```
1. GENERATE   Draft the next spine step's content (concept, comparison, layers,
              cheat sheet, quiz) from the fixed episode template.
2. BUILD      Commit MD/MDX + assets to the GitHub repo; Astro builds the page.
3. DEPLOY     GitHub Actions publishes to GitHub Pages → live canonical URL.
4. SELF-CHECK ► GATE: automated checks must pass before anything is posted —
              - every comparison cell filled (no TODO/empty)
              - page returns HTTP 200 and renders
              - links valid, no broken Mermaid/diagram
              - cheat sheet present
              If any check fails: HALT, do not post, notify you instead.
5. PUBLISH    Post to LinkedIn via your logged-in browser: short authoritative
              caption + link to the live episode. (Web-app-first: the post drives
              traffic to the interactive page, it is not the deliverable itself.)
6. LOG        Append to a public changelog / episode index on the site.
```

The **self-check gate** in step 4 is the guardrail we keep even under full autonomy — it means the worst case is a *skipped* post, never a *broken* one under your name.

**Note on prerequisites (to set up before first autonomous run):** a GitHub repo I can push to, and a confirmed logged-in LinkedIn browser session I can drive on schedule. LinkedIn has no friction-free free API for automated personal posting, so the browser path is deliberate.

---

## 8. Episode roadmap

**Pass 1 — the vanilla spine + native platform comparison (≈8 weeks, twice weekly)**

| Wk | Tue | Fri |
|---|---|---|
| 1 | Ep01 Intake & need | Ep02 Spend analysis & category strategy |
| 2 | Ep03 Sourcing & RFx | Ep04 Supplier evaluation & selection |
| 3 | Ep05 Negotiation | Ep06 Contract lifecycle management |
| 4 | Ep07 Supplier onboarding & master data | Ep08 Requisitioning & guided buying |
| 5 | Ep09 Purchase order management | Ep10 Goods & service receipt |
| 6 | Ep11 Invoice & 3-way match | Ep12 Payment & working capital |
| 7 | Ep13 Supplier performance (SPM/SRM) | Ep14 Risk, compliance & ESG |
| 8 | Ep15 Spend intelligence & the loop | Ep16 Season 1 capstone: the full spine as one system |

**Pass 2 — composites (open-ended):** for each step, a deep dive into a specific real-world multi-vendor stack (e.g., "Sourcing composite: Ariba + Celonis + Zip + S/4HANA — where the seams leak and how to seal them"). This is where the L7 thesis gets proven repeatedly, and where the series can run indefinitely.

**Episode 1 is Intake & need** — the true beginning, per the ordered-system narrative.

---

## 9. Why this wins (the recipe for success)

1. **Ordered system, not scattered tips** — nobody else teaches the whole spine in sequence.
2. **Radical fairness** — same rubric for every vendor, explicit best/worst. Credibility compounds.
3. **Genuinely useful free tools** — interactive simulators people *use*, not posts they scroll past.
4. **The synergy thesis** — a repeatable, defensible point of view (standalone ≠ enough) that becomes associated with your name.
5. **Relentless consistency** — twice a week, autonomous, for months. Cadence is what builds authority.
6. **A compounding library** — every episode makes the whole Codex more complete and more citable. By month three it's a reference; by month six it's *the* reference.

---

## 10. Open items before we build

- Confirm the GitHub repo (existing or new) and that I have push access.
- Confirm the LinkedIn logged-in browser session I'll drive.
- Confirm cadence days/time (proposed Tue & Fri, 9:00 AM).
- Confirm generator choice (Astro recommended) — or defer to me.
- Then: I scaffold the repo, build the Episode 1 template end-to-end as the reference implementation, and we review before switching the schedule on.

*End of v0.1 — bring your edits and we iterate.*
