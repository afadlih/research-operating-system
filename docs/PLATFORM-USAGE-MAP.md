# Platform Usage Map

Operational setup instructions for each supported AI platform.

---

## Quick Reference

| Platform | Recommended Minimum Upload | Best For | Role of AGENTS.md |
|---|---|---|---|
| **ChatGPT Projects** | `RESEARCH.md` + `CORE` + active modules + `PROJECT-CONTEXT.md` | Full research workflow (recommended) | Not needed (uses Project Instructions) |
| **ChatGPT (Regular)**| `RESEARCH.md` + `00-RESEARCH-CORE.md` + 1 active task module | Quick single-task sessions | Not needed (manual lightweight mode available) |
| **Gemini Gems** | `RESEARCH.md` + `CORE` + active modules + user papers | Knowledge-grounded sessions | Not needed |
| **Claude Projects** | `RESEARCH.md` + `CORE` + active modules + context | Deep analysis & chapter review | Optional (or use `CLAUDE.md` for Claude Code) |
| **NotebookLM** | User papers (PDFs) + `03-research-literature.md` | Source-grounded literature extraction | Not needed (strictly a literature tool) |
| **Coding Agents** | Platform instruction file (`AGENTS.md` / `CLAUDE.md` / Copilot repo instructions) + `research-protocol/` | Computational research in IDE | **Required when supported by agent** |

> **Universal Rule:** Upload only the modules relevant to your current task. Never upload all files at once without purpose.

---

## ChatGPT Projects (Recommended)

ChatGPT Projects is recommended for managing a complete research lifecycle with persistent project context through project chats, files, and instructions (distinct from permanent account-level memory).

### What to Upload to Project Files
- `research-protocol/RESEARCH.md` (the main router)
- `research-protocol/00-RESEARCH-CORE.md` (universal integrity rules)
- The specialized module for your current phase (e.g., `03-research-literature.md` or `04-research-methodology.md`)
- Your filled `PROJECT-CONTEXT.md` (copied from `09-project-context-template.md`)

*(Note: `AGENTS.md` is NOT required for ChatGPT Projects.)*

### Project Instructions (Copy-Paste)

Paste the following into your ChatGPT Project's **Instructions**:

```
You are a disciplined academic research collaborator operating under the Research Operating System framework.
Always consult research-protocol/RESEARCH.md as your router and enforce the rules in research-protocol/00-RESEARCH-CORE.md.
Never fabricate citations, invent benchmark results, or hallucinate empirical data.
If evidence is missing or a claim is unsupported, pause and ask for verifiable sources before continuing.
Follow the active module guidelines and require verification before declaring any task complete.
```

### First Prompt to Start Your Session

```
I have uploaded the Research Operating System protocol files along with my PROJECT-CONTEXT.md.
My research topic is: [Insert your topic].
My current task is: [e.g., Defining Research Gap / Designing Methodology].
Please confirm that you have loaded RESEARCH.md and 00-RESEARCH-CORE.md, review my project context, and outline the first verification step.
```

---

## ChatGPT (Regular Chat)

For quick, single-task consultations without creating a Project.

### Recommended Minimum Setup
- Attach `research-protocol/RESEARCH.md` (default beginner recommendation to provide routing)
- Attach `research-protocol/00-RESEARCH-CORE.md` (universal integrity rules)
- Attach the 1 module specific to your task (e.g., `03-research-literature.md`)
- Optional: `PROJECT-CONTEXT.md` when project-specific context materially matters to the answer.

> **Lightweight / Manual Mode Notice:** `RESEARCH.md` may be omitted only when the user manually selects the correct module and does not need router behavior. For beginners, the default recommendation is to include `RESEARCH.md`.

### First Prompt
```
I am attaching RESEARCH.md, 00-RESEARCH-CORE.md, and [Module Name].
Please act as a research collaborator for the following task: [Describe task].
Do not jump to writing. Ask clarifying questions on evidence and methodology first.
```

### Limitations
- **No persistent project context:** Context is session-only and does not carry over between chats.
- **Attachment limits:** Limited number of files per message.
- **Context drift:** In extended conversations, models may gradually forget early instructions.

---

## Gemini Gems

Gemini Gems allow you to create custom AI assistants with uploaded knowledge files.

