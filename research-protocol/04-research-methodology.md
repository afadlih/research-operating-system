# research-methodology

> Research design, variable definition, operationalization, sampling, controls, validity, bias, protocol design, methodological justification, and defensible study construction.

## 1. Purpose

This module complements `00-RESEARCH-CORE.md`.

Use it whenever research work involves:

- choosing a research design;
- defining variables or constructs;
- operationalizing concepts;
- selecting a population or sample;
- defining inclusion and exclusion criteria;
- choosing controls or comparison groups;
- planning data collection;
- designing observational or experimental procedures;
- evaluating threats to validity;
- justifying methodological decisions;
- aligning the method with the research question.

The goal is not to make a methodology section look complete.

The goal is to ensure that the study design can **actually generate evidence capable of answering the research question**.

Priority order:

**research-question alignment > validity > measurement quality > bias control > methodological transparency > reproducibility > elegance**

---

## 2. Boundary With the Core

This module must never weaken `00-RESEARCH-CORE.md`.

The core governs:

- research integrity;
- evidence;
- traceability;
- verification;
- reproducibility;
- claim calibration.

This module governs how evidence is generated.

A beautifully written method is still invalid if:

- the design cannot answer the research question;
- variables are poorly defined;
- sampling is biased;
- controls are missing;
- data collection introduces systematic error;
- the analysis does not match the design.

Methodological correctness comes before methodological presentation.

---

## 3. Methodology Principle

Every methodological choice must answer:

1. What research question does this choice serve?
2. What evidence is needed to answer that question?
3. Why can this design produce that evidence?
4. What assumptions does the design make?
5. What bias can enter?
6. What alternative designs were available?
7. Why is this design acceptable under the study constraints?
8. What limits remain after the design is implemented?

Methodology should be built from the research question outward.

Preferred direction:

**research problem -> research question -> required evidence -> design -> measurement -> data collection -> analysis -> conclusion boundaries**

---

# 4. RESEARCH DESIGN SELECTION

## M-01. The Design Must Match the Research Question

Do not choose a design because it is common or convenient.

Examples:

**Descriptive question**

> What patterns exist?

May require:

- descriptive statistics;
- content analysis;
- observational data.

**Comparative question**

> Does method A differ from method B?

May require:

- controlled comparison;
- matched conditions;
- repeated evaluation.

**Associational question**

> Is X related to Y?

May require:

- correlational or regression design.

**Causal question**

> Does X cause Y?

Requires a design that supports causal inference.

## M-02. Do Not Use Causal Language With Non-Causal Designs

Observational association does not prove causation.

If the design cannot isolate causal effects, use bounded wording:

- associated with;
- related to;
- correlated with;
- predictive of.

## M-03. Experimental Designs Require Controlled Manipulation

An experiment generally requires:

- a manipulated condition;
- a comparison condition;
- a defined outcome;
- procedures that reduce alternative explanations.

Do not call a study experimental merely because software or models are tested.

## M-04. Observational Designs Require Confounding Awareness

If variables are not manipulated, identify plausible confounders.

Do not treat observed differences as isolated effects automatically.

## M-05. Exploratory Research Must Be Labeled Honestly

Exploratory work is valid.

Do not disguise exploratory analysis as confirmatory hypothesis testing.

Distinguish:

- exploratory;
- confirmatory;
- descriptive;
- predictive;
- explanatory;
- causal.

---

# 5. RESEARCH QUESTION ALIGNMENT

## M-06. Every Research Question Must Be Operationally Answerable

A good research question must map to:

- observable data;
- measurable variables;
- identifiable comparisons;
- interpretable outcomes.

If the RQ cannot be connected to a measurement or analysis, it is not yet operational.

## M-07. One Research Question Should Not Hide Multiple Unrelated Questions

Bad:

> How accurate, usable, efficient, fair, and secure is the system?

This combines multiple constructs and may require multiple methods.

Split where necessary.

## M-08. Research Objectives Must Match the RQs

Do not create objectives that introduce new goals not represented in the research questions.

## M-09. Hypotheses Must Be Derived, Not Invented After Results

If hypotheses are confirmatory, define them before analyzing the outcome.

