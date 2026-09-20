# User Guide (English)

A complete guide to setting up and using the Research Operating System with your AI platform.

---

## What You Need

- An AI platform account (ChatGPT, Gemini, Claude, or NotebookLM)
- The Research Operating System files (from this repository)
- Your research topic or project materials

No coding skills are required for standard research workflows.

---

## Quick Start (5 Steps)

### 1. Download or Clone This Repository

Download this repository as a ZIP, or clone it using Git:

```bash
git clone https://github.com/afadlih/research-operating-system.git
```

### 2. Choose Your Platform

See the [Platform Usage Map](PLATFORM-USAGE-MAP.md) for detailed platform-specific setup instructions.

- **Recommended for full research:** ChatGPT Projects or Claude Projects (provides persistent project context through project chats, files, and instructions).
- **Recommended for literature grounding:** NotebookLM.
- **Recommended for computational research:** Cursor, Windsurf, or Claude Code using the platform-native instruction file (`AGENTS.md` or `CLAUDE.md`).

### 3. Copy Protocol Files to Your Project

Create your research project folder and copy the protocol directory:

```
my-research-project/
|-- AGENTS.md                 # Optional: adapted for supported coding agents
|-- PROJECT-CONTEXT.md        # Copied & filled from 09-project-context-template.md
|-- research-protocol/        # Copied from this repo
|   |-- RESEARCH.md
|   |-- 00-RESEARCH-CORE.md
|   \-- [active-modules].md
\-- literature/               # Your sources, notes, and drafts
```

**What to copy:**
- `research-protocol/` folder containing `RESEARCH.md`, `00-RESEARCH-CORE.md`, and relevant modules.
- `09-project-context-template.md` (fill out and save as `PROJECT-CONTEXT.md`).
- `AGENTS.md` (optional - only when your coding agent supports it; otherwise adapt to platform-native files like `CLAUDE.md`).

**What you create:**
- `PROJECT-CONTEXT.md` (your research topic, questions, constraints, and parameters).
- Your actual literature papers, data, scripts, and drafts.

### 4. Upload Core + Task-Specific Module

Every session requires:
1. `research-protocol/RESEARCH.md` - the main router
2. `research-protocol/00-RESEARCH-CORE.md` - universal research rules

Add the module that matches your current phase in the Canonical Research Lifecycle:

| Lifecycle Stage | Upload These Modules |
|---|---|
| Problem Definition | `03-research-literature.md` |
| Evidence / Literature Review | `03-research-literature.md` + `01-research-writing.md` |
| Research Gap Identification | `03-research-literature.md` + `04-research-methodology.md` |
| Research Question Formulation | `04-research-methodology.md` |
| Methodology Design | `04-research-methodology.md` (+ `02-research-human.md` if human subjects) |
| Data / Experiment Execution | `04-research-methodology.md` + `05-research-experiment.md` |
| Statistical Analysis | `06-research-analysis.md` + `05-research-experiment.md` |
| Writing & Conclusion | Active module + `01-research-writing.md` |
| Final Audit | `07-research-audit.md` + all modules used |

*(Note on regular ChatGPT chat: RESEARCH.md may be omitted only when the user manually selects the correct module and does not need router behavior. Default recommendation includes RESEARCH.md.)*

### 5. Start With a Structured Prompt

Use the Prompt Library ([English](../prompts/PROMPT-LIBRARY-EN.md) | [Indonesia](../prompts/PROMPT-LIBRARY-ID.md)) for ready-made prompts, or tell the AI:

```
I am starting a research project using the Research Operating System.
I have loaded RESEARCH.md and 00-RESEARCH-CORE.md.
My topic is: [Insert Topic].
Help me define:
- problem statement
- evidence needed
- methodological feasibility
Do not jump directly to writing prose.
```

---

## Canonical Research Lifecycle

Follow this progressive order throughout your study:

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

## Do's and Don'ts

### DO

- Always load `00-RESEARCH-CORE.md` for every task.
- Load only the modules you need right now.
- Fill out `PROJECT-CONTEXT.md` so the AI understands your constraints.
- Verify claims against actual published papers before accepting them.
- Run the audit module (`07-research-audit.md`) before finalizing any chapter.

### DO NOT

- Upload all files at once without purpose.
- Skip from problem definition straight to writing manuscript prose.
- Accept AI output without checking evidence and source attribution.
- Allow AI to invent citations, benchmarks, or sample statistics.
- Treat AI suggestions as verified empirical facts.

---

## Research Integrity Disclaimer

Research OS supports research quality; **it does not guarantee it**.
It does not guarantee thesis acceptance, flawless methodology, or AI detector bypass. It provides verification-first guardrails to help researchers maintain academic integrity.

---

## Common Mistakes

| Mistake | Why It Causes Problems | Better Approach |
|---|---|---|
| Uploading all 14 protocol files | Overloads context window and degrades instruction following | Upload only `CORE` + `RESEARCH.md` + active module |
| Asking AI to write a thesis chapter first | Produces generic, unverified text with fake citations | Complete literature and methodology phases first |
| Relying on AI for literature citations | LLMs can hallucinate titles, authors, and DOIs | Upload real papers/PDFs or verify in Google Scholar/Scopus |
| Using `AGENTS.md` in ChatGPT web | Adds redundant coding instructions to a non-coding chat | Use `RESEARCH.md` + `CORE` for ChatGPT web |
| Skipping the audit check | Leaves unaddressed confounding variables or methodology gaps | Run `07-research-audit.md` before submission |

---

## Next Steps

- [START-HERE.md](../START-HERE.md) - quick onboarding overview
- [Platform Usage Map](PLATFORM-USAGE-MAP.md) - platform-specific copy-paste guides
- [File Function Map](FILE-FUNCTION-MAP.md) - detailed index of every file
- [Prompt Library (EN)](../prompts/PROMPT-LIBRARY-EN.md) - 16 categorized prompts
- [RESEARCH.md](../research-protocol/RESEARCH.md) - the main router with full routing table
