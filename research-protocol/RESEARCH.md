# RESEARCH.md

> Router and orchestration file for the modular research protocol.

## 1. Purpose

This file is the entry point for all research-related work.

It does not replace the specialized modules.

Its job is to decide:

- which research module(s) must be loaded;
- in what order they should be applied;
- which file is authoritative when rules overlap;
- how to avoid loading unnecessary modules;
- how to move from research planning to final writing and verification.

Always read this file first for research tasks.

---

## 2. Core Rule

`00-RESEARCH-CORE.md` is always the primary research governance file.

All specialized modules extend the core.

No specialized module may weaken:

- research integrity;
- evidence requirements;
- validity;
- traceability;
- reproducibility;
- verification;
- calibrated claims.

When rules conflict:

1. `00-RESEARCH-CORE.md`
2. task-specific module
3. `01-research-writing.md`
4. local formatting preference

Correctness outranks style.

---

## 3. Available Modules

### `00-RESEARCH-CORE.md`

Always load for research work.

Use for:

- research integrity;
- evidence discipline;
- purpose tests;
- source-of-truth hierarchy;
- uncertainty;
- traceability;
- verification;
- delivery gates;
- general audit rules.

### `01-research-writing.md`

Load when the task involves producing or editing research prose.

Use for:

- academic writing;
- paraphrasing;
- source integration;
- synthesis;
- terminology consistency;
- results/discussion/conclusion writing;
- author voice;
- natural scholarly prose;
- writing quality audit.

### `02-research-human.md`

Load when people are part of the study.

Use for:

- participants;
- respondents;
- consent;
- privacy;
- questionnaires;
- interviews;
- usability studies;
- human annotation;
- expert evaluation;
- human judgment;
- human-in-the-loop systems;
- qualitative participant data;
- accessibility.

### `03-research-literature.md`

Load when the task involves literature or source-based evidence.

Use for:

- literature search;
- source quality;
- source selection;
- primary vs secondary evidence;
- evidence hierarchy;
- synthesis;
- claim-to-source traceability;
- research gap construction;
- systematic/structured reviews;
- evidence matrices.

### `04-research-methodology.md`

Load when designing or reviewing the study method.

Use for:

- research design;
- research-question alignment;
- variables;
- constructs;
- operationalization;
- population;
- sampling;
- inclusion/exclusion;
- controls;
- confounding;
- validity;
- data collection protocol;
- qualitative/mixed methods;
- methodological justification.

### `05-research-experiment.md`

Load when computational or empirical experiments are executed or reviewed.

Use for:

- experiment execution;
- train/validation/test discipline;
- leakage prevention;
- baseline fairness;
- hyperparameter tuning;
- random seeds;
- repeated runs;
- benchmark integrity;
- ablation;
- sensitivity;
- robustness;
- artifact preservation;
- experiment logging;
- reproducibility.

### `06-research-analysis.md`

Load when interpreting data or experiment results.

Use for:

- descriptive statistics;
- hypothesis testing;
- effect size;
- confidence intervals;
- assumptions;
- multiple comparisons;
- correlation;
- regression;
- classification metrics;
- calibration;
- model comparison;
- uncertainty;
- qualitative analysis;
- limitations;
- conclusion discipline.

---

## 4. Minimal Loading Rule

Do not load every module by default.

Load only what the task requires.

Always load:

`00-RESEARCH-CORE.md`

Then load the smallest relevant set of specialized modules.

Examples:

### Literature-only task

Load:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `01-research-writing.md` only if prose is being drafted or edited

### Methodology design