Post-hoc patterns should be reported as exploratory.

---

# 6. CONSTRUCT DEFINITION

## M-10. Define Abstract Constructs Explicitly

Examples:

- usability;
- trust;
- engagement;
- performance;
- fairness;
- robustness;
- satisfaction;
- learning outcome.

Do not assume these terms have one universal meaning.

State what the construct means in the current study.

## M-11. Distinguish Construct From Measurement

Example:

**Construct**

> usability

**Possible measurements**

- task completion;
- SUS score;
- time on task;
- error rate.

The measurement is not the construct itself.

## M-12. Competing Definitions Must Be Resolved

If the literature uses multiple definitions, choose one and justify it.

Do not combine incompatible definitions silently.

---

# 7. OPERATIONALIZATION

## M-13. Every Variable Must Have an Operational Definition

For each variable, specify:

- what it represents;
- how it is measured;
- units or scale;
- source;
- transformation;
- timing where relevant.

## M-14. Proxy Measures Must Be Identified as Proxies

Example:

> Number of clicks was used as a proxy for interaction effort.

Do not present a proxy as the construct itself.

## M-15. Operationalization Must Preserve Meaning

Avoid measurements that are convenient but poorly aligned with the construct.

Example:

> accuracy

is not automatically equivalent to:

> model quality.

## M-16. Threshold-Based Definitions Need Justification

Examples:

- high risk;
- successful task;
- positive sentiment;
- acceptable latency.

If these depend on thresholds, explain the threshold.

---

# 8. VARIABLE ROLES

## M-17. Identify Variable Roles Clearly

When relevant, distinguish:

- independent variable;
- dependent variable;
- control variable;
- confounder;
- mediator;
- moderator;
- covariate;
- outcome;
- predictor.

Do not use these labels loosely.

## M-18. Do Not Control for Variables Without Reason

Over-control can distort interpretation.

Only include controls that are theoretically or methodologically justified.

## M-19. Potential Confounders Must Be Considered

Ask:

> Could a third factor explain the observed relationship?

If yes, account for it through:

- design;
- matching;
- randomization;
- stratification;
- statistical adjustment;
- limitation reporting.

---

# 9. POPULATION AND SAMPLING

## M-20. Define the Target Population

Clarify who or what the study intends to represent.

Examples:

- Indonesian high-school students;
- GitHub repositories meeting specific criteria;
- Indonesian-language product reviews;
- images from a defined benchmark;
- users of a specific application.

## M-21. Distinguish Target Population From Accessible Population

Target population:

> what the study wants to generalize to.

Accessible population:

> what the researcher can actually sample.

Do not treat them as identical without justification.

## M-22. Sampling Method Must Be Explicit

Examples:

- random sampling;
- stratified sampling;
- convenience sampling;
- purposive sampling;
- snowball sampling;
- census;
- benchmark dataset sampling.

## M-23. Sampling Choice Requires Justification

Do not write only:

> Convenience sampling was used.

Explain why, and state the resulting limitation.

## M-24. Sample Size Needs a Reason

Possible justifications include:

- power analysis;
- prior literature;
- population size;
- saturation logic;
- benchmark constraints;
- exhaustive inclusion;
- feasibility constraints.

Do not invent a sample-size formula if it was not used.

## M-25. Large Samples Do Not Automatically Remove Bias

A biased sample remains biased even when large.

## M-26. Sampling Frame Must Be Relevant

If the sampling frame excludes part of the intended population, report the limitation.

---

# 10. INCLUSION AND EXCLUSION CRITERIA

## M-27. Criteria Must Be Defined Before Analysis When Possible

Avoid changing criteria to improve results.

## M-28. Inclusion Criteria Must Serve the Research Scope

Examples:

- publication language;
- minimum data completeness;
- age range;
- model type;
- repository activity;
- diagnosis status;
- date range.

## M-29. Exclusion Must Be Transparent

Report:

- what was excluded;
- how much;
- why.

## M-30. Exclusion Must Not Depend on Desired Outcomes

Never remove cases merely because they reduce performance or contradict expectations.

---

# 11. GROUP AND CONDITION DESIGN

