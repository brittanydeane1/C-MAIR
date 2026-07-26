# Study Design

*What we did, and why we did it that way. For the scoring rubric see [scoring_and_latency.md](scoring_and_latency.md); for the evaluator process see [evaluator_process.md](evaluator_process.md).*

---

## Overview

C-MAIR's pilot is an exploratory, fully crossed feasibility study: **3 models × 5 scenarios × 10 physician evaluators × 6 scoring domains** (900 domain-level ratings in total). Every evaluator scores every response, which allows inter-rater reliability to be estimated directly — the pilot's primary outcome.

The study proceeds in three phases:

1. **Instrument development (completed).** Scenario writing, reference-standard development, rubric drafting, and calibration material creation.
2. **Evaluation (in progress).** Ten physicians independently score all fifteen model responses. Target completion: September 2026.
3. **Analysis (pending).** Reliability and feasibility analysis per the locked [analysis plan](analysis_plan.md).

## The clinical scenarios

Five standardized scenarios were developed, each set explicitly within Trinidad and Tobago's healthcare system:

1. Persistent uncontrolled Type 2 Diabetes Mellitus with healthcare access barriers
2. Hepatocellular carcinoma
3. Acute pancreatitis
4. Atrial fibrillation
5. Paraquat poisoning

All scenarios are fully synthetic. No real patient data was used at any stage.

**Why these are not textbook cases.** The scenarios are deliberately complex, context-rich vignettes rather than idealized examination cases. Each one combines several dimensions at once: clinical reasoning, patient safety, resource limitations, socioeconomic barriers, cultural context (e.g., bush medicine, dietary patterns), occupational exposures, psychosocial factors, local referral pathways, and public formulary constraints (CDAP). The goal is **ecological validity** — the cases should resemble what an internal medicine registrar actually receives in a Trinidad and Tobago public hospital, where clinical problems arrive tangled with system and social realities. This is not "red teaming": there is no adversarial intent to trick the models. The scenarios are hard because real practice is hard.

**Why five.** Each evaluator scores fifteen long clinical responses across six domains — a substantial commitment for practising physicians volunteering their time. Five scenarios is the realistic ceiling for careful, unhurried scoring at pilot scale, and depth of evaluation matters more than breadth when the objective is testing the instrument rather than ranking models.

**Scope note.** The scenarios are evaluated from the **internal medicine registrar's perspective**, but three present through acute or emergency settings. This reflects how internal medicine is actually practised in Trinidad and Tobago's public system, where registrars receive acute referrals directly. The scope is best described as *acute and ambulatory adult general medicine*.

**One scenario is public.** To protect the scenarios from entering future model training data, only one complete worked exemplar is published ([instruments/exemplar_case.md](../instruments/exemplar_case.md)). See [data_access.md](data_access.md).

## The models and how responses were generated

Three frontier models were evaluated: **GPT 5.5**, **Claude Opus 4.8**, and **Gemini 3.6 Flash**.

Responses were generated on **5 July 2026** through each model's **consumer chat interface**, using identical prompt text for every model. One response per model per scenario was captured verbatim (15 responses total).

Two points are documented here for transparency:

- **Consumer interfaces expose no inference controls.** Temperature, sampling parameters, and true system prompts cannot be set in consumer apps. The prompt included an instruction requesting deterministic, consistent output, but prompt-level instructions cannot enforce reproducible generation. The captured responses are single samples.
- **Why consumer interfaces anyway.** This was a deliberate choice, not a shortcut. Physicians in Trinidad and Tobago who use these tools use them through the consumer apps — not the developer API. Evaluating the models as clinicians actually encounter them is the ecologically valid choice for a study about real-world clinical usability. A future study may add version-pinned API generation as a comparison arm; see [limitations_and_ethics.md](limitations_and_ethics.md).

## Reference standards

For each scenario, a **Case Reference Standard** defines the principal diagnosis, non-negotiable management steps, a safety trap, the resource constraints in play, and the contextual elements a well-adapted response should use.

Two senior physicians independently reviewed each scenario, reference standard, and the scoring rubric. Points of disagreement or ambiguity were discussed until consensus was reached, and ambiguities identified during this process were recorded as explicit "ambiguity flags" within each reference standard rather than hidden. The finalized standards were then adopted for calibration and formal scoring.

We use the term *reference standard* rather than *gold standard* deliberately: these documents encode expert consensus, including judgment calls, and expert consensus can be wrong. This is acknowledged as a limitation in [limitations_and_ethics.md](limitations_and_ethics.md).

## The evaluators

Ten physicians practising in Trinidad and Tobago serve as evaluators. None had previously evaluated AI systems — which is representative of the physician population any real-world deployment would rely on, but which also creates a reliability risk. That risk motivated the calibration programme described in [evaluator_process.md](evaluator_process.md): an evaluator handbook, worked scoring examples, a structured calibration session, and a short orientation video, all completed before formal scoring.

**Blinding.** Evaluators are blinded to model identity; models are labelled Model 1, 2, and 3 (randomly assigned). Because frontier models have recognizable styles, blinding may be imperfect — so after scoring, each evaluator records a guess of each model's identity, converting an unmeasurable weakness into a measurable one. Scenario presentation order was fixed rather than randomized, which is noted as a limitation.

## Why these design choices

- **Why an exploratory pilot?** A benchmark is only as good as its scoring instrument. Before any large-scale claims can be made, the rubric, calibration process, and data collection workflow must be shown to work. Running a large study on an unvalidated instrument would waste the scarcest resource in this field: physician time.
- **Why physician evaluators?** Whether a management plan is *implementable* in a Trinidad and Tobago public hospital is a clinical judgment. Automated metrics and lay raters cannot assess whether a referral pathway is realistic, a drug is on the public formulary, or a timeline survives contact with an actual waitlist.
- **Why Trinidad and Tobago?** It is the Principal Investigator's practice setting, which makes feasibility judgments verifiable rather than speculative. Its public system has well-characterized structures (CDAP formulary, RHA referral pathways, named tertiary centres) against which model recommendations can be concretely checked. And it is representative of resource-constrained health systems globally — the setting where the gap between model assumptions and reality is largest and least studied.
- **Why evaluate *when* adaptation happens?** See [scoring_and_latency.md](scoring_and_latency.md).

---

*Related documents: [scoring_and_latency.md](scoring_and_latency.md) · [evaluator_process.md](evaluator_process.md) · [analysis_plan.md](analysis_plan.md) · [limitations_and_ethics.md](limitations_and_ethics.md) · [data_access.md](data_access.md)*
