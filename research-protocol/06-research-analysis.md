# research-analysis

> Statistical analysis, uncertainty, effect sizes, assumptions, hypothesis testing, model interpretation, qualitative analysis, sensitivity, limitations, and disciplined conclusion-making.

## 1. Purpose

This module complements:

- `00-RESEARCH-CORE.md`
- `04-research-methodology.md`
- `05-research-experiment.md`

Use it whenever research involves interpreting collected data or experimental outputs.

Typical uses include:

- descriptive statistics;
- hypothesis testing;
- confidence intervals;
- effect-size analysis;
- regression;
- correlation;
- classification metrics;
- model comparison;
- residual analysis;
- subgroup analysis;
- sensitivity analysis;
- uncertainty estimation;
- qualitative coding;
- mixed-method interpretation;
- limitation analysis;
- result interpretation;
- conclusion construction.

The goal is not to produce statistically impressive output.

The goal is to transform evidence into **valid, calibrated, traceable conclusions**.

Priority order:

**correct interpretation > uncertainty awareness > effect magnitude > statistical significance > narrative simplicity**

---

## 2. Boundary With Other Modules

This module does not replace:

- `04-research-methodology.md` for study design;
- `05-research-experiment.md` for experiment execution;
- `02-research-human.md` for human-evaluation validity;
- `01-research-writing.md` for final prose quality.

The methodology determines what can be inferred.

The experiment determines what evidence was produced.

The analysis determines what the evidence supports.

The writing module determines how that conclusion is communicated.

Do not use analysis to repair a fundamentally invalid design.

---

## 3. Analysis Principle

Every analytical step should answer:

1. What question is being answered?
2. What data support the analysis?
3. What assumptions are required?
4. Are those assumptions reasonable?
5. What quantity is being estimated?
6. What uncertainty remains?
7. What alternative explanations exist?
8. What conclusion is justified?
9. What conclusion is not justified?

Analysis should move:

**data -> summary -> test/estimate -> uncertainty -> interpretation -> bounded conclusion**

not:

**desired conclusion -> selective statistic -> narrative**

---

# 4. DATA SANITY BEFORE ANALYSIS

## A-01. Inspect Data Before Formal Analysis

Before hypothesis testing or modeling, verify when relevant:

- sample count;
- missing values;
- duplicate records;
- impossible values;
- category balance;
- label distribution;
- range;
- units;
- coding consistency.

Do not begin statistical interpretation before confirming that the dataset is internally plausible.

## A-02. Analysis Must Use the Intended Final Dataset

Confirm that the analyzed data match the methodology.

If exclusions, filters, or transformations changed the dataset, record them.

## A-03. Derived Variables Must Be Traceable

For every derived variable, preserve:

- formula;
- source variables;
- transformation;
- units;
- handling of missing values.

## A-04. Unit Consistency Must Be Verified

Do not combine:

- milliseconds and seconds;
- percentages and proportions;
- normalized and raw values;

without explicit conversion.

---

# 5. DESCRIPTIVE STATISTICS

## A-05. Describe the Data Before Testing It

Useful descriptive summaries may include:

- count;
- mean;
- median;
- standard deviation;
- interquartile range;
- minimum;
- maximum;
- frequency;
- proportion.

Choose summaries appropriate to the data distribution.

## A-06. Mean Is Not Always the Best Summary

For skewed distributions, median and IQR may be more informative.

Do not use mean automatically.

## A-07. Standard Deviation and Standard Error Are Different

Standard deviation describes variability in observations.

Standard error describes uncertainty in an estimated statistic.

Do not interchange them.

## A-08. Percentages Need Denominators

Bad:

> 60% succeeded.

Better:

> 60% (30 of 50 participants) completed the task.

Use denominators when useful for interpretation.

---

# 6. DISTRIBUTION AND ASSUMPTIONS

## A-09. Statistical Tests Have Assumptions

Potential assumptions include:

- independence;
- normality;
- equal variance;
- linearity;
- homoscedasticity;
- sufficient expected cell counts;
- absence of severe multicollinearity.

Check assumptions relevant to the chosen method.

## A-10. Do Not Perform Assumption Checks Mechanically

An assumption test is not useful merely because a textbook lists it.

Focus on assumptions that materially affect inference.

## A-11. Visual Diagnostics Can Be More Informative Than a Single Test

Use when relevant:

- histogram;
- Q-Q plot;
- residual plot;
- scatter plot.

Do not rely only on one p-value for distributional assessment.