Load:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md` if method justification depends on prior work
3. `04-research-methodology.md`
4. `02-research-human.md` if people are involved
5. `01-research-writing.md` if writing the methodology section

### Computational experiment

Load:

1. `00-RESEARCH-CORE.md`
2. `04-research-methodology.md`
3. `05-research-experiment.md`
4. `06-research-analysis.md` when interpreting results
5. `01-research-writing.md` when documenting results

### Human-subject study

Load:

1. `00-RESEARCH-CORE.md`
2. `04-research-methodology.md`
3. `02-research-human.md`
4. `06-research-analysis.md`
5. `01-research-writing.md`

### Literature review chapter

Load:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `01-research-writing.md`

---

## 5. Task Routing Table

| Task | Required Modules |
|---|---|
| Define research problem | CORE + LITERATURE |
| Build research questions | CORE + METHODOLOGY |
| Find papers | CORE + LITERATURE |
| Evaluate sources | CORE + LITERATURE |
| Build research gap | CORE + LITERATURE + METHODOLOGY |
| Write literature review | CORE + LITERATURE + WRITING |
| Design methodology | CORE + METHODOLOGY |
| Define variables | CORE + METHODOLOGY |
| Sampling design | CORE + METHODOLOGY + HUMAN if participants |
| Questionnaire design | CORE + METHODOLOGY + HUMAN |
| Interview design | CORE + METHODOLOGY + HUMAN |
| Human annotation | CORE + HUMAN + METHODOLOGY |
| Expert evaluation | CORE + HUMAN + METHODOLOGY |
| Build ML experiment | CORE + METHODOLOGY + EXPERIMENT |
| Compare models | CORE + EXPERIMENT + ANALYSIS |
| Hyperparameter tuning | CORE + EXPERIMENT |
| Prevent leakage | CORE + METHODOLOGY + EXPERIMENT |
| Statistical testing | CORE + ANALYSIS |
| Interpret results | CORE + ANALYSIS |
| Error analysis | CORE + EXPERIMENT + ANALYSIS |
| Write results | CORE + ANALYSIS + WRITING |
| Write discussion | CORE + LITERATURE + ANALYSIS + WRITING |
| Write conclusion | CORE + ANALYSIS + WRITING |
| Audit whole thesis | ALL relevant modules |
| Final research verification | CORE + all modules used in the study |

---

## 6. Research Lifecycle

Use this sequence unless the study design requires another justified order.

### Phase 1: Problem and Evidence Base

Load:

- CORE
- LITERATURE

Produce:

- problem definition;
- terminology map;
- source map;
- state of research;
- unresolved issues;
- candidate research gap.

Gate:

> Is the problem evidence-based and worth investigating?

### Phase 2: Research Question and Design

Load:

- CORE
- LITERATURE
- METHODOLOGY
- HUMAN when applicable

Produce:

- research question;
- objectives;
- hypotheses if applicable;
- variables;
- operational definitions;
- population;
- sampling;
- data collection;
- validity plan.

Gate:

> Can this design produce evidence that answers the research question?

### Phase 3: Experimental Execution

Load:

- CORE
- METHODOLOGY
- EXPERIMENT
- HUMAN when human evaluation is involved

Produce:

- experiment configuration;
- data splits;
- baselines;
- tuning plan;
- logs;
- artifacts;
- executed results.

Gate:

> Were the experiments actually executed under a fair, leakage-free, traceable protocol?

### Phase 4: Analysis

Load:

- CORE
- ANALYSIS
- EXPERIMENT
- HUMAN where applicable

Produce:

- descriptive analysis;
- statistical analysis;
- uncertainty;
- error analysis;
- interpretation;
- limitation register.

Gate:

> What do the results actually support, and what do they not support?

### Phase 5: Academic Writing

Load:

- CORE
- relevant task module(s)
- WRITING

Produce:

- literature review;
- methodology;
- results;
- discussion;
- conclusion;
- abstract.

Gate:

> Does the prose accurately represent the verified research?

### Phase 6: Final Audit

Load all modules that were used in the project.

Run:

- integrity audit;
- literature audit;
- methodology audit;
- human audit if applicable;
- experiment audit;
- analysis audit;
- writing audit;
- final Research Delivery Gate.

No final PASS without concrete evidence.

---

## 7. Research Read

Before substantial work, state the current research context internally or explicitly when useful.

Use:

> **Research Read:** `<research type>` in `<domain>`, addressing `<research question or goal>`, using `<data/method>`, with `<unit of analysis>`, evaluated by `<protocol>`, current task `<artifact or stage>`.

Example:

> **Research Read:** experimental NLP research on Indonesian sentiment classification, comparing IndoBERT with classical ML baselines on the same dataset, using macro-F1 as the primary metric; current task is methodology design.

If important context is unknown, mark it as unknown.

Do not invent missing research details.

---

## 8. Source-of-Truth Hierarchy

When research artifacts conflict, use:

1. raw data;
2. experiment output/artifact;
3. actual implementation;
4. experiment configuration/log;
5. methodological record;
6. manuscript;
7. memory or assumption.

Do not silently reconcile conflicting artifacts.

Report the discrepancy.

Example:

> The manuscript states an 80:20 split, but the current implementation uses 70:30. This must be reconciled before the result is treated as final.

---

## 9. Evidence Classification

For important claims, track whether they come from:

- `SOURCE`
- `DATA`
- `EXPERIMENT`
- `CALCULATION`
- `INTERPRETATION`
- `ASSUMPTION`
- `UNKNOWN`

Do not allow:

`ASSUMPTION -> FACT`

without evidence.

Do not allow:

`INTERPRETATION -> RESULT`

without clear labeling.

---

## 10. Uncertainty

Use calibrated uncertainty when it materially affects reasoning.

- `[Pasti]` = directly verified
- `[Kemungkinan Besar]` = strong inference with uncertainty
- `[Menebak]` = speculative or insufficient evidence

Do not add labels mechanically.

Use them when confidence matters.

---

## 11. Audit Severity

Use:

### CRITICAL

Threatens:

- integrity;
- validity;
- reproducibility;
- correctness;
- central conclusion.

Examples:

- fabricated source;
- fabricated result;
- test leakage;
- invalid causal inference;
- unsupported experimental claim.

### MAJOR

Materially weakens:

- interpretation;
- comparison;
- methodological quality;
- evidence strength.

Examples:

- unfair baseline;
- inappropriate metric;
- weak sampling logic;
- citation that only partially supports a claim.

### MINOR

Primarily affects:

- consistency;
- readability;
- formatting;
- reporting completeness.

Examples:

- terminology drift;
- unclear table caption;
- inconsistent abbreviation.

---

## 12. Unified Audit Format

Use the rule prefix from the relevant module.

Examples:

- `R-XX` = core
- `W-XX` = writing
- `H-XX` = human
- `L-XX` = literature
- `M-XX` = methodology
- `E-XX` = experiment
- `A-XX` = analysis

Format:

> **RULE | SEVERITY | LOCATION**  
> **Problem:** what is wrong.  
> **Why:** why it matters.  
> **Evidence:** where the issue is visible.  
> **Impact:** what claim or result is affected.  
> **Correction:** what should change.  
> **Verification:** how to confirm the correction.

Do not report vague criticism without evidence.

---

## 13. Editing Rule

When editing research content, default to:

**preserve -> correct -> clarify -> tighten -> restructure only when necessary**

Do not rewrite valid content merely to make it sound different.

Do not introduce:

- unsupported facts;
- new results;
- new citations;
- stronger claims;
- invented limitations;
- fabricated methodological details.

---

## 14. Verification Rule

Never claim:

- PASS;
- validated;
- verified;
- reproducible;
- significant;
- robust;
- fixed;
- working;
- final;

without the relevant evidence.

Examples:

Bad:

> Experiment passed.

Better:

> **E-05 PASS:** final test data were not accessed during tuning; the experiment log records one final evaluation after model selection.

Bad:

> Citation verified.

Better:

> **L-23 PASS:** the cited paper directly supports the statement about the reported method and result.

---

## 15. Stop Conditions

Stop and report the issue instead of continuing as if everything is valid when:

- the source does not support a key claim;
- required data are missing;
- the experiment was never run;
- the methodology cannot answer the RQ;
- a critical artifact conflicts with the manuscript;
- data leakage invalidates the evaluation;
- the requested conclusion exceeds the evidence;
- a citation cannot be verified;
- a result cannot be traced to an artifact.

Do not fill critical gaps with plausible assumptions.

---

## 16. No Yes-Machine Behavior

Do not agree with the researcher merely because they proposed an idea.

If a stronger approach exists, explain it.

When correcting, use:

**what is wrong -> why -> correct concept -> evidence/reason -> impact -> correction -> verification**

If the researcher's reasoning is already strong, say so without inventing criticism.

---

## 17. Requirement vs Preference

Distinguish:

- **requirement**
- **recommended practice**
- **trade-off**
- **preference**

Example:

Using Python is usually a preference/tooling choice.

Keeping final test data independent is a methodological requirement.

Do not present preferences as universal research laws.

---

## 18. Change of Position

Do not change a conclusion merely because the researcher pushes back.

Change only when:

- new evidence appears;
- a stronger source is found;
- an assumption changes;
- an error is discovered;
- the previous conclusion was overconfident.

When changing, state what evidence caused the update.

---

## 19. Final Research Delivery Gate

Before treating a research artifact as final, confirm all relevant module gates have passed.

Minimum final checks:

### Integrity

- no fabricated source;
- no fabricated result;
- no unverified experiment claim;
- no unsupported citation;
- no hidden assumption presented as fact.

### Literature

- key claims are sourced;
- source quality is appropriate;
- synthesis is analytical;
- research gap is evidence-based.

### Methodology

- RQ and method align;
- variables are operationalized;
- sampling is justified;
- threats to validity are addressed.

### Human

When applicable:

- participants are appropriately handled;
- instrument quality is acceptable;
- privacy/consent concerns are addressed;
- human judgment is reported as judgment.

### Experiment

When applicable:

- no leakage;
- fair baselines;
- tuning is traceable;
- artifacts exist;
- results are reproducible enough for the claim.

### Analysis

- assumptions are checked;
- uncertainty is reported;
- effect magnitude is interpreted;
- conclusions stay within evidence.

### Writing

- terminology is consistent;
- no citation distortion;
- no generic filler;
- no overclaiming;
- prose reflects actual research.

A material failure means the artifact is not final.

---

## 20. Recommended Folder Structure

```text
research-protocol/
|
|-- RESEARCH.md
|-- 00-RESEARCH-CORE.md
|-- 01-research-writing.md
|-- 02-research-human.md
|-- 03-research-literature.md
|-- 04-research-methodology.md
|-- 05-research-experiment.md
`-- 06-research-analysis.md
```

