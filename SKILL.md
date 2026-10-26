---
name: bottleneck-stock-scanner
description: Build diversified, research-only public-equity bottleneck reports with one company per supply-chain theme, and classify every stock's bottleneck thesis as either Probably Temporary or Potentially Hard to Scale. Use for bottleneck stock scans, one-theme-per-stock watchlists, supply-chain chokepoint research, bottleneck durability checks, or requests to distinguish a short-lived shortage from a structurally difficult-to-scale constraint.
---

# Bottleneck Stock Scanner V2.1

V2.1 keeps the V2 seven-test framework and the conservative five-condition rule unchanged. It adds run-to-run traceability (changes since last scan), borderline-score disclosure, aggregate thematic exposure, archived evidence packets, and sensitivity notes.

Produce a diversified public-equity research report that starts with demand, maps the full supply chain, identifies the binding constraint, and determines whether the selected company controls a temporary shortage or a potentially durable chokepoint.

Keep one stock per theme. Do not turn one popular trade into several nominally different themes.

Place this disclaimer prominently near the beginning of every report:

> Important: This report is for research and education only. It is not financial advice, not a recommendation to buy or sell securities, and does not consider personal risk tolerance, time horizon, tax situation, or portfolio. Small-cap and thematic stocks can be extremely volatile.

Do not provide buy or sell recommendations, price targets, entry prices, or position sizes.

## Load the durability framework

Read [references/durability-classification.md](references/durability-classification.md) completely before researching or classifying candidates. Apply its definitions, three-clock model, seven tests, evidence standards, and conservative decision rule to every stock.

## Set the scope

Use the user's requested scope. If material choices are missing and clarification is necessary, ask no more than three short questions covering candidate count, geography, theme exclusions, or risk preference.

Otherwise use these defaults:

- Candidates: 10
- Market: U.S.-listed securities, including ADRs when appropriate
- Themes: AI infrastructure, semiconductor manufacturing or packaging, grid and power, critical minerals, energy storage, cybersecurity, defense autonomy, healthcare infrastructure or nuclear medicine, plus other distinct themes that clear the evidence bar
- Risk mix: combine established incumbents with a limited number of higher-risk asymmetric candidates
- Research date: today's actual date

## Apply the candidate methodology

Apply every step to every candidate:

1. **Name the demand wave.** Identify the end-market driver and the measurable demand unit.
2. **Map the supply chain.** Trace the necessary inputs, equipment, services, infrastructure, approvals, and customer qualification steps.
3. **Locate the binding constraint.** Identify the layer with the lowest realistic qualified-output ceiling rather than the layer receiving the most publicity.
4. **Connect the company.** Explain whether the company controls, solves, supplies, or merely depends on the bottleneck.
5. **Classify durability.** Assign exactly one required durability indicator using the reference framework:
   - `Probably Temporary`
   - `Potentially Hard to Scale`
6. **State confidence.** Assign `Low`, `Medium`, or `High` confidence and explain the largest uncertainty.
7. **Validate current demand and company exposure.** Cite recent orders, backlog conversion, approvals, customer agreements, utilization, pricing, capacity, filings, or comparable evidence.
8. **Apply the risk penalty.** Downgrade for balance-sheet weakness, valuation risk, customer concentration, regulation, execution delays, cyclicality, dilution, or geopolitical exposure. Assign `Low`, `Medium`, `Medium-High`, `High`, or `Very High` risk.

Do not equate a hard industry problem with a strong company moat. Require evidence that the selected company can capture economic value from the constraint.

## Enforce the durability indicator

Display the indicator for every stock in the summary table and its deep dive.

Use these exact labels:

- **Probably Temporary** — use an amber badge or cell when styling permits.
- **Potentially Hard to Scale** — use a blue or teal badge or cell when styling permits.

Always print the text. Never communicate the classification through color alone. Do not use green or red because the indicator is not a trading recommendation.

Classify `Potentially Hard to Scale` only when the evidence supports all of the following:

1. At least one important non-capital time gate exists, such as permitting, specialized equipment, yield learning, tacit expertise, regulatory approval, or customer qualification.
2. Qualified supply is unlikely to catch required demand within the stated research horizon even after announced and realistically fundable expansion.
3. Substitution, redesign, recycling, efficiency gains, or lower-spec alternatives are unlikely to remove the constraint faster than demand grows.
4. Entry history, minimum efficient scale, switching costs, scarce-resource access, or regulation provides evidence of a genuine barrier.
5. The company controls or solves the constraint and shows plausible value capture through pricing, margins, contracts, returns on capital, share stability, or another verified mechanism.

If any condition is unsupported, use `Probably Temporary`. If evidence is insufficient or genuinely mixed, set the indicator to `Probably Temporary`, set confidence to `Low`, and explain what evidence could change the result. Never invent a neutral third label.

Treat the indicator as horizon-dependent. State the applicable horizon, normally 12–24 months for cyclical shortages and 3–5 years for structural constraints, but adjust it to the industry's actual construction, qualification, or regulatory cycle.

