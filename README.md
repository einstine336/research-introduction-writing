# Research Introduction Writing

A skill for building clear, persuasive research Introductions: explain how existing approaches work, identify a specific limitation, and connect that limitation to the proposed method.

Designed for research Introductions targeting CCF A conferences and SCI Q1 journals, with a focus on problem formulation, research motivation, and evidence-grounded argumentation.

## What it does

- **Study an Introduction.** Explain the role of each paragraph and how it leads to the research problem and method.
- **Strengthen the motivation.** Replace broad claims such as "insufficient interaction" with a concrete limitation and the conditions under which it matters.
- **Position the contribution.** Acknowledge what the closest prior work already achieves, then explain what remains unresolved.
- **Revise a draft.** Improve paragraph flow and connect design choices to the stated problem while preserving technical content, citations, and LaTeX.

## How it works

The skill helps build the connections between:

> Existing approach -> specific limitation -> supported explanation -> design principle -> method -> evidence

This is a reasoning guide, not a fixed paragraph template. The structure follows the research question, the actual method, and the available evidence.

## Installation

Clone this repository into your skills directory.

**macOS / Linux**

```bash
git clone https://github.com/einstine336/research-introduction-writing.git ~/.codex/skills/research-introduction-writing
```

**Windows PowerShell**

```powershell
git clone https://github.com/einstine336/research-introduction-writing.git "$env:USERPROFILE/.codex/skills/research-introduction-writing"
```

If you use a custom `CODEX_HOME`, place the repository under its `skills/` directory instead. For a project-specific installation, use `.agents/skills/research-introduction-writing/` in your project.

Restart your client after installation. No additional runtime dependencies are required.

## Usage

Invoke `$research-introduction-writing` and provide the text or research details you want to work on. Prompts and responses can be in English or Chinese.

**Analyze an example**

```text
Use $research-introduction-writing to analyze this Introduction paragraph by paragraph.
Explain how it moves from prior work to a specific limitation and then motivates the method.
```

**Improve a draft**

```text
Use $research-introduction-writing to revise my Introduction.
Strengthen the connection between prior-work limitations and our method.
Preserve the LaTeX structure and citation keys, and use only the evidence I provide.
```

**Develop the argument**

```text
Use $research-introduction-writing to help organize an Introduction from these notes.
I have included the task, closest prior approaches, method, and results.
Suggest an argument outline and draft the motivation paragraphs.
```

For drafting and revision, include the research task, closest prior approaches, actual method, and available observations or results. Missing evidence remains an open question rather than becoming an invented claim.

## Inside the skill

- [SKILL.md](SKILL.md): task selection, workflow, and writing constraints.
- [Pattern library](references/pattern-library.md): ways to connect limitations, explanations, and design choices.
- [Writing playbook](references/writing-playbook.md): practical revision moves and argument checks.

The skill loads supporting guidance as needed and adapts it to the requested task.
