# Local Scoring Cross-Check

A lightweight checklist for approximating the five gates when the external scoring model is unavailable, and for sanity-checking its output when it is available. It does not replace the model. It bounds the uncertainty and keeps the scan usable if the model changes or is unreachable.

Scores here are approximate. Label them `local cross-check` in the report and never mix them with model scores in the same table column without saying so.

## How to score each gate

Start at 0.50. Add or subtract for each item that is supported by a dated, cited source. Clamp to 0.00–1.00. Pass threshold is 0.75, the same as the model.

| Gate | Add 0.10 each (max +0.50) | Subtract 0.10 each |
|---|---|---|
| 1. Non-capital time gate | Multi-year permit or approval; sole-source or capacity-constrained tools; yield learning curve documented; customer qualification of 12+ months; tacit know-how with evidence of failed entrants | Standard multi-vendor equipment; qualification under 6 months; output roughly proportional to capex |
| 2. Qualified supply vs demand | Gap persists after funded projects in an independent forecast; lead times rising; long-term contracts or prepayments; utilization near ceiling; announced capacity not yet qualified | Funded projects close the gap within the horizon; lead times falling; inventory building; spot prices normalizing |
| 3. Workaround clock | Few acceptable substitutes; requalification long; input intensity flat or rising; recycling or redesign immature | Active customer redesign; second sourcing announced; input intensity falling faster than demand grows |
| 4. Entry barriers | Observed entrant failures; large minimum efficient scale; switching costs documented; regulation or scarce-resource access | Successful recent entrants; share moving readily; low capital or know-how requirement |
| 5. Company control and value capture | Controls an unavoidable layer; gross margin or pricing power survives normalized utilization; take-or-pay or deposits; stable share; return on incremental capital above cost of capital | Commodity response; customer concentration; backlog cancellable or low margin; margin spike only at peak utilization |

## Interpreting results

- Any gate below 0.75 means `Probably Temporary`, as in the main rule.
- A gate within 0.10 of 0.75 is borderline. State what a 0.05–0.10 move does to the label.
- If the local score and the model score differ by more than 0.10 on any gate, note the disagreement and the evidence that explains it, and use the lower of the two for the label.
- If the model is unavailable, use local scores, set confidence no higher than `Medium`, and say so in the methodology.
