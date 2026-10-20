# Introduction Argument Patterns

Use these patterns to choose the reasoning move that a draft needs. Examples are hypothetical writing exercises, not findings or summaries of particular studies. Support the manuscript's technical statements with its own evidence and verified citations.

## Selection guide

| Pattern | Use when | Main question |
| --- | --- | --- |
| Cost of a natural alternative | An obvious solution is relevant but has a documented practical cost | Which part of the cost is necessary, and which might be avoided? |
| A changed assumption | A successful mechanism is used under different conditions | Which operation relies on an assumption that no longer holds? |
| Difficult cases hidden by averages | Overall performance conceals meaningful variation | What happens under the conditions that matter for the task? |
| Relevance of auxiliary information | Extra information helps only under certain conditions | Which information should influence the target decision? |
| Component responsibilities | Learned components do not serve their intended roles | What is each component expected to represent or preserve? |
| Remaining constraints in the closest work | A recent method already addresses the broad gap | What important requirement remains unmet? |
| Interaction with preservation | A new operation must preserve an existing capability | What should change, and what must remain available? |

## Cost of a natural alternative

### Argument move

Establish the task requirement, introduce the most direct solution, and explain its demonstrated resource or process cost. Distinguish necessary work from avoidable repetition. Derive the proposed efficiency principle from that distinction before introducing the implementation.

### Hypothetical example

A system could rerun a full analysis after every small input update. If measurements show that most intermediate outputs remain valid, the motivation can focus on detecting which work must be repeated.

### Evidence and boundaries

Quantify the relevant cost when measurements exist. Explain assumptions and tradeoffs when they do not. Do not infer equivalent output quality from lower cost or claim that the obvious alternative has failed without a comparison.

## A changed assumption

### Argument move

Acknowledge why the mechanism works in its established setting. Identify a condition that changes, locate the operation affected by that change, and explain the consequence at the level supported by evidence. State the requirement for adapting the operation.

### Hypothetical example

A comparison rule may assume measurements use a common scale. If a new setting combines differently calibrated instruments, discuss the calibration assumption before motivating a normalization procedure.

### Evidence and boundaries

A plausible dependency supports a hypothesis, not automatic proof. Avoid declaring a family of methods universally ineffective because one assumption changes in a particular setting.

## Difficult cases hidden by averages

### Argument move

Introduce an observable case that the aggregate result does not explain. Establish why it matters to the task. Use subgroup measurements, if available, to assess its extent. Separate that observation from the proposed mechanism and explain how the design investigates or addresses it.

### Hypothetical example

An average error rate may conceal substantially higher errors on inputs with incomplete measurements. A concrete case explains the failure condition; a subgroup comparison measures the difference.

### Evidence and boundaries

Do not treat an example as prevalence evidence or a subgroup gap as proof of a unique cause. Define the subgroup using meaningful task conditions and preserve the uncertainty in the explanation.

## Relevance of auxiliary information

### Argument move

Explain what the additional information could contribute to the target decision. Identify when it is useful and what irrelevant variation it may also introduce. Motivate selection, weighting, or integration according to observed needs and the actual implementation.

### Hypothetical example

Historical records can inform a forecast, but records collected under a different operating regime may be less relevant. Explain the regime difference before introducing a relevance-based weighting rule.

### Evidence and boundaries

Related information is not necessarily beneficial in every case. Do not invent negative transfer or claim that filtering is required when the material only establishes uncertainty about relevance.

## Component responsibilities

### Argument move

Describe the intended role of each component, identify observations suggesting a role mismatch, and connect the proposed change to that mismatch. If a later step handles a remaining difficulty, explain the actual dependency.

### Hypothetical example

A shared representation is intended to capture stable information, while another component models temporary variation. If analysis shows that short-lived signals dominate the shared representation, use that observation to motivate a separation constraint.

### Evidence and boundaries

Component names do not establish what was learned. Responsibilities must match the information paths and training procedure. Do not invent the failure of an intermediate design to create a sequential narrative.

## Remaining constraints in the closest work

### Argument move

Begin with the closest relevant method's actual achievement. Explain its assumptions, dependencies, or remaining limitations under the current task conditions. Derive the requirement that distinguishes the proposed work.

### Hypothetical example

A recent approach already handles variable input sizes but requires manually specified operating boundaries. A new study can target variable inputs under automatically estimated boundaries without claiming that variable-size processing itself is unaddressed.

### Evidence and boundaries

Verify that the cited method has the stated requirement. Distinguish an unmet task need from a general weakness. Discuss the strongest relevant counterexample rather than a convenient weaker baseline.

## Interaction with preservation

### Argument move

Explain the benefit sought from a new operation and the existing capability that must remain available. Describe the potential conflict only to the extent supported by observations or a clearly stated hypothesis. Introduce the actual mechanism used to balance those requirements.

### Hypothetical example

An update may improve adaptation to recent inputs while reducing consistency on an established workload. If evaluations establish this tradeoff, motivate an update procedure that also preserves relevant earlier behavior.

### Evidence and boundaries

A preservation objective does not prove preservation. Report the relevant evaluations when available and avoid guarantees based only on the architecture.

## Combining patterns

- Use the closest-work pattern to establish what remains unresolved before explaining a changed assumption.
- Use difficult-case analysis to distinguish the observed problem from its possible mechanism.
- Combine auxiliary-information reasoning with component responsibilities only when the actual system supports that relationship.
- Explain parallel, sequential, or collaborative designs according to the implementation.
- Choose the patterns needed by the draft rather than applying the entire library.
