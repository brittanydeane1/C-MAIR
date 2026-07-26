# Data Access Policy

*What is public, what is withheld and why, and how to request access.*

---

## Public in this repository

- All documentation and the study protocol
- The complete Evaluator Handbook, including the fully worked exemplar case (CMAIR-IM-EX01) with two verbatim model responses and their scoring
- Aggregate results, the de-identified ratings dataset, and analysis code — added when analysis completes

## Withheld, and why

- **The five test scenarios** (CMAIR-IM-001 through 005)
- **Their Case Reference Standards**
- **The fifteen raw model responses**

The reason is training-data contamination. Anything published openly on the web can be absorbed into future model training corpora. If the test scenarios became training data, future models could perform well on them by memorization rather than adaptation, and the scenarios would be useless for follow-up studies or longitudinal comparison. Withholding them is the same logic behind held-out test sets in major AI benchmarks.

The public exemplar case exists precisely so this gating costs no transparency about *method*: it shows the full pipeline — scenario, model responses, domain-by-domain scoring with justifications — on a case that is deliberately excluded from the evaluation set.

- **Individual evaluator-level data** is additionally protected by the evaluator participation agreements; only de-identified data will be released.

## Requesting access to withheld materials

Researchers with a legitimate scholarly purpose (peer review, replication, methodological research, benchmark development for resource-constrained health systems) may request the gated materials by contacting the Principal Investigator (via GitHub Issues or the contact route in the [README](../README.md)) with:

1. Who you are and your affiliation (independent researchers welcome)
2. The purpose of the request
3. Agreement not to redistribute the materials or include them in any model training corpus

Requests are reviewed case by case by the Principal Investigator. If the scenarios are eventually retired from longitudinal use, they will be released openly.

## Licensing

See [LICENSE.md](../LICENSE.md): public documentation is CC BY 4.0; future analysis code is Apache-2.0; withheld materials remain all rights reserved and are governed by this policy.

---

*Related documents: [README](../README.md) · [LICENSE.md](../LICENSE.md) · [study_design.md](study_design.md) · [limitations_and_ethics.md](limitations_and_ethics.md)*
