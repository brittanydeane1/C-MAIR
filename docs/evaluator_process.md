# Evaluator Process

*How the ten physician evaluators are recruited, prepared, calibrated, and how they score. The scoring rules themselves live in the [Evaluator Handbook](../instruments/) and are summarized in [scoring_and_latency.md](scoring_and_latency.md).*

---

## Who the evaluators are

Ten physicians practising in Trinidad and Tobago. None had previously evaluated AI systems. Evaluators participate as **co-investigators**, not research subjects: each signs a participation agreement covering their role, the time commitment, data handling, and their individual choice of **named credit or anonymity** in project outputs. Named evaluators will be credited as members of the C-MAIR Evaluator Group.

## Why calibration was necessary

During reference-standard development, the two senior physicians found that the draft rubric contained ambiguities — places where two competent clinicians could reasonably score the same response differently. Combined with the evaluators' lack of AI-evaluation experience, this predicted poor scoring consistency if evaluators were simply handed the rubric cold. Four calibration components were therefore built **before** formal scoring:

1. **The Evaluator Handbook** — a plain-language scoring manual with written anchors for every score level in every domain, scoring principles (score clinical quality, not personal style; equivalent intent earns equal scores; do not reward or punish length), and the "name-dropping" verification rules.
2. **Worked scoring examples** — a complete case (published as the [exemplar](../instruments/exemplar_case.md)) with two contrasting model responses scored domain-by-domain with written justifications, showing evaluators the difference between location-tagging and operational localization.
3. **A structured calibration session** — evaluators work through scoring together before independent scoring begins, surfacing interpretation differences while they can still be resolved.
4. **A short orientation video** — explaining the project's purpose and scoring methodology, so evaluators understand *why* they are scoring, not just how.

One honest caveat: because no scoring was collected before calibration, this pilot measures *post-calibration reliability* — it cannot quantify how much the calibration itself improved consistency. A pre/post calibration design is planned for future work ([limitations_and_ethics.md](limitations_and_ethics.md)).

## The scoring workflow

Each evaluator, working independently:

1. Verifies the Case ID on the response matches the Answer ID on the scoring form — a guard against misfiled scores.
2. Reads the clinical scenario, then the model response.
3. Scores all six domains (0–4) using the Handbook anchors and the Case Reference Standard's critical-elements key for that scenario.
4. Records brief justifications.
5. Repeats for all 15 responses (3 models × 5 scenarios).
6. After completing all scoring, records a guess of each model's identity — a check on blinding integrity, since frontier models have recognizable styles.

Evaluators are blinded to model identity throughout (Models 1, 2, 3). Questions arising mid-scoring go to the Principal Investigator and are logged; clarifications are shared with all evaluators identically or with none, so no single evaluator scores with private guidance.

## Design principle: respect physician time

Every element of this workflow — five scenarios rather than twenty, a scannable handbook rather than a protocol binder, structured forms rather than free-text reports — exists because the evaluators are practising clinicians volunteering scarce time. A methodology that burns out its raters does not scale; demonstrating a sustainable evaluator experience is itself one of this pilot's feasibility outcomes.

---

*Related documents: [scoring_and_latency.md](scoring_and_latency.md) · [study_design.md](study_design.md) · [limitations_and_ethics.md](limitations_and_ethics.md) · [Evaluator Handbook](../instruments/)*
