# Start Here

Welcome! This guide will help you get started with the Research Operating System (Research OS) in under 5 minutes.

---

## What Is Research OS?

Research OS is a collection of **modular protocol files** that you upload to AI platforms (ChatGPT, Gemini, Claude, etc.) to transform them into a disciplined research partner.

Instead of AI generating speculative answers, it will:

- Demand verifiable evidence before formulating claims
- Adhere to structured academic research lifecycles
- Flag unsupported conclusions, leakage, and confounding variables
- Maintain academic traceability and integrity

**It does NOT write your thesis or paper for you.** It helps you conduct research properly with evidence-first AI assistance.

---

## Canonical Research Lifecycle

Research OS follows a strict evidence-before-claims lifecycle. Every stage requires verified outputs before advancing to the next:

```
Problem
  -> Evidence / Literature
    -> Research Gap
      -> Research Question
        -> Methodology
          -> Data / Experiment
            -> Analysis
              -> Writing & Conclusion
                -> Audit
```

**Do not skip ahead.** Each phase builds upon verified outputs from the previous phase.

---

## Beginner Journey

Follow this recommended sequence from first discovery to verified research:

```
1. README.md                     -> High-level overview, philosophy, and boundaries
2. START-HERE.md                 -> 5-minute setup, project layout, and copy rules
3. Choose Language               -> English (docs/USER-GUIDE-EN.md) or Indonesia (docs/USER-GUIDE-ID.md)
4. Choose Platform               -> ChatGPT Projects, Claude, Gemini, NotebookLM, or Coding Agents
5. Create / Fill PROJECT-CONTEXT -> Fill out 09-project-context-template.md as PROJECT-CONTEXT.md
6. Choose Current Research Task  -> Match task against the Canonical Research Lifecycle
7. Upload Core + Active Module   -> Always 00-RESEARCH-CORE.md + RESEARCH.md + active module
8. Run Prompt Template           -> Pick prompt from prompts/PROMPT-LIBRARY-EN.md or ID
9. Verify & Audit                -> Run audit checks before accepting claims or drafting
```

---

## How to Organize Your Research Project

When working on a real thesis or research paper, create a dedicated project folder and copy the protocol files into it:

```
my-research-project/
|-- AGENTS.md
|   # Optional: adapted for supported coding agents
|
|-- PROJECT-CONTEXT.md
|   # Created by user from 09-project-context-template.md
|
|-- research-protocol/
|   |-- RESEARCH.md
|   |-- 00-RESEARCH-CORE.md
|   \-- [relevant-modules].md
|
|-- literature/
|-- methodology/
|-- experiments/
|-- analysis/
\-- manuscript/
```

### File Origin Breakdown

**FROM RESEARCH OS (COPIED):**
- `RESEARCH.md` (main router)
- `00-RESEARCH-CORE.md` (universal integrity rules - always loaded)
- Relevant specialized modules for your active phase
- `09-project-context-template.md` (template to copy and fill)
- `AGENTS.md` (when applicable for supported coding agents)

**CREATED BY USER:**
- `PROJECT-CONTEXT.md` (filled with your research topic, questions, and parameters)
- Research questions and hypotheses
- Literature collection (PDFs, notes, synthesis matrices)
- Datasets, survey instruments, and code
- Experiment outputs and logs
- Statistical analyses and tables
- Manuscript drafts (LaTeX / Word chapters)

---

## Step-by-Step Setup

### Step 1 - Choose Your Language

- **Bahasa Indonesia** - [docs/USER-GUIDE-ID.md](docs/USER-GUIDE-ID.md)
- **English** - [docs/USER-GUIDE-EN.md](docs/USER-GUIDE-EN.md)

### Step 2 - Understand the Router

Read [research-protocol/RESEARCH.md](research-protocol/RESEARCH.md) - this is the **main control router** that maps your current task to specific modules.

### Step 3 - Pick Modules for Your Stage

