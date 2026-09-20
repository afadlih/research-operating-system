# research-experiment

> Experimental execution, reproducibility, leakage prevention, baseline fairness, tuning discipline, benchmark integrity, logging, repeated runs, ablation, robustness checks, and evidence verification.

## 1. Purpose

This module complements `00-RESEARCH-CORE.md` and `04-research-methodology.md`.

Use it whenever research involves computational, empirical, or controlled experiments, especially:

- machine learning;
- deep learning;
- NLP;
- computer vision;
- recommender systems;
- optimization;
- simulation;
- software performance studies;
- benchmarking;
- model comparison;
- ablation studies;
- sensitivity analysis;
- repeated stochastic runs;
- retrieval systems;
- LLM evaluation;
- experimental prototypes.

The goal is not to produce impressive numbers.

The goal is to ensure that experimental results are:

- reproducible;
- comparable;
- leakage-free;
- traceable;
- honestly tuned;
- statistically interpretable;
- robust enough for the claim;
- tied to preserved artifacts.

Priority order:

**experimental validity > reproducibility > fair comparison > traceability > robustness > performance**

---

## 2. Boundary With the Core and Methodology

This module must never weaken:

- `00-RESEARCH-CORE.md`
- `04-research-methodology.md`

The core defines integrity and verification.

The methodology module defines the research design.

This module governs **how the experiment is actually executed**.

If the implementation deviates from the methodology, the actual experiment becomes the source of truth for what was executed, and the discrepancy must be reported.

Do not silently rewrite the manuscript to make an accidental procedure appear planned.

---

## 3. Experimental Principle

Every experiment should answer a specific question.

Before execution, state:

1. What hypothesis or comparison is being tested?
2. What variables change?
3. What variables remain fixed?
4. What data are used?
5. What metric determines the result?
6. What source of randomness exists?
7. What artifacts will be saved?
8. What outcome would support or weaken the hypothesis?

Do not run experiments merely because they are easy to add.

---

# 4. EXPERIMENT IDENTITY

## E-01. Every Experiment Needs a Stable Identifier

Use a stable experiment ID.

Example:

`EXP-2026-09-001`

or:

`bert-base_seed42_lr2e-5_v3`

The exact naming scheme may vary, but each result should map to a specific configuration.

## E-02. Results Must Be Traceable to Configuration

A result without a recoverable configuration is weak evidence.

At minimum, preserve where relevant:

- code version;
- dataset version;
- split;
- preprocessing;
- model;
- parameters;
- seed;
- hardware;
- software environment;
- timestamp.

## E-03. Do Not Overwrite Experiment History

Do not reuse one result file for multiple experiments unless versioning is preserved.

Experimental history should remain auditable.

---

# 5. DATA SPLIT INTEGRITY

## E-04. Split Before Fitting Data-Dependent Transformations

For predictive evaluation, perform the split before fitting transformations such as:

- standardization;
- normalization;
- feature selection;
- imputation;
- vocabulary fitting;
- target encoding;
- dimensionality reduction.

Fit only on training data unless the method explicitly requires otherwise.

## E-05. Test Data Must Remain Untouched

The test set must not influence:

- feature engineering;
- threshold selection;
- hyperparameter tuning;
- architecture selection;
- model choice;
- early stopping;
- prompt revision.

If test data influence decisions, it is no longer a clean final test.

## E-06. Validation Data Must Be Separate From Final Test Data

Use validation data for development decisions.

Use test data for final evaluation.

Do not repeatedly inspect test performance while iterating.

## E-07. Split Strategy Must Match Data Structure

Random split is not always appropriate.

Consider:

- temporal split;
- group split;
- subject-level split;
- site-level split;
- stratified split;
- leave-one-group-out;
- nested cross-validation.

## E-08. Duplicate Leakage Must Be Checked

Duplicates or near-duplicates across splits can inflate performance.

Check for:

- exact duplicates;
- paraphrases;
- image variants;
- augmented copies;
- repeated user records;
- overlapping documents;
- code clones.

## E-09. Temporal Leakage Must Be Prevented

Do not use future information to predict the past.

For time-dependent problems, ensure all features available at prediction time would truly have existed then.

---