## M-31. Comparison Groups Must Be Meaningful

A comparison must help answer the RQ.

Do not include a control group that does not represent a useful alternative.

## M-32. Conditions Must Differ Only in Intended Factors When Possible

If multiple factors change simultaneously, causal interpretation becomes ambiguous.

## M-33. Treatment and Control Conditions Need Equivalent Procedures

Keep non-target conditions comparable when possible:

- time;
- hardware;
- instructions;
- dataset;
- environment;
- interface;
- preprocessing.

## M-34. Random Assignment Should Be Used When Appropriate

Random assignment can reduce systematic group differences.

If it is not possible, state why and consider alternative controls.

## M-35. Matching Requires Clear Matching Criteria

Do not claim samples are matched without explaining:

- matching variables;
- matching procedure;
- residual imbalance.

---

# 12. RANDOMIZATION

## M-36. Randomization Must Be Real

Do not claim randomization if assignment was:

- sequential;
- convenient;
- manually selected;
- deterministic.

## M-37. Record Random Seeds When Relevant

For computational procedures, preserve random seeds where they materially affect reproducibility.

## M-38. Randomization Does Not Guarantee Perfect Balance

Check balance rather than assuming it.

---

# 13. BLINDING

## M-39. Blinding Should Be Used When Expectation Can Bias Outcomes

Potential targets:

- participants;
- evaluators;
- annotators;
- analysts.

## M-40. State Who Was Blinded

Do not write:

> The study was blinded.

Specify:

- participant-blinded;
- evaluator-blinded;
- analyst-blinded.

## M-41. If Blinding Is Impossible, Report the Risk

Do not pretend the bias does not exist.

---

# 14. MEASUREMENT QUALITY

## M-42. Measurement Must Be Valid for the Construct

Ask:

> Does this instrument measure what the study claims it measures?

## M-43. Reliability and Validity Are Different

Reliability:

> measurement consistency.

Validity:

> whether the measurement represents the intended construct.

A reliable instrument can still be invalid.

## M-44. Use Validated Instruments When Appropriate

If a validated scale exists and matches the population/context, consider it.

Do not modify validated instruments casually.

## M-45. Modified Instruments Require Transparency

If items, translation, scale points, or wording are changed, report the modification.

## M-46. Measurement Error Must Be Considered

Sources may include:

- instrument limitations;
- participant misunderstanding;
- sensor noise;
- annotation disagreement;
- coding errors;
- timing differences.

---

# 15. DATA COLLECTION PROTOCOL

## M-47. Data Collection Must Be Procedurally Defined

Record when relevant:

- who collects data;
- when;
- where;
- with what instrument;
- in what order;
- under what conditions.

## M-48. Procedures Must Be Consistent Across Comparable Cases

If procedures differ, document why.

## M-49. Time Can Be a Confounder

If data collection spans a period where external conditions change, consider time effects.

## M-50. Environment Can Affect Measurements

Examples:

- network speed;
- lighting;
- device type;
- operating system;
- classroom conditions;
- workload;
- external events.

Control or report where relevant.

---

# 16. DATA PROVENANCE

## M-51. Every Dataset Must Have Provenance

Record:

- source;
- creator/provider;
- acquisition method;
- date/version;
- license or access condition when relevant;
- transformations.

## M-52. Derived Data Must Be Traceable

If the final dataset is filtered or transformed, preserve the transformation steps.

## M-53. Synthetic Data Must Be Labeled

Do not mix synthetic and real data without disclosure.

Explain:

- generation method;
- proportion;
- purpose;
- limitations.

---

# 17. MISSING DATA

## M-54. Missing Data Must Be Quantified

Do not say:

> Some values were missing.

Report the extent.

## M-55. Missingness Mechanism Should Be Considered

When relevant, consider whether missingness may be:

- random;
- conditionally random;
- systematically related to the variable or outcome.

## M-56. Missing-Data Handling Requires Justification

Possible approaches:

- deletion;
- simple imputation;
- model-based imputation;
- missingness indicator;
- complete-case analysis.

Do not choose based only on convenience.

## M-57. Imputation Must Not Leak Information

