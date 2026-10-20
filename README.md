# Computer Science Introduction Writing

A skill for analyzing, drafting, and revising research Introductions in computer science, with a focus on machine learning, computer vision, natural language processing, multimodal learning, information retrieval, and data mining.

Designed for research Introductions targeting CCF A conferences and SCI Q1 journals. It helps establish a meaningful research question, explain the closest prior approaches, and connect computational mechanisms to design choices and evidence.

## What it does

- **Study an Introduction.** Explain how the background narrows to a research object and how each paragraph motivates the next question or design.
- **Frame the contribution.** Distinguish a new task or setting, a newly characterized challenge, a method improvement, and an efficiency or process improvement.
- **Strengthen the motivation.** Locate the issue in representations, interaction granularity, training objectives, generalization conditions, inference dependencies, or computational cost.
- **Position the contribution.** Acknowledge what the closest prior work already achieves, then explain what remains unresolved.
- **Revise a draft.** Improve paragraph flow and connect design choices to the stated problem while preserving technical content, citations, and LaTeX.

## How it works

The skill supports both task-first and mechanism-first arguments. A task-first Introduction establishes an unmet requirement or meaningful condition before examining existing solutions. A mechanism-first Introduction inspects an established operation to derive a precise research question.

Both routes connect:

> Task requirement -> existing capability -> concrete difficulty -> supported explanation or hypothesis -> design principle -> method -> evidence

The structure follows the research question, actual implementation, and available evidence. For systems, security, software engineering, or theory papers, the guidance adapts to their research objects and assumptions.

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
I have included the task setting, closest prior approaches, method, and results.
Help me choose a problem framing, suggest an argument outline, and draft the motivation paragraphs.
```

For drafting and revision, include the inputs and outputs, available information and constraints, closest prior approaches, actual method, and available observations or results. Missing evidence remains an open question rather than becoming an invented claim.

## Inside the skill

- [SKILL.md](SKILL.md): task selection, workflow, and writing constraints.
- [Pattern library](references/pattern-library.md): computer science examples for problem framing and method motivation.
- [Writing playbook](references/writing-playbook.md): contribution framing, computational anchors, paragraph development, and evidence checks.

The skill loads supporting guidance as needed and adapts it to the requested task.