# 6. LABEL AND TARGET LEAKAGE

## E-10. Target Information Must Not Leak Into Features

Examples:

- derived columns using future outcomes;
- labels embedded in filenames;
- post-outcome metadata;
- annotations created using the target;
- prompt context containing the answer.

## E-11. Preprocessing Must Not Use Label Information Unless Intended

Feature selection using the full dataset can leak target information.

Perform supervised selection inside training folds.

## E-12. Retrieval Systems Must Check Corpus Contamination

For retrieval-augmented systems, inspect whether:

- evaluation answers exist verbatim in the retrieval corpus;
- benchmark solutions are indexed;
- future documents leak into historical queries;
- training and evaluation documents overlap.

---

# 7. BASELINE FAIRNESS

## E-13. Baselines Must Be Relevant

A baseline should represent:

- a simple reasonable method;
- an established prior method;
- a current competitive method;
- a task-specific reference system.

Do not choose intentionally weak baselines.

## E-14. Baselines Need Comparable Conditions

Where possible, use the same:

- data;
- split;
- preprocessing;
- metric;
- evaluation code;
- hardware constraints;
- budget.

## E-15. Baselines Need Appropriate Tuning

Do not heavily tune the proposed method while leaving baselines at poor defaults.

The comparison should reflect reasonable effort.

## E-16. Do Not Give the Proposed Method Extra Information

All compared methods should receive comparable information unless the additional information is the research variable being studied.

## E-17. Baseline Reproduction Must Be Honest

If baseline results are taken from prior work rather than reproduced, label them clearly.

Do not present literature numbers as if produced under the current protocol.

---

# 8. HYPERPARAMETER TUNING

## E-18. Tuning Strategy Must Be Documented

Examples:

- manual tuning;
- grid search;
- random search;
- Bayesian optimization;
- Hyperband;
- validation-based iteration.

## E-19. Search Space Must Be Recorded

For automated tuning, preserve:

- parameters searched;
- ranges;
- distributions;
- number of trials;
- optimization metric;
- stopping criteria.

## E-20. Best-on-Test Is Invalid Tuning

Never choose configuration based on test-set performance.

## E-21. Manual Tuning Still Counts as Tuning

If repeated human adjustments are made after seeing validation results, report that as tuning.

Do not call the configuration "default" if it was manually optimized.

## E-22. Tuning Budget Should Be Comparable

If one method receives far more optimization budget, discuss the fairness implication.

---

# 9. RANDOMNESS AND REPEATED RUNS

## E-23. One Stochastic Run May Be Insufficient

For stochastic methods, one run may reflect luck.

Consider repeated runs when:

- initialization matters;
- sampling is stochastic;
- optimization is unstable;
- results vary materially by seed.

## E-24. Record Seeds

Preserve random seeds for:

- data split;
- model initialization;
- augmentation;
- sampling;
- generation;
- simulation.

## E-25. Report Distribution, Not Only Best Run

When repeated runs are relevant, report:

- mean;
- standard deviation;
- median;
- range;
- confidence interval;

as appropriate.

Do not report only the best run unless the research question specifically concerns best-case performance.

## E-26. Seed Selection Must Not Be Cherry-Picked

Do not choose a favorable seed after inspecting outcomes and then present it as typical.

---

# 10. CROSS-VALIDATION

## E-27. Cross-Validation Must Match Data Independence

Standard k-fold is inappropriate when observations are grouped or time-dependent.

Use group-aware or time-aware variants where necessary.

## E-28. Preprocessing Must Occur Inside Each Fold

Any fitted preprocessing step belongs inside the fold training pipeline.

## E-29. Hyperparameter Tuning and Evaluation May Require Nested CV

When data are limited and tuning is extensive, nested cross-validation may reduce optimistic bias.

## E-30. Do Not Average Incompatible Folds Carelessly

If fold sizes or class distributions differ substantially, choose aggregation appropriately.

---

# 11. METRIC IMPLEMENTATION

## E-31. Metric Definition Must Be Exact

Specify:

- formula;
- averaging method;
- positive class;
- threshold;
- weighting;
- aggregation.

## E-32. Use One Metric Implementation Consistently

Avoid computing the same named metric differently across models.