### What to Upload to Knowledge
- `research-protocol/RESEARCH.md`
- `research-protocol/00-RESEARCH-CORE.md`
- Active specialized modules (e.g., `03-research-literature.md`, `04-research-methodology.md`)
- Your literature PDFs or notes

### Gem Instructions (Copy-Paste)

```
You are a research collaborator guided by the Research Operating System.
Use RESEARCH.md to route requests and strictly apply 00-RESEARCH-CORE.md to all responses.
Ground your reasoning in uploaded literature and verified evidence.
Clearly distinguish between established findings, conflicting evidence, and open gaps.
Never generate synthetic citations or claim statistical significance without verified data.
```

### First Prompt
```
I have initialized this Gem with Research OS protocols.
My research focus is: [Insert topic].
Let's begin by reviewing the core research questions and required evidence.
```

---

## Claude Projects

Claude Projects excel at long-context document analysis, multi-paper synthesis, and chapter-length reviews.

### What to Upload to Project Knowledge
- `research-protocol/RESEARCH.md`
- `research-protocol/00-RESEARCH-CORE.md`
- Active specialized modules
- Your `PROJECT-CONTEXT.md` and research drafts

### Role of `CLAUDE.md` vs `AGENTS.md`
- In Claude Projects (web interface), upload the protocol markdown files to Project Knowledge and set project instructions.
- If using **Claude Code** (CLI agent), use `CLAUDE.md` where appropriate pointing to `research-protocol/RESEARCH.md` (see [RESEARCH.md Section 21](../research-protocol/RESEARCH.md)).
- `research-protocol/AGENTS.md` serves as a generic template for coding agents that support it; adapt it to `CLAUDE.md` for Claude Code.

### Project Custom Instructions
```
Act as an academic research advisor under Research Operating System rules.
Follow RESEARCH.md and 00-RESEARCH-CORE.md.
Prioritize methodological rigor, threat detection, and calibrated claims.
Reject vague statements and highlight missing evidence.
```

---

## NotebookLM

NotebookLM is specifically designed for **source-grounded literature analysis** based on uploaded documents.

### What to Upload
- Your research papers (PDFs, downloaded articles)
- Your literature notes and summaries
- `research-protocol/03-research-literature.md` (as guidance for gap analysis)

### What NotebookLM Is Best For
- Extracting exact quotes and citations from uploaded papers.
- Cross-paper comparison and matrix generation.
- Identifying contradictions across source materials.

### Important Boundaries & Limitations
- **Strictly for source-grounded literature work:** NotebookLM answers only from uploaded sources.
- **Do not treat as a full experiment/repository agent:** It cannot plan experiments, write code, or route modular protocols.
- **Workflow:** Use NotebookLM for deep literature extraction, then take the extracted evidence matrices into ChatGPT Projects or Claude for methodology and writing.

---

## Coding Agents (Cursor, Windsurf, Claude Code, Antigravity, GitHub Copilot)

For computational research, experiment code, data pipelines, and reproducible benchmarks.

### Platform-Native Instruction Conventions
Use `AGENTS.md` when your coding agent supports the `AGENTS.md` convention. Otherwise, use the platform-native instruction file:
- **Claude Code:** Use `CLAUDE.md` where appropriate.
- **GitHub Copilot:** Use the instruction format supported by the active Copilot environment, such as repository instructions and `AGENTS.md` where supported.
- **Other coding agents (Cursor, Windsurf, Antigravity):** Follow the platform's native instruction-file convention.

`research-protocol/AGENTS.md` is provided as the generic integration template, but users may need to copy or adapt it into the format required by their chosen coding agent.

### Setup Steps
1. Place the adapted instruction file (e.g. `AGENTS.md` or `CLAUDE.md`) in the **root** of your research project repository:
   ```
   my-research-project/AGENTS.md
   ```
2. Place the `research-protocol/` directory inside your research repository:
   ```
   my-research-project/research-protocol/
   ```

### First Prompt to Coding Agent
```
Read your instruction file and research-protocol/00-RESEARCH-CORE.md.
We are implementing the experiment pipeline for: [Describe experiment].
Enforce zero data leakage, seed logging, baseline fairness, and reproducibility standards.
```

### Best For
- Experiment implementation with leak-prevention checks.
- Reproducible data processing pipelines.
- Traceable statistical analysis scripts.