## A-12. Large Samples Can Make Normality Tests Over-Sensitive

A statistically significant normality test does not automatically mean a parametric analysis is unusable.

Interpret diagnostics in context.

## A-13. Small Samples Can Hide Assumption Violations

A non-significant assumption test with low sample size does not prove the assumption holds.

---

# 7. HYPOTHESIS TESTING

## A-14. Define the Hypothesis Before Interpreting the Test

State:

- null hypothesis;
- alternative hypothesis;
- test statistic;
- significance level when applicable;
- one-sided or two-sided design.

## A-15. p-Value Is Not the Probability That the Null Hypothesis Is True

Do not interpret:

> p = 0.03

as:

> There is a 97% probability that the alternative hypothesis is true.

## A-16. Statistical Significance Is Not Effect Importance

A very small effect can be statistically significant in a large sample.

Always consider magnitude.

## A-17. Non-Significance Is Not Proof of No Effect

A non-significant result may reflect:

- small effect;
- insufficient power;
- high variance;
- poor measurement;
- genuinely negligible effect.

Avoid:

> There is no difference.

Prefer:

> The analysis did not detect a statistically significant difference under the current design.

when appropriate.

## A-18. One-Sided Tests Need Prior Justification

Do not switch to a one-sided test after seeing the direction of results.

## A-19. Significance Thresholds Are Conventions, Not Laws

Do not treat `p < 0.05` as a universal boundary between truth and falsehood.

---

# 8. EFFECT SIZE

## A-20. Report Effect Magnitude When It Matters

Potential measures include:

- mean difference;
- standardized mean difference;
- odds ratio;
- risk ratio;
- correlation coefficient;
- eta-squared;
- partial eta-squared;
- rank-based effect measures.

Choose according to design.

## A-21. Effect Size Must Match the Question

Do not report a standardized effect merely because software outputs it.

## A-22. Interpret Effect Size in Context

Generic labels such as:

- small;
- medium;
- large;

may not reflect domain importance.

Prefer domain-relevant interpretation when possible.

## A-23. Practical Importance Can Differ From Statistical Significance

A statistically significant 0.1% performance improvement may be irrelevant.

A statistically uncertain but operationally large effect may still deserve investigation.

---

# 9. CONFIDENCE INTERVALS AND UNCERTAINTY

## A-24. Report Uncertainty Around Important Estimates

Examples:

- confidence intervals;
- credible intervals;
- bootstrap intervals;
- standard errors;
- prediction intervals.

## A-25. Confidence Intervals Must Be Interpreted Correctly

Do not describe a frequentist 95% confidence interval as:

> There is a 95% probability that the true parameter lies inside this specific interval.

Use wording consistent with the method.

## A-26. Wide Intervals Indicate Imprecision

Do not hide wide uncertainty behind a point estimate.

## A-27. Narrow Intervals Do Not Guarantee Validity

A precise estimate from biased data can still be wrong.

---

# 10. MULTIPLE COMPARISONS

## A-28. Multiple Testing Increases False-Positive Risk

If many hypotheses are tested, consider:

- correction;
- hierarchical testing;
- pre-specified primary outcomes;
- explicit exploratory labeling.

## A-29. Do Not Search Many Tests and Report Only the Significant Ones

This is selective reporting.

Preserve the actual analysis plan and relevant outcomes.

## A-30. Exploratory Analysis Must Be Labeled Exploratory

Post-hoc findings can be useful.

Do not present them as pre-specified confirmation.

---

# 11. CORRELATION

## A-31. Correlation Does Not Establish Causation

A correlation may reflect:

- direct relation;
- reverse causation;
- confounding;
- shared measurement artifact;
- chance.

## A-32. Pearson and Spearman Are Not Interchangeable

Choose based on:

- measurement scale;
- relationship shape;
- outliers;
- assumptions.

## A-33. A Near-Zero Correlation Does Not Rule Out Nonlinear Relationships

Inspect the data when the research question requires it.

## A-34. Correlation Magnitude Needs Context

A coefficient of `0.30` may be meaningful in one domain and weak in another.

---

# 12. REGRESSION ANALYSIS

## A-35. Model Specification Must Follow the Research Question

Do not add predictors only because they improve fit.

## A-36. Coefficients Require Correct Interpretation

Interpret according to:

- scale;
- transformation;
- link function;
- interaction terms.

## A-37. Multicollinearity Must Be Considered

Highly correlated predictors can destabilize coefficient interpretation.

## A-38. Residual Diagnostics Matter