## E-33. Sanity-Check Metric Code

Validate metric implementation using:

- library reference implementation;
- small known example;
- manual calculation;
- unit test.

## E-34. Primary Metric Must Be Predefined When Possible

Do not switch the main metric after seeing results because another metric looks better.

---

# 12. CLASS IMBALANCE

## E-35. Class Distribution Must Be Reported

State the distribution when it materially affects evaluation.

## E-36. Resampling Must Occur Only on Training Data

Do not oversample or undersample before the split.

## E-37. Accuracy Alone May Be Misleading

Consider metrics such as:

- macro-F1;
- balanced accuracy;
- precision/recall;
- PR-AUC;

when appropriate.

## E-38. Threshold Tuning Must Use Validation Data

Do not optimize thresholds on final test labels.

---

# 13. EARLY STOPPING AND CHECKPOINTING

## E-39. Early Stopping Requires a Defined Signal

Document:

- monitored metric;
- patience;
- minimum improvement;
- validation set.

## E-40. Checkpoint Selection Must Not Use Test Results

Choose checkpoints using training/validation evidence.

## E-41. Save the Actual Evaluated Checkpoint

Do not report results from a checkpoint that cannot be recovered.

---

# 14. COMPUTE ENVIRONMENT

## E-42. Record Environment Details When Material

Preserve where relevant:

- OS;
- Python/R version;
- framework version;
- CUDA version;
- GPU/CPU;
- RAM;
- package lockfile;
- container image;
- compiler.

## E-43. Hardware Differences Can Affect Performance Claims

For runtime, throughput, memory, or energy comparisons, hardware must be controlled or explicitly reported.

## E-44. Do Not Compare Runtime Across Incompatible Environments

A faster number on different hardware is not a fair efficiency comparison.

---

# 15. CODE VERSIONING

## E-45. Experiments Must Map to Code Version

Prefer:

- commit hash;
- release tag;
- immutable archive.

## E-46. Uncommitted Changes Must Be Recorded

If an experiment uses code not yet committed, preserve a patch or archive.

## E-47. Configuration Should Be Externalized When Possible

Use config files or command-line arguments rather than manually editing code for every run.

This reduces hidden experiment drift.

---

# 16. EXPERIMENT LOGGING

## E-48. Log More Than the Final Metric

Useful logs may include:

- experiment ID;
- configuration;
- seed;
- epoch;
- loss;
- validation metrics;
- runtime;
- resource use;
- warnings;
- failures.

## E-49. Failed Runs Must Not Disappear

Preserve failed or aborted runs when they inform:

- instability;
- memory limits;
- configuration problems;
- robustness.

## E-50. Distinguish Invalid Runs From Poor Runs

A run may be excluded if it is invalid due to:

- corrupted data;
- software crash before completion;
- misconfiguration.

Do not exclude merely because performance is low.

---

# 17. ARTIFACT PRESERVATION

## E-51. Preserve Raw Outputs

Where relevant, save:

- predictions;
- probabilities;
- generated text;
- confusion matrices;
- checkpoints;
- logs;
- metrics;
- retrieval traces.

## E-52. Derived Tables Must Be Reconstructable

A manuscript table should be reproducible from preserved experiment outputs.

## E-53. Manual Copying Is High Risk

Avoid manually transferring numbers from logs to tables when automation is possible.

If manual transfer is necessary, verify carefully.

---

# 18. BENCHMARK INTEGRITY

## E-54. Benchmark Rules Must Be Followed

If a benchmark defines:

- split;
- metric;
- submission format;
- prohibited data;
- evaluation server;

follow those rules.

## E-55. Do Not Tune on Hidden Test Feedback

Repeated leaderboard submissions can become indirect test-set tuning.

Treat leaderboard feedback carefully.

## E-56. Benchmark Contamination Must Be Considered

Especially for large pretrained models, evaluation items may have appeared in training data.

Acknowledge contamination risk where relevant.

## E-57. Benchmark Performance Is Not Universal Performance

Do not generalize beyond the benchmark without additional evidence.

---

# 19. ABLATION STUDIES

## E-58. Ablation Must Answer a Component Question

An ablation should test:

> What changes when component X is removed or altered?

