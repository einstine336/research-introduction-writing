# Writing Playbook

## Identify argument functions

For a supplied Introduction, record what each relevant passage contributes:

| Location | New understanding | What it builds on | Why the next step follows | Evidence type |
| --- | --- | --- | --- | --- |
| Actual section, page, or paragraph | A concise statement | Prior facts, citations, or observations | The next question or design requirement | Definition, illustration, result, hypothesis, or method description |

Use this table for passage-level learning requests. During direct revision, the analysis can remain internal while the deliverable is coherent prose.

## Develop a concrete limitation

The examples below are hypothetical revision exercises. Adapt the reasoning to the actual task and do not treat the examples as established results.

### Locate the operation

Broad claim: existing methods cannot model the relationships sufficiently.

Ask which objects are compared, what makes the comparison meaningful, and which condition changes. Explain how that change could affect the operation. For example, comparisons between measurements may depend on consistent calibration. Use the changed-assumption pattern when that dependency is supported.

### Define the relevant granularity

Broad claim: existing methods lack fine-grained modeling.

Identify the unit of prediction, the unit of interaction, and why any difference matters. Check whether the closest work already addresses the issue. If it does, examine its remaining task-specific assumptions rather than repeating the broad gap.

### Explain auxiliary relevance

Broad claim: related information needs more complete integration.

Specify what the additional information contributes to the target decision, when it is relevant, and what observations support a concern about its use. Then explain the actual selection or integration operation. More information alone does not establish a need for more interaction.

### Explain component roles

Broad claim: the method adds components to address overfitting.

State the intended responsibilities, the observations suggesting a mismatch, and how each change addresses it. Describe a sequential relationship only if the later operation depends on the earlier one.

## Examine a natural alternative

When an obvious alternative directly addresses the research question, use concrete facts to explain:

- What it already achieves.
- Its additional assumptions, resources, or preprocessing.
- Which observed cost or remaining difficulty matters for the current goal.
- How the actual design addresses that difficulty.

Without relevant experiments or verified literature, discuss conditions and research questions rather than inventing a failed baseline. A writing request does not automatically require new experiments.

## Match explanations to evidence

| Available material | Supported writing move | Unwarranted upgrade |
| --- | --- | --- |
| An illustrative example | Explain a phenomenon and its implications | Claim it is universal across the data |
| A subgroup performance gap | Report a difference under the stated conditions | Declare a mechanism the sole proven cause |
| An association between a factor and a benefit | Propose or support a related explanation | State a general causal law |
| A component ablation | Describe its task contribution in the tested configuration | Claim every implied mechanism has been validated |
| A method's architecture | Explain operations and design purposes | Guarantee performance, robustness, or optimality |

## Connect the limitation to the design

Work through the connections that the current material supports:

1. Describe how the closest relevant approach operates.
2. State the condition under which its behavior becomes a concern.
3. Locate the operation or dependency involved.
4. Distinguish the observation from the proposed explanation.
5. State the design requirement in plain language.
6. Explain how the actual method implements it.
7. Limit the outcome claim to the available evidence.

This is a diagnostic sequence, not a mandatory paragraph order. A missing link may require clarification or a narrower claim rather than another module or experiment.

## Describe relationships between designs

- **Parallel complementarity:** Operations address related but distinct difficulties. Explain their roles and where their outputs meet.
- **Sequential processing:** A later operation addresses a difficulty that remains after an earlier one. Describe the actual dependency.
- **Collaborative preservation:** A primary operation enables change while another mechanism preserves a required capability. Explain both requirements and the evidence for their interaction.

Choose the relationship that matches the implementation. Do not change component identities, ordering, or responsibilities to imitate a narrative.

## Check the revised argument

- Can the reader understand what makes the prior approach work?
- Is the limitation tied to clear conditions and an accurate account of the closest prior work?
- Does evidence support the explanation, or is it clearly a hypothesis?
- Does the method act on the previously identified difficulty?
- Do relationships between components match the implementation?
- Do result and contribution claims reflect evidence already obtained?
- Is importance repeatedly asserted, the same distinction overexplained, or limited prior attention used in place of a concrete rationale?

Use clear scientific subjects and actions. Preserve necessary uncertainty and actual limitations. Avoid repetitive disclaimers and unsupported claims of priority or guarantees.
