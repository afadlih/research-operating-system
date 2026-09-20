# Start Here

Welcome! This guide will help you set up the Research Operating System in under 5 minutes.

---

## What Is Research OS?

Research OS is a set of **instruction files** that you upload to AI platforms (ChatGPT, Gemini, Claude, etc.) to make them follow proper research methodology.

Instead of AI giving you generic answers, it will:

- Ask for evidence before making claims
- Follow structured research workflows
- Flag unsupported conclusions
- Maintain academic integrity

**It does NOT write your thesis for you.** It helps you do research properly with AI assistance.

---

## Setup Steps

### Step 1 — Read the README

Read [README.md](README.md) to understand what the system does and how it is structured.

### Step 2 — Choose Your Language

Pick the user guide for your preferred language:

- **Bahasa Indonesia** — [docs/USER-GUIDE-ID.md](docs/USER-GUIDE-ID.md)
- **English** — [docs/USER-GUIDE-EN.md](docs/USER-GUIDE-EN.md)

### Step 3 — Understand the Router

Read [research-protocol/RESEARCH.md](research-protocol/RESEARCH.md) — this is the **main control file** that decides which modules to use for each task.

### Step 4 — Pick Your Workflow

Choose the workflow that matches your current research stage:

| Stage | What You Need |
|---|---|
| Finding a topic | CORE + LITERATURE |
| Literature review | CORE + LITERATURE + WRITING |
| Research question and gap | CORE + LITERATURE + METHODOLOGY |
| Methodology design | CORE + METHODOLOGY (+ HUMAN if applicable) |
| Running experiments | CORE + METHODOLOGY + EXPERIMENT |
| Analyzing results | CORE + ANALYSIS + EXPERIMENT |
| Writing chapters | CORE + relevant module + WRITING |
| Final audit | CORE + ALL modules used |

### Step 5 — Upload to Your AI Platform

See [docs/PLATFORM-USAGE-MAP.md](docs/PLATFORM-USAGE-MAP.md) for platform-specific upload instructions.

### Step 6 — Use Prompt Templates

Use ready-made prompts from the Prompt Library ([English](prompts/PROMPT-LIBRARY-EN.md) | [Indonesia](prompts/PROMPT-LIBRARY-ID.md)) to get started quickly.

---

## Important Rules

1. **Never load every file at once** without a specific purpose. Load only what your current task needs.
2. **Always load `00-RESEARCH-CORE.md`** — it contains the universal research integrity rules.
3. **Follow the workflow order:** Router → Module → Task → Audit.
4. **Do not skip the audit phase.** It ensures your research meets integrity standards.

---

## Common Questions

**Q: Do I need coding skills?**
No. You just upload files to your AI platform and use the prompts.

**Q: Which AI platform is best?**
ChatGPT Projects is recommended for the full workflow. See the [Platform Usage Map](docs/PLATFORM-USAGE-MAP.md) for details.

**Q: Can I use this for non-CS research?**
Yes! The system supports 10+ research domains. See [10-research-domain-adaptation.md](research-protocol/10-research-domain-adaptation.md).

**Q: Will AI write my entire thesis?**
No. Research OS prevents that. It helps you think and research — not skip the work.
