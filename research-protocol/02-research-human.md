# research-human

> Human-centered research quality, participant integrity, instrument accessibility, annotation reliability, human evaluation, privacy, usability, and responsible reporting.

## 1. Purpose

This module complements `00-RESEARCH-CORE.md`.

Use it whenever research involves people directly or indirectly, including:

- participants;
- respondents;
- interviewees;
- users;
- annotators;
- expert evaluators;
- human judges;
- usability testers;
- survey respondents;
- human-in-the-loop workflows;
- subjective ratings;
- human feedback.

The goal is to ensure that human involvement is not treated as an afterthought.

Human-facing research must remain:

- ethically aware;
- methodologically defensible;
- accessible;
- transparent;
- privacy-conscious;
- resistant to hidden exclusion;
- honest about subjectivity and uncertainty.

Priority order:

**participant integrity > measurement validity > accessibility > privacy > evaluation reliability > reporting clarity**

---

## 2. Boundary With the Core

This module must never weaken `00-RESEARCH-CORE.md`.

The core governs:

- integrity;
- evidence;
- validity;
- reproducibility;
- traceability;
- verification.

This module adds depth for human-related concerns.

If a human-centered procedure produces a methodologically invalid result, the result remains invalid even if the writing is polished.

If an instrument is inaccessible to part of the intended population, that limitation affects research validity, not merely presentation quality.

---

## 3. Human-Centered Principle

Human-centered research quality is not a final checklist.

It must be considered across:

**research design -> recruitment -> consent -> instrument design -> pilot -> data collection -> annotation/evaluation -> analysis -> reporting**

For every human-related decision, ask:

1. Who is included?
2. Who is unintentionally excluded?
3. What does the participant need to understand?
4. What burden is imposed?
5. What bias can the procedure introduce?
6. What privacy risk is created?
7. What uncertainty exists in human judgment?
8. What evidence supports any claim about users or participants?

---

# 4. PARTICIPANT INCLUSION AND EXCLUSION

## H-01. Define the Target Population Clearly

State who the research intends to study.

Do not use vague labels such as:

- users;
- students;
- professionals;
- general public;

without relevant scope.

Clarify when needed:

- age range;
- educational background;
- domain experience;
- language;
- geographic context;
- technical experience;
- other inclusion characteristics.

Do not collect irrelevant demographics.

## H-02. Hidden Exclusion Must Be Reported

A procedure may exclude people even when the eligibility criteria do not.

Examples:

- mobile-only access;
- high-bandwidth requirement;
- technical vocabulary;
- visual-only instructions;
- incompatible device requirements;
- inaccessible interaction design.

If the procedure excludes part of the intended population, report it.

## H-03. Convenience Samples Must Not Be Presented as Representative

If the sample is convenient, local, institutional, or narrow, do not generalize automatically.

Example:

> Fifty students from one class participated.

Do not conclude:

> Users in general prefer...

Prefer:

> Among the students who participated in this study...

Scope claims to the actual sample.

## H-04. Participant Characteristics Must Be Observed, Not Assumed

Do not infer participant characteristics that were not collected.

Bad:

> Younger users preferred the interface.

if age was not recorded.

If a characteristic was not measured, do not use it to explain results.

## H-05. Exclusion Criteria Must Be Justified

Do not remove participant data because:

- the answer looks strange;
- the score is low;
- the result weakens the hypothesis;
- the participant disagrees with the expected outcome.

Valid exclusion rules may include:

- duplicate response;
- incomplete submission;
- eligibility failure;
- failed attention check;
- technical corruption.

Report exclusions and reasons.

## H-06. Post-Hoc Exclusion Requires Transparency

If an exclusion rule was created after data collection, state that clearly.

Do not present it as pre-specified.

---

# 5. PARTICIPANT BURDEN

## H-07. Every Task Must Serve the Research

Questionnaires, interviews, and experiments should not be longer than necessary.

For every task or item, ask:

> What construct, variable, validity check, or research question does this serve?

If there is no clear purpose, remove it.

## H-08. Fatigue Can Affect Data Quality

Long procedures can change:

- attention;
- accuracy;
- response quality;
- dropout;
- task performance.

If burden is substantial, consider:

- breaks;
- shorter forms;
- randomized block order;
- pilot timing;
- reporting completion rates.

## H-09. Do Not Treat Dropout as Invisible

Track where relevant:

- recruited;
- started;
- completed;
- excluded;
- analyzed.

If many participants leave, investigate whether dropout may be systematic.

---

