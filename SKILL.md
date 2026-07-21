---
name: or-writing-polishing
description: Build, restructure, polish, audit, or complete method-driven operations research manuscripts for journals such as TRE, TRC, COR, EJOR, IJOC, OMEGA, RESS, Transportation Science, and INFORMS-style outlets. Use when the user asks for OR paper architecture, six-section manuscript structure, model/algorithm/experiment writing, worked examples for mathematical models, algorithm explanation depth, contribution-gap alignment, literature strategy, citation integrity, appendix planning, architecture/workflow figure design, experiment plot recommendations, English figure titles, figure/table polish, AI-like writing detox, Chinese-to-English academic writing, or publication-quality OR manuscript revision.
---

# OR Writing and Polishing

Use this skill as the default entry point for method-driven OR/MS manuscripts: a decision problem \(P\), a modelling paradigm \(M\), a solution algorithm \(A\), and evidence from benchmarks, ablations, and real cases.

It combines:

- OR paper architecture: problem-model-algorithm-experiment-conclusion logic.
- Unified polishing: Nature-style clarity, INFORMS/OR-MS accountability, and AI-artifact detox.
- Integrity controls: real literature only, evidence-bounded claims, reproducible figures/tables, and honest limitations.

## First Decision

Classify the task before writing.

- `Architecture`: outline, section structure, contribution design, page budget, appendix plan.
- `Drafting`: abstract, introduction, literature review, model, algorithm, experiments, discussion, conclusion.
- `Revision`: restructure an existing manuscript, compress/expand sections, align OR style, reduce report-like structure.
- `Polishing`: improve English, translate Chinese drafts, detox AI-like prose, sharpen claims.
- `Audit`: check gap-contribution-evidence alignment, citation integrity, notation, experiments, figures, or overclaims.

For architecture or full-paper rebuilding, read `references/or-paper-architecture.md`.
For polishing, detox, citation integrity, and final quality control, read `references/polishing-and-integrity.md`.

## Mandatory Four-Question Intake Gate

For a new full-paper architecture, drafting, rebuilding, or submission-preparation task, first inspect the current project folder read-only, then ask exactly these four questions in one concise grouped message before drafting or editing manuscript content:

1. `Journal:` What is the intended journal or journal family?
2. `Problem:` What decision problem should the manuscript solve?
3. `Model:` What model or modelling family should the manuscript build?
4. `Algorithm:` What solution algorithm or algorithm family should the manuscript use?

The project-folder scan is internal preparation and is not a fifth question. Do not silently replace any of the four questions with an inference from local files. When the folder strongly suggests an answer, include that answer as a proposed default inside the relevant question and ask the user to confirm or correct it. If the user has already answered one or more items explicitly in the same request, restate those answers and ask only for confirmation or the unresolved items while preserving the four-item intake record.

Do not start long-form drafting, rebuild a manuscript, or switch templates until the intake is answered. If the user explicitly says to proceed without answering, document assumptions for all four items and continue. Skip this gate only for a narrow polishing, translation, audit, citation, or figure/table task when journal, problem, model, and algorithm choices are not being created or changed.

## Journal-Specific LaTeX Template Gate

After the journal is confirmed and before drafting or rebuilding the manuscript, check the journal's current official Guide for Authors for its required LaTeX class, article layout, bibliography style, and submission-file rules. Download the journal-specific LaTeX template package from the official publisher, journal, or publisher-authorized Overleaf source when one is specified. If the user has already supplied the same official package locally, verify its contents and use it instead of downloading a duplicate.

If no journal is selected, or the selected Elsevier journal has no dedicated template, download and use the current official Elsevier article template from `https://www.elsevier.com/researcher/author/policies-and-guidelines/latex-instructions`. Select `elsarticle`, CAS single-column, or CAS double-column only according to the official journal guidance and package documentation; do not recreate an approximate house template or merely borrow a class declaration while retaining a custom manuscript structure.

Treat the downloaded package as the manuscript's mother template. Preserve its class files, front-matter commands, bibliography style, fonts, spacing, and sample file organization unless the journal explicitly permits a change. Record the template source URL, access date, package/version clues, selected class, and selection rationale in the project notes. Compile inside the official template before substantive writing and again before delivery. When preparing Elsevier Editorial Manager source files, follow the current official instruction that submission files must be placed at one folder level rather than in subfolders.

## Four-Stage Manuscript Workflow

Use this four-stage workflow for full OR manuscript creation, rebuilding, or submission preparation.

1. `Pre-manuscript intake.` Read the current project folder, identify available data/code/templates/results, complete the mandatory four-question intake, then pass the journal-specific LaTeX template gate before drafting.
2. `Formal manuscript writing.` Build the manuscript from title, abstract, six-section body, data/code availability, acknowledgements, appendices, and references. Keep the OR spine visible from the title through the conclusion.
3. `Polishing and integrity audit.` After the structure and evidence are in place, polish argument, language, notation, tables, figures, citations, result arithmetic, reproducibility, and reviewer-risk points. Do not polish unsupported claims into stronger claims.
4. `Submission package delivery.` When requested, deliver the complete manuscript package: main manuscript source/PDF, title page if needed, cover letter, highlights, graphical or textual abstract if required, data/code availability wording, conflict-of-interest statement, author contributions, and any required supplementary files.

Do not skip directly to prose drafting when the task is a new full paper. Apply the mandatory four-question intake gate first; if the user explicitly asks to proceed without answering, make documented assumptions and continue.
## Pre-Manuscript Intake Workflow

Before drafting or rebuilding a full OR manuscript, do not jump directly into section writing. First establish the project foundation, target outlet, decision problem, model family, and solution method.

1. `Read the current project folder first.` Inspect the working directory before proposing a paper logic. List and skim available data files, algorithm scripts, solver outputs, LaTeX templates, existing manuscripts, figures, bibliography files, notes, reference papers, and generated results. Use this scan to identify what is already available, what can be rerun, what template should be used, and what evidence is missing. Prefer local files over assumptions.
2. `Ask for the intended journal or journal family.` If the user provides a target journal, check the journal's scope, article type, author guidelines, template requirements, reference style, page or word expectations, data/code policy, and recent article style before drafting. If no target is provided, proceed with the default applied OR profile in this skill and state the assumption.
3. `Ask what problem the manuscript should solve.` Invite the user to provide reference papers, reviewer comments, problem notes, or desired application framing. If the user does not provide a specific problem, infer candidate OR research problems from the folder contents, available data, existing scripts, and domain clues, then propose a focused decision problem rather than a broad topic.
4. `Ask what model the manuscript should build.` Invite the user to provide reference papers or a preferred modelling paradigm. If none is provided, match the decision structure to mainstream OR model families, such as VRP/VRPTW, TOP/OP, stochastic programming, robust or distributionally robust optimization, queueing, scheduling, location, inventory, assignment, network flow, or bilevel optimization. Explain why the selected model fits the data, uncertainty, resource constraints, and decision timing.
5. `Ask what solution algorithm is desired.` Invite the user to provide reference algorithms or papers. If none is provided, search or identify frontier solver families for the chosen OR problem, such as exact decomposition, branch-and-cut, branch-and-price, matheuristics, HGS, ALNS, LNS, CP-SAT/MIP, reinforcement learning, or learning-guided heuristics. Choose a strong citable base method, diagnose its weakness for the target model, and add only controlled modules that can be justified and ablated.
6. `Document assumptions before drafting.` If the user asks to proceed without answering all questions, continue autonomously using folder evidence and OR conventions, but record the assumed journal style, problem statement, model family, algorithm family, and evidence plan. These assumptions should be revisited before finalizing the manuscript.

