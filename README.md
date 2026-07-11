# OR Writing and Polishing Skill

This repository contains a Codex skill for operations research and management science manuscript work.

It is designed for method-driven OR/MS papers that combine a decision problem, a mathematical model, a solution algorithm, and computational evidence. The skill helps with manuscript architecture, drafting, revision, polishing, citation integrity, figure/table design, and submission-readiness checks for journals such as Transportation Research series journals, Computers & Operations Research, European Journal of Operational Research, Omega, Reliability Engineering & System Safety, Transportation Science, IJOC, and related INFORMS-style outlets.

## What It Does

- Builds OR paper architecture around the chain: problem -> model -> algorithm -> evidence -> implications.
- Supports six-section manuscript planning: introduction, literature review, model, solution method, computational study, and conclusion.
- Polishes Chinese or English academic drafts into publication-oriented OR prose.
- Audits contribution-gap-evidence alignment, notation consistency, result traceability, and citation integrity.
- Provides guidance for algorithm explanation, pseudocode, appendices, workflow figures, experiment tables, and submission packages.

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── academic-figure-design.md
    ├── or-paper-architecture.md
    └── polishing-and-integrity.md
```

## Main Files

- `SKILL.md`: The main Codex skill definition and operating instructions.
- `references/or-paper-architecture.md`: Manuscript architecture rules for method-driven OR papers.
- `references/polishing-and-integrity.md`: Polishing, AI-writing detox, evidence control, and integrity checks.
- `references/academic-figure-design.md`: Scientific figure, workflow diagram, table, and experiment visualization guidance.
- `agents/openai.yaml`: Agent configuration metadata.

## Typical Use Cases

Use this skill when working on:

- OR/MS manuscript outlines, abstracts, introductions, literature reviews, model sections, algorithm sections, computational studies, or conclusions.
- Full-paper restructuring for applied OR journals.
- Chinese-to-English academic writing for OR manuscripts.
- Reviewer-risk audits before submission.
- Figure title polishing, workflow figure planning, experiment table design, or appendix planning.
- Contribution statements, highlights, cover letters, and submission package checks.

## Installation

Copy or clone this repository into your Codex skills directory:

```powershell
git clone git@github.com:raichll/OR-Writing.git C:\Users\15010\.codex\skills\or-writing-polishing
```

If a local copy already exists, back it up or update it with Git:

```powershell
cd C:\Users\15010\.codex\skills\or-writing-polishing
git pull
```

## Skill Metadata

The skill is registered as:

```yaml
name: or-writing-polishing
```

Codex should use it when the user asks for OR paper architecture, OR manuscript polishing, method-driven manuscript revision, model/algorithm/experiment writing, contribution-gap alignment, academic figure planning, citation integrity, or submission-style OR paper preparation.

## Maintenance Notes

- Keep `SKILL.md` as the single entry point.
- Put longer domain rules in `references/` and link to them from `SKILL.md`.
- Avoid adding fabricated citation examples, unverifiable journal claims, or placeholder experiment results.
- When updating writing rules, preserve the OR spine: decision problem, model, algorithm, evidence, and bounded implication.