## Research with a source chain

Perform live research for every report.

For each stock:

1. Obtain at least one current primary company source, such as a filing, earnings release, investor presentation, official transcript, or product and capacity announcement.
2. Obtain at least one independent perspective from a customer, supplier, competitor, regulator, government agency, standards body, recognized research lab, or fund-manager research publication.
3. Use a reputable newswire or high-quality industry publication when it adds necessary context or challenges management's claim.
4. Search for disconfirming evidence, including new capacity, falling lead times, substitute technologies, customer redesigns, second sourcing, inventory increases, price normalization, and entrant progress.

Use sources published within roughly the last six months for current financial, backlog, capacity, pricing, order, and approval claims. Use older sources for structural history, scientific constraints, prior cycles, or foundational methods only when they remain relevant and are paired with current evidence.

Record the publication date and direct URL for each source. Cite claims where they appear.

Do not rely solely on the selected company's management. Do not treat announced nameplate capacity as qualified output. Do not use an unsourced market-size estimate.

If a candidate lacks sufficient evidence, drop it and substitute another. If fewer than the requested number clear the evidence bar, deliver fewer and say why.

## Reject hidden concentration

Before finalizing the list, compare the actual demand drivers and revenue sensitivities of all candidates.

Replace a candidate when two stocks depend primarily on the same underlying spending pool or constraint, even if their products have different names. Examples of hidden overlap include two AI data-center suppliers, two uranium-price exposures, or two grid-equipment companies driven by the same transformer shortage.

Also compute the aggregate thematic exposure of the final list (see report section 5, "Hidden-concentration check"). Partial overlaps that do not justify replacement must be disclosed, not omitted.

## Score gates and disclose borderline results

If the environment provides a scoring model for the five Potentially Hard to Scale conditions (for example, gate scores from 0 to 1 with a 0.75 pass threshold), apply these V2.1 rules. If no scoring model is available, use the local cross-check in [references/scoring-crosscheck.md](references/scoring-crosscheck.md) and label the scores as approximate.

- Keep the pass rule unchanged: every one of the five gates must be at or above 0.75.
- Flag any gate within 0.10 of the threshold (0.65–0.85) as **borderline**, whether it passed or failed. State the gate and score, for example `supply lag 0.77` or `supply lag 0.74 (fail)`.
- Record the scoring model identifier (for example `jev-1.13.0`) and the evaluation prompt, or a short prompt description plus a version hash. Never omit the model string.
- For each borderline gate, write a one-sentence sensitivity note: what a 0.05–0.10 move would do to the durability indicator. A passing gate within 0.05 above the threshold means the label would flip to `Probably Temporary` if the gate fell; a failing gate within 0.05 below means the label could flip to `Potentially Hard to Scale` only if the other four gates also pass.
- Expect run-to-run variation near 0.75. Do not treat 0.76 and 0.90 as equivalent evidence. When a borderline result drives the label, set confidence no higher than `Medium`.

## Archive evidence packets

For every stock, save the evidence packet used for classification and scoring as one Markdown or JSON file named `evidence/{TICKER}.md` (or `.json`) using [references/evidence-packet-template.md](references/evidence-packet-template.md). Each packet must contain dated excerpts, direct URLs, and a source-type label (primary company, independent, newswire or industry, disconfirming).

Deliver the packets alongside the PDF, either as a folder or as `evidence_packets_YYYY-MM-DD.zip`. If the user wants them committed or linked, place them under `reports/YYYY-MM-DD/evidence/`. Do not include unused sources.

## Produce the V2 report

Save the final report as a PDF unless the user requests another format. Use the PDF workflow available in the environment and verify the rendered pages visually.

Use this filename:

`diversified_bottleneck_stock_report_v2_1_YYYY-MM-DD.pdf`

Structure the report in this order:

### 1. Header

- Title: `Diversified Bottleneck Stock Research Report — V2.1`
- Subtitle: `{N} research candidates across {N} different themes`
- Prepared date and evidence cutoff date

### 2. Disclaimer

Use the required disclaimer near the beginning.

### 3. Executive summary

Explain the demand-wave and chokepoint premise in one short paragraph. Report:

- Number classified `Probably Temporary`
- Number classified `Potentially Hard to Scale`
- Any requested themes that failed the evidence bar
- The principal uncertainty affecting the scan

### 4. Changes since last scan (required)

Place this section after the executive summary and before the ranked table. Keep it to half a page or less.

If a prior report is available (ask the user for it, or locate it in the repo or conversation), cover:

- Names added and names dropped, each with a one-sentence reason (new evidence, model variation, theme substitution, or concentration)
- Rank moves of two or more places
- Durability indicator or confidence changes
- Any gate that crossed, or moved within 0.10 of, 0.75, with old and new scores
- One-sentence rationale for every material change

Use a compact table (`Ticker | Change | Prior → Current | Reason`) or short bullets. Distinguish genuine evidence changes from run-to-run scoring variation.