Ask the journal, problem, model, and algorithm questions concisely in one short grouped message. Treat the project scan as internal preparation, not an additional question. Once enough information is available, produce a contribution ledger and manuscript plan before writing long prose.
## Core OR Spine

A method-driven OR paper must read as one unbroken argument:

`real decision problem -> mathematical problem P -> limitations of existing work -> model M + algorithm A -> evidence that the gap is closed -> theoretical and practical meaning`

Three hard rules:

- Gap and contribution must match one-to-one and in the same order.
- Every contribution must be redeemed later by a theorem, proposition, algorithmic result, table, figure, ablation, benchmark, or case result.
- Every nontrivial modelling choice needs justification. Assumptions are argued, not merely stated.

## Standard Six-Section Structure

Use six main sections unless the target journal or user specifies otherwise.

1. `Introduction`: background, state of practice/literature, gap, motivation, contributions, paper organization.
2. `Literature review`: three substantive streams: problem/application setting, model/decision formulation, and algorithm/solution method. Do not use meta titles such as `Problem line` or `Model line`; write publication-style subsection titles. Each stream should first review the literature in 2-3 coherent paragraphs, then use the final paragraph only for synthesis, gap, and how the manuscript responds. Do not mention `this paper`, `the proposed model`, the model name, or the algorithm name in the middle of the literature-review paragraphs unless the whole paragraph is explicitly the final gap paragraph. Each stream must end with a separate synthesis-and-gap paragraph that states the unresolved issue and points to how later sections address it. Vary the paragraph openings and rhetorical texture across streams; avoid repeating formulaic transitions such as `In summary` at the start of every gap paragraph.
3. `Problem formulation`: decision setting, notation, data-to-parameter construction, uncertainty representation, full formulation, assumptions, remarks. Use the shorter `Model` only when the section is purely mathematical and the decision context has already been defined elsewhere.
4. `Solution method`: exact/heuristic/decomposition/learning-assisted algorithm, theoretical properties, pseudocode, complexity or convergence where supported.
5. `Computational study`: benchmark comparison, ablation, real case, paradigm comparison, sensitivity, statistical tests where possible.
6. `Conclusion`: theoretical implications, practical/managerial implications, limitations and future work.

Appendix: proofs, long pseudocode, implementation details, hyperparameters, extra experiments, data processing, and extended derivations.

For applied OR manuscripts, the Conclusion should not merely restate the abstract. Prefer three compact paragraphs: theoretical implications, practical or managerial implications, and limitations/future directions. The theoretical paragraph should distinguish modelling implications from algorithmic or methodological implications when both exist. The practical paragraph should state the real decision problem the paper helps solve. The limitations paragraph should be candid about data, assumptions, computation, generalizability, and credible extensions.

## Introduction Architecture Rule

For applied OR manuscripts, write the Introduction as a compact argument rather than a miniature project report. Use the following paragraph-level sequence unless the target journal or user specifies another structure:

1. Background: define the real decision setting, policy or practice pressure when relevant, and why the problem matters operationally.
   Do not add country-specific laws, national policy narratives, or governance slogans unless the user asks for that framing or the manuscript's contribution depends on it. Dataset provenance, such as a city or country name in the data section, is still appropriate.
2. State of practice/literature: summarize what existing scholars and methods have already addressed, with enough citations to show the paper enters a real research conversation.
3. Gap: state what remains unresolved in decision, modelling, and algorithmic terms. The gap should be narrower than the whole literature and should lead directly to the model and algorithm.
4. Motivation/approach: state what model and solution method the paper proposes and why these choices fit the decision setting.
5. Contributions: list three to five contribution items, ordered as model, algorithm/method, and empirical or managerial evidence where applicable.
6. Paper organization: briefly state what each remaining section does.

For a full applied OR article, the Introduction should usually cite at least 15--25 relevant works when the problem spans an application domain, routing/optimization, learning or prediction, and algorithms. Do not force a citation count, but if the Introduction has too few citations to establish the problem, state of practice, gap, and method positioning, expand it before polishing. Keep detailed dataset descriptions, full experiment settings, and long numerical tables in the computational-study section unless a small motivating statistic is essential.

The transition from the background paragraph to the state-of-practice/literature paragraph must be explicit. The background should end, or the next paragraph should begin, by translating the real setting into an OR decision abstraction: who decides, what is selected or scheduled, what is uncertain, and what resource is scarce. The second paragraph should then review OR or analytics research that addresses this same abstraction, not jump abruptly from policy or industry context to a generic list of methods.

Avoid detailed mathematical notation in the Introduction. The Introduction may name the model class, uncertainty type, objective logic, and decision tradeoff, but symbols, variables, equation-level notation, and parameter names should normally first appear in the model section where they can be defined properly. Do not keep an explanatory paragraph in the Introduction if it merely previews notation that will be taught in Section 3.

Avoid rhetorical questions in the Introduction and contribution statement. Applied OR writing should state the decision transformation declaratively, for example by saying what the model enables, what uncertainty it handles, and what decision criterion changes. When contributions need more detail, use compact paragraph-level items rather than one dense paragraph. Contribution labels should be specific short phrases that summarize the actual contribution, such as `\paragraph{(i) Robust routing formulation for uncertain demand.}` or `\paragraph{(ii) Leakage-audited prediction-to-optimization interface.}` Avoid generic internal labels such as `Model contribution`, `Algorithm contribution`, or `Empirical contribution` unless the journal explicitly prefers them. Separate distinct methodological contributions, such as a learning or parameter-estimation module and a routing or optimization algorithm, when they solve different parts of the decision pipeline. Each contribution item should map to a specific gap and later evidence in the manuscript.

## Formal Manuscript Writing Workflow

For a complete applied OR manuscript, write in this order while using the detailed rules in the following sections. This section is a navigation checklist; the hard requirements are preserved in the dedicated rules below.