| Canonical Lifecycle Stage | Required Protocol Files |
|---|---|
| Problem Definition | `CORE` + `RESEARCH.md` + `03-research-literature.md` |
| Evidence / Literature Review | `CORE` + `03-research-literature.md` + `01-research-writing.md` |
| Research Gap Identification | `CORE` + `03-research-literature.md` + `04-research-methodology.md` |
| Research Question Formulation | `CORE` + `04-research-methodology.md` |
| Methodology Design | `CORE` + `04-research-methodology.md` (+ `02-research-human.md` if human subjects) |
| Data / Experiment Execution | `CORE` + `04-research-methodology.md` + `05-research-experiment.md` |
| Statistical Analysis | `CORE` + `06-research-analysis.md` + `05-research-experiment.md` |
| Writing & Conclusion | `CORE` + active module + `01-research-writing.md` |
| Final Audit | `CORE` + all modules used + `07-research-audit.md` |

### Step 4 - Upload to Your AI Platform

See [docs/PLATFORM-USAGE-MAP.md](docs/PLATFORM-USAGE-MAP.md) for operational platform instructions:
- **ChatGPT Projects:** Upload `RESEARCH.md`, `CORE`, active modules, and `PROJECT-CONTEXT.md`. Provides persistent project context through project chats, files, and instructions.
- **ChatGPT (Regular Chat):** Recommended minimum is `RESEARCH.md` + `00-RESEARCH-CORE.md` + 1 module. (*Note: RESEARCH.md may be omitted only when the user manually selects the correct module and does not need router behavior.*)
- **Gemini Gems:** Upload protocol files into Gem Knowledge and set system instruction.
- **Claude Projects:** Add protocol files to Project Knowledge and set project custom instructions.
- **NotebookLM:** Upload your research papers/PDFs and `03-research-literature.md` for source-grounded literature extraction.
- **Coding Agents:** Use `AGENTS.md` when your coding agent supports the `AGENTS.md` convention. Otherwise, use the platform-native instruction file (e.g., `CLAUDE.md` for Claude Code).

### Step 5 - Use Ready-Made Prompts

Copy structured prompts from the Prompt Library:
- [English Prompt Library](prompts/PROMPT-LIBRARY-EN.md)
- [Pustaka Prompt Bahasa Indonesia](prompts/PROMPT-LIBRARY-ID.md)

---

## Important Rules

1. **Never upload all files at once.** Upload only what your current research phase requires.
2. **Always include `00-RESEARCH-CORE.md`.** It contains universal integrity rules and evidence discipline.
3. **Follow the canonical sequence:** Problem -> Evidence / Literature -> Research Gap -> Research Question -> Methodology -> Data / Experiment -> Analysis -> Writing & Conclusion -> Audit.
4. **Do not skip the audit phase.** It helps verify that your work meets integrity standards.
5. **AGENTS.md is for coding agents.** If you are using ChatGPT Projects, Claude Projects, or Gemini Gems, you do NOT need `AGENTS.md`.

---

## Research Integrity Disclaimer

Research OS supports research quality; **it does not guarantee it**.
It does not guarantee thesis acceptance, flawless methodology, or specific AI detector scores. It provides structured verification guardrails so that you can produce defensible, evidence-backed academic work.

---

## Frequently Asked Questions

**Q: Do I need programming skills?**
No. You only upload markdown files to your chosen AI platform and paste the prompt templates.

**Q: Which AI platform is recommended?**
ChatGPT Projects or Claude Projects provide persistent project context through project chats, files, and instructions, making them ideal for the full workflow. See [Platform Usage Map](docs/PLATFORM-USAGE-MAP.md) for details.

**Q: Can I use this for non-computer-science fields?**
Yes. The framework supports 10+ academic disciplines including Education, Psychology, Health, Business, Law, and Social Sciences. See [10-research-domain-adaptation.md](research-protocol/10-research-domain-adaptation.md).

**Q: Will AI write my entire thesis or paper?**
No. Research OS is explicitly designed to guard against that. It acts as an inquisitive, critical research collaborator that requires evidence and validates logic - you remain the author.
