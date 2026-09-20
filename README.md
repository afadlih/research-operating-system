# Research Operating System v1.0.0

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](CHANGELOG.md)

**A modular AI-powered research framework that turns AI into a disciplined research collaborator - not an answer generator.**

> Use AI to support real academic research: literature review, methodology design, experiment validation, analysis, and writing - with built-in evidence discipline and integrity checks.

---

## Table of Contents

- [What Is This?](#what-is-this)
- [Who Is This For?](#who-is-this-for)
- [How It Works](#how-it-works)
- [Beginner Journey](#beginner-journey)
- [Using in Your Research Project](#using-in-your-research-project)
- [Supported Platforms](#supported-platforms)
- [Repository Structure](#repository-structure)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

---

## What Is This?

Research Operating System (Research OS) is a collection of structured protocol files that you upload to AI platforms (ChatGPT, Gemini, Claude, etc.) to transform them into a **research-aware collaborator**.

It helps with:

- **Literature review** - source evaluation, evidence synthesis, gap identification
- **Research planning** - problem definition, research question formulation
- **Methodology design** - research design, variables, sampling, validity
- **Experiment validation** - leakage prevention, baseline fairness, reproducibility
- **Analysis** - statistical testing, uncertainty, interpretation boundaries
- **Academic writing** - evidence-based prose, terminology consistency, citation accuracy

### What It Is NOT

- It is NOT an automatic thesis generator
- It is NOT a tool that writes papers for you
- It is NOT a shortcut to skip real research work

### What It Maintains

- Evidence traceability
- Research integrity
- Verification discipline
- Reproducibility standards
- Calibrated claims (no overclaiming)

---

## Who Is This For?

| User | Use Case |
|---|---|
| **Undergraduate students** | Thesis/skripsi research with proper methodology |
| **Graduate students** | Systematic literature reviews, experiment design |
| **Researchers** | AI-assisted research with integrity guardrails |
| **Academic supervisors** | Audit and review student research quality |
| **Anyone using AI for research** | Reduce hallucination risk and catch unsupported claims |

---

## How It Works

![Research Operating System Workflow](assets/images/research-operating-system-workflow.png)

The system uses a **modular architecture**:

1. **Router** (`RESEARCH.md`) - determines which modules to load based on your task
2. **Core** (`00-RESEARCH-CORE.md`) - universal research integrity rules (always loaded)
3. **Specialized Modules** - loaded only when needed:
   - `01` Writing | `02` Human subjects | `03` Literature | `04` Methodology | `05` Experiment | `06` Analysis
4. **Support Files** - audit, decision log, project context template, domain adaptation, background generator

**Principle: load only what you need.** Never upload all files at once without purpose.

---

## Beginner Journey

Follow this recommended sequence from first discovery to verified research:

```
README
  -> START-HERE.md
    -> Choose Language (EN or ID)
      -> Choose Platform (ChatGPT, Claude, Gemini, NotebookLM, Coding Agents)
        -> Choose Research Task (Topic, Literature, Methodology, etc.)
          -> Upload Required Files (Router + CORE + Active Module)
            -> Use Prompt Template (from Prompt Library)
              -> Verify / Audit (before finalizing claims)
```

---

## Using in Your Research Project

To use Research OS in your thesis or paper repository, copy only the protocol files into your working project:

```
my-research-project/
|-- AGENTS.md                 # Optional: for coding agents (Cursor, Windsurf, Copilot)
|-- PROJECT-CONTEXT.md        # User-created: copied from 09-project-context-template.md
|-- research-protocol/        # Copied from Research OS
|   |-- RESEARCH.md           # Main router
|   |-- 00-RESEARCH-CORE.md   # Universal integrity rules (always required)
|   \-- [relevant-modules].md # Only the modules needed for your active phase
|-- literature/               # User-created: your papers, PDFs, notes, synthesis tables
|-- methodology/              # User-created: study design, instruments, sampling
|-- experiments/              # User-created: experiment code, notebooks, data runs
|-- analysis/                 # User-created: analysis scripts, tables, stats output
\-- manuscript/               # User-created: drafts, LaTeX / Word chapter files
```

**What you copy from this repository:**
- `research-protocol/` folder (or just `RESEARCH.md`, `00-RESEARCH-CORE.md`, and your active modules).
- `09-project-context-template.md` (fill out and save as `PROJECT-CONTEXT.md` in your project).
- `AGENTS.md` (optional, only if using IDE coding agents like Cursor or Windsurf).

**What you create yourself:**
- Your own research topic, research questions, data, literature papers, experiment code, and manuscript text.

---

## Supported Platforms

| Platform | What to Upload | Best For | Guide |
|---|---|---|---|
| **ChatGPT Projects** | `RESEARCH.md` + `CORE` + active modules + context | Full research workflow (recommended) | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |
| **ChatGPT (Regular)**| `CORE` + 1 active task module | Quick single-task sessions | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |
| **Gemini Gems** | `RESEARCH.md` + `CORE` + knowledge files | Knowledge-based research sessions | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |
| **Claude Projects** | `RESEARCH.md` + `CORE` + active modules | Deep analysis and long-context review | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |
| **NotebookLM** | Papers + `03-research-literature.md` | Source-grounded literature extraction | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |
| **Coding Agents** | `AGENTS.md` + `research-protocol/` | Computational research in IDE | [Platform Map](docs/PLATFORM-USAGE-MAP.md) |

> Note: `AGENTS.md` is specifically for IDE coding agents (Cursor, Windsurf, Copilot, Antigravity). Web AI platforms (ChatGPT Projects, Claude, Gemini) only need `RESEARCH.md`, `00-RESEARCH-CORE.md`, and the active modules.

---

## Repository Structure

```
research-operating-system/
|
|-- README.md                          # You are here
|-- START-HERE.md                      # Beginner onboarding guide
|-- LICENSE                            # MIT License
|-- CONTRIBUTING.md                    # How to contribute
|-- CHANGELOG.md                       # Version history
|
|-- docs/                              # User documentation
|   |-- USER-GUIDE-EN.md               # English user guide
|   |-- USER-GUIDE-ID.md               # Panduan pengguna (Indonesia)
|   |-- FILE-FUNCTION-MAP.md           # What each file does
|   \-- PLATFORM-USAGE-MAP.md         # Platform-specific setup
|
|-- prompts/                           # Ready-to-use prompt templates
|   |-- PROMPT-LIBRARY-EN.md          # Prompt collection (English)
|   \-- PROMPT-LIBRARY-ID.md          # Pustaka prompt (Indonesia)
|
|-- research-protocol/                 # Core protocol files
|   |-- RESEARCH.md                    # Main router (start here for research)
|   |-- AGENTS.md                      # AI agent configuration (optional for coding agents)
|   |-- 00-RESEARCH-CORE.md            # Universal research rules (always required)
|   |-- 01-research-writing.md         # Academic writing module
|   |-- 02-research-human.md           # Human subjects module
|   |-- 03-research-literature.md      # Literature review module
|   |-- 04-research-methodology.md     # Methodology design module
|   |-- 05-research-experiment.md      # Experiment validation module
|   |-- 06-research-analysis.md        # Analysis module
|   |-- 07-research-audit.md           # Final audit module
|   |-- 08-research-decision-log.md    # Decision tracking template
|   |-- 09-project-context-template.md # Template for PROJECT-CONTEXT.md
|   |-- 10-research-domain-adaptation.md # Multi-domain support
|   \-- 11-research-background-generator.md # Background section guide
|
\-- assets/
    \-- images/                        # Diagrams and visuals
```

---

## Documentation

| Document | Description |
|---|---|
| [START-HERE.md](START-HERE.md) | Beginner onboarding guide |
| [User Guide (EN)](docs/USER-GUIDE-EN.md) | English setup and usage |
| [Panduan Pengguna (ID)](docs/USER-GUIDE-ID.md) | Panduan Bahasa Indonesia |
| [File Function Map](docs/FILE-FUNCTION-MAP.md) | What each file does |
| [Platform Usage Map](docs/PLATFORM-USAGE-MAP.md) | Operational platform setup |
| [Prompt Library (EN)](prompts/PROMPT-LIBRARY-EN.md) | Ready-to-use prompts (English) |
| [Pustaka Prompt (ID)](prompts/PROMPT-LIBRARY-ID.md) | Prompt siap pakai (Indonesia) |
| [RESEARCH.md](research-protocol/RESEARCH.md) | Main research router |

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting.

---

## License

This project is licensed under the [MIT License](LICENSE).
