# Platform Usage Map

Setup instructions for each supported AI platform.

---

## Quick Reference

| Platform | What to Upload | Best For |
|---|---|---|
| **ChatGPT Projects** | `AGENTS.md` + `RESEARCH.md` + needed modules | Full research workflow (recommended) |
| **ChatGPT (regular chat)** | `RESEARCH.md` + `00-RESEARCH-CORE.md` + needed module | Quick single-task research |
| **Gemini Gems** | `RESEARCH.md` + knowledge files | Knowledge-based research sessions |
| **Claude Projects** | `RESEARCH.md` + modules | Deep analysis and long-context tasks |
| **NotebookLM** | Papers + `03-research-literature.md` | Literature analysis and evidence extraction |
| **Coding Agents** | `AGENTS.md` | Computational research in IDE |

> **Rule:** Upload only the modules relevant to your current task. Do not upload everything at once.

---

## ChatGPT Projects (Recommended)

ChatGPT Projects is the recommended platform for the full research workflow.

### Setup

1. Create a new Project in ChatGPT.
2. Upload these files to the Project:
   - `research-protocol/AGENTS.md`
   - `research-protocol/RESEARCH.md`
   - `research-protocol/00-RESEARCH-CORE.md`
   - The specialized modules you need (see [File Function Map](FILE-FUNCTION-MAP.md))
   - Your `PROJECT-CONTEXT.md` (if you have one)
3. Set the Project Instructions to:

```
Use RESEARCH.md as the router.
Load modules based on the current task.
Do not fabricate evidence, citations, or results.
```

### Tips

- Start with CORE + one module, then add more as your research progresses.
- Upload your own papers/sources for literature review tasks.
- Use the Prompt Library ([EN](../prompts/PROMPT-LIBRARY-EN.md) | [ID](../prompts/PROMPT-LIBRARY-ID.md)) to get started.

---

## ChatGPT (Regular Chat)

For quick, single-task research without a full Project setup.

### Setup

1. Open a new chat.
2. Attach these files:
   - `research-protocol/RESEARCH.md`
   - `research-protocol/00-RESEARCH-CORE.md`
   - The module for your specific task
3. Tell ChatGPT what task you are working on.

### Limitations

- No persistent project context between chats.
- Fewer files can be attached compared to Projects.

---

## Gemini Gems

### Setup

1. Create a new Gem.
2. Upload the protocol files as knowledge.
3. Set the Gem instructions to reference `RESEARCH.md` as the router.

### Tips

- Gemini works well for knowledge-heavy tasks.
- Upload your research papers alongside the protocol files.

---

## Claude Projects

### Setup

1. Create a new Project in Claude.
2. Add protocol files to Project Knowledge.
3. Alternatively, create a `CLAUDE.md` file with the research protocol pointer from [RESEARCH.md Section 21](../research-protocol/RESEARCH.md).

### Tips

- Claude excels at long-context analysis.
- Good for reviewing entire thesis chapters.

---

## NotebookLM

### Setup

1. Create a new Notebook.
2. Upload your research papers as sources.
3. Upload `research-protocol/03-research-literature.md` for literature analysis guidance.

### Best For

- Literature analysis and evidence extraction.
- Comparing multiple papers.
- Building evidence matrices.

### Limitations

- Not ideal for the full research workflow.
- Use alongside another platform for methodology/experiment work.

---

## Coding Agents (Cursor, Windsurf, Antigravity, etc.)

### Setup

1. Place `research-protocol/AGENTS.md` in your project root or agent configuration.
2. The agent will follow research integrity rules when working on computational research tasks.

### Best For

- Experiment code that needs research discipline.
- Data processing scripts with traceability requirements.
- Computational reproducibility.
