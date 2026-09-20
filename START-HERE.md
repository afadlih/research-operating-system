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

## Beginner Journey

Follow this recommended path from first start to verified research:

```
1. README.md                     -> High-level overview and philosophy
2. START-HERE.md                 -> 5-minute setup and project layout
3. Choose Language               -> English (docs/USER-GUIDE-EN.md) or Indonesia (docs/USER-GUIDE-ID.md)
4. Choose Platform               -> ChatGPT, Claude, Gemini, NotebookLM, or Coding Agents
5. Copy Files to Your Project    -> Set up my-research-project/ folder structure
6. Choose Current Task           -> Finding Topic, Literature, Methodology, Experiments, Writing
7. Upload Core + Active Module   -> Always 00-RESEARCH-CORE.md + the module for current task
8. Run Prompt Template           -> Pick prompt from prompts/PROMPT-LIBRARY-EN.md or ID
9. Verify & Audit                -> Run audit checks before accepting claims or drafting
```

---

## How to Organize Your Research Project

When working on a real thesis or research paper, create a dedicated project folder and copy the protocol files into it:

```
my-research-project/
|-- AGENTS.md                 # Optional: for coding agents (Cursor, Windsurf, Copilot)
|-- PROJECT-CONTEXT.md        # User-created: copied from 09-project-context-template.md
|-- research-protocol/        # Copied from Research OS
|   |-- RESEARCH.md           # Main router
|   |-- 00-RESEARCH-CORE.md   # Universal integrity rules (always required)
|   \-- [relevant-modules].md # Only the modules needed for your active phase
|-- literature/               # User-created: your PDFs, papers, synthesis matrices
|-- methodology/              # User-created: instruments, questionnaires, protocols
|-- experiments/              # User-created: code, notebooks, dataset splits
|-- analysis/                 # User-created: statistical scripts, outputs, tables
\-- manuscript/               # User-created: drafts, chapter notes, LaTeX/Word files
```

### Which files come from where?

- **From Research OS (copied):**
  - `research-protocol/` folder containing `RESEARCH.md`, `00-RESEARCH-CORE.md`, and any modules you plan to use.
  - `09-project-context-template.md` (fill this out and save as `PROJECT-CONTEXT.md`).
  - `AGENTS.md` (*optional* - only copy if you use IDE coding agents like Cursor or Windsurf).
- **Created by you:**
  - `PROJECT-CONTEXT.md` (filled with your research topic, questions, and parameters).
  - Your actual literature papers, data, scripts, and drafts.

---

## Step-by-Step Setup

### Step 1 - Choose Your Language

- **Bahasa Indonesia** - [docs/USER-GUIDE-ID.md](docs/USER-GUIDE-ID.md)
- **English** - [docs/USER-GUIDE-EN.md](docs/USER-GUIDE-EN.md)

### Step 2 - Understand the Router

Read [research-protocol/RESEARCH.md](research-protocol/RESEARCH.md) - this is the **main control router** that maps your current task to specific modules.

### Step 3 - Pick Modules for Your Stage

| Research Stage | Required Protocol Files |
|---|---|
| Finding a topic / problem | `CORE` + `03-research-literature.md` |
| Literature review & synthesis | `CORE` + `03-research-literature.md` + `01-research-writing.md` |
| Research question & gap | `CORE` + `03-research-literature.md` + `04-research-methodology.md` |
| Methodology design | `CORE` + `04-research-methodology.md` (+ `02-research-human.md` if human subjects) |
| Running experiments | `CORE` + `04-research-methodology.md` + `05-research-experiment.md` |
| Analyzing results | `CORE` + `06-research-analysis.md` + `05-research-experiment.md` |
| Writing chapters | `CORE` + active module + `01-research-writing.md` |
| Final audit | `CORE` + all modules used + `07-research-audit.md` |

### Step 4 - Upload to Your AI Platform

See [docs/PLATFORM-USAGE-MAP.md](docs/PLATFORM-USAGE-MAP.md) for exact copy-paste instructions for ChatGPT Projects, Claude, Gemini, NotebookLM, and Coding Agents.

### Step 5 - Use Ready-Made Prompts

Copy structured prompts from the Prompt Library:
- [English Prompt Library](prompts/PROMPT-LIBRARY-EN.md)
- [Pustaka Prompt Bahasa Indonesia](prompts/PROMPT-LIBRARY-ID.md)

---

## Important Rules

1. **Never upload all files at once.** Upload only what your current research phase requires.
2. **Always include `00-RESEARCH-CORE.md`.** It contains universal integrity rules and evidence discipline.
3. **Follow the research sequence:** Problem -> Evidence -> Method -> Experiment -> Analysis -> Writing -> Audit.
4. **Do not skip the audit phase.** It helps verify that your work meets integrity standards.
5. **AGENTS.md is for coding agents.** If you are using ChatGPT Projects, Claude Projects, or Gemini Gems, you do NOT need `AGENTS.md`.

---

## Frequently Asked Questions

**Q: Do I need programming skills?**
No. You only upload markdown files to your chosen AI platform and paste the prompt templates.

**Q: Which AI platform is recommended?**
ChatGPT Projects or Claude Projects provide persistent project memory and document upload, making them ideal for the full workflow. See [Platform Usage Map](docs/PLATFORM-USAGE-MAP.md) for details.

**Q: Can I use this for non-computer-science fields?**
Yes. The framework supports 10+ academic disciplines including Education, Psychology, Health, Business, Law, and Social Sciences. See [10-research-domain-adaptation.md](research-protocol/10-research-domain-adaptation.md).

**Q: Will AI write my entire thesis or paper?**
No. Research OS is explicitly designed to guard against that. It acts as an inquisitive, critical research collaborator that requires evidence and validates logic - you remain the author.
