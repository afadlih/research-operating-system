# 10-research-domain-adaptation

> Domain adaptation layer for applying the research operating system
> across different academic fields.

## 1. Purpose

This module extends the general research protocol.

The core research system remains universal:

    research problem
            ↓
    research question
            ↓
    evidence
            ↓
    method
            ↓
    data
            ↓
    analysis
            ↓
    conclusion
            ↓
    verification

However, different disciplines require different methodological
emphasis.

This file helps select the appropriate modules based on research domain.

------------------------------------------------------------------------

# 2. Universal Rule

Regardless of discipline:

Always prioritize:

    evidence > assumption

    validity > appearance

    research question > preferred method

    verification > confidence

    traceability > plausibility

The domain changes the implementation.

The research principles remain the same.

------------------------------------------------------------------------

# 3. Domain Selection

Identify the dominant research domain.

Possible domains:

-   Computer Science / Artificial Intelligence
-   Engineering
-   Education
-   Psychology
-   Health / Medicine
-   Business / Management
-   Economics
-   Social Science
-   Law
-   Humanities

A project may use multiple domains.

Example:

AI education system:

    Computer Science
    +
    Education
    +
    Human-centered research

------------------------------------------------------------------------

# 4. Computer Science / Artificial Intelligence

## Recommended Modules

Primary:

    00-CORE
    03-LITERATURE
    04-METHODOLOGY
    05-EXPERIMENT
    06-ANALYSIS
    01-WRITING

Additional:

    02-HUMAN

when user studies or human evaluation exists.

------------------------------------------------------------------------

## Important Checks

Focus on:

-   dataset quality;
-   train/test separation;
-   leakage prevention;
-   baseline fairness;
-   reproducibility;
-   model comparison;
-   metric selection;
-   computational cost;
-   error analysis.

------------------------------------------------------------------------

## Typical Research Flow

    Problem

    ↓

    Dataset / Environment

    ↓

    Method

    ↓

    Experiment

    ↓

    Evaluation

    ↓

    Error Analysis

    ↓

    Conclusion Boundary

------------------------------------------------------------------------

## Common Risks

Avoid:

-   claiming state-of-the-art without fair comparison;
-   comparing incompatible benchmarks;
-   tuning on test data;
-   reporting only best runs;
-   ignoring variance.

------------------------------------------------------------------------

# 5. Engineering Research

## Recommended Modules

Primary:

    CORE
    METHODOLOGY
    EXPERIMENT
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   system design;
-   requirements;
-   performance;
-   reliability;
-   safety;
-   validation;
-   practical constraints.

------------------------------------------------------------------------

## Common Evidence

Examples:

-   prototype testing;
-   simulation;
-   benchmark;
-   field measurement;
-   stress testing.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   prototype success = real-world success;
-   laboratory condition = operational condition;
-   performance claim without test condition.

------------------------------------------------------------------------

# 6. Education Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    HUMAN
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   learning construct definition;
-   educational intervention;
-   participant selection;
-   instrument validity;
-   classroom context;
-   ethical considerations.

------------------------------------------------------------------------

## Typical Variables

Examples:

-   learning outcome;
-   motivation;
-   engagement;
-   achievement;
-   perception.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   claiming learning improvement without appropriate measurement;
-   generalizing from one classroom;
-   using invalid questionnaires;
-   confusing satisfaction with learning effectiveness.

------------------------------------------------------------------------

# 7. Psychology Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    HUMAN
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   construct validity;
-   measurement reliability;
-   sampling;
-   psychological scales;
-   confounding variables;
-   ethical procedures.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   treating correlation as causation;
-   using unclear constructs;
-   interpreting small samples broadly;
-   modifying validated instruments without explanation.

------------------------------------------------------------------------

# 8. Health / Medicine Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    HUMAN
    ANALYSIS
    WRITING

Additional specialized review may be required.

------------------------------------------------------------------------

## Important Checks

Focus on:

-   participant safety;
-   ethics approval;
-   clinical validity;
-   measurement accuracy;
-   patient privacy;
-   risk assessment.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   unsupported medical claims;
-   insufficient clinical evidence;
-   confusing statistical significance with clinical importance.

