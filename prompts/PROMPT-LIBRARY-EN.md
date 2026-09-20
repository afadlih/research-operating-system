# Prompt Library

A collection of ready-to-use prompts for the Research Operating System. Copy and paste these into your AI platform after uploading the required protocol files.

---

## Getting Started

### Start a New Research Project

> **Required modules:** CORE

```
I am starting a research project.

Use the Research Operating System.

Help me define:
- problem statement
- evidence needed
- feasibility assessment
- potential research questions

Do not jump directly to writing.
Do not fabricate sources or citations.
```

### Load Project Context

> **Required modules:** CORE + PROJECT-CONTEXT

```
Here is my project context: [paste or upload 09-project-context-template.md]

Review my current research state.
Identify what has been completed and what remains.
Flag any inconsistencies between stated methodology and current progress.
```

---

## Literature Review

### Analyze Papers

> **Required modules:** CORE + LITERATURE

```
Analyze these papers.

Extract for each paper:
- research objective
- methodology used
- key findings
- limitations stated by authors
- limitations I should note
- possible contribution to research gap

Separate source facts from your interpretation.
Mark anything uncertain as [INTERPRETATION].
```

### Build Evidence Matrix

> **Required modules:** CORE + LITERATURE

```
Based on the papers I have provided, build an evidence matrix.

Columns:
- Author(s) and Year
- Research Question / Objective
- Method
- Key Finding
- Limitation
- Relevance to my research

Do not add papers I have not provided.
Do not fabricate authors, years, or findings.
```

### Identify Research Gap

> **Required modules:** CORE + LITERATURE + METHODOLOGY

```
Based on the literature I have reviewed, help me identify a research gap.

Requirements:
- The gap must emerge from actual reviewed evidence.
- Show which studies support the gap claim.
- Explain why the gap matters.
- Assess whether this gap is addressable in my study scope.

Do not claim "no research has been done" unless verified.
```

### Systematic Search Strategy

> **Required modules:** CORE + LITERATURE

```
Help me design a systematic literature search strategy.

Research topic: [your topic]

Define:
- search keywords and Boolean combinations
- target databases (Scopus, WoS, IEEE, ACM, etc.)
- inclusion criteria
- exclusion criteria
- year range justification
- quality assessment criteria

Follow PRISMA guidelines where applicable.
```

---

## Methodology

### Design Research Methodology

> **Required modules:** CORE + METHODOLOGY

```
Help me design the research methodology.

Research question: [your RQ]

Define:
- research design type and justification
- variables (independent, dependent, control)
- operational definitions
- population and sampling strategy
- data collection method
- validity and reliability plan
- threats to validity

The method must be able to answer the research question.
Do not suggest methods without justification.
```

### Questionnaire / Survey Design

> **Required modules:** CORE + METHODOLOGY + HUMAN

```
Help me design a research questionnaire.

Research variable: [your variable]
Target respondents: [description]

Requirements:
- items must align with operational definition
- use validated scales where possible
- explain Likert scale or measurement choice
- address content validity plan
- address reliability testing plan (e.g., Cronbach's alpha threshold)

Do not create items that cannot be traced to the research variable.
```

### Sampling Strategy

> **Required modules:** CORE + METHODOLOGY

```
Help me determine sampling strategy and sample size.

Population: [description]
Research design: [your design]

Address:
- sampling technique and justification
- sample size calculation or rule
- inclusion/exclusion criteria
- potential sampling bias
- generalizability boundaries
```

---

## Experiment

### Design Experiment Protocol

> **Required modules:** CORE + METHODOLOGY + EXPERIMENT

```
Help me design an experiment protocol.

Research context: [your context]

Define:
- dataset description and source
- train/validation/test split strategy
- baseline models or methods
- proposed method
- evaluation metrics and justification
- hyperparameter tuning strategy
- random seed and reproducibility plan
- number of runs
- leakage prevention checklist

Do not claim any result before the experiment is executed.
```

### Experiment Leakage Check

> **Required modules:** CORE + EXPERIMENT

```
Review my experiment design for potential data leakage.

Check:
- Was test data used during training or tuning?
- Was feature engineering applied before splitting?
- Is there temporal or group leakage?
- Are evaluation metrics computed on the correct split?
- Were hyperparameters selected using test performance?

Report each issue with severity (CRITICAL / MAJOR / MINOR).
```

