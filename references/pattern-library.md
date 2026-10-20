# Argument Patterns for Computer Science Introductions

Choose the reasoning move that the current draft needs. The examples below are hypothetical computer science writing exercises, not summaries of particular studies or empirical findings. The manuscript's technical claims require its own evidence and verified citations.

## Selection guide

| Pattern | Use when | Main question |
| --- | --- | --- |
| A task requirement becomes a research question | Existing formulations do not cover a meaningful need or condition | What must the system do, and what changes relative to the closest formulation? |
| A natural alternative has a relevant cost | An obvious solution works under assumptions or resources that matter to the study | Which cost or dependency motivates another approach? |
| A computation relies on a changed assumption | A familiar operation is used with different representations or input conditions | What makes this operation appropriate, and which condition has changed? |
| Aggregate results conceal a difficult condition | A meaningful input group behaves differently | Why does this condition matter, and what does the evidence actually establish? |
| Auxiliary information requires task relevance | Extra features or supervision do not have the same value for every target decision | What should be selected, weighted, or shared? |
| Learning shifts component responsibilities | The learned behavior differs from intended roles | Which objective or information path permits the mismatch? |
| The closest solution leaves a joint requirement | Prior work already solves part of the broad problem | What additional constraint must be satisfied at the same time? |
| Richer interaction must preserve useful structure | An integration step may disrupt information the task still needs | What should the operation add, and what should it preserve? |

## A task requirement becomes a research question

**Argument move.** Narrow the application to a concrete prediction, retrieval, generation, or decision requirement. Explain what existing task formulations assume or optimize. Identify the changed input, available information, output requirement, or constraint, and show why it creates a meaningful question.

**Hypothetical example.** A retrieval setting supplies complete queries during evaluation, while a target application receives partially specified queries. Explain what information is absent and what a useful retrieval result should satisfy. Check whether existing partial-query or robustness formulations already cover the setting before calling it a new task.

**Writing decisions.** A new task needs a substantive formulation difference. A difficult condition within an existing task can be framed as a newly studied challenge without renaming the task. A phenomenon worth understanding can be established before diagnosing a method.

**Evidence boundary.** Use supplied use cases, observations, definitions, or verified literature. Do not invent real-world prevalence, claim the setting is unprecedented without checking the closest work, or substitute a new module name for a research question.

## A natural alternative has a relevant cost

**Argument move.** Explain the direct solution a reader would reasonably consider. Acknowledge what it achieves, identify its relevant measured cost or dependency, and distinguish necessary computation from avoidable repetition. Derive the efficiency or process requirement before describing the implementation.

**Hypothetical example.** A retrieval service can rebuild its entire index after each data update. If measurements show that only a small portion changes, the motivation can concern selective recomputation while preserving the required retrieval behavior.

**Writing decisions.** Specify whether the cost concerns training, inference, preprocessing, memory, latency, or supervision. Connect the proposed change to the particular cost under discussion.

**Evidence boundary.** Reduced FLOPs do not establish reduced wall-clock latency; lower resource use does not establish equal quality. State the operating conditions and tradeoff supported by the available results.

## A computation relies on a changed assumption

**Argument move.** Explain why an established operation is appropriate in its original setting. Identify the representations it consumes, the assumption behind the operation, and the condition that changes. Locate the proposed intervention at the affected computation.

**Hypothetical example.** A retrieval score compares embeddings produced by separately adapted encoders. If observations suggest that their scales or geometry differ, explain why this matters for the comparison and which representation or scoring operation is being adjusted.

**Writing decisions.** Name the objects and the operation before using labels such as mismatch, incompatibility, or misalignment. Distinguish an observed distribution difference from evidence that it harms the target computation.

**Evidence boundary.** A plausible dependency supports a hypothesis. Do not claim that attention, similarity comparison, or another method family universally fails under heterogeneous inputs.

## Aggregate results conceal a difficult condition

**Argument move.** Introduce a concrete input condition, explain why the intended task must handle it, and use available subgroup evidence to establish the observed difficulty. Investigate a possible mechanism separately before motivating a design.

