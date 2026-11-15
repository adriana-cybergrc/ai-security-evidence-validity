# ai-security-evidence-validity

Research scope: temporal validity, assurance continuity, and selective revalidation of AI security evidence under model, data, configuration, and dependency changes.

## Research status

- **R1 initial line (C1–C4): CLOSED — no distinct original contribution established.**
- **C5: PROPOSED / UNDER PRIOR-ART REVIEW — no originality claim.**
- This repository records research hypotheses and evidence; a structural scaffold passing validation does not establish scientific novelty, correctness, or validity.

## R1 closure decision

The initial line was closed after prior-art comparison showed substantial overlap with established work on safety-case change-impact analysis, incremental assurance, ML safety-case evolution, safe regression-test selection under dynamic/undeclared dependencies, and evidence reuse in AI pipelines.

The closest direct works include:
- Mukhopadhyay & Nalla (2026), [Reusing Assurance Evidence in AI Pipelines](https://arxiv.org/abs/2610.27672): evidence validity, sufficient conditions for incremental/full decision equivalence, undeclared dependencies, and an empirical replay of 714 DVC pipelines.
- Goswami (2026), [Assurance Envelopes for Autonomous Coding Agents](https://arxiv.org/abs/2609.16302): minimum-cost evidence selection over typed inference graphs; obligation discovery is explicitly left outside the contribution.
- Cheng et al. (2022), [Facilitating Change Implementation for Continuous ML-Safety Assurance](https://arxiv.org/abs/2209.11632): change impact on ML safety-case evidence.
- Fung et al. (2018), [MMINT-A: Automated Change Impact Assessment on Assurance Cases](https://doi.org/10.1007/978-3-319-99229-7_7).
- Elsner & Pretschner (2023), [DIRTS: Dependency Injection Aware Regression Test Selection](https://doi.org/10.1109/ICST57152.2023.00046).
- Palmskog, Celik & Gligoric (2020), [Practical Machine-Checked Formalization of Change Impact Analysis](https://doi.org/10.1007/978-3-030-45237-7_9).
- Diemert et al. (2023), [Incremental Assurance Through Eliminative Argumentation](https://doi.org/10.56094/jss.v58i1.215).

The closure is a research decision, not a claim that these works solve every possible assurance problem. See `docs/decisions/R1_CANDIDATE_CLOSURE_2026-11-14.md`.

## Current candidate

**C5 — Certifiable Completeness of Change-Conditioned Assurance Obligations under Partial System Observability**

Research question, preliminary:
> Under what explicit observability and modeling assumptions can the completeness of a change-conditioned assurance-obligation set be certified, and what lower bound on unresolved obligations remains when relevant system context or defeaters are unobserved?

C5 is deliberately separated from evidence selection and dependency-impact propagation. Its target is the adequacy/completeness of the obligations against which evidence is selected. This is a proposed direction only; requirements completeness, assurance-case completeness, defeater analysis, and optimal information acquisition are substantial prior-art domains and must be examined before any originality claim.

See `docs/research-candidates/C5_CHARTER.md`.

## Governance

- No implementation until closest prior art and reduction analysis pass.
- No originality claim from terminology gaps or an unreviewed combination of known methods.
- Define assumptions, counterexamples, falsifiers, baselines, and acceptance criteria before experiments.
- Preserve negative results and distinguish proposed, experimental, validated, rejected, and inconclusive outcomes.
- No merge to `main`, publication, or further implementation without review and explicit approval.