1. `Front matter`: title, author/title page if needed, abstract, and keywords.
2. `Six-section body`: Introduction, Literature review, Problem formulation or Model, Solution method, Computational study, and Conclusion.
3. `Post-body sections`: Data and code availability, Acknowledgements, appendices or supplementary material, and references.
4. `Submission files`: cover letter, highlights, title page, conflict-of-interest statement, author contributions, graphical or textual abstract, and supplementary files when the target journal requests them.

Do not weaken the default applied OR profile when using this checklist, but always respect the target journal's stated page, word, figure, table, appendix, and supplement limits first. When a target journal gives an upper bound, draft toward the upper part of the allowed range without exceeding it, shifting proofs, long tables, extra experiments, and implementation logs to online supplements when allowed. If the target journal gives no clear page or word limit and the user does not request a short article or note, preserve the normal full-paper targets: 10,000--12,000 main-text words, a compiled manuscript of at least 25 pages, normally 25--30 pages, a six-section main body, and at least 50 references for the environmental-inspection routing manuscript profile.

## Applied OR Manuscript Profile

For applied OR manuscripts intended to resemble common styles in Transportation Research series journals, Omega, EJOR, COR, and related Elsevier OR/MS outlets, use the following default profile unless the user specifies another target:

- Main-text length should normally target 10,000--12,000 words, excluding references and usually excluding appendices, data/code availability, acknowledgements, and supplementary materials.
- For a complete applied OR manuscript or submission-style full draft, first check the intended journal's page and word limits. If a limit exists, treat that limit as binding and aim for a complete manuscript near the allowed upper range while preserving readability. If no journal-specific limit exists, the compiled manuscript should be at least 25 pages unless the user explicitly requests a short article, note, or proposal; treat fewer than 25 pages as an incomplete draft, not as a final manuscript. The default no-limit target is 25--30 pages, with expansion coming from substantive introduction depth, literature synthesis, model explanation, algorithm detail, computational design, robustness checks, appendices, and evidence interpretation rather than filler.
- Preserve a six-section main body: Introduction, Literature review, Model, Solution method, Computational study, and Conclusion.
- After the six-section body, include Data and code availability, Acknowledgements when appropriate, appendices or supplementary material, and references.
- Use an applied OR title style that foregrounds the application domain, data-driven or learning-assisted decision support, and the modelling/algorithmic contribution. Avoid vague titles that only name a technique.
- Write the abstract in a classic five-sentence pattern: background, decision problem, proposed model, algorithm and results, and theoretical/practical significance. Keep it under 250 words unless the journal requires a tighter limit.
- Use concise manuscript keywords, normally 4--6 items and 1--3 words per item. Prefer focused terms such as `Inspection dispatch`, `Risk prediction`, `Team orienteering`, `Robust routing`, or `Conformal calibration`. Avoid journal subject-area labels, broad phrases, or database taxonomy phrases such as `OR in environment and climate change`, `Artificial intelligence in OR`, or `Machine learning in OR` unless the submission system explicitly requires them in a separate subject-area field.
- In the abstract, describe empirical data at a high level, such as `a full-year dispatch ledger`, `multi-city transaction data`, or `public benchmark instances`. Avoid exact row counts, column counts, missing-value counts, or other granular data-audit details unless the scale itself is the central contribution; place those details in the computational-study data subsection.
- In the abstract result sentence, report concrete effect sizes rather than listing benchmark names. For the current environmental-inspection routing manuscript, express reported improvements with percent signs such as `52.2\%`, not prose such as `percentage points`.
- Keep the prose close to TR series, Omega, EJOR, and similar OR journal conventions: decision-maker first, operational tension clear, model assumptions explicit, algorithmic novelty bounded, computational evidence traceable, and managerial implications tied to results.

## Subsection Economy Rule

For journal-style OR manuscripts, avoid project-report fragmentation.

- Each main section should normally contain 3-5 subsections.
- If a section needs more than 5 subsections, merge adjacent material into broader analytical blocks.
- Use paragraph-level transitions instead of excessive `subsubsection` headings when the content is explanatory rather than a distinct manuscript unit.
- Section 5 should usually be organized as: data/baselines/computational setting, algorithm performance comparison, ablation experiments, model or real-case validation, and sensitivity analysis. When both public benchmark data and real-world case data are used, state both data sources at the start of Section 5 and explain their different roles.
- For learning-assisted OR manuscripts with two substantive algorithmic components, such as an AI prediction/calibration algorithm and an optimization, exact, decomposition, or routing algorithm, Section 5 should make that dual structure explicit. Use 5.1 for all data sources, benchmark methods, computing environment, parameter settings, and metric formulas; use 5.2 for separate algorithm comparisons of the AI component and the OR solver against their own credible baselines; use 5.3 for ablations of each proposed module, skipping only modules for which no implemented ablation exists; use 5.4 for the real-world model validation or case study against decision-policy baselines; and use 5.5 for sensitivity or robustness checks when needed. Do not scatter prediction metrics, solver benchmarks, ablations, and real-case policy tables across unrelated subsections.
- Appendices may contain more support blocks, but the main text should preserve a clean six-section journal structure.

## Computational Study Entry Rule

The first subsection of Section 5 must be the experiment setting, not only metrics.
Use a title such as `Computational setting and evaluation design`.
It should give the reader all information needed to understand how the experiments were run before any result is interpreted:

- computing environment: operating system, CPU/logical cores if known, memory if known, programming language, solver, solver interface, time limit, threads/gap if specified;
- case data: source file or case name, temporal/spatial resolution, sample size, target variable, event threshold, training/calibration/test split, and held-out event counts;
- standard or benchmark datasets: list each public/standard set used, state its role, and state explicitly if the paper has no external standard benchmark because the study is case-driven;
- comparison algorithms or strategies: exact models, heuristics, threshold rules, no-action/all-action baselines, decomposition variants, and why each is fair;
- experimental factors: threshold levels, scenario sizes, cost ratios, reliability tolerances, budget values, random seeds, repetitions, and sensitivity ranges;
- evaluation metrics: definitions, units, denominator caveats, and which contribution each metric supports.

For OR manuscripts that combine algorithm development and an applied model, separate the evidence layers clearly: public benchmark tests usually support generic algorithm performance; ablation tests support algorithmic novelty; real-world case tests support model value and managerial relevance; sensitivity analysis supports robustness and parameter interpretation. Do not bury CPU, solver, random seed, and parameter settings in later result subsections.

For papers built on a classical OR problem family, the computational data design should normally have two primary parts. The first part is the problem-matched public standard benchmark for the core problem, such as VRP/VRPTW benchmarks for VRP papers, TOP/OP benchmarks for orienteering papers, knapsack benchmarks for knapsack papers, and facility-location benchmarks for location papers. The second part is the real-world or constructed case dataset that demonstrates the applied decision value. Do not use a neighbouring problem's benchmark as the main standard set merely because it has convenient coordinates or scripts; if such data are useful, label them as supplementary smoke tests or implementation checks.

