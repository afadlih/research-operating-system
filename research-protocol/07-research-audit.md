# research-audit

> Cross-module research auditing, final consistency checks, PASS/FAIL
> verification, and research readiness assessment.

## 1. Purpose

This module performs the final audit across all research modules.

It does not replace:

-   `00-RESEARCH-CORE.md`
-   `01-research-writing.md`
-   `02-research-human.md`
-   `03-research-literature.md`
-   `04-research-methodology.md`
-   `05-research-experiment.md`
-   `06-research-analysis.md`

Its purpose is to verify that all parts of the research system remain
aligned.

Priority:

**integrity \> alignment \> evidence \> verification \> presentation**

------------------------------------------------------------------------

## 2. Cross-Module Alignment Audit

Check:

### Research Question ↔ Method

Question:

> Does the selected method actually generate evidence required by the
> research question?

FAIL examples:

-   causal claim with observational design;
-   usability claim without user evaluation;
-   performance claim without experiment.

------------------------------------------------------------------------

### Method ↔ Experiment

Question:

> Was the implemented procedure consistent with the planned methodology?

Check:

-   dataset;
-   variables;
-   sampling;
-   preprocessing;
-   experimental conditions;
-   evaluation protocol.

------------------------------------------------------------------------

### Experiment ↔ Analysis

Question:

> Does analysis correctly represent executed experiments?

Check:

-   metric calculation;
-   experiment IDs;
-   artifact traceability;
-   statistical procedure;
-   uncertainty.

------------------------------------------------------------------------

### Analysis ↔ Conclusion

Question:

> Does the conclusion stay within what the analysis supports?

Check:

-   overclaiming;
-   unsupported generalization;
-   causal language;
-   ignored uncertainty.

------------------------------------------------------------------------

### Literature ↔ Research Gap

Question:

> Does the identified gap actually emerge from reviewed evidence?

Check:

-   source support;
-   synthesis quality;
-   comparison;
-   unresolved problem.

------------------------------------------------------------------------

### Writing ↔ Evidence

Question:

> Does the manuscript accurately communicate verified research?

Check:

-   citation accuracy;
-   terminology;
-   claim strength;
-   consistency.

------------------------------------------------------------------------

## 3. Final Research Audit Matrix

  Area                          Status          Evidence
  ----------------------------- --------------- ----------
  Research question alignment   PASS/FAIL       
  Literature foundation         PASS/FAIL       
  Methodological validity       PASS/FAIL       
  Human considerations          PASS/FAIL/N/A   
  Experimental validity         PASS/FAIL/N/A   
  Analysis validity             PASS/FAIL       
  Writing integrity             PASS/FAIL       
  Reproducibility               PASS/FAIL/N/A   

A PASS requires concrete evidence.

------------------------------------------------------------------------

## 4. Final Audit Finding Format

Use:

> **RULE \| SEVERITY \| LOCATION**
>
> Problem:
>
> Evidence:
>
> Impact:
>
> Correction:
>
> Verification:

------------------------------------------------------------------------

## 5. Research Completion Decision

Allowed statuses:

### READY

All critical checks passed.

### READY WITH LIMITATIONS

No critical failure exists, but limitations must remain visible.

### NOT READY

At least one critical methodological, integrity, or evidence issue
remains.

Never mark:

-   complete;
-   validated;
-   verified;

without evidence.

------------------------------------------------------------------------

## 6. Final Principles

**Alignment before completion**

**Evidence before confidence**

**Verification before PASS**

**Traceability before publication**

**Integrity before appearance**