Fit imputation logic using training data only when performing predictive evaluation.

---

# 18. BIAS

## M-58. Identify Plausible Bias Sources

Potential sources:

- selection bias;
- survivorship bias;
- measurement bias;
- observer bias;
- recall bias;
- social desirability bias;
- confirmation bias;
- publication bias;
- sampling bias;
- annotation bias.

## M-59. Bias Must Be Addressed, Not Merely Named

For each important bias:

1. explain how it can enter;
2. explain what was done to reduce it;
3. report residual risk.

## M-60. Researcher Expectations Can Bias Procedures

Where relevant, use:

- predefined criteria;
- blinding;
- automated procedures;
- independent evaluation;
- documented decision rules.

---

# 19. CONFOUNDING

## M-61. Confounders Must Be Plausible, Not Invented

Do not list every imaginable variable.

Focus on factors that can realistically affect both exposure/predictor and outcome.

## M-62. Confounding Control Must Match the Design

Possible approaches:

- randomization;
- matching;
- restriction;
- stratification;
- statistical adjustment.

## M-63. Statistical Adjustment Does Not Automatically Remove All Confounding

Residual and unmeasured confounding may remain.

Do not overstate adjusted results.

---

# 20. INTERNAL VALIDITY

## M-64. Internal Validity Asks Whether the Observed Effect Is Credible Within the Study

Threats may include:

- confounding;
- selection bias;
- history effects;
- maturation;
- instrumentation changes;
- attrition;
- contamination;
- regression to the mean;
- data leakage.

## M-65. Internal Validity Must Be Evaluated Before Generalization

A study with poor internal validity cannot be rescued by broad external claims.

---

# 21. EXTERNAL VALIDITY

## M-66. External Validity Concerns Generalization

Ask whether results may generalize across:

- populations;
- domains;
- languages;
- datasets;
- institutions;
- time periods;
- environments.

## M-67. Benchmark Performance Is Not Automatically Real-World Performance

A controlled benchmark may not capture:

- distribution shift;
- user behavior;
- operational constraints;
- unseen edge cases.

## M-68. Generalization Claims Must Match Evidence

Do not claim broad applicability from one narrow context.

---

# 22. CONSTRUCT VALIDITY

## M-69. Construct Validity Requires Alignment Between Concept and Measurement

If the study claims to measure:

> trust

but only measures:

> willingness to click a button

the construct may be underrepresented.

## M-70. Avoid Mono-Operation Bias When Important

A complex construct measured with only one narrow indicator may be incomplete.

Use multiple indicators when justified.

---

# 23. STATISTICAL CONCLUSION VALIDITY

## M-71. The Design Must Support the Planned Analysis

Check:

- sample size;
- variability;
- independence;
- distribution assumptions;
- multiple comparisons;
- measurement reliability.

## M-72. Low Statistical Power Must Be Acknowledged

A non-significant result is not proof of no effect.

## M-73. Multiple Testing Increases False-Positive Risk

If many hypotheses are tested, consider appropriate correction or qualification.

---

# 24. QUALITATIVE METHODOLOGY

## M-74. Qualitative Design Must Fit the Research Aim

Examples may include:

- case study;
- thematic analysis;
- grounded theory;
- phenomenology;
- content analysis;
- ethnography.

Do not select a label only because it sounds appropriate.

## M-75. Sampling Logic Differs From Quantitative Sampling

Qualitative sampling may be guided by:

- information richness;
- theoretical relevance;
- saturation;
- diversity of perspectives.

Do not force quantitative representativeness concepts onto qualitative designs.

## M-76. Saturation Must Be Explained

Do not claim saturation without explaining:

- what type;
- how assessed;
- under what coding process.

## M-77. Researcher Reflexivity May Be Relevant

If interpretation depends strongly on researcher judgment, document relevant positionality or analytical influence.

---

# 25. MIXED METHODS

## M-78. Mixed Methods Requires Integration

Using both numbers and interviews does not automatically create a mixed-methods design.

Explain how qualitative and quantitative evidence interact.

## M-79. State the Integration Point

Examples:

- design stage;
- data collection;
- analysis;
- interpretation.

