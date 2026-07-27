# Limitations and Ethical Considerations

*Every limitation of this pilot, stated openly, with why it was accepted and how future work addresses it — followed by the study's ethical framework.*

---

## Limitations

A pilot's limitations are design features when they are chosen deliberately and disclosed fully. Each entry below explains the limitation, why it is acceptable at pilot stage, and the planned remedy.

**Five scenarios.** Too few to characterize model performance; enough to test whether the rubric and workflow function. Chosen to keep evaluator burden sustainable for volunteer clinicians. *Future work:* a larger scenario bank once the instrument is validated.

**Single specialty perspective (internal medicine registrar), single country.** Findings cannot generalize to other specialties or health systems — but the *methodology* is designed to. Trinidad and Tobago was chosen because feasibility judgments there are verifiable by the study team. *Future work:* additional specialties, additional Caribbean territories, and other resource-constrained systems.

**Ten evaluators, all new to AI evaluation.** A small rater pool limits the precision of reliability estimates, and novice evaluators risk inconsistent rubric interpretation. The calibration programme (handbook, worked examples, calibration session, orientation video) is the mitigation — and testing whether that programme suffices is itself a study aim. *Future work:* a larger rater pool and formal rater-training evaluation.

**Calibration effect unmeasured.** No scoring was collected before calibration, so the pilot measures post-calibration reliability, not calibration's improvement over baseline. Accepted because the priority was protecting the integrity of the formal scores. *Future work:* a pre/post calibration design.

**Limited claim scope from single-sample, consumer-interface generation.** Responses are single draws from continuously updated systems accessed without parameter control or version pinning, so exact regeneration is impossible. This follows from the study's design rationale rather than being a compromise: the unit of analysis is what a physician actually receives when they ask once, which is how these tools are used at the bedside (see [study_design.md](study_design.md)). The consequence is a constraint on what may be claimed — findings describe what a physician would have received on 5 July 2026, not how any named model behaves in general. Model-level statements in this work should be read accordingly. *Future work:* version-pinned API generation with repeated sampling as a separate comparison arm, answering the distinct question of model capability.

**Fixed scenario order; imperfect blinding.** Presentation order was not randomized, so order effects cannot be excluded. Frontier models have recognizable styles, so blinding by label (Model 1/2/3) may not survive contact with experienced users; the post-scoring model-identity guess measures this rather than leaving it unknown. *Future work:* randomized presentation order; style-normalized response formatting.

**Reference-standard bias.** The reference standards encode the consensus of two senior physicians, including judgment calls that other competent clinicians could contest — for example, the pancreatitis scenario commits to scorpion envenomation (*Tityus trinitatis*) as the principal diagnosis on strong but circumstantial evidence, and some listed management elements reflect sound local practice rather than universal standards. The mitigation is structural: the standards are explicitly framed as panel *expectations* rather than required content, and evaluators are instructed that a clinically sound alternative approach is not a deficiency (protocol amendment of 26 July 2026, made before any scoring commenced — see [CHANGELOG](../CHANGELOG.md)). Ambiguities identified during development were recorded as explicit flags in the standards rather than suppressed, and the term "reference standard" (not "gold standard") is used throughout to keep the epistemic status honest. Residual risk remains that scoring partly reflects agreement with the panel. *Future work:* larger expert panels and formal consensus methods (e.g., Delphi).

**Anchoring risk in calibration materials.** The worked exemplar shows one response scoring perfectly, which could lead evaluators to pattern-match its *style* rather than its substance. Disclosed here; evaluator justifications will be reviewed for evidence of style-based scoring. *Future work:* calibration examples spanning more score profiles.

**No external validation; exploratory throughout.** No independent group has replicated any part of this methodology, and all analyses are estimation-oriented. This is what "pilot" means, and no claim in this repository exceeds that status. *Future work:* the definitive study, external collaborators, and formal ethics review — see below.

## Ethical considerations

**No patient data.** All five scenarios and the exemplar case are fully synthetic, constructed from general clinical experience. No real patient records, identifiable details, or case notes were used at any stage.

**Evaluators as co-investigators.** The ten physician evaluators participate as collaborators, not research subjects. Each signs a participation agreement covering role, time commitment, data handling, and an individual choice between named credit and anonymity. Individual-level scoring data will be released only in de-identified form.

**Institutional review.** C-MAIR is currently an independent, physician-led initiative without an institutional home, and this pilot — involving no patients and no human-subjects data collection beyond expert annotation by co-investigators — proceeded without formal ethics committee review. This is stated transparently rather than presented as an exemption ruling. Formal ethics review (through The University of the West Indies or an equivalent body) will be sought before any definitive study, and institutional collaboration is an explicit near-term goal.

**The self-harm scenario.** One scenario involves intentional paraquat ingestion. It is included because paraquat poisoning is an epidemiologically significant presentation in Trinidad and Tobago and a demanding test of locally adapted management. The scenario is handled clinically and contains no method detail beyond what evaluation requires.

**Conflicts of interest.** This study received no funding, access, or input from any AI developer. Models were accessed through standard consumer subscriptions purchased by the study team. Future collaboration with frontier AI laboratories is an explicit goal of the C-MAIR programme and will be disclosed if and when it materializes.

**Why this work matters ethically.** Large language models tuned to high-resource healthcare assumptions do not fail uniformly: they fail hardest for patients in resource-constrained systems, where their confident recommendations are least implementable. Building locally led evaluation capacity is a prerequisite for these tools serving such populations safely — that equity concern, as much as scientific interest, motivates C-MAIR.

---

*Related documents: [study_design.md](study_design.md) · [evaluator_process.md](evaluator_process.md) · [analysis_plan.md](analysis_plan.md) · [data_access.md](data_access.md)*
