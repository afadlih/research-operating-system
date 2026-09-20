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

- **Recommended for full research:** ChatGPT Projects or Claude Projects.
- **Recommended for literature grounding:** NotebookLM.
- **Recommended for computational research:** Cursor, Windsurf, or Claude Code using `AGENTS.md`.

### 3. Copy Protocol Files to Your Project

Create your research project folder and copy the protocol directory:

```
my-research-project/
|-- PROJECT-CONTEXT.md        # Copied & filled from 09-project-context-template.md
|-- research-protocol/        # Copied from this repo
|   |-- RESEARCH.md
|   |-- 00-RESEARCH-CORE.md
|   \-- [active-modules].md
\-- literature/               # Your sources, notes, and drafts
```

### 4. Upload Core + Task-Specific Module

Every session requires:
1. `research-protocol/RESEARCH.md` - the main router
2. `research-protocol/00-RESEARCH-CORE.md` - universal research rules

Add the module that matches your current phase:

| Your Task | Upload These Modules |
|---|---|
| Finding a research topic | `03-research-literature.md` |
| Literature review | `03-research-literature.md` + `01-research-writing.md` |
| Defining research questions | `04-research-methodology.md` |
| Designing methodology | `04-research-methodology.md` (+ `02-research-human.md` if human subjects) |
| Running experiments | `04-research-methodology.md` + `05-research-experiment.md` |
| Analyzing results | `06-research-analysis.md` + `05-research-experiment.md` |
| Writing chapters | Active module + `01-research-writing.md` |
| Final audit | `07-research-audit.md` + all modules used |

*(Note: `AGENTS.md` is only needed if you are using IDE coding agents like Cursor or Windsurf.)*

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

## Research Workflow Lifecycle

Follow this progressive order throughout your study:

```
Problem Definition -> Research Questions -> Literature Evidence -> Methodology Design
-> Data Collection -> Experiment Validation -> Statistical Analysis -> Academic Writing -> Final Audit
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

## Common Mistakes

| Mistake | Why It Causes Problems | Better Approach |
|---|---|---|
| Uploading all 14 protocol files | Overloads context window and degrades instruction following | Upload only `CORE` + active module |
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
