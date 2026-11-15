# R1 Candidate Closure Record — 2026-11-14

## Decision

**CLOSED — C1, C2, C3, and C4/C4-R do not proceed as independent research candidates.**

This decision means that the investigated formulations did not establish a sufficiently distinct contribution against the identified prior art. It does not mean that the broad problem of AI security assurance evidence is solved.

## Candidates covered

- **C1 — Collective sufficiency of evidence for an assurance claim:** not retained as a standalone novelty claim; assurance-case structure, argument validity, and evidence sufficiency are established topics.
- **C2 — Shared dependencies and change propagation:** not retained as a standalone novelty claim; assurance-case change-impact analysis, architecture-to-GSN mapping, and regression impact analysis predate this work.
- **C3 — Selective revalidation equivalent to full evaluation:** not retained as a standalone novelty claim; incremental verification, safe regression-test selection, and incremental assurance already address closely related guarantees.
- **C4 — Assurance preservation under incomplete dependency knowledge:** rejected as an independent candidate due to direct overlap with AI-pipeline evidence reuse under undeclared dependencies, conservative invalidation, and incremental/full decision equivalence.
- **C4-R — Identifiability boundaries / argument-structure-based selectivity:** not retained. The indistinguishability argument in its generic form is elementary under partial observation; the proposed evidence-selection angle also overlaps with recent work on task-conditioned assurance envelopes.

## Decisive prior art

1. **Mukhopadhyay & Nalla (2026), arXiv:2610.27672**, *Reusing Assurance Evidence in AI Pipelines: Validity Conditions, a Fail-Closed Release Gate, and a Replay of 714 Public Data Version Control Pipelines*. Direct overlap: evidence validity, dependency completeness, stale evidence from undeclared dependencies, sufficient conditions for incremental/full decision equivalence, and empirical measurements across 714 DVC pipelines. The version examined is an arXiv preprint submitted 20 October 2026; final journal publication was not confirmed in this review. https://arxiv.org/abs/2610.27672
2. **Goswami (2026), arXiv:2609.16302**, *Assurance Envelopes for Autonomous Coding Agents: Minimum-Cost Evidence for Software Change*. Direct overlap with minimum-cost evidence selection over typed inference graphs, AND/OR argument structure, and task-conditioned evidence sufficiency. The author explicitly leaves obligation discovery and downstream agent benefit open. https://arxiv.org/abs/2609.16302
3. **Cheng et al. (2022), arXiv:2209.11632**, *Facilitating Change Implementation for Continuous ML-Safety Assurance*. Semantic tags and argument-tree queries identify evidence invalidated by changes. https://arxiv.org/abs/2209.11632
4. **Fung et al. (2018)**, *MMINT-A: A Tool for Automated Change Impact Assessment on Assurance Cases*. https://doi.org/10.1007/978-3-319-99229-7_7
5. **Björnander, Land & Graydon (2012)**, *A Method to Formally Evaluate Safety Case Evidences against a System Architecture Model* (GAGE). GSN/AADL mapping for impact analysis.
6. **Elsner & Pretschner (2023)**, *DIRTS: Dependency Injection Aware Regression Test Selection*. https://doi.org/10.1109/ICST57152.2023.00046
7. **Palmskog, Celik & Gligoric (2020)**, *Practical Machine-Checked Formalization of Change Impact Analysis*. https://doi.org/10.1007/978-3-030-45237-7_9
8. **Diemert et al. (2023)**, *Incremental Assurance Through Eliminative Argumentation*. https://doi.org/10.56094/jss.v58i1.215
9. **Idmessaoud, Dubois & Guiochet (2022)**, *Uncertainty Elicitation and Propagation in GSN Models of Assurance Cases*. https://doi.org/10.1007/978-3-031-14835-4_8

## Findings

- Evidence validity, argument sufficiency, dependency impact, selective re-execution, and conservative handling of undeclared dependencies are each established or directly addressed in prior work.
- Merely representing incomplete dependency knowledge as a family of possible graphs does not establish a distinct contribution.
- Generic indistinguishability under partial observation is not, by itself, a novel theorem.
- Replacing dependency graphs with assurance argument graphs or AND/OR inference graphs does not establish novelty; minimum-cost evidence selection over such graphs has also been proposed.
- Any future candidate must identify a result beyond these methods, with explicit assumptions, counterexamples, baselines, and a falsifiable advantage.

## What is preserved

All scaffold files, research questions, hypotheses, and negative findings remain part of the research record. This closure does not delete prior artifacts or imply that previous structural validation established scientific validity.

## Follow-on

C5 is opened as a **proposed candidate only** in `docs/research-candidates/C5_CHARTER.md`. It is not approved for implementation and has no established originality claim.
