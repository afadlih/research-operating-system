# research-literature

> Literature search, source evaluation, evidence hierarchy, synthesis, citation traceability, research-gap construction, and defensible scholarly review.

## 1. Purpose

This module complements `00-RESEARCH-CORE.md`.

Use it whenever research work involves:

- finding academic sources;
- building a literature review;
- comparing prior studies;
- defining the state of research;
- evaluating source quality;
- constructing a research gap;
- supporting methodological choices;
- identifying limitations in prior work;
- synthesizing evidence across studies;
- verifying whether a claim is actually supported by literature.

The goal is not to collect as many papers as possible.

The goal is to build a **traceable, relevant, critically evaluated evidence base** that supports the research problem, method, interpretation, and gap.

Priority order:

**relevance > source quality > direct support > methodological comparability > recency where relevant > quantity**

---

## 2. Boundary With the Core

This module must never weaken `00-RESEARCH-CORE.md`.

The core governs:

- integrity;
- validity;
- evidence;
- traceability;
- reproducibility;
- verification.

This module adds deeper rules for literature work.

If a source is weak, unclear, inaccessible, or does not support a claim, do not compensate with confident prose.

If the literature does not establish a point, say so.

---

## 3. Literature Review Principle

A literature review is not a paper collection.

It is a structured answer to questions such as:

1. What is already known?
2. How has the problem been studied?
3. What methods and datasets have been used?
4. Where do findings agree?
5. Where do findings conflict?
6. What limitations recur?
7. Which claims are well-supported?
8. Which questions remain unresolved?
9. What evidence justifies the current study?

A literature review should move from **evidence -> synthesis -> implication**, not from citation count -> conclusion.

---

# 4. SEARCH STRATEGY

## L-01. Search Must Follow the Research Question

Do not begin by searching only the preferred method.

Build search concepts from:

- research problem;
- population/domain;
- phenomenon;
- task;
- method where relevant;
- evaluation;
- known synonyms.

Example structure:

**problem concept + domain + task + method/evaluation terms**

The search should reflect the information need, not just the technology the researcher wants to use.

## L-02. Use Multiple Search Terms for the Same Concept

Technical fields often use different terminology.

Build a query map containing:

- canonical term;
- synonyms;
- abbreviations;
- older terminology;
- spelling variants;
- domain-specific terminology.

Do not assume one keyword captures the field.

## L-03. Separate Discovery Queries From Verification Queries

Discovery query:

> broad enough to find relevant work.

Verification query:

> narrow enough to verify a specific claim, method, dataset, or finding.

Do not use broad discovery results as direct evidence for precise claims.

## L-04. Record Search Logic When the Review Requires Reproducibility

For systematic or structured review work, record when relevant:

- database/search engine;
- date searched;
- query;
- filters;
- date range;
- language;
- inclusion criteria;
- exclusion criteria.

Do not claim a systematic process if the search was informal.

## L-05. Search Beyond the First Page of Results When Necessary

High ranking does not equal highest relevance or quality.

Do not treat search-engine position as evidence hierarchy.

## L-06. Backward and Forward Chaining Can Strengthen Coverage

When a highly relevant source is found:

- inspect its references;
- inspect later work that cites it;
- identify foundational studies;
- identify direct replications or extensions.

Use chaining purposefully, not mechanically.

---

# 5. SOURCE SELECTION

## L-07. Relevance Is Mandatory

A high-quality paper is still irrelevant if it does not address the claim or problem.

For each candidate source, ask:

1. Does it study the same or a closely related problem?
2. Is the population/domain relevant?
3. Is the method comparable?
4. Is the evaluation relevant?
5. Does it support a claim needed in the current research?

## L-08. Prefer Primary Evidence for Primary Claims

For claims about:

- experimental findings;
- method performance;
- dataset properties;
- proposed algorithms;
- benchmark results;

prefer the original paper or official source.

Secondary sources may help with orientation but should not replace primary evidence when the original is available.

## L-09. Reviews Are Useful for Mapping, Not Automatic Substitution

Systematic reviews and survey papers are valuable for:

- terminology;
- field mapping;
- recurring themes;
- identifying major studies;
- understanding consensus or disagreement.

But verify important primary claims in the original studies when needed.

## L-10. Source Type Must Match Claim Type

Examples:

- method definition -> original paper or authoritative technical source;
- software behavior -> official documentation;
- benchmark result -> original benchmark paper/report;
- population statistic -> official dataset/institutional source;
- scholarly interpretation -> peer-reviewed literature when possible.

Do not use a source merely because it is easy to cite.

---

# 6. SOURCE QUALITY

## L-11. Evaluate Methodological Quality, Not Prestige Alone

Do not assume a source is strong only because it appears in a famous venue.

Check when relevant:

- research design;
- sample size;
- dataset quality;
- baseline fairness;
- statistical analysis;
- reproducibility;
- external validity;
- limitations.

Venue reputation can inform trust, but it does not replace source evaluation.

## L-12. Distinguish Peer Review Status

Identify whether a source is:

- peer-reviewed article;
- conference paper;
- preprint;
- technical report;
- thesis;
- official documentation;
- dataset card;
- blog;
- forum post;
- company marketing page.

Use the source type appropriately.

## L-13. Preprints Require Calibrated Use

A preprint may be technically valuable, but do not silently present it as peer-reviewed.

If review status matters, state it.

## L-14. Retractions and Corrections Matter

If a paper has been retracted, corrected, or seriously challenged, do not cite it as normal evidence without noting that status.

## L-15. Predatory or Unverifiable Sources Require Caution

Red flags can include:

- unverifiable journal information;
- suspicious publication process;
- missing editorial transparency;
- fake indexing claims;
- unclear authorship;
- inaccessible methodology.

Do not use a source merely because it has a PDF and citation metadata.

---

# 7. RECENCY AND FOUNDATIONAL WORK

## L-16. Recent Does Not Automatically Mean Better

Recent work is useful for:

- current state of the field;
- updated benchmarks;
- newly available models;
- recent regulations or standards.

Older work may be essential when it is:

- foundational;
- original;
- theoretically important;
- still authoritative.

## L-17. Use Recency According to the Claim

For fast-changing technologies, recent evidence matters more.

For mathematical definitions or established theory, older foundational sources may remain appropriate.

## L-18. Do Not Use Arbitrary Date Cutoffs Without a Reason

A five-year window may be appropriate for one topic and inappropriate for another.

Explain the cutoff when it materially shapes the evidence base.

---

# 8. SOURCE EXTRACTION

## L-19. Extract More Than the Abstract

Do not base detailed methodological claims only on abstracts.

When relevant, inspect:

- methods;
- dataset;
- experimental setup;
- results;
- limitations;
- supplementary material.

## L-20. Build a Source Evidence Record

For each important source, capture:

- citation identity;
- research question/objective;
- dataset/population;
- method;
- baseline;
- evaluation;
- key result;
- limitation;
- relevance to current study;
- exact claim supported.

## L-21. Separate Source Fact From Your Interpretation

Useful extraction structure:

**Source reports:** what the paper explicitly states.

**Researcher interpretation:** what you infer from those facts.

Do not merge them.

## L-22. Record Limitations Explicitly

Do not extract only positive findings.

Capture:

- sample limitations;
- dataset limitations;
- methodological weaknesses;
- uncertainty;
- contradictory results;
- threats to validity.

---

# 9. CLAIM-TO-SOURCE TRACEABILITY

## L-23. Every Important Literature Claim Needs Direct Support

For each important claim, be able to answer:

> Which source supports this exact statement?

If no source can be identified, weaken, remove, or label the statement as interpretation.

## L-24. One Citation Does Not Automatically Support an Entire Paragraph

Citations should be placed close to the claims they support.

Do not use a citation as decoration at the end of a long paragraph.

## L-25. Avoid Citation Cascades Without Verification

Do not cite Source B for a claim that B attributes to Source A without checking A when the original claim matters.

This reduces citation distortion.

## L-26. Verify Numerical Claims Against the Original Source

If literature provides:

- accuracy;
- sample size;
- effect size;
- percentages;
- benchmark scores;

verify the number directly.

Do not copy numerical claims from a secondary summary without confirmation when accuracy matters.

---

# 10. COMPARABILITY

## L-27. Do Not Compare Raw Scores Across Incompatible Studies

Two studies may differ in:

- dataset;
- split;
- preprocessing;
- metrics;
- class distribution;
- hardware;
- evaluation protocol;
- random seed;
- model version.

Therefore:

> 91% in Study A

is not automatically better than:

> 89% in Study B.

## L-28. Compare Methods Only Under Relevant Conditions