## E-59. Change One Meaningful Factor at a Time Where Possible

If multiple components change simultaneously, attribution becomes ambiguous.

## E-60. Ablation Conditions Must Be Comparable

Keep other settings fixed.

## E-61. Negative Ablation Results Are Still Informative

If removing a component does not hurt performance, report it.

Do not hide it because it weakens the proposed contribution.

---

# 20. SENSITIVITY ANALYSIS

## E-62. Test Sensitivity When Results Depend on Arbitrary Choices

Potential targets:

- threshold;
- random seed;
- sample size;
- preprocessing;
- window size;
- top-k;
- temperature;
- regularization;
- class weights.

## E-63. Sensitivity Analysis Should Explore Plausible Ranges

Do not choose only values that make the method look stable.

## E-64. Report Fragility Honestly

If performance collapses under small parameter changes, that is relevant evidence.

---

# 21. ROBUSTNESS TESTING

## E-65. Robustness Must Be Defined

Robustness may refer to:

- noise;
- distribution shift;
- adversarial perturbation;
- missing features;
- domain change;
- input variation;
- seed variation.

Do not use "robust" without defining the stressor.

## E-66. Robustness Claims Need Dedicated Evidence

High average performance is not enough.

## E-67. Stress Tests Should Match Realistic Risks

Do not create arbitrary perturbations unrelated to the deployment or research context.

---

# 22. ERROR ANALYSIS

## E-68. Aggregate Metrics Are Not Enough

Inspect errors when the research question benefits from it.

Examples:

- confusion patterns;
- subgroup errors;
- failure categories;
- qualitative model failures;
- outliers.

## E-69. Error Categories Need Clear Definitions

Do not invent categories after seeing examples without documenting the process.

## E-70. Include Counterexamples

A strong method can still fail in important ways.

Preserve representative failure cases.

---

# 23. SUBGROUP ANALYSIS

## E-71. Subgroups Must Be Justified

Do not create many subgroups after seeing results just to find favorable patterns.

## E-72. Small Subgroups Require Caution

Report uncertainty.

Do not overinterpret tiny samples.

## E-73. Multiple Subgroup Tests Increase False-Positive Risk

Use appropriate qualification or correction.

---

# 24. STATISTICAL COMPARISON OF MODELS

## E-74. Model Comparison Should Reflect Paired Structure

If two models are evaluated on the same samples, use methods appropriate for paired observations when statistical testing is needed.

## E-75. Statistical Significance Is Not Practical Significance

A tiny difference can be statistically detectable but practically irrelevant.

## E-76. Confidence Intervals Are Often More Informative Than Bare p-Values

When appropriate, report effect magnitude and uncertainty.

## E-77. Do Not Test Every Metric Without a Plan

Avoid statistical fishing.

---

# 25. LLM EXPERIMENTS

## E-78. Record Model Identity Precisely

Preserve when relevant:

- provider;
- model name;
- model version;
- access date;
- API version.

Hosted models may change over time.

## E-79. Record Prompt Structure

Preserve:

- system prompt;
- user template;
- few-shot examples;
- tool instructions;
- context construction.

## E-80. Record Generation Parameters

Examples:

- temperature;
- top-p;
- max tokens;
- seed if supported;
- response format.

## E-81. Repeated Generation May Be Necessary

For stochastic generation, one response may be insufficient.

## E-82. Human Evaluation Must Follow `02-research-human.md`

Do not treat preference as factual correctness.

## E-83. Prompt Iteration Must Be Treated as Tuning

If prompts are revised after seeing evaluation outputs, document that process.

## E-84. Evaluation Set Must Not Be Used for Prompt Development

Use a development set when possible.

---

# 26. RETRIEVAL EXPERIMENTS

## E-85. Separate Retrieval and Generation Metrics

Do not collapse retrieval quality and generation quality into one vague score.

## E-86. Record Retrieval Configuration

Examples:

- embedding model;
- chunk size;
- overlap;
- index type;
- top-k;
- reranker;
- filters.

## E-87. Check Retrieval Leakage

Do not allow the corpus to contain hidden answer keys or evaluation solutions without disclosure.

## E-88. Inspect Retrieved Evidence