## M-80. Resolve Contradictory Findings Explicitly

If qualitative and quantitative results differ, do not hide the discrepancy.

Analyze it.

---

# 26. COMPUTATIONAL RESEARCH DESIGN

## M-81. Computational Studies Still Need Methodological Design

Code execution alone is not a methodology.

Specify:

- task definition;
- data;
- preprocessing;
- baseline;
- model;
- tuning;
- evaluation;
- statistical comparison;
- reproducibility.

## M-82. Dataset Split Is Part of the Design

Define:

- training;
- validation;
- test;
- cross-validation;
- temporal split;
- group split.

Choose based on the problem.

## M-83. Random Split Is Not Always Appropriate

For temporal, grouped, repeated-subject, or hierarchical data, random splitting may leak structure.

## M-84. Test Data Must Remain Independent

Do not use test data for:

- feature decisions;
- parameter tuning;
- threshold selection;
- model selection.

## M-85. Repeated Experiments May Be Necessary

For stochastic algorithms, one run may not represent typical performance.

Use repeated runs or confidence intervals when justified.

---

# 27. PROTOCOL DEVIATIONS

## M-86. Deviations Must Be Recorded

If the actual method differs from the planned method, document:

- what changed;
- why;
- when;
- effect on interpretation.

## M-87. Do Not Rewrite History

Do not make post-hoc decisions appear pre-planned.

Transparency is better than artificial methodological neatness.

---

# 28. FEASIBILITY AND CONSTRAINTS

## M-88. Constraints Can Justify Design Choices

Examples:

- limited sample access;
- computational resources;
- licensing;
- time;
- hardware;
- institutional restrictions.

A constrained design can still be valid within a narrower claim.

## M-89. Constraints Must Not Be Used to Hide Invalidity

If a constraint makes the research question unanswerable, narrow or redesign the study.

---

# 29. ETHICAL-METHODOLOGICAL INTERFACE

## M-90. Ethics and Methodology Can Affect Each Other

Examples:

- privacy constraints may limit data collection;
- informed consent may change sampling;
- risk minimization may change procedures.

Document important effects.

## M-91. Ethical Approval Does Not Prove Methodological Validity

Ethical review and methodological rigor are separate.

---

# 30. PILOTING

## M-92. Pilot Studies Should Test the Procedure

A pilot may assess:

- instrument clarity;
- timing;
- feasibility;
- technical reliability;
- recruitment;
- variance;
- expected failure modes.

## M-93. Pilot Changes Must Be Documented

If the pilot changes the protocol, record the revision.

## M-94. Pilot Results Must Not Be Overgeneralized

A pilot is not automatically powered for substantive conclusions.

---

# 31. PRE-REGISTRATION AND PRE-SPECIFICATION

## M-95. Pre-Specification Can Reduce Analytical Flexibility

When applicable, define before analysis:

- hypotheses;
- primary outcome;
- exclusion rules;
- analysis plan;
- subgroup analyses.

## M-96. Deviations From Pre-Specification Must Be Disclosed

Post-hoc analysis can still be useful.

Label it correctly.

---

# 32. METHOD JUSTIFICATION

## M-97. Every Major Methodological Choice Needs One-Line Justification

Before finalization, be able to answer:

- Why this design?
- Why this population?
- Why this sample?
- Why this instrument?
- Why this variable?
- Why this control?
- Why this split?
- Why this metric?
- Why this analysis?

If the answer is only:

> because it is common,

the justification is weak.

## M-98. Literature Can Support a Choice, but Does Not Replace Fit

A method used successfully elsewhere may still be inappropriate here.

Evaluate local fit.

---

# 33. METHODOLOGY TRACEABILITY MATRIX

When useful, maintain:

| Research Question | Required Evidence | Variable/Construct | Data Source | Method | Analysis | Conclusion Boundary |
|---|---|---|---|---|---|---|

The matrix should reveal any RQ that lacks evidence or any analysis not linked to an RQ.

---

# 34. VARIABLE DICTIONARY

For complex studies, maintain:

| Variable | Role | Definition | Measurement | Scale/Unit | Source | Transformation |
|---|---|---|---|---|---|---|