When benchmark data have actually been downloaded and benchmark experiments have been run, replace planning language such as `should be used`, `should be replaced`, or `recommended benchmark design` in the main computational-study text with executed-result language. State where the public instances came from, how many were downloaded or extracted, which subset was selected, what script generated the results, and the exact time limits and metrics. Placeholder benchmark tables may remain only in appendices or work notes; the main text should report traceable generated tables and figures.

Do not leave blank cells, dashes, or placeholder rows in main-text result tables for an experiment that supports a contribution. If the experiment has not been run, either run it, move the design template to author work notes, or remove the table from the submission manuscript. Do not use a small preliminary experiment as the main support for a central contribution.

Every experiment named in the abstract, introduction, contribution list, computational-study design, data/code statement, or figure caption must have a corresponding result table, figure, or explicit removal before submission. Conversely, every main result table and figure must be referenced and interpreted in the text. During revision, audit stale artifacts: old single-day pilots, old dates in route maps, orphan figures, captions copied from another figure, and tables whose numbers no longer match the current experimental file. If a pilot instance makes several algorithms collapse to the same solution, either explain the degeneracy and move it to an appendix or remove it from the main evidence layer.

Abstract result sentences must be arithmetically reproducible from main tables. Before compiling a revision, recompute every reported percentage, distance reduction, coverage change, and "same coverage" claim from the displayed table values. If the metric depends on a special denominator, define that denominator in the table note or nearby text. Do not keep old run numbers after rerunning experiments; revise the abstract, results prose, captions, and data/code statement together.

When adding extra experiments late in a manuscript, prefer a focused diagnostic test over a long unfocused benchmark sweep. Define the subset by a defensible instance feature such as scale, capacity tightness, uncertainty level, or route-competition intensity; state that role explicitly; and report generated output files, seeds or fixed settings, time limits, and metrics. Do not add an appendix table merely because it exists: include it only when it clarifies a contribution, supports an ablation, or explains where the proposed method has an advantage.

Benchmark-algorithm tables should usually use a clean two-column format: `Method` and `Description`. Put the algorithm name and key citation, solver name, or `(proposed)` marker in the `Method` column. Use the `Description` column to state the mechanism and experimental role in one concise paragraph. Avoid splitting benchmark tables into many narrow columns such as `main rule`, `role`, and `notes` unless the paper genuinely needs parameter-level comparison.

Algorithm benchmark tables must list algorithms, not model classes. Each important baseline algorithm should carry a representative citation, solver source, or canonical implementation reference in the `Method` entry or in the description. Remove weak, redundant, or uninterpreted baselines from the main table rather than leaving unexplained abbreviations. If a baseline is kept, explain what algorithmic mechanism it tests and why it is a fair comparator.

For stochastic heuristics, do not base a main superiority claim on a single fixed seed when the reported improvement is marginal. Use at least 10 seeds for the main stochastic comparison whenever runtime allows, report `mean ± sd`, and add paired statistical evidence such as a Wilcoxon signed-rank test plus a paired bootstrap confidence interval. Report the effect estimate, interval, and test result directly. If statistical support is weak, revise the contribution or add evidence instead of inserting defensive meta-commentary into the manuscript.

For heuristic, matheuristic, decomposition, or learning-guided algorithm comparisons, do not rely only on the final solution obtained after each method's default iteration count. Different methods can hide different computational budgets behind default parameters. Use fair comparison designs: (i) give every method the same wall-clock budget and compare gap, reward, cost, hit rate, and variance; and/or (ii) fix a target gap or objective threshold and compare time-to-target plus the fraction of runs that reach the target within the time cap. State whether the gap is relative to a proven optimum, a best-known solution, or the best solution found in the experiment. If possible, add an anytime curve or a small multiple-budget table. If a proposed method is better only under a longer runtime, reposition the claim around model fit, robustness, or application value rather than generic algorithmic dominance. Runtime comparisons should report hardware, language, solver versions, thread count, time cap, restart policy, and whether preprocessing time is included.

Do not put self-undermining meta-commentary in a submission manuscript. Remove phrases such as `not universal dominance`, `not a full dominance claim`, `only implementation evidence`, `merely a pilot`, `controlled pilot extension`, `the results should not be read as`, or explanations that a method was implemented after the main experiment. These phrases describe the author's confidence or workflow rather than the scientific result. Replace them with direct reporting: identify the instance subset, computational budget, comparator, metric, numerical improvement, statistical uncertainty, and any condition under which the ranking changes. If the evidence is too narrow to support a central contribution, strengthen the experiment or narrow the contribution before submission. Do not retain a strong contribution statement and then negate it repeatedly in the results, captions, conclusion, or limitations.

When exploring a new algorithm for a classical OR problem, start from a strong recent algorithm family or solver configuration that is credible for that problem class, such as HGS, ALNS, branch-and-price, logic-based Benders, CP-SAT/MIP, or reinforcement-learning baselines where appropriate. Add only a small number of problem-specific modules unless there is clear evidence for more complexity. For each added module, state its search role, the equation or score it changes, and the failure mode it is intended to address; then verify it with an ablation under the same time budget or the same target gap. Do not present a module as an innovation only because it is combined with another heuristic.

Every modelling novelty needs a decisive baseline that could plausibly explain the same gain. For robust routing with learned node rewards, include a fixed-premium nominal baseline such as solving a deterministic model with rewards \(\mu_i-\delta_i\). For risk-aware models, include a nominal optimization baseline and a simple ranking or rule baseline. If the proposed method beats only the tailored baseline but not the strongest nominal solver, state that narrower contribution directly.

Do not leave exact-validation tables as protocols when the manuscript claims a new heuristic for a classical OR problem. For small instances, run a MILP/CP/exact or bounded solver where feasible and report incumbent, best bound, gap, runtime, and domain metrics such as positives, distance, missed demand, unserved reward, or capacity use. If bounds are loose under short time limits, report that limitation honestly and explain why large-scale experiments rely on the heuristic.

When reviewers question a heuristic's algorithmic contribution, do not immediately replace it with an unimplemented exact or decomposition method. First decide whether the paper needs (i) an exact/bounded validation layer for small instances, (ii) a stronger baseline or ablation, (iii) a multi-seed/statistical rerun, or (iv) a repositioning of the contribution from algorithmic dominance to model fit and decision support. Benders decomposition, branch-and-price, column generation, or other exact frameworks should be introduced as manuscript contributions only when the master problem, subproblem, cut or pricing logic, stopping criteria, and computational evidence are actually implemented. Otherwise, discuss them candidly as future work and use CP/MILP/solver bounds as validation evidence.
When upgrading a learning-assisted OR paper from deterministic predict-then-optimize to a two-stage stochastic or recourse model, make the modelling change real rather than rhetorical. Define the first-stage variables, the random variables, and the second-stage recourse variables; specify how scenarios are generated from calibrated predictions; include finite recourse capacities when the recourse layer is meant to change decisions; and compare against the deterministic predict-then-optimize baseline using the same held-out instances. If the stochastic model starts from a strong deterministic route, state this as a warm start and evaluate whether recourse improves objective, unresolved exposure, realized positives, or only auditability. Report capacity-dependent results honestly when recourse helps mainly under tight resources.

