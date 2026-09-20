# User Guide (English)

A complete guide to setting up and using the Research Operating System with your AI platform.

---

## What You Need

- An AI platform account (ChatGPT, Gemini, Claude, or NotebookLM)
- The Research Operating System files (this repository)
- Your research topic or materials

No coding skills required.

---

## Step-by-Step Setup

### 1. Download This Repository

Click the green **Code** button on GitHub and select **Download ZIP**, or clone:

```bash
git clone https://github.com/afadlih/research-operating-system.git
```

### 2. Choose Your Platform

See the [Platform Usage Map](PLATFORM-USAGE-MAP.md) for detailed platform-specific instructions.

**Recommended:** ChatGPT Projects for the full workflow.

### 3. Upload the Core Files

Every research task requires at minimum:

1. `research-protocol/RESEARCH.md` — the main router
2. `research-protocol/00-RESEARCH-CORE.md` — universal research rules

### 4. Upload Task-Specific Modules

Based on your current task, add the relevant module(s):

| Your Task | Upload These Modules |
|---|---|
| Finding a research topic | `03-research-literature.md` |
| Literature review | `03-research-literature.md` + `01-research-writing.md` |
| Defining research questions | `04-research-methodology.md` |
| Designing methodology | `04-research-methodology.md` (+ `02-research-human.md` if involving people) |
| Running experiments | `04-research-methodology.md` + `05-research-experiment.md` |
| Analyzing results | `06-research-analysis.md` + `05-research-experiment.md` |
| Writing chapters | Relevant module + `01-research-writing.md` |
| Final audit | `07-research-audit.md` + all modules used |

### 5. Start With a Prompt

Use the Prompt Library ([English](../prompts/PROMPT-LIBRARY-EN.md) | [Indonesia](../prompts/PROMPT-LIBRARY-ID.md)) for ready-made prompts, or tell the AI:

```
I am starting a research project.
Use the Research Operating System.
Help me define:
- problem
- evidence needed
- feasibility
Do not jump directly to writing.
```

---

## Research Workflow

Follow this general order:

```
Problem → Research Question → Literature Evidence → Methodology
→ Data Collection → Experiment → Analysis → Writing → Final Audit
```

**Do not skip ahead.** Each stage builds on the previous one.

---

## Do's and Don'ts

### DO

- Always load `00-RESEARCH-CORE.md` for every task
- Load only the modules you need right now
- Follow the router's task routing table
- Verify claims with evidence before accepting them
- Run the final audit before declaring work complete

### DO NOT

- Upload all files at once without purpose
- Skip from problem definition straight to writing
- Accept AI output without checking evidence
- Let AI fabricate citations or results
- Treat AI suggestions as verified facts

---

## Common Mistakes

| Mistake | Why It's a Problem | What to Do Instead |
|---|---|---|
| Uploading all 14 files at once | Confuses the AI, wastes context | Upload only what your current task needs |
| Skipping literature review | Your research gap has no evidence basis | Build evidence first, then identify gaps |
| Accepting AI-generated citations | AI can fabricate authors, DOIs, and dates | Verify every citation against actual sources |
| Writing before methodology is solid | Your writing will need complete rewrites | Design methodology first, write second |
| Skipping the audit | Integrity issues go undetected | Always run `07-research-audit.md` at the end |

---

## Domain Support

The system works across 10+ research domains:

- Computer Science / AI
- Engineering
- Education
- Psychology
- Health / Medicine
- Business / Management
- Economics
- Social Science
- Law
- Humanities

See [10-research-domain-adaptation.md](../research-protocol/10-research-domain-adaptation.md) for domain-specific guidance.

---

## Need Help?

- [File Function Map](FILE-FUNCTION-MAP.md) — what each file does
- [Platform Usage Map](PLATFORM-USAGE-MAP.md) — platform setup details
- [Prompt Library (EN)](../prompts/PROMPT-LIBRARY-EN.md) — ready-to-use prompts
- [Pustaka Prompt (ID)](../prompts/PROMPT-LIBRARY-ID.md) — prompt siap pakai
- [RESEARCH.md](../research-protocol/RESEARCH.md) — the main router with full task routing table