------------------------------------------------------------------------

# 9. Business / Management Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    HUMAN
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   organizational context;
-   market variables;
-   survey validity;
-   sampling;
-   practical significance.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   overgeneralizing from one company;
-   treating correlation as business causation;
-   using weak survey instruments.

------------------------------------------------------------------------

# 10. Economics Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   economic assumptions;
-   causal identification;
-   variables;
-   data quality;
-   model specification.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   causal claims from simple correlation;
-   ignoring confounding;
-   unexplained model assumptions.

------------------------------------------------------------------------

# 11. Social Science Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    HUMAN
    ANALYSIS
    WRITING

------------------------------------------------------------------------

## Important Checks

Focus on:

-   social context;
-   participant diversity;
-   qualitative/quantitative fit;
-   interpretation limits.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   imposing researcher assumptions;
-   ignoring participant perspective;
-   excessive generalization.

------------------------------------------------------------------------

# 12. Law Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    WRITING

Possible:

    HUMAN
    ANALYSIS

depending on design.

------------------------------------------------------------------------

## Important Checks

Focus on:

-   legal reasoning;
-   source authority;
-   doctrinal consistency;
-   comparative framework;
-   interpretation boundaries.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   treating all legal sources as equal;
-   ignoring jurisdiction;
-   unsupported legal interpretation.

------------------------------------------------------------------------

# 13. Humanities Research

## Recommended Modules

Primary:

    CORE
    LITERATURE
    METHODOLOGY
    WRITING

Possible:

    HUMAN
    ANALYSIS

------------------------------------------------------------------------

## Important Checks

Focus on:

-   interpretation;
-   historical context;
-   source criticism;
-   conceptual clarity;
-   argument structure.

------------------------------------------------------------------------

## Common Risks

Avoid:

-   unsupported interpretation;
-   removing historical context;
-   confusing opinion with analysis.

------------------------------------------------------------------------

# 14. Interdisciplinary Research

Many modern projects combine fields.

Example:

AI healthcare:

    Computer Science
    +
    Medicine
    +
    Human Research

Example:

AI education:

    Computer Science
    +
    Education
    +
    Human Evaluation

------------------------------------------------------------------------

## Rule

Do not force the project into one discipline.

Identify:

1.  primary domain;
2.  supporting domains;
3.  required modules.

------------------------------------------------------------------------

# 15. Domain Routing Table

  Research Type          Main Modules
  ---------------------- ---------------------------------------------------------
  AI / ML                Core + Literature + Methodology + Experiment + Analysis
  Software Engineering   Core + Methodology + Experiment
  Education              Core + Literature + Methodology + Human + Analysis
  Psychology             Core + Methodology + Human + Analysis
  Medicine               Core + Literature + Methodology + Human + Analysis
  Business               Core + Literature + Methodology + Human + Analysis
  Economics              Core + Literature + Methodology + Analysis
  Social Science         Core + Literature + Methodology + Human + Analysis
  Law                    Core + Literature + Methodology + Writing
  Humanities             Core + Literature + Methodology + Writing

------------------------------------------------------------------------

# 16. Using AI With Domain Adaptation

Prompt example:

    I am conducting research in the field of Education.

    Use:
    10-research-domain-adaptation.md

    Select the relevant modules.

    Research topic:
    [topic]

    Current task:
    [task]

    Check:
    - methodological fit;
    - evidence requirements;
    - domain-specific risks.

------------------------------------------------------------------------

# 17. Domain Adaptation Rule

Domain adaptation changes:

-   examples;
-   risks;
-   preferred methods;
-   evaluation concerns.

It does not change:

-   evidence requirements;
-   honesty rules;
-   verification rules;
-   traceability requirements.

------------------------------------------------------------------------

# 18. Final Principle

A good research system is not:

    one method for every field

It is:

    one integrity framework

    +

    domain-specific execution rules

The research question determines the method.

The domain determines the constraints.

The evidence determines the conclusion.
