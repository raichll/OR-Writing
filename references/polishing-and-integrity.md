# Polishing and Integrity Reference

Use this reference for OR/MS manuscript polishing, detox, citation integrity, and final quality control.

## Unified Polishing Principles

- Fix argument before sentences.
- Preserve the author's meaning unless reconstruction is requested.
- Do not invent data, references, mechanisms, theorems, proofs, experiments, or managerial implications.
- If evidence is missing, flag it instead of strengthening the claim.
- Write for the target reader first, then the target journal.
- Prefer precise claims with explicit boundaries over prestige language.
- Avoid em dashes by default; use commas, parentheses, or full stops.

## OR/MS Style Calibration

OR readers expect:

- a clearly named decision maker,
- decision variables and what they control,
- objective function and why it matches the decision problem,
- constraints and their operational meaning,
- uncertainty representation and how it is constructed,
- algorithmic logic and why it is valid or useful,
- computational evidence that matches the claims,
- managerial/practical implications that follow from the model, not generic policy advice.

## AI-Artifact Detox

Watch for:

- broad background that never narrows to the decision problem,
- gap claims with no cited support,
- contribution bullets that are not redeemed later,
- formula dumping without prose justification,
- undefined notation,
- report-like headings and excessive subheadings,
- too many bullets where paragraphs should develop logic,
- inflated adjectives such as novel, powerful, comprehensive, robust, transformative without evidence,
- repeated transitions such as "therefore", "furthermore", "moreover" without actual progression,
- decorative limitations that do not constrain claims.

Repair by:

- reverse-outlining each paragraph,
- giving each paragraph one job,
- converting parallel bullets into prose unless the list is genuinely useful,
- defining symbols before equations,
- adding interpretation after equations,
- moving implementation clutter to appendix,
- replacing hype with evidence.

## Citation Integrity

For every citation:

- verify author, year, title, journal/conference, volume/issue/pages, DOI or official URL,
- match the citation to the exact claim it supports,
- prefer version of record for published papers,
- use arXiv only for preprints or when the official record is unavailable,
- remove unverifiable references.
- remove or correct any entry whose DOI resolves to a different title or source,
- remove uncited bibliography entries unless they are intentionally reserved for supplementary material,
- keep recent or frontier references conservative: if formal publication cannot be verified, cite them as preprints or omit them.

For literature review:

- do not pile many citations behind one sentence,
- group by problem/model/algorithm stream,
- end each stream with a gap,
- include recent top-journal work and classic foundations.

Recommended target for a 30-page OR method paper:

- 40-70 references total,
- 10-20 recent papers from the last 3-5 years where relevant,
- 5-10 foundational papers.

## Figure and Table Quality

Figures should defend a claim, not decorate the paper.

Before drawing or revising a figure, define:

1. The claim the figure must support.
2. The evidence chain across panels.
3. The risk of misinterpretation.
4. Whether every number comes from data, model output, or a traceable calculation.

Figure rules:

- use multi-panel figures when they reduce cognitive load,
- avoid overlapping labels, oversized titles, and dense legends,
- keep color semantics consistent across figures,
- prefer editable PDF/SVG plus high-resolution PNG/TIFF,
- do not manually alter plotted values,
- cite data source or generated table if needed.

Table rules:

- each table should answer a specific claim,
- include units and metric definitions,
- avoid excessive decimals,
- explain infeasible, missing, or masked entries,
- keep benchmark settings fair and traceable.

## Final Manuscript Checklist

- Gap count equals contribution count, and order matches.
- Each contribution points to a theorem, algorithm result, table, or figure.
- Literature review has problem/model/algorithm streams, each ending in a gap.
- Model assumptions and parameters are justified.
- Notation is consistent across model, algorithm, experiments, and appendix.
- Exact reformulations and tractable approximations are clearly distinguished.
- Experiments include benchmark comparison, ablation, real case, and paradigm/sensitivity analysis when feasible.
- Statistical tests or uncertainty intervals are used when claims require them.
- Limitations are specific, not defensive repetition.
- References are real and claim-matched.
- Figures and tables are generated from traceable data or model outputs.
- Main-result tables contain only the intended main strategies or algorithms; sensitivity and ablation rows are kept in separate tables.
- A raw-data-to-result chain can be reconstructed from scripts, metadata, solver outputs, and generated table/figure files.
- Any live DOI or metadata audit failures have been corrected, removed, or explicitly flagged for author verification.