Inspect when relevant:

- residual distribution;
- heteroscedasticity;
- influential points;
- nonlinearity;
- autocorrelation.

## A-39. Adjusted Associations Are Not Automatically Causal Effects

Statistical control does not remove all confounding.

---

# 13. CLASSIFICATION METRICS

## A-40. Accuracy Must Be Interpreted With Class Distribution

High accuracy may reflect majority-class dominance.

## A-41. Precision and Recall Answer Different Questions

Precision:

> Of predicted positives, how many were correct?

Recall:

> Of actual positives, how many were detected?

Do not use them interchangeably.

## A-42. F1 Depends on the Averaging Scheme

Specify:

- binary;
- macro;
- micro;
- weighted.

## A-43. ROC-AUC and PR-AUC Serve Different Contexts

For strongly imbalanced data, PR-AUC may be more informative.

## A-44. Threshold-Dependent Metrics Need Threshold Disclosure

Report how the classification threshold was chosen.

---

# 14. CALIBRATION

## A-45. Accuracy and Calibration Are Different

A model can be accurate but poorly calibrated.

## A-46. Probability Claims Require Calibration Evidence

If predicted probabilities are interpreted as confidence, evaluate calibration where relevant.

Potential tools:

- reliability diagram;
- Brier score;
- expected calibration error.

## A-47. Calibration Must Be Evaluated on Held-Out Data

Do not assess calibration only on training data.

---

# 15. MODEL COMPARISON

## A-48. Compare Under Equivalent Conditions

Before interpreting differences, verify:

- same test set;
- same metric;
- same preprocessing;
- comparable tuning budget;
- comparable data access.

## A-49. Small Metric Differences Need Uncertainty Analysis

A difference of `0.003` may be meaningless if run-to-run variability is larger.

## A-50. Best Mean Score Is Not Automatically a Meaningful Winner

Consider:

- variance;
- effect magnitude;
- uncertainty;
- practical cost;
- robustness.

Do not rank methods beyond what evidence supports.

## A-51. Literature Scores Are Not Directly Comparable Unless Protocols Match

Do not mix internal experiment results and external benchmark numbers as if they came from one controlled comparison.

---

# 16. STOCHASTIC RESULTS

## A-52. Analyze Variation Across Runs

For repeated stochastic runs, consider:

- mean;
- standard deviation;
- confidence interval;
- median;
- distribution.

## A-53. Do Not Report Only the Best Seed

Best-run reporting exaggerates typical performance.

## A-54. Stability Is Part of Performance

A slightly lower but stable method may be analytically different from a high-variance method.

Do not ignore variance.

---

# 17. OUTLIERS

## A-55. Outliers Must Not Be Removed Automatically

An outlier may represent:

- measurement error;
- valid rare case;
- distribution tail;
- subgroup;
- data-entry mistake.

Investigate first.

## A-56. Outlier Removal Needs a Rule

Document:

- criterion;
- timing;
- number removed;
- reason.

## A-57. Sensitivity With and Without Outliers Can Be Useful

If conclusions change materially, report that instability.

---

# 18. MISSING DATA ANALYSIS

## A-58. Quantify Missingness

Report:

- variables affected;
- amount missing;
- pattern if relevant.

## A-59. Missingness Can Bias Results

Do not assume complete cases are representative.

## A-60. Compare Missing-Data Strategies When Material

If conclusions depend on how missing values are handled, perform sensitivity analysis.

---

# 19. SUBGROUP ANALYSIS

## A-61. Subgroups Need Prior or Theoretical Justification

Avoid creating many post-hoc subgroups to search for favorable findings.

## A-62. Small Subgroups Require Wider Uncertainty

Do not make strong claims from tiny subgroup samples.

## A-63. Interaction Tests Are Often Better Than Separate Significance Tests

Do not conclude subgroup differences merely because one subgroup is significant and another is not.

## A-64. Multiple Subgroup Analyses Need Multiplicity Awareness

Treat extensive subgroup exploration as exploratory unless properly planned.

---

# 20. ERROR ANALYSIS

## A-65. Analyze Failure Patterns, Not Only Aggregate Scores

Useful questions:

- Which classes fail most?
- Which inputs produce systematic errors?
- Are errors concentrated in one subgroup?
- Are failures semantically similar?
- Are there rare but severe failures?

## A-66. Error Categories Need Defined Criteria

Avoid arbitrary post-hoc categories without documentation.

## A-67. Counterexamples Should Be Preserved