For robust or conservative models, report realized-outcome trade-off frontiers, not only robust objective values. A robust solution may reduce verified positives, served demand, or realized profit while improving worst-case value. Tables should therefore pair worst-case or lower-tail reward with realized outcomes, coverage, cost, and distance across robustness budgets. Directly answer whether robustness is buying stability at the price of missed discoveries or lower realized service.

When a manuscript claims a robust, stochastic, fuzzy, or distributionally robust variant of a classical OR problem, cite problem-specific uncertainty literature in addition to generic robust-optimization sources. For example, a robust or stochastic orienteering paper should discuss uncertain rewards/profits/weights, stochastic travel or service times, chance constraints, adaptive stochastic orienteering, and correlated orienteering where relevant. Then state precisely how the proposed model differs from that stream.

Do not overextend the conceptual frame beyond the actual formulation. If the model is a Bertsimas-Sim budgeted uncertainty set, do not describe it as a fuzzy, Wasserstein, DRO, min-max regret, or correlation model unless those objects are explicitly formulated and evaluated. Such variants can be listed as future work or extensions, but the main model section should claim only what the equations implement.

For reproducible OR objectives with mixed units, report how every term is normalized into the objective unit. State the units of rewards, distances/times, missed-service penalties, scaling coefficients, and how these coefficients were fixed or tuned. If a table reports a scalar objective beside large raw distances or costs, add enough explanation for readers to reconstruct the relative weights.

Remove or report every algorithmic hyperparameter introduced in equations. If a proposed repair or scoring formula uses weights such as \(\eta\), \(\lambda\), \(\kappa\), or robustness budgets, include their default values and validation rule. If an implementation uses a lexicographic or parameter-free rule instead, write that rule directly rather than leaving unused tunable weights in the manuscript.

For empirical datasets with missing labels, state how unlabeled records are handled in training, calibration, prediction metrics, and downstream route evaluation. For figures or tables with coverage percentages, define the denominator in the caption or nearby text, especially when small denominators can create visually impressive but trivial values such as 100%.

## Reviewer-Driven Major Revision Rule

When revising an OR manuscript from reviewer comments, classify each major criticism before editing: already satisfied, text-only clarification, evidence rerun, or claim repositioning. If the issue is already satisfied, do not duplicate experiments or inflate the paper; point to the exact section, table, figure, equation, or appendix and make only small wording clarifications if needed.

For novelty objections, add the decisive competing baseline rather than a weak convenient one. If a reviewer argues that the proposed mechanism may be equivalent to a simpler transformation, include that transformation as a named baseline or ablation. If the proposed method beats that baseline but not the strongest general solver, position the contribution around the specific mechanism, model fit, or application setting rather than generic dominance.

For robustness objections, avoid circular evidence. Do not evaluate a robust algorithm only on an uncertainty layer designed to favour that algorithm. Use fitted uncertainty parameters, held-out realized outcomes, independently generated perturbations, external scenarios, or resampling rules whose construction is separate from the promoted algorithm module.

For literature-positioning objections, add problem-specific literature before generic theory. A robust routing paper should not rely only on general robust optimization; it should also discuss robust, stochastic, chance-constrained, adaptive, correlated, or profit-uncertain variants of the same routing family when relevant. After adding this literature, explicitly narrow the manuscript's claim to the formulation actually solved.

For conceptual-overreach objections, remove labels and examples that the equations do not support. Budgeted uncertainty does not by itself model correlation, Wasserstein ambiguity, fuzzy membership, or min-max regret. If those concepts are useful, move them to future work and state that the current model uses a simpler auditable approximation.

For technical reproducibility objections, check for hidden placeholders and unreported choices: blank validation tables, dashes in result cells, single-seed superiority claims, undefined denominators, mixed-unit objectives, omitted hyperparameters, and unexplained missing labels. Each item should be filled, removed, moved to a protocol appendix, or explicitly bounded before compiling a revision.

Remove author-facing scaffolding from submission text. Phrases such as `should vary`, `can train`, `submission-ready rerun`, `recommended implementation log`, `reporting template`, and `main manuscript should report` belong in work notes, not in the article. If a planned analysis is not part of the evidence, place it in limitations/future work using completed-study tense and avoid presenting it as a delivered result.

Do not scatter these items across the manuscript. Section 3 may define abstract data-to-parameter mappings when they are part of the model, such as how an event indicator is computed from a threshold or how a scenario set enters the formulation. However, empirical dataset description belongs in Section 5: case name, sample size, columns, split, held-out event counts, benchmark datasets, and dataset figures/tables should be placed in the first computational-study subsection. Avoid titles such as `Problem definition and data` in Section 3 unless the journal explicitly requests a separate data section before the model.

## Model Explanation and Worked Example Rule

Section 3 must teach the model, not only display it.
For method-driven OR papers, the model section should normally include:

- a clear decision-maker sentence: who chooses what, when, and with what information;
- a short explanation of every set, parameter, uncertain quantity, and decision variable before it enters a displayed formulation;
- operational meaning after the objective and after each non-obvious constraint group;
- a compact worked example when the formulation has binary logic, reliability constraints, scenario indexing, decomposition structure, or nonstandard costs;
- a small explanatory figure when the worked example has an important spatial, temporal, or network tradeoff that is easier to understand visually;
- a statement of which elements are illustrative and which are empirical, so examples are never mistaken for real results;
- a short link from the worked example to the computational model.

For applied OR papers, prefer a publication-style Section 3 title such as `Problem formulation` when the section combines decision context, parameter construction, formulation, worked example, and assumptions. This title signals that the section connects the real operational problem to the mathematical model, rather than presenting equations in isolation.

When presenting a mathematical formulation, do not alternate one displayed constraint with one explanatory sentence throughout the section. State the objective and then list related constraints in coherent groups, using equation labels where needed. After the formulation, explain the role of the objective terms and constraint groups together. The explanation should be substantive, not a list of term names: state what each objective term rewards or penalizes, what operational tradeoff it creates, how soft penalties differ from hard feasibility, and why any threshold or missed-service term is included. For constraints, explain each block by its modelling function, such as selection, assignment, depot balance, flow conservation, time propagation, soft time windows, resource limits, and variable domains. Explicitly describe how linking and big-\(M\) constraints activate only when the relevant visit or arc is used. This reads closer to EJOR/Omega/TR-style OR modelling and avoids a fragmented textbook tone.

