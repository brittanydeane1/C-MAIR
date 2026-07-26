# Analysis Plan

*Written and published before evaluator scoring completes, so that the analysis is specified in advance rather than shaped by the data. Any amendment after this date will be recorded in the [CHANGELOG](../CHANGELOG.md) with its rationale.*

---

## What this pilot measures

The primary outcomes concern the **methodology**, not the models:

1. **Inter-rater reliability** — do ten physicians using this rubric produce consistent scores?
2. **Feasibility** — can the evaluation actually be completed as designed?
3. **Blinding integrity** — did evaluators identify the models despite blinding?

Model scores are secondary and will be reported descriptively only. This pilot will not rank models or declare a "best" model, because five scenarios cannot support such a claim.

## Primary analyses

**Inter-rater reliability, per domain.** For each of the six domains (across all 15 responses, 10 raters):

- **Krippendorff's alpha with ordinal weighting** — primary metric. Chosen because the scores are ordinal (0–4), it accommodates any missing ratings, and it is the standard reliability coefficient in annotation research.
- **ICC(2,1)** (two-way random effects, absolute agreement, single-rater) — secondary metric, appropriate because the design is fully crossed and future studies will rely on single raters per response.
- **Percent exact agreement and percent within-one-point agreement** — reported alongside, because coefficients are abstract and clinicians reading this work deserve an interpretable number.

Interpretation will be cautious. With 15 rated responses per domain, confidence intervals will be wide. The purpose is estimation — learning roughly where reliability sits, and which domains are weakest, to design the definitive study — not hypothesis testing. Domains with low reliability will be examined qualitatively (evaluator justifications) to locate the rubric ambiguity responsible.

**Feasibility metrics.** Evaluator completion rate; missing or invalid ratings; scoring queries raised during evaluation and their nature; time to completion where captured.

**Blinding integrity.** Accuracy of evaluators' model-identity guesses compared with chance (33%). If models were widely identified, this is reported plainly as a limitation on blinding.

## Secondary (descriptive and exploratory) analyses

- **Domain score distributions** by model and by scenario — reported as medians and ranges, without ranking claims.
- **The universal-vs-local gap.** The motivating observation predicts a specific pattern: high scores on universal domains (Clinical Reasoning, Patient Safety) alongside lower scores on Trinidad-specific domains (Resource Adaptation, Contextual Adaptation, Adaptation Latency). Whether this pattern appears will be reported as **hypothesis-generating only** — this pilot is not powered to test it.
- **Adaptation Latency validity check.** Correlation of latency scores with Resource and Contextual Adaptation scores, to assess whether latency captures distinct signal or is redundant. High correlation would suggest the construct needs sharpening before the definitive study; that would be a useful pilot finding, not a failure.

## The dataset

One row per evaluator × scenario × model × domain:

| Variable | Type | Values |
|---|---|---|
| evaluator_id | categorical | E01–E10 |
| scenario_id | categorical | CMAIR-IM-001 … 005 |
| model_id | categorical | M1, M2, M3 (blinded labels) |
| domain | categorical | reasoning, safety, resource, context, latency, communication |
| score | ordinal integer | 0–4 |
| justification | free text | evaluator's brief rationale |
| model_guess | categorical | recorded once per evaluator per model, post-scoring |

A de-identified version of this dataset will be released in this repository with the results. Analysis code (open source, Apache-2.0) will be released alongside it so every reported number can be recomputed.

---

*Related documents: [study_design.md](study_design.md) · [scoring_and_latency.md](scoring_and_latency.md) · [limitations_and_ethics.md](limitations_and_ethics.md) · [data_access.md](data_access.md)*