# 6. VOLUNTARY PARTICIPATION AND CONSENT

## H-10. Participation Must Be Voluntary

Be careful when recruitment involves power relationships, such as:

- teacher and student;
- supervisor and employee;
- manager and subordinate;
- clinician and patient.

Formal agreement does not automatically mean the participant felt free to refuse.

## H-11. Informed Consent Is Not a Checkbox

A consent form should communicate, in proportion to the study:

- study purpose;
- procedure;
- expected duration;
- relevant risks or discomforts;
- data collected;
- intended data use;
- withdrawal rights where applicable;
- contact information where required.

Do not hide material information behind vague language.

## H-12. Consent Language Must Be Understandable

Participant-facing consent should match the comprehension level of the target population.

Do not use unnecessary legalistic or technical wording.

## H-13. Consent Does Not Remove Methodological Responsibility

A participant agreeing to a procedure does not make a poor research design valid.

Consent and validity are separate requirements.

---

# 7. PRIVACY AND DATA MINIMIZATION

## H-14. Collect Only Data Needed for the Research

For every personal field, ask:

> Why is this necessary for the research question or analysis?

If there is no defensible reason, do not collect it.

Potentially unnecessary fields include:

- full name;
- address;
- phone number;
- exact birth date;
- institution;
- exact location;
- personal identifiers.

## H-15. Do Not Call Data Anonymous Without Justification

Removing names does not automatically make data anonymous.

Combinations such as:

- age;
- institution;
- role;
- location;
- timestamp;
- free-text responses;

may re-identify participants.

Use terminology accurately:

- anonymous;
- pseudonymous;
- de-identified;
- coded.

## H-16. Free-Text Data Can Contain Identifiers

Open responses may contain names, locations, employers, or personal events.

Inspect and handle such content appropriately before public release.

## H-17. Privacy Claims Must Be Verifiable

Do not write:

> participant data were fully anonymous

unless the process actually supports that claim.

Use precise wording.

---

# 8. INSTRUMENT ACCESSIBILITY

## H-18. Instrument Language Must Match the Population

The wording of instructions and questions should be understandable to the intended participants.

Do not accidentally measure reading difficulty instead of the target construct.

## H-19. Separate Research Terminology From Participant-Facing Language

Technical language may be appropriate in the thesis but inappropriate in the instrument.

Bad participant-facing wording:

> Evaluate the inference latency of the multimodal model.

Better:

> How quickly did the system respond after you submitted the input?

when that wording matches the construct.

## H-20. Avoid Ambiguous Questions

Bad:

> Was the system easy and fast to use?

This combines two constructs.

Prefer separate items:

> The system was easy to use.

> The system responded quickly.

## H-21. Avoid Leading Questions

Bad:

> How helpful was the new feature that improved productivity?

The wording already assumes a positive effect.

Use neutral wording.

## H-22. Avoid Double-Barreled Items

Each item should primarily measure one thing.

Do not combine:

- usefulness and ease;
- speed and satisfaction;
- accuracy and trust;

unless the construct is intentionally composite and validated.

## H-23. Avoid Double Negatives

Bad:

> I do not think the system is not difficult to use.

Prefer direct wording.

## H-24. Response Scales Must Be Consistent

Do not randomly reverse scale direction.

If reverse-coded items are used, do so for a methodological reason and document it.

## H-25. Not-Applicable Options Should Exist When Needed

Do not force participants to judge something they did not experience.

Where appropriate, provide options such as:

- not applicable;
- did not experience;
- do not know.

Do not add such options automatically if the measurement design requires a forced choice.

---

# 9. ACCESSIBILITY OF DIGITAL INSTRUMENTS

## H-26. Do Not Assume Usability From Researcher Experience

A form is not accessible merely because the researcher can complete it.

Consider, when relevant:

- readable text size;
- contrast;
- keyboard navigation;
- screen-reader compatibility;
- mobile layout;
- zoom;
- visible focus;
- understandable errors;
- touch target size.

## H-27. Do Not Rely on Color Alone

If status or meaning is communicated through color, also use:

- labels;
- icons;
- patterns;
- line styles;
- text.

This applies to:

- questionnaires;
- dashboards;
- experimental interfaces;
- research figures.

## H-28. Error Messages Must Be Informative

Bad:

> Invalid input.

Better:

> Enter a value between 1 and 5.

Participant-facing errors should help users recover.

## H-29. Zoom and Reflow Must Be Considered

If the instrument is web-based, verify that content remains usable when text is enlarged or viewed on a narrow screen.

