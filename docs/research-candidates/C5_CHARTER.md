# C5 — Certifiable Completeness of Change-Conditioned Assurance Obligations under Partial System Observability

**Status:** REJECTED — NO-GO (2026-11-14)  
**Originality:** NOT ESTABLISHED  
**Implementation:** NOT AUTHORIZED  
**Repository status:** Preserved as a negative research record

## 1. Original motivation

C5 investigated whether the completeness of change-conditioned assurance obligations could be certified when relevant system context, assumptions, or defeaters are only partially observable.

It was intentionally distinguished from dependency-impact analysis, evidence selection, evidence caching, and incremental/full execution equivalence.

## 2. Preliminary research question

Under what explicit observability and modeling assumptions can the completeness of a change-conditioned assurance-obligation set be certified, and what lower bound on unresolved obligations remains when relevant system context, assumptions, or defeaters are unobserved?

## 3. Formal sketches examined

Let (M) be a partial model, (Gamma(M)) its admissible concretizations, (Delta) a change, and (Omega(s,Delta)) the obligations required in context (s).

The examined universal/existential classification was:

[
Omega^{-}(M,Delta)=igcap_{sinGamma(M)}Omega(s,Delta)
]

[
Omega^{+}(M,Delta)=igcup_{sinGamma(M)}Omega(s,Delta)
]

[
U(M,Delta)=Omega^{+}(M,Delta)\setminusOmega^{-}(M,Delta)
]

The interpretation was:
- (Omega^{-}): obligations necessary in every admissible concretization;
- (Omega^{+}): obligations necessary in at least one admissible concretization;
- (U): obligations whose necessity is indeterminate under the partial model.

This construction is mathematically coherent as a classification, but it maps directly to universal/existential reasoning over concretizations and three-valued semantics for partial specifications. It does not itself establish a new algorithm or theorem.

## 4. Why C5 was rejected

1. **Assurance-case completeness overlap:** completeness, argument adequacy, assumptions, hazards, and defeaters are established assurance-case concerns.
2. **Automated semantic analysis overlap:** goal-directed ASP and Assurance 2.0 tooling already analyze semantic properties of assurance arguments, including completeness-related conditions.
3. **Partial-model checking reduction:** universal/existential classification across concretizations is established partial-specification / three-valued model-checking semantics.
4. **Generic impossibility is insufficient:** indistinguishable contexts with different obligations imply a basic information-theoretic impossibility, not a distinct contribution by itself.
5. **Obligation-universe problem remains:** verifying all obligations in a supplied vocabulary does not prove that the vocabulary contains every relevant obligation. A non-oracular generator with a completeness guarantee was not established.
6. **No nontrivial lower bound:** no result stronger than generic partial-observability limits was demonstrated.

## 5. Rejection criteria triggered

- The proposed result reduces to established assurance-case completeness and semantic assessment.
- The proposed formal classification reduces to established partial-model / three-valued model checking.
- A certificate over a manually supplied obligation universe would be circular with respect to open-world completeness.
- No independent, non-oracular completeness certificate or stronger lower bound was established.

## 6. Preserved negative findings

- Generic indistinguishability proposition: valid, but not novel as formulated.
- (Omega^{-}), (Omega^{+}), and (U) classification: valid formal sketch, but reducible to partial-specification semantics.
- Assurance 2.0 / ASP overlap: decisive prior-art risk.
- Requirements completeness, defeater analysis, and information acquisition remain mature neighboring areas.
- No code, benchmark, prototype, or dataset was created or authorized.

## 7. Final decision

**NO-GO — C5 is closed as an independent research candidate.**

This rejection applies to the current formulation and its examined variants. It does not assert that all research on AI security assurance obligations is exhausted. Any future proposal must introduce a materially different formal object or guarantee and pass a new prior-art reduction before implementation.
