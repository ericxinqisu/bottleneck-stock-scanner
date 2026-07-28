---
name: bottleneck-stock-scanner
description: Build a diversified bottleneck-style stock research report — one stock per supply-chain theme where demand could force attention toward a scarce product, capability, or infrastructure layer. Use when the user asks for a "bottleneck" stock scan, a one-theme-per-stock watchlist, or research candidates across supply-chain chokepoints.
---

# Bottleneck Stock Scanner

Produce a diversified, research-only stock report that identifies **one company per major supply-chain theme** where a demand wave is colliding with a hard-to-scale chokepoint. The goal is breadth across themes — never ten stocks in the same trade.

**This is research and education only, not financial advice.** Every report must carry that disclaimer at the top and avoid recommendations to buy or sell.

## When to use

- "Run me a bottleneck scan"
- "Give me a diversified watchlist of supply-chain bottleneck stocks"
- "Update / refresh the bottleneck stock report"
- Any request for stocks framed around scarcity, chokepoints, or supply-chain constraints across multiple themes

## Before you start: clarify scope

If the user hasn't specified, ask 1–3 short clarifying questions via `AskUserQuestion`:

- **Number of candidates** (default 10)
- **Geography / market** (default U.S.-listed)
- **Themes to include or exclude** (defaults span: AI infrastructure, semiconductor packaging, grid/power, critical minerals, energy storage, cybersecurity, defense autonomy, healthcare/nuclear medicine — but you can swap in biotech, water, agriculture, space, etc.)
- **Risk appetite** (whether to lean toward small-cap asymmetric picks vs. large-cap incumbents)

Skip clarification only if the user explicitly says "use defaults" or "same as last time."

## Methodology (apply to each candidate)

1. **Demand wave.** Name the macro driver — what is growing fast enough to strain supply?
2. **Supply-chain map.** Identify the component, service, or capacity layer that must scale for that demand to be met.
3. **Bottleneck.** Favor layers that are technically difficult, capacity-constrained, regulated, strategically important, or protected by customer qualification barriers.
4. **Validation.** Cite recent orders, backlog, product approvals, customer agreements, management commentary, or market behavior — with dates. No validation, no inclusion.
5. **One stock per theme.** Never stack multiple picks on the same theme. This is the core diversification rule.
6. **Risk penalty.** Downgrade for balance-sheet weakness, high valuation, customer concentration, regulatory issues, execution delays, or geopolitical exposure. Each candidate gets a risk label: Low / Medium / Medium-High / High / Very High.

## Research workflow

1. **Refresh the date** in bash so the report header is accurate.
2. **For each theme, do live research** — use web search / fetch tools (or a deep-research harness for thorough cross-checking) to pull the latest earnings release, order announcement, or sector news. Prefer primary sources (company IR pages, SEC filings) and reputable wires (Reuters, Bloomberg, AP). Capture exact URLs and publication dates.
3. **Verify every validation claim.** Numbers (backlog, capital raises, revenue, FDA approvals) must come from a cited primary source published within roughly the last 6 months. If you can't verify, drop the stock and substitute another.
4. **Reject theme crowding.** Before finalizing the list, scan for hidden overlap (e.g., two "AI data center" picks dressed up as different themes). If overlap exists, replace one.
5. **Do not invent tickers, executives, dollar figures, or dates.** If a fact isn't in your sources, omit it rather than guessing.

## Output format

Save as a **PDF** to the user's selected workspace folder (use the `pdf` skill if available). Filename pattern: `diversified_bottleneck_stock_report_YYYY-MM-DD.pdf`. If the user explicitly asks for a different format (e.g., Markdown, Word), follow that instead.

Structure the document in this order:

**1. Header**
- Title: "Diversified Bottleneck Stock Research Report"
- Subtitle: "{N} research candidates across {N} different investment themes"
- Prepared date (today's actual date)

**2. Disclaimer box** (verbatim or close to):
> Important: This report is for research and education only. It is not financial advice, not a recommendation to buy or sell securities, and does not consider your personal risk tolerance, time horizon, tax situation, or portfolio. Small-cap and thematic stocks can be extremely volatile.

**3. Executive Summary** — one short paragraph explaining the bottleneck-scanner premise and the three traits the strongest candidates share (large demand wave + hard-to-scale chokepoint + customer/market validation).

**4. One-Theme-Per-Stock Watchlist table** with columns: Rank | Ticker | Theme | Scanner thesis (1–2 sentences) | Risk.

**5. Model Methodology** — the 6-step list above, in prose form.

**6. Per-stock deep dives** — one section per ticker, in this exact shape:
- Heading: `TICKER - Company Name`
- Sub-heading: `Theme: {theme name} bottleneck`
- 1 paragraph: thesis + the specific validation evidence (with dates and dollar figures from cited source)
- `What to monitor` — 3 bullets of forward-looking signals
- `Key risks` — 3–4 bullets
- Italic source line at the bottom: `Source: {primary source}, {date}.`

**7. How to Use This Watchlist** — 4 short paragraphs covering: it's a research funnel not buy-recs, avoid hidden concentration, use thesis invalidation (define what would prove each thesis wrong), prefer staged research (spreadsheet → 10-Q/10-K → competitors → valuation).

**8. Selected Sources** — bulleted list of every URL cited, formatted as `**Label:** https://...`

## Style rules

- Plain, neutral language. No hype, no superlatives ("best", "must-own", "explosive").
- Never include price targets, "buy below X", or position-sizing advice.
- Every concrete claim (backlog size, capital raise, FDA approval, earnings figure) must have a dated source.
- Risk labels must reflect real fragility — don't soften them to make the list look balanced.
- If a theme has no candidate that clears the validation bar, leave it out and note in the executive summary that fewer than N themes met the criteria this cycle.

## Verification step (do not skip)

Before delivering, re-read the draft and check: (a) each ticker has a primary-source citation with a date in roughly the last 6 months, (b) no two picks share a hidden theme, (c) the disclaimer is present, (d) risk labels are consistent with the per-stock risk bullets, (e) all URLs in Selected Sources actually appear in the body, and vice versa.

Present the finished PDF with a download link and a one-sentence summary. Do not re-explain the contents — the user can open the file.