Do not select only examples that make the system look good.

## A-68. Error Analysis Can Refine Interpretation but Not Retroactively Change the Test Set

Do not modify evaluation data after inspecting failures unless creating a new clearly separated study phase.

---

# 21. SENSITIVITY ANALYSIS

## A-69. Test Important Analytical Choices

Potential targets:

- threshold;
- exclusion rules;
- imputation;
- transformation;
- statistical model;
- seed aggregation;
- subgroup definition.

## A-70. A Robust Conclusion Should Survive Reasonable Alternatives

If a conclusion disappears under minor analytical changes, report the fragility.

## A-71. Sensitivity Analysis Is Not Cherry-Picking

Evaluate plausible alternatives systematically, not only those that preserve the preferred result.

---

# 22. ROBUSTNESS OF CONCLUSIONS

## A-72. Distinguish Model Robustness From Conclusion Robustness

A model may be robust to noise while the statistical conclusion remains fragile.

## A-73. Robustness Claims Need a Defined Stressor

Examples:

- distribution shift;
- label noise;
- parameter variation;
- subgroup shift;
- missing features.

## A-74. Do Not Use "Robust" as a Generic Positive Adjective

Use it only when a robustness test exists.

---

# 23. BAYESIAN ANALYSIS

## A-75. Priors Must Be Reported

Document:

- prior family;
- parameters;
- rationale.

## A-76. Posterior Probability Must Be Interpreted Correctly

Bayesian probability statements differ from frequentist confidence intervals.

Do not mix interpretations.

## A-77. Prior Sensitivity May Matter

If conclusions change substantially under reasonable priors, report that.

---

# 24. QUALITATIVE ANALYSIS

## A-78. Qualitative Analysis Needs an Explicit Analytical Approach

Examples:

- thematic analysis;
- content analysis;
- grounded theory coding;
- framework analysis.

Do not write:

> Responses were analyzed qualitatively.

without explaining how.

## A-79. Coding Must Be Traceable

Record when relevant:

- coding stages;
- codebook;
- coder identity;
- revisions;
- disagreement process.

## A-80. Themes Must Be Grounded in Data

Themes should be supported by:

- recurring patterns;
- representative excerpts;
- counterexamples where relevant.

## A-81. Frequency Is Not the Only Measure of Importance

A rare theme may still be analytically important.

Do not reduce qualitative analysis to counts unless the design calls for it.

## A-82. Researcher Interpretation Must Be Visible

Do not imply that themes appeared automatically.

Explain the analytical process.

---

# 25. MIXED-METHOD ANALYSIS

## A-83. Quantitative and Qualitative Results Must Be Integrated

Do not place them in separate chapters and call that integration.

## A-84. Define How One Evidence Type Informs the Other

Possible relationships:

- explanation;
- convergence;
- complementarity;
- contradiction;
- expansion.

## A-85. Contradictory Evidence Must Be Preserved

If survey scores are positive but interviews reveal serious usability problems, analyze the discrepancy.

Do not choose one side silently.

---

# 26. CAUSAL INTERPRETATION

## A-86. Causal Claims Require Causal Identification

Ask:

1. What is the treatment/exposure?
2. What is the outcome?
3. What alternative explanations exist?
4. What design element blocks them?
5. What assumptions are required?

## A-87. Temporal Order Alone Does Not Prove Causality

`X happened before Y` is necessary for many causal claims but not sufficient.

## A-88. Statistical Adjustment Alone Does Not Prove Causality

Regression can adjust measured confounders.

Unmeasured confounding may remain.

## A-89. Use Causal Language Proportionally

Prefer:

- associated with;
- consistent with;
- may contribute to;

when causal evidence is incomplete.

---

# 27. PRACTICAL SIGNIFICANCE

## A-90. Ask Whether the Effect Matters in Practice

Examples:

- Is a 0.5 ms improvement meaningful?
- Is a 1-point survey difference noticeable?
- Is a 0.3% accuracy gain worth double the compute cost?

## A-91. Operational Cost Can Change Interpretation

Consider when relevant:

- latency;
- memory;
- energy;
- API cost;
- annotation cost;
- implementation complexity.

## A-92. Practical Significance Must Not Replace Statistical Rigor

A large-looking effect still needs valid measurement.

---

# 28. UNCERTAINTY COMMUNICATION

## A-93. Distinguish Known, Estimated, and Unknown

Use:

- observed;
- estimated;
- inferred;
- uncertain;
- not measured.