The preferred worked example is small enough to verify by hand, usually two or three periods and two or three scenarios. It should show how a candidate decision creates misses, false alarms, switching, objective value, and any reliability feasibility issue. Use a small table plus prose, and add a simple figure when it clarifies route geometry, timing, scenario interaction, or selection logic. For example figures, prefer multiple simple panels over one crowded diagram when the example compares states or policies. Generate each panel as a separate editable PDF or vector asset, then assemble the panels in LaTeX with `minipage` or the journal's subfigure mechanism. This is an author-side production workflow only; do not mention panel file generation, PDF splitting, or LaTeX assembly in manuscript prose, captions, or notes. A useful three-panel pattern is: candidate instance, benchmark or naive decision, and proposed-model decision. Keep labels short, keep geometry consistent across panels, and explain in the caption what each panel teaches. Separate parameter text from route geometry whenever possible: put probabilities, deadlines, prizes, or scenario values in a compact information band/table and keep the map or network area for nodes and arcs only. Never let labels overlap route lines, nodes, or arrows; preview every panel at the final manuscript scale and revise label placement, curvature, opacity, and whitespace until the figure remains legible. Do not turn the example into a second case study. Avoid inventing empirical-looking data; label the example as illustrative and keep it separate from the computational-study results.

Write assumptions as argued modelling statements, not as a bare numbered list. Prefer paragraph-style labels such as `\textbf{Assumption 1 (Information availability).}` followed by a short explanation of what the assumption permits, what it excludes, and how it affects the formulation or experiments. When an assumption concerns dependence, information timing, calibration, static planning, travel-time approximation, or service deferral, state the modelling consequence explicitly. This style makes assumptions read like EJOR/Omega/TR modelling prose rather than project notes.

## Solution Method Rule

Section 4 must introduce the proposed algorithm or solution workflow as a complete method, not merely name a solver.

For decomposition, column-generation, cutting-plane, branch-and-cut, or other exact/enhanced algorithms, Section 4 should teach the algorithmic lineage before presenting the proposed method: start from the classical base algorithm, explain the strongest relevant frontier enhancement, and then show exactly what the paper changes. This progression helps reviewers see that the proposed method is a targeted extension of a known algorithmic family rather than an isolated trick.
For OR manuscripts, the solution section should normally include:

- frontier positioning before enhancement: first identify the relevant current algorithm families for the problem, such as exact/decomposition methods, metaheuristics, matheuristics, learning-guided heuristics, or reinforcement-learning/neural solvers, then justify which family is adopted as the base;
- algorithmic positioning: what is exact, heuristic, decomposition-based, learning-assisted, or only an extension;
- innovation scope: state precisely what is new in the paper and what is adopted from established methods;
- input-output definition: data, parameters, scenario set, model variant, solver controls, and returned decisions/metrics;
- complete pseudocode for the proposed workflow in the main text;
- decomposition pseudocode if Benders, column generation, Lagrangian relaxation, or another iterative algorithm is presented;
- validity or convergence statement when supported, and a precise description of the computational role when the method is a practical workflow;
- implementation details that affect reproducibility, with long engineering details moved to the appendix.

If the method has multiple substantive stages, such as prediction-then-optimization, scenario-generation-then-solve, clustering-then-routing, or screening-then-scheduling, organize Section 4 by those stages. Each stage that contributes to the method should have its own input-output definition, key formulas, pseudocode, cited methodological foundation, and innovation-scope paragraph. Do not force a two-stage structure on papers with only one algorithm; use the number of stages implied by the contribution.

When proposing an enhanced heuristic or hybrid algorithm, write it as a controlled modification of a strong and citable base method rather than as an arbitrary mixture. State the diagnosed weakness of the base method in the target problem, then add, remove, or tune only the modules that address that weakness. Typical acceptable enhancements include problem-specific decoding, repair, neighborhood selection, adaptive operator weighting, route elimination, split procedures, calibration-aware scoring, warm starts, or parameter customization. Keep the number of proposed modules small unless experiments can isolate them. Each added module should have a formula, pseudocode step, parameter default, ablation variant, and result table or figure that demonstrates its role. Compare the proposed method with the strongest credible solver using the same computational budget and state the observed advantages by instance class and metric.

When naming a manuscript method, separate the model name from the algorithm name. Use one acronym or short name for the formulation or decision framework and another for the solver or search procedure. Avoid algorithm names that append the problem acronym to a base solver in a way that implies the method is usable only for that single model, unless that narrow scope is intentional. The algorithm name should describe the transferable search idea, such as robust marginal-gain search, calibrated repair, or uncertainty-aware neighborhood search, while the model name should describe the decision formulation.

Keep experimental benchmark definitions out of Section 4 unless a benchmark is itself a method component. Baseline algorithms, comparison policies, ablation variants, and fairness rules normally belong in Section 5's computational setting or experiment-design subsection.

For decomposition methods, make the mechanics auditable before giving pseudocode:

- write the relaxed master problem or its essential constraints;
- define the separation problem or separation scan, including what counts as a violated cut;
- explain what information is carried across iterations;
- explain how the proposed selection rule differs from one-cut, multi-cut, deepest-cut, or static selection;
- state whether the selection rule changes validity, optimality, only convergence behaviour, or only implementation efficiency;
- connect each algorithm component to one empirical output such as runtime, iterations, cuts, gap, or convergence status.

Do not overclaim algorithmic novelty. If the empirical engine is direct CPLEX, say so. The innovation can still lie in the formulation, the data-to-scenario pipeline, the reliability-aware optimization workflow, or the auditable failure-diagnostic loop.

## Pseudocode Style Rule

Do not typeset pseudocode as an ordinary table. Use a proper algorithm environment whenever LaTeX supports it, preferably `algorithm` with `algpseudocode` or the journal's native algorithm style.
The preferred OR style is:

- a numbered algorithm caption, for example `Algorithm 1 Reliability-constrained robust warning optimization`;
- `Require:` for inputs and `Ensure:` for outputs;
- numbered steps with clear indentation;
- structured keywords such as `Initialize`, `For`, `Repeat`, `If`, `Then`, `Else`, `Return`, and `End If`;
- mathematical symbols consistent with the model section;
- compact lines, avoiding paragraph-length steps;
- no table-like `Input/Output/1/2/3` layout unless the journal forbids algorithm packages.

For decomposition algorithms, show initialization, master solve, subproblem/separation, cut selection, cut addition, and stopping criterion. For workflow algorithms, show data split, scenario generation, model construction, solve, evaluation, sensitivity loop, and output generation. The pseudocode should look like a publishable OR algorithm, not a project checklist.