Before making cross-paper comparisons, check:

- same task?
- same dataset?
- same metric?
- same evaluation procedure?
- same population?
- same constraints?

If not, state the limitation.

## L-29. "Outperforms Previous Work" Requires Evidence

Do not write this unless the studies are sufficiently comparable.

Safer wording:

> The reported score is higher than those reported in several prior studies, although the evaluation settings differ and do not support a direct performance ranking.

---

# 11. LITERATURE SYNTHESIS

## L-30. Organize by Analytical Structure

Possible structures:

- theme;
- method family;
- problem category;
- dataset;
- chronology when meaningful;
- theoretical perspective;
- empirical finding;
- research limitation.

Do not default to paper-by-paper order.

## L-31. Synthesis Must Explain Relationships

Useful synthesis questions:

- Which studies agree?
- Which disagree?
- Why might results differ?
- Which methods dominate?
- What assumptions differ?
- Which datasets are repeatedly used?
- Which evaluation weaknesses recur?

## L-32. Separate Consensus From Frequency

Many papers repeating the same assumption does not automatically prove the assumption is correct.

Ask whether independent evidence supports it.

## L-33. Contradictory Evidence Must Be Preserved

Do not erase disagreement to create a clean narrative.

Report:

- conflicting findings;
- possible methodological reasons;
- unresolved uncertainty.

## L-34. Do Not Force Synthesis Where Studies Are Not Comparable

Sometimes the correct synthesis is:

> The studies cannot be directly compared because they use different tasks and evaluation protocols.

That is better than false integration.

---

# 12. RESEARCH GAP CONSTRUCTION

## L-35. A Gap Must Be Evidence-Based

A defensible gap may involve:

- unanswered question;
- missing population;
- missing context;
- missing comparison;
- unresolved contradiction;
- methodological limitation;
- inadequate evaluation;
- lack of replication;
- limited external validity;
- missing real-world validation.

## L-36. Difference Is Not Automatically a Gap

Bad:

> Prior work used CNN, while this study uses LSTM. Therefore, a research gap exists.

This is only a method difference.

A gap must explain why the difference matters scientifically.

## L-37. "No Study Has..." Requires Strong Evidence

Absolute absence claims are difficult to prove.

Avoid:

> No previous study has investigated...

unless the search strategy supports that conclusion.

Prefer calibrated wording:

> No directly comparable study was identified in the reviewed literature.

or:

> Few studies found in this review examine...

## L-38. The Gap Must Connect to the Research Question

A gap is useful only if the current study can address it.

Do not identify a gap that the proposed method cannot actually resolve.

## L-39. The Gap Must Not Be Manufactured From Limitations Alone

A prior limitation becomes a meaningful gap only when:

1. it matters to the field;
2. it remains unresolved;
3. the current study addresses it.

## L-40. Distinguish Knowledge Gap From Implementation Gap

Examples:

**knowledge gap**

> It is unknown whether method X generalizes to domain Y.

**comparison gap**

> Existing studies evaluate X and Y under different protocols.

**evaluation gap**

> Prior work reports accuracy but not calibration or subgroup performance.

**application gap**

> The method has not been evaluated in the operational context required by the current problem.

Use the appropriate type.

---

# 13. METHOD JUSTIFICATION FROM LITERATURE

## L-41. Literature Can Justify a Method, but Not Replace Reasoning

Bad:

> Random Forest was selected because many studies used it.

Better:

> Random Forest was included because prior studies show it is a strong baseline for tabular classification, and its characteristics fit the available feature structure.

## L-42. A Popular Method Is Not Automatically Appropriate

Popularity does not prove suitability for:

- the dataset;
- sample size;
- task;
- constraints;
- interpretability needs.

## L-43. Use Literature to Identify Reasonable Baselines

A baseline should reflect:

- established prior approaches;
- common simple methods;
- relevant current methods.

Do not choose only weak baselines.

---

# 14. THEORY AND CONCEPTS

## L-44. Definitions Need Appropriate Sources

For technical concepts, prefer:

- original formulation;
- authoritative textbook;
- standard;
- official technical documentation;
- strong review source.

Avoid citing random secondary pages for foundational definitions when stronger sources exist.

## L-45. Competing Definitions Must Be Acknowledged

If a concept has multiple accepted definitions, do not silently present one as universal.

State the chosen definition and why it fits the study.

