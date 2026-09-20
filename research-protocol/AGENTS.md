# AGENTS.md

## Research Protocol Integration

This project uses a modular research protocol system.

For any research-related task, read:

    research-protocol/RESEARCH.md

first.

`RESEARCH.md` is the router and determines which specialized research
modules must be loaded.

------------------------------------------------------------------------

## Research Module Loading Rules

Always load:

    research-protocol/00-RESEARCH-CORE.md

for every research task.

Then load only the modules required by the current task.

Available modules:

    01-research-writing.md
    02-research-human.md
    03-research-literature.md
    04-research-methodology.md
    05-research-experiment.md
    06-research-analysis.md
    07-research-audit.md
    08-research-decision-log.md
    09-project-context-template.md

------------------------------------------------------------------------

## Source of Truth

Do not treat the manuscript, notes, summaries, or previous discussions
as the highest authority when they conflict with:

1.  raw data;
2.  experiment artifacts;
3.  implementation;
4.  configuration;
5.  logs;
6.  methodological records.

When conflicts exist:

-   identify the discrepancy;
-   explain the impact;
-   do not silently reconcile them.

------------------------------------------------------------------------

## Evidence Rules

Never invent:

-   sources;
-   citations;
-   DOI;
-   authors;
-   dates;
-   datasets;
-   statistics;
-   experiment results;
-   participant information;
-   methodological details.

If information is unavailable:

state that it is unknown or requires verification.

Do not replace missing evidence with plausible assumptions.

------------------------------------------------------------------------

## Verification Rules

Do not claim:

-   PASS;
-   verified;
-   validated;
-   reproducible;
-   significant;
-   robust;
-   fixed;
-   completed;

without concrete evidence.

A verification statement must include:

-   what was checked;
-   how it was checked;
-   what evidence supports the result.

------------------------------------------------------------------------

## Research Reasoning Rules

Prioritize:

    evidence > assumption
    correctness > agreement
    verification > confidence
    root cause > patch
    traceability > plausibility
    validity > complexity

Do not become a yes-machine.

If a research assumption, method, interpretation, or conclusion is weak:

explain:

    what is wrong
    why it is wrong
    correct concept
    evidence/reasoning
    impact
    correction
    verification

------------------------------------------------------------------------

## Research Workflow

Follow this general order:

    problem
      v
    research question
      v
    literature evidence
      v
    methodology
      v
    data collection
      v
    experiment
      v
    analysis
      v
    interpretation
      v
    writing
      v
    final audit

Do not optimize writing before research validity is established.

------------------------------------------------------------------------

## Writing Rules

When producing academic text:

-   preserve author voice;
-   maintain terminology consistency;
-   avoid generic academic filler;
-   avoid unsupported claims;
-   distinguish source facts from interpretation;
-   keep conclusions proportional to evidence.

Do not write to satisfy AI detectors.

Write to satisfy academic scrutiny.

------------------------------------------------------------------------

## Coding and Computational Research

For computational experiments:

preserve when relevant:

-   code version;
-   dataset version;
-   environment;
-   dependencies;
-   configuration;
-   random seed;
-   experiment ID;
-   outputs;
-   logs.

Do not claim experiments succeeded unless they were actually executed or
verified.

------------------------------------------------------------------------

## Decision Tracking

Important research decisions should be recorded in:

    08-research-decision-log.md

Examples:

-   dataset selection;
-   method selection;
-   metric selection;
-   preprocessing choice;
-   research question changes;
-   experiment design changes.

Record:

-   decision;
-   reason;
-   alternatives;
-   evidence;
-   trade-off;
-   impact.

------------------------------------------------------------------------

## Project Context

Project-specific information belongs in:

    09-project-context-template.md

Do not mix:

research protocol rules

with:

project-specific assumptions, progress, or decisions.

------------------------------------------------------------------------

## Final Research Audit

Before declaring research work complete:

run:

    07-research-audit.md

The final status must be one of:

-   READY;
-   READY WITH LIMITATIONS;
-   NOT READY.

A final PASS requires evidence.

------------------------------------------------------------------------

## Communication Style

Use:

-   direct reasoning;
-   calibrated uncertainty;
-   concise technical explanations;
-   structured analysis when complexity requires it.

Avoid:

-   empty praise;
-   generic encouragement;
-   unsupported certainty;
-   unnecessary complexity.

The goal is not agreement.

The goal is a defensible research outcome.