For Benders and cutting-plane algorithms, give the complete computational loop in equations and pseudocode: master relaxation, subproblem or separation problem, dual or adversarial cut generation, cut scoring, cut selection, cut addition, incumbent update, lower/upper bound update, and stopping rule. Define every algorithmic symbol before the pseudocode; avoid symbol-heavy pseudocode that is not explained in prose. Every new symbol introduced in Section 4 must be defined either immediately at first use or in a compact algorithmic-notation table placed before the formulas that use it. This includes generic MIP symbols, cut-pool symbols, incumbent symbols, dual variables, bounds, tolerances, scoring functions, history vectors, and algorithm parameters.

When introducing a deepest-cut, metric-guided, history-guided, or geometry-aware cut rule, state clearly whether the new module changes the feasible region, changes the cut inequality, or only changes the ranking/selection of otherwise valid cuts. A common reviewer-friendly structure is: a lemma for cut validity, a proposition for the reduction or dominance relation relative to the classical rule, and a theorem for finite convergence or tolerance convergence under standard exact-solve assumptions.

For algorithms inspired by frontier methods, cite the representative base papers and strongest recent comparators. The manuscript should move from `classical method` to `frontier method` to `proposed enhancement` using formulas, not only narrative. If the enhancement uses historical cut normals, learned scores, or a matrix/norm update, provide the explicit update formula and explain how it affects search geometry.

For OR pseudocode, use mathematical notation only where it clarifies a key scoring rule, feasibility check, or update. Do not turn an algorithm into a dense block of symbols. Each algorithm should be preceded by a short bridge paragraph that defines any algorithm-only objects such as populations, offspring, removal sets, diversity scores, repair keys, current route time, or insertion positions. Inside the pseudocode, combine readable action verbs with the most important formulas, for example `train the classifier`, `decode by positive robust gain`, `repair omitted nodes using key \(R_i\)`, and reserve displayed formulas for quantities already introduced in the surrounding text. Do not introduce a new symbol, weight, or algorithmic parameter in pseudocode unless it has been defined in the model, the bridge paragraph, or the implementation settings. If a line contains more than two new symbols, rewrite it as prose plus a reference to the equation that defines the calculation.

## Appendix Style Rule

Use appendices to support, not re-argue, the main paper.

- Label appendices as `Appendix A`, `Appendix B`, `Appendix C`, and `Appendix D` when there are multiple support blocks.
- Every appendix must be cited from the main text or a nearby methodological statement; uncited appendices should be removed or moved to supplementary material.
- Put proofs, extensions, implementation details, derivations, and extra sensitivity logic in appendices, but keep main claims and main evidence in the body.
- Avoid long explanatory prose in appendices. Use short bridge sentences plus connected derivations.
- Do not write a pattern of one sentence followed by one display equation repeatedly. Combine minor definitions inline and reserve displayed equations for important formulations, cuts, recursions, or constraints.
- Use compact notation tables or grouped equations when they reduce prose.
- Appendix equations should extend or justify the main model; they should not introduce a second paper inside the paper.

## Workflow Figure Rule

For OR method papers, workflow figures should be treated as schematic-led scientific figures, not decorative flowcharts.
Before drawing, define the figure's core claim, the evidence chain, and the review risk.
Use the following standards:

- arrange the main methodological pipeline as a small number of visually dominant modules;
- place secondary components, diagnostics, and robustness checks in a quieter support layer;
- use short labels and line breaks rather than paragraph text inside boxes;
- keep arrows sparse, directional, and noncrossing whenever possible;
- use one neutral family, one signal family, and one accent color;
- ensure every box corresponds to a real model, data-processing, algorithmic, or evaluation component in the manuscript;
- export editable SVG/PDF plus high-resolution PNG;
- preview the figure and fix text overflow, label collisions, arrow crossings, and illegible math before compiling the manuscript.

Do not invent visual modules merely to make a diagram look richer. A good workflow figure should make the problem-model-algorithm-experiment chain easier to audit.
When the user asks for a top-conference-style method architecture diagram, experiment chart recommendation, or English figure title, apply the more detailed rules in `references/academic-figure-design.md`.

## Writing Workflow

1. Identify \(P\), \(M\), and \(A\).
2. Build a contribution ledger:
   `Gap -> Contribution -> Manuscript location -> Evidence -> Scope`.
3. Choose the section structure and page budget.
4. Draft from evidence outward. Do not invent results, data, citations, proofs, or managerial implications.
5. Keep notation consistent across model, algorithm, experiments, and appendix.
6. Make experiments redeem contributions, not merely show that the proposed method wins.
7. Polish after structure is correct. Sentence fluency cannot rescue a broken argument.
8. Run the final OR manuscript checklist.

## Literature Rules

Use real, verified references only.

- For a 30-page method paper, target 40-70 references.
- For the current environmental-inspection routing manuscript profile, use at least 50 references and add more only when they strengthen the argument, benchmark positioning, or empirical design.
- Include 10-20 recent top-journal papers from the last 3-5 years where appropriate.
- Include 5-10 classic/foundational papers.
- Literature quotas, such as the balance between classic and frontier references, are manuscript-design controls for the author and should not be explicitly announced in the body text.
- In the literature review, let the balance appear through the argument and citations rather than writing meta-statements such as "this review uses X references".
- Search and verify live when the user asks for current/frontier literature, recent references, exact citations, DOI, or submission-ready bibliography.
- Never fabricate authors, years, titles, journals, pages, volumes, or DOI.
- If a source cannot be verified, remove it or mark it for author verification.
- Before submission, run a reference integrity audit: every cited key must exist in the bibliography, every bibliography entry should be cited unless there is a deliberate appendix reason, and DOI metadata must match the claimed title and source. A DOI that resolves to a different title is worse than a missing DOI and should be corrected or removed.
- Treat arXiv/preprint records as preprints unless a version of record is verified. Do not cite a preprint as a formally published journal article merely because a title appears online.
- When the user or target journal requests no preprints, remove arXiv/preprint references from both the manuscript and bibliography. Use the version of record if it exists; otherwise replace the claim with published literature or narrow the claim. Do not leave uncited preprint entries in the `.bib` file for a submission package.

## Data and Result Integrity Audit

For manuscript results, require a traceable chain:

`raw data -> processing script -> model/solver output -> result CSV/JSON -> table/figure generator -> manuscript`

Use this audit before finalizing a computational OR paper:

- Check that raw data filenames, sample sizes, split points, thresholds, and event counts in the manuscript match generated metadata.
- Re-run the data-preparation, solver, and figure/table scripts when feasible.
- Confirm that main-result tables filter only the intended strategies or algorithms; sensitivity, ablation, and grid rows should not leak into the main comparison unless explicitly labelled.
- Confirm that figures read from generated CSV/JSON/model outputs, not manually typed values.
- Confirm that all infeasible, missing, NaN, or denominator-sensitive metrics are explained in the text or table notes.
- Keep an audit artifact when useful, such as `reference_integrity_audit.csv`, `metadata.json`, hashes of raw data, or solver logs. Do not cite these as evidence unless they are included in the submission package or supplementary material.
- If a result cannot be traced from data or code, remove it or mark it as needing author verification. Do not smooth, repair, or invent numerical values to improve the story.