## A-94. Do Not Hide Uncertainty Behind Definitive Language

Bad:

> The method improves generalization.

Better:

> Under the evaluated dataset and split, the method produced higher test macro-F1, but broader generalization was not tested.

## A-95. Report Residual Uncertainty

Even after a statistically significant result, uncertainty remains about:

- external validity;
- measurement;
- model assumptions;
- unmeasured confounding.

---

# 29. LIMITATIONS

## A-96. Limitations Must Follow From the Evidence and Design

Good limitations identify:

- what is constrained;
- why it matters;
- what inference is affected.

## A-97. Separate Methodological Limitation From Future Work

A limitation explains current uncertainty.

Future work proposes a next step.

Do not merge them mechanically.

## A-98. Do Not Use Generic Limitations as Decoration

Bad:

> Time and resources were limited.

Better:

> The study used a single institution and convenience sampling, so population-level generalization is limited.

## A-99. Limitations Should Calibrate, Not Destroy, the Study

Do not exaggerate limitations to the point that valid results appear meaningless.

State their actual effect.

---

# 30. RESULTS VS DISCUSSION

## A-100. Results Report What Happened

Results may include:

- descriptive statistics;
- model scores;
- effect estimates;
- confidence intervals;
- test statistics.

## A-101. Discussion Explains What the Results May Mean

Discussion may include:

- interpretation;
- comparison with prior work;
- plausible mechanisms;
- limitation;
- implication.

## A-102. Do Not Introduce Hidden Results in Discussion

If evidence matters to interpretation, report it transparently in the results.

---

# 31. CONCLUSION DISCIPLINE

## A-103. Every Conclusion Must Trace Back to Evidence

For every important conclusion, identify:

- analysis;
- result;
- source artifact.

## A-104. Do Not Convert "No Evidence" Into "Evidence of No Effect"

Be precise about non-significant findings.

## A-105. Do Not Generalize Beyond the Evaluation Scope

Bound the conclusion to:

- population;
- dataset;
- environment;
- timeframe;
- metric;
- experimental condition.

## A-106. Avoid Binary Winner Narratives When Evidence Is Mixed

If Method A has higher accuracy but worse latency and greater variance, report the trade-off.

Do not collapse multidimensional evidence into a simplistic winner unless the research question defines a single decision criterion in advance.

---

# 32. ANALYTICAL VISUALIZATION

## A-107. Visualizations Must Reveal Evidence, Not Decorate Results

Use charts to show:

- distribution;
- uncertainty;
- comparison;
- trend;
- relationship;
- error pattern.

## A-108. Avoid Misleading Axes

Do not truncate axes in ways that exaggerate small differences unless clearly justified.

## A-109. Show Uncertainty When Relevant

Consider:

- error bars;
- confidence bands;
- distributions;
- box plots;
- violin plots.

## A-110. Do Not Hide Individual Variation Behind Averages When It Matters

Where appropriate, show raw points or distributional summaries.

---

# 33. ANALYSIS PROVENANCE

## A-111. Every Final Statistic Should Be Reproducible

Trace:

**raw/processed data -> analysis code -> output -> manuscript**

## A-112. Preserve Analysis Scripts

Do not rely on undocumented spreadsheet calculations for critical results when reproducible code is feasible.

## A-113. Record Software and Package Versions When Material

Statistical behavior can vary by software version.

## A-114. Manual Edits to Results Must Be Avoided

Do not manually alter output values in tables or figures.

Generate from source data when possible.

---

# 34. ANALYSIS PLAN TEMPLATE

A useful analysis record:

> **Analysis ID:**  
> **Research Question:**  
> **Dataset/Artifact:**  
> **Outcome Variable:**  
> **Predictors/Groups:**  
> **Primary Metric/Test:**  
> **Assumptions:**  
> **Effect Size:**  
> **Uncertainty Measure:**  
> **Multiple-Testing Plan:**  
> **Missing-Data Strategy:**  
> **Sensitivity Checks:**  
> **Software/Version:**  
> **Output Artifact:**  
> **Interpretation Boundary:**

---

# 35. RESULT-TO-CONCLUSION MATRIX

Maintain when useful:

| Research Question | Analysis | Result | Uncertainty | Supported Conclusion | Unsupported Conclusion |
|---|---|---|---|---|---|

This helps prevent overclaiming.

---

# 36. STATISTICAL CLAIM MATRIX

For important claims:

| Claim | Statistic | Effect Size | Uncertainty | Assumptions Checked? | Status |
|---|---|---|---|---|---|

