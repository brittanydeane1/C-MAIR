# Changelog

All notable changes to the C-MAIR pilot study protocol and repository are recorded here. Protocol amendments after publication of the [analysis plan](docs/analysis_plan.md) will include their rationale.

## [0.1.0] — 2026-07 — Protocol-stage repository

### Completed before this release

- **2026 (first half):** Five clinical scenarios developed (Clinical Scenario Bank v1); Case Reference Standards developed by two senior physicians through independent review and consensus, with ambiguity flags recorded per case; six-domain scoring rubric drafted and refined.
- **2026 (first half):** Calibration programme built: Evaluator Handbook v1 (including the fully scored worked exemplar CMAIR-IM-EX01), structured calibration session materials, orientation video.
- **2026-07-05:** Model responses generated — GPT 5.5, Claude Opus 4.8, Gemini 3.6 Flash via consumer chat interfaces; one response per model per scenario, captured verbatim; models blinded as Model 1/2/3.
- **2026-07:** Evaluator recruitment underway (ten physicians, co-investigator model, individual credit choice).

### Added in this release

- Public repository: README, study design, scoring rubric and Adaptation Latency documentation, evaluator process, locked analysis plan, limitations and ethics, data access policy, Evaluator Handbook v1, public exemplar case, licensing.
- ### Protocol amendments

- **2026-07-26 — Reference standards clarified as panel expectations (made before any scoring commenced).** The Case Reference Standards previously headed their management lists "non-negotiable management steps," and the Evaluator Handbook instructed that absence of a listed element should lower the relevant domain score. Both were reworded: lists are now "expected core management elements," described as neither exhaustive nor exclusive, and evaluators are instructed that a clinically sound alternative approach is not a deficiency — a missing element prompts consideration of whether something clinically important is absent, rather than an automatic deduction. *Rationale:* the original wording risked scoring agreement with the reference panel's practice preferences rather than clinical quality. The six scoring domains, the 0–4 anchored scale, the domain anchors, the scenarios, and the captured model responses are unchanged. All ten evaluators were notified identically before beginning; no scoring had taken place under the previous wording. Reissued as `instruments/C-MAIR_Case_Reference_Guide_v2.pdf`.

### Upcoming

- **Target 2026-09-05:** Evaluator scoring complete.
- **v1.0.0:** Results release — reliability and feasibility findings, de-identified ratings dataset, analysis code.