Optional project-level research records:

```text
research/
|
|-- context/
|   |-- RESEARCH-CONTEXT.md
|   `-- terminology.md
|
|-- literature/
|   |-- search-log.md
|   |-- evidence-matrix.md
|   `-- gap-matrix.md
|
|-- methodology/
|   |-- variable-dictionary.md
|   |-- validity-register.md
|   `-- protocol.md
|
|-- experiments/
|   |-- experiment-log.md
|   |-- configs/
|   |-- raw-results/
|   `-- result-provenance.md
|
|-- analysis/
|   |-- analysis-plan.md
|   |-- outputs/
|   `-- result-to-conclusion.md
|
`-- audits/
    |-- literature-audit.md
    |-- methodology-audit.md
    |-- experiment-audit.md
    |-- analysis-audit.md
    `-- final-audit.md
```

The protocol files define how to work.

The project records preserve what actually happened.

Do not mix them.

---

## 21. Recommended Agent Entry Pointer

For an AI agent entry file such as:

- `AGENTS.md`
- `CLAUDE.md`
- `GEMINI.md`
- another equivalent instruction file

use a pointer similar to:

```md
## Research Protocol

For any research-related task, read `research-protocol/RESEARCH.md` first.

`RESEARCH.md` is the router.

Always load `research-protocol/00-RESEARCH-CORE.md`, then load only the specialized modules required by the current task.

Do not treat draft manuscripts as the source of truth when they conflict with raw data, experiment artifacts, implementation, or methodological records.

Do not claim PASS, verification, reproducibility, significance, robustness, or completion without concrete evidence.
```

Keep the pointer short.

The detailed rules belong in the protocol files, not in the agent entry file.

---

## 22. Final Principles

**Core first, specialized modules second**  
**Load only what the task needs**  
**Evidence before prose**  
**Method before experiment**  
**Experiment before interpretation**  
**Interpretation before conclusion**  
**Verification before PASS**  
**Actual artifacts before manuscript claims**  
**Critical correction before stylistic polishing**  
**Research integrity before convenience**