If no prior report exists, state `First scan: no prior report to compare.` Never skip the section or invent a prior state.

### 5. One-theme-per-stock watchlist

Use these columns:

`Rank | Ticker | Theme | Durability indicator | Confidence | Borderline gates | Scanner thesis | Risk`

Keep the scanner thesis to one or two sentences. Ensure every durability cell uses one of the two exact labels. In `Borderline gates`, list each gate within 0.10 of 0.75 with its score, or write `None`.

Follow the table with a **Hidden-concentration check** paragraph describing the overlap tests performed, then the **Aggregate thematic exposure** paragraph: state how many of the names are primarily or secondarily exposed to the same large spending pool (especially AI data-center capex), name them and the degree of exposure, and list the remaining names with their distinct budgets or commodity drivers. Example structure: "Of the 10 names, X are primarily or secondarily exposed to AI-related capex (list, with degree). The remaining names draw on distinct budgets or commodity prices (list)."

### 6. V2.1 methodology

Briefly explain:

- The demand-versus-qualified-supply comparison
- The three clocks: demand, qualified supply, and workaround
- The seven durability tests
- The distinction between industry scarcity and company value capture
- The conservative classification rule
- The scoring model identifier and prompt or prompt hash, the 0.75 threshold, and the borderline band (within 0.10)
- A **Sensitivity** subsection: which gates are borderline and how the label would change if each moved by 0.05–0.10
- Where the evidence packets are archived

### 7. Per-stock deep dives

Use this exact structure for every stock:

1. `TICKER — Company Name`
2. `Theme: {distinct bottleneck theme}`
3. `Durability indicator: {Probably Temporary | Potentially Hard to Scale}`
4. `Confidence: {Low | Medium | High}`
5. `Research horizon: {stated horizon}`
   - Add `Borderline gates: {gate score, ...}` and a one-sentence sensitivity note when any gate is within 0.10 of 0.75.
6. **Thesis** — demand wave, specific bottleneck, company connection, and current dated validation
7. **Three-clock assessment**
   - Demand clock
   - Qualified-supply clock
   - Workaround clock
8. **Why the indicator may be right** — two to four evidence-backed points
9. **Evidence against the indicator** — at least two genuine counterpoints
10. **Company value capture** — explain control of the bottleneck and evidence from pricing, margins, contracts, share, or returns
11. **What would flip the indicator** — define observable invalidation conditions
12. **What to monitor** — three forward-looking signals
13. **Key risks** — three to four stock-specific risks
14. **Sources** — dated source list with direct links

Do not omit counterevidence. A deep dive without a credible bear case fails verification.

### 8. How to use the watchlist

Explain that:

- The report is a research funnel, not a list of recommendations.
- A temporary bottleneck can still produce a short earnings windfall.
- A hard-to-scale bottleneck can still be a poor investment because value capture, balance sheet, or valuation may be unfavorable.
- Research should proceed from filings to competitors, customers, valuation, and thesis invalidation.

### 9. Selected sources

List every URL used in the body and no unused URLs. Format each entry as:

`**Source label — publication date:** https://...`

End the report with one line: `Evidence packets archived at {link or path}.`

## Write neutrally

- Use plain, specific language.
- Avoid hype and superlatives such as “best,” “must-own,” “explosive,” or “guaranteed.”
- Separate facts, management claims, outside estimates, and the report's inference.
- Label uncertainty and scenario assumptions.
- Avoid false precision when data are unavailable.
- Explain why a classification was assigned, not just what it is.
- Keep fund-manager opinions distinct from company filings and scientific or engineering evidence.

## Verify before delivery

Confirm all of the following:

- The disclaimer is present.
- The `Changes since last scan` section is present (or states first scan) and covers added/dropped names, rank moves of two or more places, gate threshold crossings, and rationales.
- The watchlist includes the `Borderline gates` column, and every gate within 0.10 of 0.75 is listed with its score and a sensitivity note.
- The scoring model identifier and prompt or hash are stated in the methodology.
- The aggregate thematic-exposure paragraph follows the hidden-concentration check.
- An evidence packet exists for every stock and the archive location is stated in the report.
- Every stock has exactly one durability indicator and a confidence level.
- Every `Potentially Hard to Scale` classification clears all five mandatory conditions.
- Every stock includes disconfirming evidence and a flip condition.
- Current validation claims use dated sources from roughly the last six months.
- Structural claims are supported by relevant sources and paired with current evidence.
- Every stock has a primary company source and an independent source.
- No two stocks share a hidden theme.
- Risk labels match the deep-dive risks.
- All body URLs appear in Selected Sources and all Selected Sources appear in the body.
- The rendered PDF has no clipping, overlap, missing glyphs, broken links, orphan headings, or unreadable tables.
- The filename includes `v2_1` and the actual preparation date.

Present the verified artifact with a direct download link and one sentence summarizing the classification mix. Do not claim validation steps passed unless they actually ran successfully.