This prevents terminology drift and analytical ambiguity.

---

# 35. THREAT-TO-VALIDITY REGISTER

Maintain a register when useful:

| Threat | Type | How It Could Affect Results | Mitigation | Residual Risk |
|---|---|---|---|---|

Types may include:

- internal;
- external;
- construct;
- statistical conclusion.

Do not include generic threats without relevance.

---

# 36. METHODOLOGY AUDIT FORMAT

Use:

> **M-XX | SEVERITY | LOCATION**  
> **Problem:** what is methodologically wrong.  
> **Why:** why the design cannot support the intended inference.  
> **Evidence:** where the issue appears.  
> **Impact:** what part of the result or conclusion is affected.  
> **Correction:** what should change.  
> **Verification:** how to confirm the corrected method.

Example:

> **M-84 | CRITICAL | Experiment design**  
> **Problem:** the test set was used to select the final classification threshold.  
> **Why:** the test set is no longer independent and the reported performance is optimistically biased.  
> **Evidence:** threshold selection is performed after inspecting test-set F1.  
> **Impact:** the final test metric cannot be treated as an unbiased generalization estimate.  
> **Correction:** select the threshold using validation data, then evaluate once on the untouched test set.  
> **Verification:** rerun the protocol with an independent test evaluation.

---

# 37. METHODOLOGY QUALITY GATE

Before marking methodology final, verify:

## Alignment

- [ ] Every RQ maps to required evidence.
- [ ] The chosen design can generate that evidence.
- [ ] Objectives and hypotheses align with RQs.
- [ ] Analysis follows from the design.

## Constructs and Variables

- [ ] Constructs are clearly defined.
- [ ] Variables have operational definitions.
- [ ] Proxy measures are identified as proxies.
- [ ] Variable roles are explicit.
- [ ] Thresholds are justified.

## Population and Sampling

- [ ] Target population is defined.
- [ ] Accessible population is distinguished where relevant.
- [ ] Sampling method is explicit.
- [ ] Sample-size reasoning is documented.
- [ ] Inclusion/exclusion criteria are justified.
- [ ] Generalization does not exceed the sample.

## Design Integrity

- [ ] Comparison groups are meaningful.
- [ ] Conditions are comparable.
- [ ] Randomization is real when claimed.
- [ ] Blinding is described accurately.
- [ ] Confounders are considered.
- [ ] Bias mitigation is documented.

## Measurement

- [ ] Instruments match the intended constructs.
- [ ] Reliability and validity are not conflated.
- [ ] Instrument modifications are disclosed.
- [ ] Measurement error is considered.

## Data Collection

- [ ] Procedure is reproducible enough for the research type.
- [ ] Environment and timing are controlled or reported.
- [ ] Data provenance is clear.
- [ ] Missing-data handling is justified.

## Validity

- [ ] Internal validity threats are considered.
- [ ] External validity is bounded.
- [ ] Construct validity is addressed.
- [ ] Statistical conclusion validity is considered.

## Computational Methodology

- [ ] Dataset splitting matches the data structure.
- [ ] Test data remain independent.
- [ ] No leakage is present.
- [ ] Stochastic variation is handled when relevant.
- [ ] Protocol deviations are documented.

Any material failure must be corrected, bounded, or explicitly reported before methodology is labeled final.

---

# 38. Recommended Workflow

Use this module in the following order:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `04-research-methodology.md`
4. `02-research-human.md` when people are involved
5. `05-research-experiment.md` for computational experiments
6. `06-research-analysis.md`
7. `01-research-writing.md`
8. final Research Delivery Gate

Methodology should define how evidence will be produced before analysis begins.

---

# 39. Final Principles

**Research question > favorite method**  
**Design fit > methodological fashion**  
**Operational clarity > abstract wording**  
**Measurement validity > convenient metrics**  
**Bias control > optimistic interpretation**  
**Transparent constraints > hidden compromises**  
**Independent test evidence > tuned test performance**  
**Defined population > vague generalization**  
**Traceable procedure > methodological appearance**  
**Validity > complexity**  
**Methodological honesty > perfect-looking protocol**
