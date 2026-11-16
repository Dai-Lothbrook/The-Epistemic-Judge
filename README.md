# The Epistemic Judge

**The Epistemic Judge** is an empirical AI evaluation project designed to test whether language models make conclusions that are proportional to the evidence they are given.

The core problem is simple but consequential: models can sound analytically confident while relying on weak, dependent, incomplete, or non-diagnostic evidence. In forecasting, intelligence analysis, policy research, and other high-stakes reasoning tasks, that failure matters. A useful system should not only retrieve or summarize evidence — it should distinguish stronger from weaker support, recognize source dependence, avoid double-counting corroboration, resist unsupported inference, and update appropriately when challenged.

This project operationalizes those questions through controlled evidence packets, paired experimental conditions, structured target-model outputs, and an auditable LLM-as-judge measurement stack.

## What the evaluation studies

The evaluation is built around **evidence proportionality**: whether a model's claims, confidence language, source weighting, and final conclusion are justified by the evidence actually available in the packet.

The design examines behaviors such as:

- distinguishing direct evidence from indirect or weakly diagnostic evidence;
- recognizing when multiple sources share the same underlying origin;
- avoiding false source independence and double-counting;
- separating absence of evidence from evidence of absence;
- identifying material limitations and missing information;
- revising or defending a conclusion appropriately when challenged;
- avoiding overclaiming when the evidence does not establish the proposition.

The project uses a small set of carefully constructed cases with controlled evidence conditions and compares multiple frontier model configurations under the same closed-evidence task.

## Measurement architecture

The project includes:

- a structured target-output schema;
- an Initial Judge for evidence-quality and conclusion-quality assessment;
- an Evidence-Dependent Challenge (EDC) stage for measuring response to epistemic challenge;
- explicit rubrics and decision rules;
- calibration anchors with known expected behavior;
- independent regular judges with selective third-judge adjudication;
- raw-output preservation, prompt hashing, model/config tracking, and Langfuse observability;
- reproducible run-matrix and execution infrastructure.

The broader aim is not merely to score models, but to build a reusable methodology for evaluating whether AI systems reason in a way that is **traceable, evidence-sensitive, and epistemically disciplined**.

## Why this matters

The same failure modes appear in forecasting and intelligence work: overweighting vivid evidence, treating correlated reports as independent confirmation, carrying forward an early conclusion after the evidence changes, and converting uncertainty into unjustified certainty.

A model that performs well on evidence proportionality should be better suited for systems that support:

- probabilistic forecasting;
- intelligence analysis;
- foreign-policy research;
- risk assessment;
- evidence synthesis;
- high-stakes decision support.

## Project status

> **Experiment in production. Full empirical execution and publication are scheduled for January 2027.**

The scientific design, judge architecture, calibration assets, and substantial execution infrastructure have already been developed. The January phase will focus on final execution, judging, analysis, and publication.

---

**Research area:** AI evaluations · epistemic reasoning · evidence weighting · forecasting · LLM-as-judge methodology