## Learning-Assisted OR Evidence Rule

For learning-assisted, predict-then-optimize, forecast-then-optimize, or data-driven OR manuscripts, the learning stage is part of the claimed method and must be instantiated in the evidence chain.

- If the title, abstract, contributions, model parameters, or algorithm inputs depend on a learned score, probability, demand forecast, reward estimate, uncertainty radius, or scenario generator, the computational study must report a real trained or fitted model unless the manuscript is explicitly a conceptual note.
- Do not use a hand-built rule proxy, manually assigned score, or placeholder probability as the main evidence for a learning-assisted contribution. Such proxies may appear only as baselines, smoke tests, or preliminary diagnostics, and their experimental role must be stated directly.
- For classification-to-routing or classification-to-optimization papers, report both predictive and prescriptive evidence: chronological or otherwise leakage-safe split, training/calibration/test counts, leakage audit, calibration method, AUC or accuracy as appropriate, PR-AUC for imbalanced labels, precision/recall/F1 when thresholds matter, Brier score or another probability-quality metric, expected calibration error or calibration plot, top-\(K\) recall when capacity is constrained, and the downstream optimization metrics generated from the fitted predictions.
- Calibration and threshold selection must use validation or calibration data, not the final test period. The test-period prediction file used by the optimizer should be named or otherwise traceable in the data/code statement.
- When a manuscript uses learned uncertainty sets, reward intervals, or ambiguity radii, explain how they are constructed from calibration residuals, ensembles, conformal intervals, fuzzy membership widths, or another reproducible source. Do not leave the uncertainty term as a symbolic promise if robustness is a contribution.
- If prediction output becomes a random reward, state whether the learned score is the reward center, a probability-scale realization, or a transformed economic prize. If the optimization uses an uncertainty radius, distinguish the prediction interval width from the downside reward radius consumed by the robust model, and report a calibration audit such as empirical coverage versus nominal coverage, ensemble spread calibration, or residual-bin diagnostics.
- Do not use an uncertainty layer designed by the authors primarily to match the proposed robust heuristic as the main evidence for robustness. Synthetic perturbations may be used only as transparent diagnostics or stress tests. The main robustness claim should be evaluated on learned uncertainty parameters, out-of-sample realized outcomes, held-out labels, independent perturbation rules, or scenario samples whose construction is separate from the algorithm modules being promoted.
- Main-text result tables must use executed language after experiments have been run. Remove phrases such as `should rerun`, `submission-ready experiment should`, `placeholder`, and `final policy claim should be based on` from submission text. If a future extension remains, move it to limitations or an appendix protocol and keep it separate from evidence supporting the main contribution.
- Downstream optimization must be rerun after the learned scores are generated. It is not sufficient to report a classifier and then reuse earlier optimization results based on manual scores.

## Polishing and Full-Manuscript Audit Workflow

Polishing starts after the manuscript has a coherent problem-model-algorithm-evidence chain. Audit the paper at four levels.

1. `Argument audit.` Check whether the gap, contribution, model, algorithm, experiments, and conclusion match one-to-one. Every contribution must be redeemed by a theorem, algorithmic result, benchmark, ablation, case result, figure, table, or appendix proof.
2. `Evidence audit.` Verify that every result named in the abstract, introduction, contribution list, captions, data/code statement, or conclusion has a corresponding generated table, figure, or traceable output. Remove stale pilots, orphan figures, placeholder tables, and old run numbers.
3. `Technical audit.` Check notation consistency, objective scaling, missing labels, hyperparameters, random seeds, exact/bounded validation, benchmark fairness, denominator definitions, calibration metrics, uncertainty construction, and sensitivity ranges.
4. `Style audit.` Remove report-like headings, author-facing scaffolding, AI-like filler, decorative prose, formula dumping, repeated transitions, rhetorical questions, unsupported novelty, and claims stronger than the evidence. Keep the style close to TR series, Omega, EJOR, COR, and INFORMS-style applied OR writing.
5. `Submission audit.` Compile the manuscript, check page count, unresolved references, duplicate labels, layout warnings, figure readability, table arithmetic, citation integrity, data/code availability, acknowledgements, and journal-specific files.
## Polishing Stance

Polishing means repairing argument, style, and integrity together.

- Fix structure before sentences.
- Remove report-like headings, decorative prose, filler transitions, formula dumping, and bullet abuse.
- Prefer clear claims with evidence and boundaries over inflated novelty.
- Keep OR style: decision maker, decision variables, objective, constraints, uncertainty, algorithmic logic, computational evidence, and implications.
- For Chinese drafts, preserve the author's intended contribution while converting to publication-quality academic English.

## Submission Package Rule

When the user asks for a complete submission package, produce journal-specific files rather than only manuscript prose.

- `Main manuscript.` Provide the cleaned manuscript source and compiled PDF using the official journal-specific template selected through the template gate, or the official Elsevier fallback when no journal-specific package exists. Preserve the template's class files, fonts, spacing, front matter, bibliography style, and figure/table conventions unless the journal explicitly allows otherwise.
- `Title page.` Create a separate title page when the journal requires author-identifying information outside an anonymized manuscript. Include title, authors, affiliations, corresponding author, conflict-of-interest statement, data availability statement, author contributions, funding or acknowledgements if applicable, and any article type only when the journal requests it.
- `Cover letter.` Write a concise journal-specific cover letter: manuscript title, article type if needed, target journal fit, one-paragraph problem and contribution summary, evidence or case basis, novelty relative to literature, suitability for the journal, data/code or ethics notes when needed, and a polite closing. Do not overclaim or repeat the abstract mechanically.
- `Highlights.` Provide 3-5 highlights, normally 85 characters or fewer each unless the journal has another rule. Each highlight should state a concrete contribution or result, not a vague importance claim.
- `Supplementary files.` Include appendices, supplementary tables, data/code availability wording, graphical abstract or research highlights if required, cleaned bibliography, generated figures, and any reproducibility notes requested by the journal.
- `Final cleanup.` Remove intermediate drafts, old PDFs, auxiliary LaTeX files, orphan figures, unused tables, and author-facing work notes from the final delivery folder when the user asks for a clean package.
## Output Defaults

For manuscript writing/revision, return:

- revised or drafted text,
- a short change/audit note,
- unresolved assumptions or items needing author verification.

For full-paper work, update files directly when a workspace manuscript exists, compile if possible, and report page count, unresolved references, and remaining layout warnings.

For audits, lead with issues ordered by severity and grounded in section/figure/table/equation references.