---

## Analysis

### Interpret Experiment Results

> **Required modules:** CORE + ANALYSIS

```
Here are my experiment results: [paste results]

Analyze:
- descriptive statistics
- performance comparison across methods
- statistical significance (if applicable)
- effect size and practical significance
- confidence intervals or uncertainty
- error analysis

Keep conclusions within what the evidence supports.
Do not overclaim. State limitations clearly.
```

### Statistical Test Selection

> **Required modules:** CORE + ANALYSIS

```
Help me select the appropriate statistical test.

Data characteristics:
- sample size: [N]
- number of groups: [N]
- data type: [continuous/ordinal/nominal]
- distribution: [normal/non-normal/unknown]
- design: [independent/paired/repeated measures]

Recommend the test, state assumptions, and explain what the result would mean.
```

---

## Writing

### Write Literature Review Section

> **Required modules:** CORE + LITERATURE + WRITING

```
Help me write the literature review section.

Based on the papers and evidence matrix I have provided:
- synthesize findings (do not just list papers)
- build a logical argument toward the research gap
- maintain consistent terminology
- distinguish source facts from interpretation
- use calibrated claim strength

Do not add citations I have not provided.
Do not use generic academic filler.
```

### Write Methodology Section

> **Required modules:** CORE + METHODOLOGY + WRITING

```
Help me write the methodology section based on my research design.

Include:
- research design overview
- population and sampling
- variables and operational definitions
- data collection procedure
- data analysis plan
- validity and reliability

Write in clear academic prose.
Do not invent methodological details I have not defined.
```

### Write Results and Discussion

> **Required modules:** CORE + ANALYSIS + WRITING

```
Help me write the results and discussion section.

Based on my actual experiment results:
- present results clearly with appropriate tables/figures
- compare with baseline and previous work
- discuss implications
- state limitations honestly
- keep discussion proportional to evidence

Do not claim results that were not produced.
Do not strengthen conclusions beyond what the data shows.
```

---

## Audit and Review

### Critical Reviewer Mode

> **Required modules:** CORE + relevant modules

```
Act as a critical research reviewer.

Review my [chapter/section/design] and identify:
- unsupported assumptions
- methodological weaknesses
- missing evidence
- overclaiming
- verification gaps

For each issue, state:
- what is wrong
- why it matters
- what should change
- how to verify the correction

Do not invent criticism without basis.
If the work is strong, say so.
```

### Full Research Audit

> **Required modules:** CORE + ALL used modules + AUDIT

```
Perform a full research audit using 07-research-audit.md.

Check alignment across:
- research question and method
- method and experiment
- experiment and analysis
- analysis and conclusion
- literature and research gap
- writing and evidence

For each area, report PASS or FAIL with evidence.
Final status must be: READY / READY WITH LIMITATIONS / NOT READY.
```

### Background Section Review

> **Required modules:** CORE + LITERATURE + WRITING + BACKGROUND-GENERATOR

```
Review my research background section using 11-research-background-generator.md.

Check:
- Is the problem clearly defined with evidence?
- Are claims supported by citations?
- Is previous research synthesized (not just listed)?
- Is the research gap evidence-based?
- Does the objective follow from the gap?
- Are there generic fillers that should be replaced?

Use the B-XX audit format for each finding.
```

---

## Domain-Specific

### Adapt for My Research Domain

> **Required modules:** CORE + DOMAIN-ADAPTATION

```
I am conducting research in the field of [your domain].

Use 10-research-domain-adaptation.md.

Select the relevant modules for my domain.

Research topic: [your topic]
Current task: [your task]

Check:
- methodological fit for this domain
- domain-specific evidence requirements
- common risks to avoid in this field
```

---

## Tips for Using These Prompts

1. **Replace bracketed text** `[like this]` with your actual information.
2. **Upload the required modules** listed above each prompt before using it.
3. **Combine prompts** as needed - start with research planning, then move to methodology, then experiment, etc.
4. **Do not use all prompts at once.** Follow the research lifecycle order.
5. **Verify AI output** against your actual sources and data.
