# OR Writing and Polishing Skill

This repository contains a Codex skill for writing, restructuring, polishing, and auditing operations research (OR) and management science (MS) manuscripts.

The skill is intended for method-driven papers where the manuscript must connect a real decision problem, a mathematical formulation, a solution algorithm, and computational evidence. It is especially useful for applied OR papers targeting journals such as the Transportation Research series, Computers & Operations Research, European Journal of Operational Research, Omega, Reliability Engineering & System Safety, Transportation Science, IJOC, and related INFORMS-style or Elsevier OR/MS outlets.

## Purpose

The skill gives Codex a specialized editorial and methodological stance for OR manuscripts. Instead of treating academic writing as generic polishing, it forces the paper to be checked against an OR argument:

```text
real decision problem
-> mathematical abstraction
-> model and algorithmic contribution
-> benchmark, ablation, and case evidence
-> theoretical and practical implications
```

This matters because many OR papers fail not at the sentence level, but at the alignment level. The introduction may promise one contribution, the model may solve a slightly different problem, the algorithm may not be justified, and the computational study may not redeem the claimed novelty. This skill is designed to catch and repair those breaks.

## What The Skill Helps With

### Manuscript Architecture

The skill can help plan or rebuild a complete OR paper. It supports a standard six-section structure:

1. Introduction
2. Literature review
3. Problem formulation or model
4. Solution method
5. Computational study
6. Conclusion

It also helps decide what belongs in appendices, how much space each section should receive, and whether the paper reads like a journal article rather than a project report.

### OR-Specific Drafting

The skill supports drafting and revising:

- titles, abstracts, and keywords;
- introduction funnels and contribution statements;
- literature-review streams;
- model sections and notation explanations;
- algorithm sections and pseudocode;
- computational-study designs;
- conclusions with theoretical and managerial implications;
- cover letters, highlights, and submission package text.

The focus is not only fluency. The skill checks whether each claim is tied to a model choice, algorithmic component, theorem, table, figure, benchmark, ablation, case study, or appendix proof.

### Polishing And Translation

The skill can polish English academic prose and translate Chinese OR drafts into publication-oriented English. It aims for clear, accountable OR writing: decision maker first, assumptions explicit, claims bounded, evidence traceable, and novelty stated without exaggeration.

It also removes common AI-like writing artifacts, including inflated transitions, decorative claims, repeated sentence templates, unsupported novelty language, and generic contribution labels.

### Integrity And Reviewer-Risk Audit

The skill includes checks for:

- contribution-gap-evidence alignment;
- notation consistency across model, algorithm, and experiments;
- unsupported claims in abstracts, introductions, captions, and conclusions;
- fabricated or unverifiable references;
- stale result numbers and manually typed table values;
- missing ablations or unfair baselines;
- overclaiming algorithmic novelty;
- weak data/code availability statements;
- appendices that are not cited or do not support the main text.

For computational OR papers, the preferred evidence chain is:

```text
raw data
-> processing script
-> solver or model output
-> result CSV/JSON
-> table or figure generator
-> manuscript
```

## When Codex Should Use This Skill

Use this skill when the task involves any of the following:

- OR/MS manuscript writing, rewriting, or polishing;
- applied OR paper architecture;
- model, algorithm, or experiment section drafting;
- operations research literature-review planning;
- contribution-gap alignment;
- algorithm explanation depth;
- pseudocode style;
- benchmark, ablation, or sensitivity-study design;
- figure title polishing or workflow figure planning;
- citation integrity checks;
- Chinese-to-English academic writing for OR papers;
- submission package preparation for OR/MS journals.

Example user requests that should trigger this skill:

```text
Polish this OR manuscript introduction.
Help me rebuild the structure of my routing paper.
Write a computational study section for this model.
Audit whether my contributions match my experiments.
Translate this Chinese OR abstract into journal-style English.
Design figure titles for my algorithm workflow and ablation plots.
Prepare highlights and a cover letter for an Elsevier OR journal.
```

## Core Writing Philosophy

The skill is built around five principles.

### 1. The Paper Must Have An OR Spine

Every section should support the same chain:

```text
decision problem -> model -> algorithm -> evidence -> implication
```

If a paragraph, figure, table, theorem, or appendix does not strengthen this chain, it should be revised, moved, or removed.

### 2. Contributions Must Be Redeemed

Each contribution should map to:

- a specific literature or practice gap;
- a specific manuscript location;
- a model, algorithm, theorem, experiment, figure, table, or case result;
- a clear boundary saying what the paper does not claim.

A useful internal ledger is:

```text
Gap -> Contribution -> Manuscript location -> Evidence -> Boundary
```

### 3. Model Choices Need Justification

Assumptions, objectives, uncertainty sets, constraints, and data-to-parameter transformations should be argued rather than merely stated. The reader should understand why the formulation fits the real decision setting.

### 4. Algorithmic Novelty Should Be Bounded

The skill discourages exaggerated claims such as "first ever" or "novel algorithm" unless the novelty is verified and supported. If the contribution is mainly in formulation, data-to-optimization design, calibration, uncertainty construction, or empirical diagnosis, the paper should say that honestly.

### 5. Polishing Cannot Repair Broken Evidence

The skill treats polishing as the final layer, not the first layer. It first checks the argument, evidence, model, algorithm, notation, and references. Sentence fluency comes after the manuscript logic is sound.

## Repository Structure

```text
.
|-- README.md
|-- SKILL.md
|-- agents/
|   `-- openai.yaml
`-- references/
    |-- academic-figure-design.md
    |-- or-paper-architecture.md
    `-- polishing-and-integrity.md
```

## File Guide

### `SKILL.md`

The main skill definition. It contains:

- trigger description and metadata;
- first-decision task classification;
- four-stage manuscript workflow;
- OR manuscript structure rules;
- introduction, literature-review, model, algorithm, experiment, conclusion, appendix, and figure rules;
- data/result integrity checks;
- submission package guidance.

This is the entry point Codex reads when deciding how to handle OR writing tasks.

### `references/or-paper-architecture.md`

Detailed architecture guidance for method-driven OR papers. It explains:

- the manuscript spine;
- six-section paper structure;
- abstract and introduction design;
- literature-review stream organization;
- model and solution-method section order;
- computational-study evidence layers;
- conclusion structure;
- page-budget and appendix-planning rules.

Use this reference when the task is about outlining, rebuilding, expanding, or auditing a full paper.

### `references/polishing-and-integrity.md`

Guidance for sentence-level and manuscript-level polishing. It focuses on:

- academic English quality;
- AI-like writing detox;
- claim control;
- citation and reference integrity;
- evidence traceability;
- final quality checks before submission.

Use this reference when the task is polishing, translation, final audit, or submission cleanup.

### `references/academic-figure-design.md`

Guidance for OR figures and tables. It covers:

- workflow and architecture diagrams;
- experiment plots;
- ablation and sensitivity figures;
- figure title writing;
- table design and caption logic;
- scientific visualization standards for manuscripts.

Use this reference when the user asks for figure planning, figure titles, workflow diagrams, or experiment visualization.

### `agents/openai.yaml`

Agent configuration metadata used by Codex-related tooling.

## Recommended Workflow

For a full manuscript project, use the skill in this order:

1. Inspect the project folder and identify existing manuscripts, data, code, figures, bibliography, and results.
2. Clarify the target journal or journal family.
3. Identify the decision problem, model family, and solution algorithm family.
4. Build a contribution ledger.
5. Draft or rebuild the six-section manuscript structure.
6. Audit model, algorithm, experiments, figures, tables, citations, and claims.
7. Polish the text after the argument and evidence are coherent.
8. Prepare submission files if requested.

For a smaller task, such as polishing one paragraph, Codex can use only the relevant parts of the skill. Even then, the prose should not make claims stronger than the supplied evidence.

## Installation

Clone this repository into your Codex skills directory:

```powershell
git clone git@github.com:raichll/OR-Writing.git C:\Users\15010\.codex\skills\or-writing-polishing
```

If a local copy already exists, update it with Git:

```powershell
cd C:\Users\15010\.codex\skills\or-writing-polishing
git pull
```

## Skill Metadata

The skill is registered as:

```yaml
name: or-writing-polishing
```

The skill description in `SKILL.md` tells Codex when to use it. In normal use, users do not need to mention the exact skill name. A request about OR manuscript structure, OR polishing, OR paper revision, contribution alignment, or OR submission preparation should be enough to trigger it.

## Maintenance Notes

- Keep `SKILL.md` as the single entry point.
- Keep long domain guidance in `references/` and link it from `SKILL.md`.
- Preserve the OR spine: decision problem, mathematical model, solution method, computational evidence, and bounded implications.
- Do not add fabricated citation examples, unverifiable literature claims, invented experiment values, or placeholder results.
- Prefer concrete journal-style rules over vague writing advice.
- When adding new guidance, make it auditable: state what Codex should check, when it should check it, and what output should change.

## License

No license has been specified yet. Add one before distributing or reusing this repository outside personal Codex skill management.
