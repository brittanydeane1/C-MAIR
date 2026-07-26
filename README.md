# C-MAIR

**Caribbean Medical AI Adaptation and Implementation Research**

> **Status: Pilot study in progress.** Physician evaluation is underway, with scoring targeted for completion in September 2026. Results will be added to this repository when analysis is complete. Until then, this repository serves as the public record of the study protocol and instruments.

C-MAIR is a physician-led research initiative studying how frontier large language models adapt to Caribbean healthcare systems. This repository documents its first pilot study: an evaluation of three frontier models on five internal medicine scenarios set in Trinidad and Tobago's public healthcare system, scored by ten practicing physicians.

**Principal Investigator:** Dr. Brittany Deane-Taylor, MBBS

---

## The research question

Can frontier large language models generate clinically safe, feasible, and contextually appropriate recommendations for patients receiving care within Trinidad and Tobago's healthcare system?

## The motivating observation

In our clinical experience, frontier models usually produce *medically correct* recommendations. The problem is that they often assume a high-resource healthcare system — on-demand imaging, unrestricted formularies, immediate subspecialty access. Many models eventually acknowledge local constraints, but only after presenting lengthy management plans built on assumptions that do not hold in Trinidad and Tobago. A physician using such a response must mentally filter, reinterpret, or discard large portions of it before arriving at a usable plan. That is added cognitive load at the point of care.

C-MAIR therefore evaluates not only *whether* a model adapts to the local context, but *when* it adapts within its response. We call this **Adaptation Latency**: a response that localizes immediately is more clinically useful than one that localizes in its final paragraph, even if both eventually "get there." This is developed fully in [docs/scoring_and_latency.md](docs/scoring_and_latency.md).

## What this pilot is — and is not

This is an intentionally small exploratory pilot. Its purpose is **not** to determine which model is "best." Its purpose is to test whether the C-MAIR methodology itself works: whether physician-led AI evaluation is practical, whether the scoring rubric functions as intended, whether physicians interpret it consistently, and whether this approach can support a larger future benchmark. Model scores will be reported descriptively, without rankings or leaderboard claims.

## Study at a glance

| Element | Detail |
|---|---|
| Design | Exploratory feasibility pilot, fully crossed |
| Setting | Trinidad and Tobago public healthcare system |
| Scope | Acute and ambulatory adult general medicine, from the internal medicine registrar's perspective |
| Scenarios | 5 context-rich clinical vignettes (fully synthetic; no patient data) |
| Models | GPT 5.5, Claude Opus 4.8, Gemini 3.6 Flash (consumer interfaces, July 2026) |
| Evaluators | 10 practicing physicians, blinded to model identity |
| Scoring | 6 domains, 0–4 anchored scale per domain |
| Reference standards | Developed by two senior physicians through independent review and consensus |

## The six scoring domains

| # | Domain | What it measures |
|---|---|---|
| 1 | Clinical Reasoning | Correct diagnosis and guideline-consistent plan |
| 2 | Patient Safety | Avoidance of harm; takes precedence over all other domains |
| 3 | Resource Adaptation | Feasibility within the described Trinidad and Tobago setting |
| 4 | Contextual Adaptation | Meaningful use of cultural, social, and economic context |
| 5 | Adaptation Latency | How *early* the response tailors itself to the local setting |
| 6 | Communication & Organization | Clinical usability; cognitive load on the reading clinician |

## Repository map

| File | What it contains |
|---|---|
| [docs/study_design.md](docs/study_design.md) | What we did and why — scenarios, models, evaluators, every design decision with its rationale |
| [docs/scoring_and_latency.md](docs/scoring_and_latency.md) | The rubric explained, including Adaptation Latency in full |
| [docs/evaluator_process.md](docs/evaluator_process.md) | How evaluators are recruited, trained, calibrated, and how they score |
| [docs/analysis_plan.md](docs/analysis_plan.md) | The analysis plan, locked before scoring completes |
| [docs/limitations_and_ethics.md](docs/limitations_and_ethics.md) | Every limitation, openly stated, with how future work addresses it; ethical considerations |
| [docs/data_access.md](docs/data_access.md) | What is public, what is withheld and why, and how to request access |
| [instruments/C-MAIR_Evaluator_Handbook_v1.pdf](instruments/) | The full scoring manual used by evaluators |
| [instruments/exemplar_case.md](instruments/exemplar_case.md) | A complete worked example: one scenario, two model responses, fully scored |
| [CHANGELOG.md](CHANGELOG.md) | Dated record of the project's development and any protocol amendments |
| [LICENSE.md](LICENSE.md) | Licensing for documentation and withheld materials |

## Why the five scenarios are not published here

Publishing evaluation scenarios places them in future model training data, which would compromise their use in follow-up studies. One complete exemplar case is public in [instruments/exemplar_case.md](instruments/exemplar_case.md) so anyone can see exactly how C-MAIR evaluation works. The five test scenarios and their reference standards are available to researchers on request — see [docs/data_access.md](docs/data_access.md).

## Future directions

If this pilot demonstrates feasibility, planned next steps include a larger scenario bank, a formally powered reliability study, collaboration with regional institutions (The University of the West Indies, CARPHA, and Caribbean health research bodies), and engagement with frontier AI developers on benchmarks for Caribbean and other resource-constrained healthcare systems. The long-term aim is a methodology that any resource-constrained health system can use to evaluate — and improve — how frontier models serve its patients. Other sectors (law, finance, agriculture, public policy) may eventually be explored, but medicine is the sole focus of the current programme.

## Citing this work

> Deane-Taylor B. C-MAIR: Caribbean Medical AI Adaptation and Implementation Research — Pilot Study Protocol. 2026. https://github.com/[username]/c-mair

## Contact

Questions, methodological critique, and expressions of interest (future evaluators, regional collaborators) are welcome — please open a GitHub Issue or contact the Principal Investigator.