**Hypothetical example.** An image classifier's overall score can conceal weaker performance on heavily compressed images. A visible example explains the input condition; a relevant subgroup evaluation measures its effect. Neither alone establishes whether the cause lies in the representation, training distribution, or decision rule.

**Writing decisions.** Explain why these cases should be solved rather than silently removed when they belong to the intended task. Keep the problem definition, subgroup construction, and proposed explanation distinct.

**Evidence boundary.** Do not invent subgroup results or treat a selected example as prevalence evidence. Use the evaluations already supplied; a prose revision does not automatically authorize a new experiment campaign.

## Auxiliary information requires task relevance

**Argument move.** Explain how an auxiliary task, feature stream, or supervision signal relates to the target objective. Discuss the direct sharing strategy and any observed condition under which it is insufficient. Derive a selection, weighting, or integration principle from the target task's needs.

**Hypothetical example.** An auxiliary classification objective may help a retrieval encoder, while also favoring features that distinguish training categories without improving ranking for the intended queries. If supported by observations, motivate target-aware use of the auxiliary signal.

**Writing decisions.** Separate availability of information from usefulness to the target decision. Explain what an actual filtering or weighting operation changes before naming its module.

**Evidence boundary.** Related tasks do not imply universal positive transfer. Do not claim negative interference, gradient conflict, or the necessity of filtering without relevant evidence or an explicitly stated hypothesis.

## Learning shifts component responsibilities

**Argument move.** Describe each component's intended role. Identify observations suggesting a different learned behavior, explain which objective or information path could permit it, and derive an intervention. If another design addresses a residual difficulty, make that dependency explicit.

**Hypothetical example.** A shared encoder is intended to capture stable content, while another component represents acquisition-specific variation. If analysis shows acquisition artifacts entering the shared features, the motivation can address that leakage and the training conditions that permit it.

**Writing decisions.** Explain why the first change may leave a relevant problem before introducing a genuinely dependent second change. Parallel components should receive parallel motivations.

**Evidence boundary.** Intended roles and module names do not establish learned behavior. An ablation showing a score improvement does not by itself prove that the claimed information separation occurred.

## The closest solution leaves a joint requirement

**Argument move.** Introduce a broad difficulty, acknowledge the closest solution that already addresses it, and identify its remaining assumption or dependency. Formulate the requirement that must be satisfied alongside the capability already achieved.

**Hypothetical example.** A document classifier needs local evidence that global pooling may suppress. A recent method already models local passages but assumes reliable external segmentation. If that assumption matters in the target setting, motivate local evidence modeling under uncertain segmentation rather than claiming that local modeling is absent.

**Writing decisions.** Compare method properties with the relevant alternatives: what capability is retained, which dependency changes, and what evidence supports the difference. Granularity and pipeline dependencies can be separate constraints.

**Evidence boundary.** Verify that the closest work has the stated dependency. Do not ignore a relevant counterexample, generalize a conditional limitation into a universal weakness, or assume that an end-to-end implementation eliminates every error source.

## Richer interaction must preserve useful structure

**Argument move.** Explain what a new interaction should add and which relationships or capabilities must remain useful. Describe the possible conflict at the level supported by evidence, then introduce the actual mechanism that balances these requirements.

**Hypothetical example.** A graph prediction model adds global context to local node features. If analysis suggests that this integration blurs distinctions needed by the prediction target, motivate an interaction rule that retains those distinctions while using context.

**Writing decisions.** More interaction is not a sufficient objective by itself. Identify the structure to preserve, why the task needs it, and where the actual design acts. Explain cooperative components through their information roles.

**Evidence boundary.** A preservation loss or architectural branch states an intention, not a demonstrated effect. Do not borrow a specific structural explanation from a writing example and present it as a finding about the current method.

## Combining patterns

- A task-first route can establish the need before inspecting the mechanisms that make it difficult.
- A mechanism-first route can reveal a precise research question by examining an existing operation.
- Use the closest-solution pattern whenever a relevant method already resolves part of the apparent gap.
- Use examples, subgroup results, and controlled comparisons for their distinct evidential roles.
- Choose a small relevant set of moves. Adapt their order to the actual study and implementation.
