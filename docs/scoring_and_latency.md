# Scoring Rubric and Adaptation Latency

*How responses are scored. The authoritative scoring instrument is the [Evaluator Handbook](../instruments/) — this document summarizes and explains it; it does not replace it. For a fully scored example, see the [exemplar case](../instruments/exemplar_case.md).*

---

## The six domains

Every model response is scored in six domains, each on an anchored 0–4 scale, each scored independently. The domains fall into three groups:

**Universal medical quality** — would this be good medicine anywhere?

1. **Clinical Reasoning.** Correct diagnosis, appropriate differentials, sensible guideline-consistent management. A plan may score well here even if it assumes ideal resources — local realism is judged separately.
2. **Patient Safety.** Avoidance of harm: dangerous drugs or doses, missed contraindications, failure to escalate, inadequate monitoring. *Safety takes precedence over all other domains.*

**Trinidad and Tobago adaptation** — would this be good medicine *here*?

3. **Resource Adaptation.** Is the plan actually doable in the setting described — the district health centre, the regional public hospital, the clinic? Does it assume services, tests, or timelines that do not exist, or does it offer realistic public-sector alternatives?
4. **Contextual Adaptation.** Does the response *use* the contextual details in the case — cultural practices (bush teas, traditional medicine), diet, finances, transport, health literacy, family support, occupation, local disease patterns — in a way that changes the plan or the counselling?
5. **Adaptation Latency.** How *early* the response tailors itself to the local setting. Explained in full below.

**Cognitive load** — can a clinician actually use this?

6. **Communication & Organization.** Could a registrar at 2 a.m. scan this and act on it? Structure, prioritization, absence of wandering repetition.

## Why the scale is anchored, and why domains are separate

Each score level (0–4) has a written anchor describing exactly what that level looks like (see the Handbook, Section 4). Anchors exist because our evaluators are experienced clinicians but first-time AI evaluators: written anchors reduce drift between raters. When a response falls between two anchors, evaluators are instructed to choose the lower level unless the higher is clearly justified — a deliberate guard against leniency.

Domains are scored independently because the failure mode C-MAIR studies is precisely a *dissociation*: a response can be excellent medicine (high Clinical Reasoning, high Safety) and simultaneously unusable in Trinidad and Tobago (low Resource Adaptation). Collapsing everything into one score would hide the very pattern the study exists to detect.

## The "name-dropping" problem

A model that writes "refer via CDAP to the nearest public hospital" has not necessarily adapted to Trinidad and Tobago — it may have simply attached local vocabulary to a generic international plan. The rubric treats every named local programme, hospital, or pathway as a **claim to be verified**: does the model explain how the service would actually be accessed? Are its assumed timelines realistic? Does the local reference change the counselling or the plan?

The Handbook's rule: **name-dropping without operational detail is superficial localization** and is scored accordingly. The [exemplar case](../instruments/exemplar_case.md) shows this distinction concretely — two clinically strong responses to the same scenario, one of which merely *tags* the location ("location tagging") while the other lets the setting reshape the entire plan ("operational localization").

## Adaptation Latency

**Definition.** Adaptation Latency is the position within a response at which the model's recommendations first become genuinely shaped by the stated healthcare context — not merely tagged with a local name.

**Why position matters.** Localization that arrives too late is localization a busy clinician never benefits from. A response that spends five paragraphs on a management plan assuming on-demand angiography and unrestricted formularies, then closes with "of course, in Trinidad and Tobago, availability may vary," forces the physician to re-read and mentally rewrite everything above it. A response that opens already adapted to the setting can be acted on directly. Both responses "eventually localize" — but their clinical usability is entirely different. Adaptation Latency captures that difference.

**How it is scored.** Evaluators rate the flow of the answer on the anchored scale — no token counting:

| Score | Anchor | Meaning |
|---|---|---|
| 4 | Immediate | The local context shapes the very first recommendations; the answer never feels generic |
| 3 | Early | The setting is clearly acknowledged within the first paragraph or first few bullets |
| 2 | Mid | Starts generic; the local context appears only after initial management is described |
| 1 | Late | Mostly generic; the setting appears only near the end |
| 0 | Never | The answer could be for any country |

**What it is not.** Latency measures *when* adaptation appears, not *how good* the adaptation is — quality is Domains 3 and 4. The three adaptation domains are deliberately separable: a response can localize immediately but shallowly (high latency score, low adaptation scores) or deeply but late (the reverse).

**A fairness note.** Some presentations legitimately begin with universal priorities — an unstable patient is resuscitated the same way everywhere. The anchors account for this: what earns a high latency score is context *shaping* the earliest recommendations, which is fully compatible with stabilization-first structure. The exemplar case's stronger response opens with airway and hemodynamics *and* is localized from its first sentence.

**Planned validity check.** The analysis will examine how latency scores correlate with Resource and Contextual Adaptation scores, to test whether latency carries distinct signal or is redundant with adaptation quality — an open question this pilot is designed to inform. See [analysis_plan.md](analysis_plan.md).

---

*Related documents: [Evaluator Handbook](../instruments/) · [exemplar_case.md](../instruments/exemplar_case.md) · [study_design.md](study_design.md) · [analysis_plan.md](analysis_plan.md)*