A claim without a traceable statistic or qualitative evidence should not be treated as final.

---

# 37. ANALYSIS AUDIT FORMAT

Use:

> **A-XX | SEVERITY | LOCATION**  
> **Problem:** what is analytically wrong.  
> **Why:** why the inference is invalid, weak, or misleading.  
> **Evidence:** the relevant output or analytical choice.  
> **Impact:** which claim is affected.  
> **Correction:** what should change.  
> **Verification:** how to confirm the corrected analysis.

Example:

> **A-17 | MAJOR | Results 4.2**  
> **Problem:** a non-significant result is interpreted as proof that the methods are equivalent.  
> **Why:** failure to reject the null does not establish equivalence.  
> **Evidence:** p = 0.18 is used to claim "no difference."  
> **Impact:** the conclusion overstates what the test supports.  
> **Correction:** state that no statistically significant difference was detected, or use an equivalence/non-inferiority design if that is the actual research question.  
> **Verification:** confirm the revised wording and, if needed, rerun an appropriate equivalence analysis.

---

# 38. ANALYSIS QUALITY GATE

Before marking analysis final, verify:

## Data Integrity

- [ ] Final analyzed dataset is identified.
- [ ] Derived variables are traceable.
- [ ] Units are consistent.
- [ ] Missingness is quantified.
- [ ] Outlier treatment is documented.

## Descriptive Analysis

- [ ] Summary statistics match the data distribution.
- [ ] Percentages have clear denominators where needed.
- [ ] Mean/median choices are justified.

## Statistical Testing

- [ ] Test choice matches the research question.
- [ ] Relevant assumptions are checked.
- [ ] One-sided tests are justified in advance.
- [ ] Non-significance is not interpreted as proof of no effect.
- [ ] Multiple testing is addressed.

## Effect and Uncertainty

- [ ] Effect magnitude is reported when relevant.
- [ ] Confidence/uncertainty intervals are included when appropriate.
- [ ] Practical significance is considered.
- [ ] Wide uncertainty is not hidden.

## Model Analysis

- [ ] Metric definitions are exact.
- [ ] Class imbalance is considered.
- [ ] Run-to-run variability is considered.
- [ ] Model comparisons use equivalent conditions.
- [ ] Calibration is checked when probability claims matter.

## Interpretation

- [ ] Correlation is not described as causation without support.
- [ ] Statistical adjustment is not treated as proof of causality.
- [ ] Observed results are separated from interpretation.
- [ ] Alternative explanations are considered.
- [ ] Generalization stays within scope.

## Qualitative/Mixed Methods

- [ ] Coding procedure is traceable.
- [ ] Themes are grounded in data.
- [ ] Contradictory evidence is preserved.
- [ ] Quantitative and qualitative evidence are genuinely integrated where required.

## Limitations and Conclusion

- [ ] Limitations are specific.
- [ ] Limitations explain their effect on inference.
- [ ] Every conclusion maps to evidence.
- [ ] No unsupported winner narrative remains.
- [ ] Unknowns remain explicitly unknown.

Any material failure must be corrected, bounded, or transparently reported before the analysis is labeled final.

---

# 39. PASS REQUIRES ANALYTICAL EVIDENCE

Bad:

> Analysis PASS.

Better:

> **A-16 PASS:** the primary comparison reports the mean difference, 95% confidence interval, effect size, and p-value; assumptions were checked and no material violation was found.

Bad:

> No bias detected.

Better:

> **Bias assessment:** no material difference was observed between included and excluded cases on the measured baseline variables; unmeasured selection bias cannot be ruled out.

Use evidence, not status language alone.

---

# 40. Recommended Workflow

Use this module in the following order:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `04-research-methodology.md`
4. `05-research-experiment.md`
5. `02-research-human.md` when human data are involved
6. `06-research-analysis.md`
7. `01-research-writing.md`
8. final Research Delivery Gate

The analysis module should interpret evidence that already exists.

It should never invent evidence to complete the narrative.

---

# 41. Final Principles

**Effect magnitude > isolated p-value**  
**Uncertainty > false precision**  
**Assumption checks > automatic testing**  
**Practical importance > significance theater**  
**Association > causation only when justified**  
**Distribution > single summary statistic**  
**Sensitivity > fragile certainty**  
**Contradictory evidence > selective narrative**  
**Bounded conclusion > broad overclaiming**  
**Traceable analysis > manual result editing**  
**Evidence-supported interpretation > preferred story**
