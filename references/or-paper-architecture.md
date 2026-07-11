# OR Paper Architecture Reference

Use this reference for method-driven OR/MS papers that propose a new problem/model plus a solution algorithm and validate it through benchmarks and real cases.

## Manuscript Spine

The paper is a single argument:

```
real unresolved decision problem
  -> mathematical abstraction P
  -> existing models or algorithms fail on P
  -> proposed model M and algorithm A
  -> benchmark + ablation + real case evidence
  -> theoretical and practical implications
```

If removing one link does not weaken the paper, that part is probably decorative.

## Six-Section Template

### Abstract

Use 200-250 words when possible:

1. One sentence for application context and importance.
2. One sentence for the unresolved gap.
3. One sentence naming the problem/framework \(P\).
4. Two sentences for model \(M\) and algorithm \(A\).
5. Two or three evidence sentences with key numbers, benchmark scale, case scale, or relative improvements.

The abstract is a proportional miniature of the manuscript.

Use dataset descriptions in the abstract at the right level of granularity. Prefer phrases such as `a full-year administrative ledger`, `a multi-period field dataset`, or `public benchmark instances` unless exact sample size is itself a core claim. Put exact row counts, column counts, missing-value counts, label distributions, and preprocessing audit details in the computational-study data subsection rather than the abstract.

### 1. Introduction

Use the six-element funnel:

1. Background: where the decision problem sits and why it matters.
2. Current state: how practice or literature currently addresses it.
3. Gap: usually three limitations, each tied to a technical challenge.
4. Motivation: why this paper can and should fill the gap.
5. Contributions: 3-4 items, each matching one gap.
6. Organization: one paragraph mapping Sections 2-6.

Between the background paragraph and the current-state paragraph, include a clear bridge from the application context to the OR abstraction. State the decision maker, the decision object, the scarce resource, and the uncertainty or constraint that makes the problem nontrivial. The current-state paragraph should then discuss OR or analytics studies that address this abstraction, rather than moving abruptly from policy background to a method list.

Keep detailed mathematical notation out of the Introduction. The Introduction can state the modelling idea and decision tradeoff, but variables, symbols, and equation-level notation should normally be introduced in Section 3. If a paragraph mainly explains notation that will be formally defined in the model section, remove it from the Introduction or move the explanation to the model section.

Contribution wording:

`We [develop/prove/design/test] ... to address [specific limitation].`

Contribution paragraph labels should summarize the contribution itself, not its category. Prefer labels such as `Robust routing formulation for uncertain demand`, `Calibration-aware prediction-to-optimization interface`, or `Case-based evidence from operational data`. Avoid generic labels such as `Model contribution`, `Algorithm contribution`, and `Empirical contribution` unless the target journal explicitly uses that convention.

Avoid broad novelty claims such as "first ever" unless verified and defensible.

### 2. Literature Review

Use three streams:

- Problem line: studies on the decision setting \(P\), variants, assumptions, and applications.
- Model line: work using the modelling paradigm \(M\), such as MILP, SP, RO, DRO, queues, networks, games, or decomposition-ready formulations.
- Algorithm line: exact, heuristic, decomposition, approximation, or learning-assisted solution methods related to \(A\).

Each stream should end with a specific gap that leads to the next section. Do not write a chronological list.

### 3. Model

Default order:

1. Problem definition and decision context.
2. Notation table, grouped by sets, indices, parameters, random/uncertain quantities, and decision variables.
3. Data-to-parameter or scenario construction if the model is data-driven.
4. Complete formulation: objective and constraints.
5. Assumptions and remarks explaining simplifications and nontrivial parameters.
6. Relation to baseline formulations, if needed.

The reader should be able to reconstruct the model after reading this section.

### 4. Solution Method

Default order:

1. Why the formulation is hard or why direct solution is insufficient.
2. Algorithm overview.
3. Components of algorithm \(A\): each component has purpose, formula/step, and supported property.
4. Pseudocode for the full algorithm, not every low-level implementation detail.
5. Theoretical properties: correctness, bounds, convergence, decomposition validity, or complexity, only when proven or cited.
6. Implementation details, with long details moved to appendix.

If the method replaces an exact model with a tractable approximation or surrogate, state whether the replacement is exact, approximate, heuristic, or empirically motivated.

### 5. Computational Study

Use four evidence layers:

1. Benchmark comparison: multiple baselines, fair settings, paired statistical tests where appropriate.
2. Ablation: remove or alter each proposed component and quantify what changes.
3. Real case: end-to-end demonstration, external validation if possible, and honest data limitations.
4. Paradigm comparison and sensitivity: compare modelling paradigms such as SP/RO/DRO/MILP/heuristics, and explain why the proposed approach works.

Each table or figure should redeem a contribution or answer a review-risk question.

For a paper built on a classical OR problem, use a two-part data architecture by default. First, use the standard public benchmark set matched to the core problem family, such as VRP/VRPTW for vehicle routing, TOP/OP for orienteering, knapsack for knapsack, or facility-location benchmarks for location models. Second, use the real-world, industrial, administrative, or constructed case dataset that demonstrates applied value. Neighbouring-problem datasets may be used only as supplementary checks and must not be described as the main standard benchmark for the focal problem.

Once the benchmark files have been downloaded and experiments have been run, write Section 5 in executed-result language. Report the source, extraction or parsing step, selected subset, script or solver, fixed seeds/time limits, generated output files, and result boundaries. Do not leave main-text phrases such as "should be replaced by benchmark results" or "recommended benchmark design" after actual benchmark evidence is available.

Main-text result tables should not contain empty cells, dashes, or planned-result placeholders when they are used to support a contribution. If the evidence is not available, move the table to an appendix as a validation protocol or remove it. If a prototype run is used, label it as such and tie it to generated output files.

Extra appendix experiments should be moderate and diagnostic unless the paper explicitly aims to be a benchmark study. Select the subset by a defensible property, such as instance scale, route-budget tightness, uncertainty intensity, or a specific module stress condition. Report the generated output files and result boundary. Include the appendix only when it clarifies where the proposed method helps or why a module matters; do not use large unfocused sweeps to pad the paper.

### 6. Conclusion

Use three parts:

- Theoretical implication: what the literature gains.
- Practical or managerial implication: what decision makers can do with the model.
- Limitations and future work: honest scope boundaries and natural extensions.

Do not introduce new results in the conclusion.

## Page Budget for a 30-Page Typeset Paper

For a complete applied OR manuscript or submission-style full draft, a compiled Elsevier-style PDF below 25 pages should be treated as incomplete unless the user explicitly asks for a short article, note, or proposal. The working target is 25-30 pages. If a compiled draft is shorter than 25 pages, expand substantive argument, model explanation, algorithm detail, computational evidence, robustness analysis, appendices, and interpretation before presenting it as complete.

Approximate allocation for Elsevier-style single-column manuscripts:

- Abstract + Introduction: 4-5 pages.
- Literature review: 3-4 pages.
- Model: 4-5 pages.
- Solution method: 6-7 pages.
- Computational study: 7-8 pages.
- Conclusion: 2-3 pages.

The solution and computational sections should usually occupy about half the paper.

## Appendix Planning

Move these to appendix:

- theorem and proposition proofs,
- long pseudocode,
- solver parameters and hyperparameters,
- extra benchmark tables,
- extra sensitivity analyses,
- long data preprocessing details,
- extended derivations.

Keep in the main text:

- problem logic,
- core model,
- algorithm idea,
- main evidence,
- interpretation.
