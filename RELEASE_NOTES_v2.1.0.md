# Bottleneck Stock Scanner v2.1.0

V2.1 makes the biweekly reports easier to compare, audit, and reproduce. The seven durability tests and the conservative rule (all five gates must be at or above 0.75 for **Potentially Hard to Scale**) are unchanged.

## What's new

- **Changes since last scan.** Every report now has a short, required section after the executive summary. It lists names added or dropped, rank moves of two or more places, durability or confidence changes, gates that crossed or approached 0.75, and a one-sentence reason for each. A first scan says so.
- **Borderline gates.** The watchlist has a new column for any gate within 0.10 of the 0.75 threshold, with its score.
- **Scoring model documentation.** The methodology must state the scoring model string (for example `jev-1.13.0`) and the evaluation prompt or a prompt hash.
- **Sensitivity notes.** Each borderline gate gets a note on how the label would change if the score moved by 0.05–0.10. Borderline results cap confidence at Medium.
- **Aggregate thematic exposure.** A paragraph after the hidden-concentration check states how much of the list shares an underlying spending pool, such as AI data-center capex, and which names draw on separate budgets.
- **Archived evidence packets.** One dated packet per stock (excerpts, URLs, source-type labels) ships with each report, and the report ends with an archive note. Template: `references/evidence-packet-template.md`.
- **Local scoring cross-check.** `references/scoring-crosscheck.md` is a rubric for approximating the five gates when the scoring model is unavailable, or for sanity-checking its output.
- **Sample reports.** `samples/` includes the 2026-10-04 and 2026-10-18 V2 reports.
- **Changelog and badges.** Added `CHANGELOG.md` and README badges.

## Changes to be aware of

- New report filename: `diversified_bottleneck_stock_report_v2_1_YYYY-MM-DD.pdf`.
- The report title is now "Diversified Bottleneck Stock Research Report — V2.1".
- The report sections are renumbered to fit the new section, and the verification checklist is extended.
- The two sample reports predate V2.1 and do not include the new sections.
- README links now point to `ericxinqisu/bottleneck-stock-scanner`.

## Download and install

Download `bottleneck-stock-scanner-v2.1.skill` below and follow the install steps in the README.

## Notice

For research and education only. Not financial advice and not a recommendation to buy or sell securities.

**Full changelog:** https://github.com/ericxinqisu/bottleneck-stock-scanner/compare/v2.0.0...v2.1.0