## H-30. Mobile Keyboard Must Not Block Required Input

If participants may use mobile devices, verify that focused fields remain visible and usable.

---

# 10. PILOT TESTING

## H-31. Pilot Test When the Instrument Is Non-Trivial

A pilot can reveal:

- ambiguous wording;
- misunderstood instructions;
- excessive duration;
- missing answer options;
- technical failures;
- confusing task flow;
- measurement problems.

A pilot improves the instrument but does not automatically establish validity.

## H-32. Pilot Findings Must Affect the Instrument

Do not run a pilot ceremonially.

If participants consistently misunderstand an item, revise or justify it.

## H-33. Distinguish Pilot Data From Main-Study Data

Do not merge pilot participants into the final dataset without a justified design decision.

---

# 11. HUMAN ANNOTATION

## H-34. Annotation Guidelines Must Be Explicit

For subjective or non-trivial labeling, provide:

- label definitions;
- positive examples;
- negative examples;
- edge cases;
- ambiguity rules.

## H-35. One Annotator Is Not Automatically Ground Truth

For subjective tasks, one person's label is still a human judgment.

Use terms such as:

- human annotation;
- expert annotation;
- reference label;

unless "ground truth" is genuinely justified.

## H-36. Inter-Annotator Agreement Must Be Considered

If multiple annotators are used, assess whether agreement matters to the task.

Select an agreement measure appropriate to:

- number of annotators;
- measurement scale;
- missing labels;
- task type.

Do not use Cohen's kappa, Fleiss' kappa, or Krippendorff's alpha by habit.

## H-37. Disagreement Is Data

Do not hide disagreement automatically.

High disagreement may indicate:

- unclear guidelines;
- ambiguous samples;
- subjective task boundaries;
- inadequate construct definition.

## H-38. Adjudication Must Be Documented

If conflicting labels are resolved, record:

- who adjudicated;
- how decisions were made;
- whether annotators saw each other's labels;
- how unresolved cases were handled.

## H-39. Annotator Training Must Be Reported When Relevant

If annotators received examples, training rounds, calibration, or feedback, document it.

---

# 12. EXPERT EVALUATION

## H-40. "Expert" Must Be Operationalized

Do not write:

> Three experts validated the system.

without explaining why they qualify.

Relevant criteria may include:

- domain experience;
- professional role;
- years of practice;
- research background;
- certification;
- task-specific expertise.

Use only criteria actually applied.

## H-41. Expert Judgment Is Still Judgment

Do not convert expert ratings into objective truth.

Prefer:

> The evaluators assigned a median score of 4 out of 5.

over:

> The system was objectively proven to be excellent.

## H-42. Expert Selection Can Introduce Bias

Report how evaluators were selected when it matters.

Avoid implying independence if evaluators were directly involved in system development.

---

# 13. HUMAN EVALUATION OF AI SYSTEMS

## H-43. Blind the Model Identity When Appropriate

If evaluator expectations could influence judgment, hide model identity when the design allows.

Do not expose:

- brand;
- model name;
- vendor;
- "baseline" versus "proposed" labels;

when those labels are irrelevant to the evaluation.

## H-44. Randomize or Counterbalance Presentation Order

If output A always appears before output B, order effects may influence preference.

Randomize or counterbalance where relevant.

## H-45. Standardize Presentation

If content quality is being evaluated, avoid giving one system:

- better formatting;
- clearer typography;
- richer metadata;
- longer context;

unless presentation itself is part of the construct.

## H-46. Preference Is Not Correctness

A preferred answer may still be factually wrong.

Keep separate constructs such as:

- preference;
- factual correctness;
- fluency;
- helpfulness;
- relevance;
- safety;
- style;
- usability.

## H-47. Human Ratings Need Defined Criteria

Do not ask evaluators to rate "quality" without defining what quality means.

Operationalize dimensions.

## H-48. Evaluator Instructions Must Be Calibrated

If two evaluators interpret "helpful" differently, the resulting scores may not be comparable.

Use examples or calibration where appropriate.

---

# 14. HUMAN-IN-THE-LOOP SYSTEMS

## H-49. Separate Model Performance From Human-System Performance

If a human edits, approves, filters, or overrides outputs, report that workflow.

Do not present:

**human + AI performance**

as:

**model-only performance**

## H-50. Document Human Intervention

When relevant, record:

- when humans intervene;
- what information they see;
- what decisions they can change;
- what actions are mandatory;
- how often intervention occurs.

