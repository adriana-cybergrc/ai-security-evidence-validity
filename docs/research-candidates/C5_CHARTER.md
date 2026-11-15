# C5 — Certifiable Completeness of Change-Conditioned Assurance Obligations under Partial System Observability

**Status:** PROPOSED / UNDER PRIOR-ART REVIEW  
**Originality:** NOT ESTABLISHED  
**Implementation:** NOT AUTHORIZED  
**Decision gate:** prior-art equivalence and formal reduction analysis

## 1. Motivation

The R1 closure review identified a recurring boundary in recent evidence-selection work: methods can select a minimum-cost subset of evidence relative to a supplied set of obligations, while the adequacy or discovery of those obligations remains an upstream problem.

C5 investigates that upstream boundary. It does **not** propose another dependency-impact selector, evidence cache, minimum-cost evidence envelope, or incremental/full execution equivalence method.

## 2. Preliminary research question

Under what explicit observability and modeling assumptions can the completeness of a change-conditioned assurance-obligation set be certified, and what lower bound on unresolved obligations remains when relevant system context, assumptions, or defeaters are unobserved?

## 3. Scope distinction

C5 concerns the adequacy of the obligation set itself:
- Which claim-relevant obligations must hold after a specified system change?
- Which contextual assumptions and defeaters can alter that obligation set?
- What can be certified from available observations?
- When is completeness unprovable without additional information?

Evidence selection and revalidation are downstream consumers of the obligation set and are outside the primary contribution.

## 4. Initial formal vocabulary

Let:
- (S) be the actual system and operational context;
- (O(S)) be the information observable to the assurance process;
- (C) be a top-level security claim;
- (A) be a structured assurance argument;
- (Delta) be a specified system change;
- (Omega(C,A,Delta,S)) be the set of obligations required to sustain (C) after (Delta);
- (widehat{Omega}) be the obligation set produced from available observations.

The central question is whether a procedure can certify:
[
Omega(C,A,Delta,S)subseteqwidehat{Omega}
]
for all admissible system contexts consistent with the observations and declared assumptions.

This expression is a research target, not an established result. The admissible context class, obligation semantics, and meaning of completeness remain to be defined.

## 5. Candidate hypothesis H5

There may exist nontrivial, explicit conditions on observability, argument structure, and defeater coverage under which a finite certificate can establish that a generated obligation set is complete for a bounded class of AI security assurance claims and changes.

The hypothesis is rejected if:
- the result reduces to ordinary requirements traceability/completeness checking;
- the result is equivalent to established assurance-case completeness or defeater-analysis methods;
- the certificate merely verifies completeness relative to a manually supplied obligation universe;
- the only sound procedure is to include every conceivable obligation;
- no independently checkable and falsifiable completeness condition can be defined.

## 6. Core theoretical risks

1. **Open-world impossibility:** if two contexts are observationally indistinguishable but imply different required obligations, exact completeness cannot be certified from the observations alone.
2. **Oracle dependence:** a manually supplied universe of all relevant obligations makes the problem circular.
3. **Trivial over-approximation:** including every possible obligation may be sound but useless.
4. **Reduction to requirements engineering:** completeness and traceability of requirements are mature topics.
5. **Reduction to assurance-case assessment:** structural completeness, argument validity, assumptions, and defeaters are established assurance concerns.
6. **Reduction to optimal information acquisition:** selecting observations that distinguish admissible contexts may be a standard active-information or decision-theoretic problem.

## 7. Prior art that must be examined first

- Goswami (2026), *Assurance Envelopes for Autonomous Coding Agents*, arXiv:2609.16302 — explicitly leaves obligation discovery outside its evidence-selection contribution: https://arxiv.org/abs/2609.16302
- Mukhopadhyay & Nalla (2026), *Reusing Assurance Evidence in AI Pipelines*, arXiv:2610.27672: https://arxiv.org/abs/2610.27672
- ISO/IEC/IEEE 15026-2:2022, assurance case structure and completeness terminology.
- GSN assurance-case completeness, argument assessment, and defeater analysis.
- Requirements completeness, bidirectional traceability, derived requirements, and change-impact analysis.
- Formal verification of requirements coverage and completeness under partial specifications.
- Active learning / optimal information acquisition under partial observability.

## 8. Required research gates

### Gate 1 — Definition
Define obligation semantics independently of the evidence-selection algorithm. Establish what counts as a required obligation and how claims, contexts, assumptions, strategies, and defeaters contribute.

### Gate 2 — Non-oracular completeness
Define a certificate whose verification does not require an oracle containing the complete obligation universe.

### Gate 3 — Impossibility and lower bounds
Construct indistinguishable admissible contexts with different obligation sets. Determine the minimum additional information needed to distinguish them, and test whether the resulting lower bound is stronger than generic partial-observation impossibility.

### Gate 4 — Prior-art reduction
Compare the formal result against assurance-case completeness, requirements traceability, defeater analysis, formal specification coverage, and information-acquisition methods.

### Gate 5 — Go / no-go
Proceed only if C5 yields a nontrivial theorem or algorithmic guarantee that cannot be reduced to the established methods above. Otherwise reject it without implementation.

## 9. Experimental policy

No code, benchmark, prototype, or dataset collection before Gates 1–4 pass. Any later experiment must compare against:
- manual obligation elicitation;
- traceability/completeness checking;
- assurance-case structural assessment;
- a conservative all-obligations baseline;
- an information-acquisition baseline, where applicable.

Measure completeness errors, false completeness certificates, unresolved obligation mass, information acquisition cost, and computational cost. Define operational metrics only after the semantics are fixed.

## 10. Current decision

C5 is a research candidate, not an approved thesis or a novelty claim. The next task is a focused literature review and formal definition of obligation completeness. No implementation or publication is authorized.