## L-46. Theory Must Connect to the Study

Do not include theory only to increase literature volume.

Every theoretical concept should help:

- define variables;
- explain relationships;
- justify hypotheses;
- interpret results.

---

# 15. LITERATURE REVIEW STRUCTURE

## L-47. Background Is Not the Same as Literature Review

Background explains:

- problem context;
- significance;
- motivation.

Literature review analyzes:

- prior research;
- evidence;
- methods;
- limitations;
- gap.

Do not merge them into a citation-heavy introduction without analytical structure.

## L-48. Use Section Structure Based on Research Logic

Possible pattern:

1. core concept;
2. prior approaches;
3. datasets/evaluation;
4. major findings;
5. limitations;
6. unresolved issue;
7. resulting research gap.

Adapt structure to the study.

## L-49. End Sections With Synthesis, Not Citation Accumulation

A section should conclude with what the evidence collectively means.

Do not end merely because enough papers have been listed.

---

# 16. SYSTEMATIC AND STRUCTURED REVIEWS

## L-50. Do Not Call a Review Systematic Without a Systematic Process

A systematic review typically requires explicit:

- search databases;
- queries;
- screening;
- inclusion/exclusion;
- selection flow;
- extraction;
- quality appraisal.

If these are absent, use a more accurate label such as:

- literature review;
- narrative review;
- structured review.

## L-51. Inclusion and Exclusion Criteria Must Be Predefined When Required

Do not change criteria simply to retain preferred papers.

If criteria change, document the change.

## L-52. Screening Must Be Traceable

Record:

- records found;
- duplicates removed;
- screened;
- excluded;
- included.

Use an appropriate flow structure when the review methodology requires it.

## L-53. Quality Appraisal Must Affect Interpretation

Do not score study quality and then ignore the score.

Weaker evidence should receive appropriately weaker interpretive weight.

---

# 17. DUPLICATION AND VERSION CONTROL

## L-54. Detect Duplicate Publications

The same study may appear as:

- preprint;
- workshop paper;
- conference paper;
- journal extension.

Do not count the same evidence multiple times as independent studies.

## L-55. Prefer the Most Complete Relevant Version

When multiple versions exist, prefer the version that best represents the final work, unless the earlier version is specifically relevant.

## L-56. Track Source Identity Carefully

Keep stable identifiers where possible:

- DOI;
- PMID;
- arXiv ID;
- official URL;
- repository identifier.

---

# 18. NEGATIVE AND NULL EVIDENCE

## L-57. Do Not Search Only for Supporting Papers

A defensible review looks for evidence that can challenge the preferred hypothesis.

Search for:

- failed replications;
- negative findings;
- alternative methods;
- contradictory results;
- limitations.

## L-58. Absence of Evidence Is Not Evidence of Absence

If few studies report an effect, do not conclude automatically that the effect does not exist.

## L-59. Publication Bias May Affect the Literature

Positive results may be overrepresented.

Mention this when it materially affects interpretation.

---

# 19. EVIDENCE WEIGHTING

## L-60. Do Not Treat All Sources Equally

Evidence weight may depend on:

- methodological quality;
- directness;
- sample;
- replication;
- relevance;
- transparency;
- consistency with independent evidence.

## L-61. Stronger Evidence Should Dominate the Synthesis

If one weak study conflicts with multiple strong direct studies, do not present the disagreement as numerically balanced without context.

## L-62. Source Count Is Not Evidence Strength

Ten low-quality sources are not automatically stronger than two rigorous directly relevant studies.

---

# 20. AI-ASSISTED LITERATURE WORK

## L-63. AI May Assist Search and Synthesis, but Must Not Invent Sources

Never accept:

- unverified citations;
- plausible titles;
- fabricated DOIs;
- invented authors;
- invented findings.

Every important source must be verifiable.

## L-64. AI Summaries Must Be Checked Against the Source

Do not cite an AI summary as if it were the paper.

Verify important claims in the original text.

## L-65. AI-Generated Search Terms Are Suggestions, Not Evidence

Use them to improve discovery, not as proof of terminology or field consensus.

## L-66. AI Must Not Fill Unread Sections With Plausible Content

If a paper section is unavailable, say that the evidence could not be verified from the accessible content.

---

# 21. LITERATURE NOTES

A useful literature note can use:

> **Source ID:**  
> **Full citation:**  
> **Source type:**  
> **Research objective:**  
> **Population/dataset:**  
> **Method:**  
> **Evaluation:**  
> **Main finding:**  
> **Limitation:**  
> **Claim(s) supported:**  
> **Relevance to current study:**  
> **Comparability notes:**  
> **Confidence in use:** verified / partial / uncertain

This structure improves traceability and reduces citation misuse.

---

# 22. CLAIM MATRIX

For important literature-dependent sections, maintain a claim matrix when useful.

| Claim | Supporting source | Direct support? | Source quality | Notes |
|---|---|---:|---|---|
| Claim A | Source 1 | Yes | High | Direct experimental result |
| Claim B | Source 2 | Partial | Medium | Requires weaker wording |
| Claim C | None | No | N/A | Remove or verify |

A claim without support must not survive merely because it sounds plausible.

---

# 23. RESEARCH GAP MATRIX

When the gap is complex, compare prior studies using dimensions such as:

| Study | Population/Dataset | Method | Evaluation | Limitation | Unresolved issue |
|---|---|---|---|---|---|

Use the matrix to identify a gap from evidence.

Do not create the gap first and then selectively choose papers that support it.

---

# 24. LITERATURE AUDIT FORMAT

Use:

> **L-XX | SEVERITY | LOCATION**  
> **Problem:** what is wrong.  
> **Why:** why it weakens the evidence base.  
> **Evidence:** the source or citation issue.  
> **Correction:** what should change.  
> **Verification:** how to verify the correction.

Example:

> **L-27 | MAJOR | Literature Review 2.3**  
> **Problem:** the paragraph states that Model A outperforms Model B based on scores from different datasets.  
> **Why:** the evaluation settings are not comparable.  
> **Evidence:** Study A uses Dataset X and macro-F1, while Study B uses Dataset Y and accuracy.  
> **Correction:** remove the direct ranking and describe the results separately.  
> **Verification:** confirm dataset and metric details in both original papers.

---

# 25. LITERATURE QUALITY GATE

Before marking a literature section final, verify:

## Search

- [ ] Search terms reflect the research question.
- [ ] Important synonyms were considered.
- [ ] Search scope is appropriate to the research claim.
- [ ] Structured/systematic claims match the actual search method.

## Source Quality

- [ ] Important claims use appropriate source types.
- [ ] Primary evidence is used where needed.
- [ ] Review/preprint status is not misrepresented.
- [ ] Suspicious or unverifiable sources are excluded or clearly qualified.

## Traceability

- [ ] Every major claim has a source.
- [ ] Citations directly support the claim.
- [ ] Numerical claims were verified.
- [ ] Secondary citations were checked against originals where necessary.

## Comparability

- [ ] Cross-study comparisons account for dataset differences.
- [ ] Metrics are comparable.
- [ ] Evaluation protocols are not treated as equivalent without evidence.
- [ ] No unsupported "outperforms previous work" claim remains.

## Synthesis

- [ ] The review does more than list papers.
- [ ] Agreement and disagreement are explicit.
- [ ] Contradictory evidence is preserved.
- [ ] Weak and strong evidence are not treated identically.
- [ ] The synthesis explains what the literature collectively means.

## Research Gap

- [ ] The gap is evidence-based.
- [ ] The gap is not merely a method difference.
- [ ] Absolute absence claims are avoided unless justified.
- [ ] The gap connects directly to the research question.
- [ ] The current study can actually address the identified gap.

Any material failure must be corrected before the literature section is labeled final.

---

# 26. Recommended Workflow

Use this module in the following order:

1. `00-RESEARCH-CORE.md`
2. `03-research-literature.md`
3. `04-research-methodology.md` when method design begins
4. `05-research-experiment.md` for computational experiments
5. `06-research-analysis.md` for analysis and interpretation
6. `01-research-writing.md` for final academic prose
7. final Research Delivery Gate

Literature work should establish the evidence base that later modules depend on.

---

# 27. Final Principles

**Direct support > citation volume**  
**Relevance > prestige**  
**Primary evidence > convenient summaries**  
**Synthesis > paper listing**  
**Comparability > raw score ranking**  
**Evidence-based gap > invented novelty**  
**Contradiction > preserved, not hidden**  
**Methodological quality > publication count**  
**Search transparency > vague claims of coverage**  
**Verified sources > plausible citations**  
**Traceability > citation decoration**