## H-51. Automation Bias Must Be Considered

Users may over-trust system suggestions.

If the research studies decision support, consider whether system confidence, wording, or interface design changes human decisions.

---

# 15. USABILITY RESEARCH

## H-52. Usability Claims Require Evidence

Do not claim:

> The system is easy to use.

based only on:

- developer opinion;
- screenshots;
- internal demonstration.

Use appropriate evidence such as:

- task completion;
- time on task;
- error rate;
- validated questionnaire;
- usability interview;
- structured observation.

## H-53. Satisfaction Is Not Effectiveness

Separate:

- effectiveness;
- efficiency;
- satisfaction.

A user can like a system while failing the task.

## H-54. Task Success Must Be Defined

State what counts as successful completion.

Do not decide after observing the results.

## H-55. Failed Tasks Must Be Analyzed

Do not report only successful interactions.

Failures may reveal:

- usability issues;
- misunderstanding;
- system defects;
- workflow mismatch.

## H-56. Observed Behavior and Self-Report Must Be Distinguished

A participant saying:

> It was easy.

is not the same evidence as:

> The task was completed without error.

Report both separately.

---

# 16. QUALITATIVE DATA

## H-57. Quotes Must Be Real

Never create a "representative quote."

Only use actual participant statements.

## H-58. Do Not Cherry-Pick Qualitative Evidence

Do not include only quotes that support the preferred conclusion.

Look for:

- recurring themes;
- disagreement;
- counterexamples;
- negative cases;
- unusual but relevant responses.

## H-59. Coding Procedure Must Be Traceable

When qualitative coding is used, document when relevant:

- coding approach;
- codebook;
- coders;
- iteration;
- disagreement handling;
- theme construction.

## H-60. Themes Do Not "Emerge" Without Analytical Work

Avoid language that hides the researcher's role.

Explain how themes were identified.

## H-61. Translation Can Change Meaning

If participant language differs from publication language, consider:

- translation method;
- preservation of nuance;
- terminology consistency.

Do not strengthen or soften participant meaning during translation.

---

# 17. HUMAN UNCERTAINTY

## H-62. Human Judgment Is Not Perfectly Precise

Ratings can vary due to:

- interpretation;
- fatigue;
- expertise;
- context;
- order;
- mood;
- ambiguity.

Do not report subjective scores as if they were error-free measurements.

## H-63. Disagreement Must Not Be Hidden

If evaluators disagree materially, report or analyze it when relevant.

## H-64. Confidence Can Be Useful When It Serves the Design

If evaluator confidence matters, measure it explicitly rather than inferring it from the rating.

---

# 18. REPORTING HUMAN DATA

## H-65. Report Participant Flow When Relevant

Useful structure:

**recruited -> eligible -> started -> completed -> excluded -> analyzed**

## H-66. Report the Actual Sample Used in Each Analysis

If sample size differs by analysis because of missing data, state it.

## H-67. Do Not Overgeneralize From Human Samples

A local sample supports local evidence unless the sampling design supports broader inference.

## H-68. Report Human Limitations Specifically

Examples:

- narrow participant demographic;
- self-selection;
- small expert panel;
- single-language instrument;
- unblinded evaluation;
- low annotator agreement;
- convenience sampling.

Avoid generic statements such as:

> The study was limited by time.

unless time genuinely affected the design.

---

# 19. ACCESSIBLE SCIENTIFIC COMMUNICATION

## H-69. Figures Must Not Depend on Color Alone

Use combinations of:

- labels;
- markers;
- line styles;
- patterns;
- annotations.

## H-70. Figure Text Must Be Readable

Check:

- axis labels;
- legend size;
- units;
- caption clarity;
- resolution;
- print readability.

## H-71. Tables Must Be Understandable Without Guessing

Avoid:

- unexplained abbreviations;
- missing units;
- excessive decimal precision;
- ambiguous metric labels.

## H-72. Accessibility Supports Scientific Clarity

Accessible presentation is not cosmetic.

If readers cannot distinguish groups, labels, or states, interpretation quality suffers.

---

# 20. HUMAN VERIFICATION STANDARD

Do not claim the following without evidence:

- participants understood the instructions;
- the instrument was easy to use;
- the system was accessible;
- experts agreed;
- annotators were reliable;
- users preferred the system;
- participants found the task easy;
- the interface was usable.

Whenever such a claim matters, state how it was verified.

---

# 21. HUMAN AUDIT FORMAT

Use:

> **H-XX | SEVERITY | LOCATION**  
> **Tell:** the observed issue.  
> **Why:** why it affects people or research validity.  
> **Evidence:** where the issue is visible.  
> **Fix:** the correction.  
> **Verification:** how to confirm the correction.

Example:

> **H-20 | MAJOR | Questionnaire item 8**  
> **Tell:** the item asks whether the system was "easy and fast to use."  
> **Why:** the item combines ease of use and perceived speed, so the response cannot be attributed to one construct.  
> **Evidence:** both constructs appear in one Likert item.  
> **Fix:** split the item into two separate statements.  
> **Verification:** pilot the revised items and confirm participants interpret them independently.

---

# 22. HUMAN SKILL CHECKLIST

Run this with the core Research Delivery Gate whenever humans are involved.

## Participants

- [ ] Target population is clearly defined.
- [ ] Inclusion criteria are explicit.
- [ ] Exclusion criteria are justified.
- [ ] Hidden access barriers have been considered.
- [ ] Sample claims do not exceed the actual sample.
- [ ] Dropout and exclusions are reported when relevant.
- [ ] Participant burden is proportionate.

## Consent and Privacy

- [ ] Participation is meaningfully voluntary.
- [ ] Consent information is understandable.
- [ ] Data collection is minimized.
- [ ] Privacy terminology is accurate.
- [ ] Identifiers are handled intentionally.
- [ ] Free-text privacy risks are considered.

## Instrument

- [ ] Instructions match participant comprehension.
- [ ] Questions are not leading.
- [ ] Questions are not double-barreled.
- [ ] Scale direction is consistent.
- [ ] Not-applicable options exist when needed.
- [ ] Pilot testing was performed when justified.
- [ ] Accessibility limitations are known.

## Human Annotation

- [ ] Label definitions are explicit.
- [ ] Edge cases are documented.
- [ ] Agreement is assessed when relevant.
- [ ] Adjudication is traceable.
- [ ] Subjective labels are not falsely presented as absolute truth.

## Expert Evaluation

- [ ] Expert eligibility is defined.
- [ ] Expert selection is reported when relevant.
- [ ] Expert opinion is reported as judgment, not objective fact.

## AI Human Evaluation

- [ ] Model identity is blinded when needed.
- [ ] Presentation order is randomized or counterbalanced when needed.
- [ ] Output formatting is comparable.
- [ ] Evaluation dimensions are operationalized.
- [ ] Preference is not confused with correctness.

## Usability

- [ ] Usability claims are evidence-based.
- [ ] Effectiveness, efficiency, and satisfaction are distinguished.
- [ ] Task success is defined.
- [ ] Failed tasks are analyzed.
- [ ] Self-report and observed behavior are separated.

## Reporting

- [ ] Human uncertainty is not hidden.
- [ ] Disagreement is reported when relevant.
- [ ] Qualitative quotes are real.
- [ ] Qualitative analysis is traceable.
- [ ] Figures do not rely on color alone.
- [ ] Tables and figures are readable and interpretable.

Any material failure must be corrected, scoped, or explicitly reported as a limitation before finalization.

---

# 23. Human Gate

Before research involving humans is labeled final, ask:

1. Is any group unintentionally excluded?
2. Does the instrument measure the intended construct?
3. Could the procedure itself bias the responses?
4. Are participants asked for unnecessary personal data?
5. Is subjective judgment presented as objective truth?
6. Are human limitations hidden?
7. Are failed interactions excluded without analysis?
8. Are participant or user claims broader than the sample?
9. Are accessibility barriers unreported?
10. Can another researcher understand how the human data were produced?

If any answer reveals a material problem:

**FAIL until corrected, bounded, or transparently reported.**

---

# 24. Recommended Workflow

Use this module in the following order:

1. `00-RESEARCH-CORE.md`
2. `02-research-human.md`
3. the relevant methodology/analysis module
4. `01-research-writing.md`
5. final Research Delivery Gate

This module should improve the validity of human-centered research, not merely make participant-facing materials look polished.

---

# 25. Final Principles

**Human involvement is part of methodology, not decoration**  
**Voluntary participation > procedural convenience**  
**Measurement validity > questionnaire length**  
**Accessibility > researcher assumptions**  
**Data minimization > collecting everything**  
**Observed evidence > assumed participant behavior**  
**Human judgment > reported as judgment, not absolute truth**  
**Disagreement > information, not noise to hide**  
**Usability evidence > developer opinion**  
**Participant scope > broad generalization**  
**Transparency > methodological neatness**