A correct final answer does not prove the retrieval component worked correctly.

---

# 27. SIMULATION EXPERIMENTS

## E-89. Simulation Assumptions Must Be Explicit

Record:

- model assumptions;
- initial conditions;
- boundary conditions;
- parameter distributions.

## E-90. Validate the Simulation When Possible

Compare against:

- known analytical result;
- empirical data;
- trusted implementation;
- conservation constraints.

## E-91. Sensitivity to Initial Conditions May Matter

Do not report one simulation trajectory as universal when outcomes vary materially.

---

# 28. PERFORMANCE BENCHMARKING

## E-92. Warm-Up Effects Must Be Considered

Runtime measurements may be affected by:

- JIT compilation;
- cache warm-up;
- model loading;
- lazy initialization.

## E-93. Repeat Timing Measurements

One timing measurement is usually insufficient.

## E-94. Define What Time Is Included

Clarify whether runtime includes:

- preprocessing;
- loading;
- inference;
- postprocessing;
- network latency.

## E-95. Report Throughput and Latency Correctly

Do not confuse:

- per-sample latency;
- batch latency;
- throughput.

## E-96. Performance Claims Require Controlled Hardware

Efficiency comparisons need comparable environments.

---

# 29. MEMORY AND RESOURCE MEASUREMENT

## E-97. Define the Resource Metric

Examples:

- peak GPU memory;
- RAM;
- disk;
- FLOPs;
- energy;
- API cost.

## E-98. Measure Under Comparable Conditions

Batch size, precision, sequence length, and caching can change resource usage.

## E-99. Do Not Infer Efficiency From Model Size Alone

Parameter count does not fully determine runtime or memory use.

---

# 30. FAILURE HANDLING

## E-100. Experiment Failures Must Be Logged

Examples:

- out-of-memory;
- NaN loss;
- timeout;
- invalid configuration;
- API failure;
- corrupted sample.

## E-101. Automatic Retry Must Be Traceable

Retries can change:

- seed;
- environment;
- API output;
- timing.

Log them.

## E-102. Silent Recovery Is Dangerous

Do not suppress failures in a way that makes incomplete experiments look successful.

---

# 31. EXPERIMENT REPRODUCIBILITY

## E-103. Reproduction Requires More Than Code

Necessary context may include:

- data;
- environment;
- config;
- seed;
- preprocessing;
- model weights;
- execution order.

## E-104. Reproducible Does Not Always Mean Bitwise Identical

Different hardware or nondeterministic kernels may cause small variation.

State the reproducibility level honestly.

## E-105. Determinism Claims Must Be Verified

Do not write:

> The experiment is fully deterministic.

unless tested.

---

# 32. EXPERIMENT CONFIGURATION TEMPLATE

A useful experiment record:

> **Experiment ID:**  
> **Question/Hypothesis:**  
> **Code version:**  
> **Dataset version:**  
> **Split:**  
> **Preprocessing:**  
> **Model:**  
> **Hyperparameters:**  
> **Seed:**  
> **Environment:**  
> **Hardware:**  
> **Primary metric:**  
> **Secondary metrics:**  
> **Start time:**  
> **End time:**  
> **Artifact paths:**  
> **Status:** completed / failed / invalid  
> **Notes:**

---

# 33. EXPERIMENT MATRIX

When comparing multiple runs, maintain:

| Experiment ID | Model | Data | Seed | Key Parameters | Metric | Result | Status |
|---|---|---|---:|---|---|---|---|

This reduces manual ambiguity.

---

# 34. RESULT PROVENANCE MATRIX

For important manuscript claims:

| Manuscript Claim | Experiment ID | Artifact | Metric Calculation | Verified? |
|---|---|---|---|---|

A number that cannot be traced to an artifact should not be treated as final.

---

# 35. EXPERIMENT AUDIT FORMAT

Use:

> **E-XX | SEVERITY | LOCATION**  
> **Problem:** what is experimentally wrong.  
> **Why:** why it threatens validity, fairness, or reproducibility.  
> **Evidence:** the observed implementation/configuration.  
> **Impact:** which results or claims are affected.  
> **Correction:** what should change.  
> **Verification:** how to confirm the fix.

Example:

> **E-05 | CRITICAL | Training pipeline**  
> **Problem:** the test set was inspected repeatedly during model development.  
> **Why:** development decisions were influenced by final evaluation data.  
> **Evidence:** test macro-F1 was logged after every architecture revision.  
> **Impact:** the reported test score is no longer an unbiased final estimate.  
> **Correction:** create a validation set for development and reserve a fresh untouched test set.  
> **Verification:** rerun model selection without accessing the final test labels, then evaluate once.

---

# 36. EXPERIMENT QUALITY GATE

Before marking experimental results final, verify:

## Data Integrity

- [ ] Split strategy matches the data structure.
- [ ] Test data were not used for development.
- [ ] No preprocessing leakage exists.
- [ ] Duplicate contamination was checked.
- [ ] Target leakage was checked.
- [ ] Retrieval contamination was checked where relevant.

## Baseline Fairness

- [ ] Baselines are meaningful.
- [ ] Conditions are comparable.
- [ ] Tuning effort is reasonably fair.
- [ ] Proposed method does not receive hidden extra information.
- [ ] Literature baseline numbers are labeled as external rather than reproduced.

## Tuning

- [ ] Tuning strategy is documented.
- [ ] Search space is recorded.
- [ ] Test data were not used for selection.
- [ ] Manual tuning is acknowledged.
- [ ] Tuning budget differences are reported.

## Randomness

- [ ] Seeds are recorded.
- [ ] Repeated runs are used when justified.
- [ ] Best-run cherry-picking is avoided.
- [ ] Variation is reported when relevant.

## Metrics

- [ ] Metric definitions are exact.
- [ ] Metric implementation is verified.
- [ ] Primary metric is predefined where possible.
- [ ] Threshold tuning uses development data.

## Environment

- [ ] Code version is known.
- [ ] Dataset version is known.
- [ ] Environment is recorded.
- [ ] Hardware is reported where performance depends on it.

## Logging and Artifacts

- [ ] Raw outputs are preserved.
- [ ] Failed runs are traceable.
- [ ] Manuscript numbers map to experiment artifacts.
- [ ] Tables can be reconstructed.
- [ ] Evaluated checkpoints can be recovered.

## Robustness

- [ ] Sensitivity was tested when arbitrary choices matter.
- [ ] Robustness claims have explicit stress tests.
- [ ] Error analysis exists where needed.
- [ ] Negative results are not hidden.

## LLM/RAG-Specific

- [ ] Model version is recorded.
- [ ] Prompt is preserved.
- [ ] Generation settings are preserved.
- [ ] Prompt tuning is documented.
- [ ] Evaluation data were not used for prompt development.
- [ ] Retrieval configuration is recorded.
- [ ] Retrieval leakage is checked.

Any material failure must be corrected, bounded, or explicitly disclosed before experimental results are labeled final.

---

# 37. PASS REQUIRES EXECUTION EVIDENCE

Do not claim:

> Experiment PASS

without evidence.

Better:

> **E-05 PASS:** the final test split was created once, never used during tuning, and evaluated only after model selection; experiment log `EXP-2026-09-001` records the single final test run.

Do not claim:

> Reproducible

without evidence.

Better:

> **Reproduction PASS:** the experiment was rerun from the recorded config and produced macro-F1 values within 0.002 of the original run.

---

# 38. Recommended Workflow

Use this module in the following order:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `04-research-methodology.md`
4. `05-research-experiment.md`
5. `02-research-human.md` when human evaluation is involved
6. `06-research-analysis.md`
7. `01-research-writing.md`
8. final Research Delivery Gate

The experiment module produces evidence.

The analysis module interprets that evidence.

The writing module communicates it.

Do not reverse that order.

---

# 39. Final Principles

**Clean test data > repeated test peeking**  
**Fair comparison > favorable comparison**  
**Traceable tuning > hidden optimization**  
**Repeated evidence > lucky seed**  
**Preserved artifacts > copied numbers**  
**Robustness evidence > robustness wording**  
**Actual execution > theoretical expectation**  
**Experiment history > overwritten results**  
**Reproducibility > undocumented success**  
**Negative results > selective reporting**  
**Validity > benchmark prestige**
