# Computer Science Introduction Writing Playbook

## Choose the contribution framing

Use the user's facts to identify the main contribution. Multiple framings may coexist, but the Introduction should make their relationship clear.

| Framing | Establish before introducing the method | Common overstatement |
| --- | --- | --- |
| New task or problem setting | Inputs, outputs, available information, constraints, practical need, and a substantive difference from the closest formulations | A new architecture is treated as a new task |
| Newly characterized challenge or explanation | A meaningful condition or observation, what existing accounts miss, and the evidence supporting the new question or explanation | A known performance issue is renamed and claimed as unprecedented |
| Method or mechanism improvement | How the closest method operates, where it becomes limited, and the design requirement that follows | Generic claims of insufficient modeling justify arbitrary modules |
| Efficiency or process improvement | The required quality, operating conditions, and resource or dependency being changed | Fewer parameters or FLOPs are presented as proof of faster deployment |

For a new setting, establish why the problem definition matters before discussing a solution. For an existing task, a precise condition or mechanism can provide a strong contribution without claiming a new task. Reserve priority claims for verified comparisons with relevant literature.

## Locate the computer science problem

Select the anchors relevant to the paper; do not turn this table into a mandatory checklist.

| Anchor | Questions to resolve from the material |
| --- | --- |
| Task formulation | What are the inputs and required outputs? What supervision, side information, or constraints differ from existing settings? |
| Representation | What information must be encoded? Which invariance or distinction does the target decision require? |
| Interaction and granularity | What units interact? Do their scale, comparability, or information paths match the prediction target? |
| Objective and optimization | What does the training objective encourage? How does that relate to intended component roles and test-time needs? |
| Generalization and adaptation | Which input conditions, categories, domains, or available signals change between training and evaluation? |
| Inference and preprocessing | Which intermediate predictions, candidate sets, or external tools does the method depend on? |
| Resources | Where do computation, memory, latency, data, or annotation costs arise, and under which conditions? |

For other computer science areas, use the actual research objects: workloads and consistency requirements in systems, adversary capabilities in security, program behaviors in software engineering, or assumptions and guarantees in theory. Do not force these studies into representation-learning language.

## Study paragraph functions

For a supplied Introduction, record what each relevant passage contributes:

| Location | New understanding | What it builds on | Why the next step follows | Evidence type |
| --- | --- | --- | --- | --- |
| Actual section, page, or paragraph | A concise statement | Prior facts, citations, or observations | The next question or design requirement | Definition, illustration, measurement, hypothesis, or method description |

Inspect how the opening narrows to the research object. Identify the point where the writing shifts from task need to existing mechanisms, from an observed difficulty to an explanation, and from that explanation to a design principle.

Show the table when the user asks to learn paragraph by paragraph. For direct revision, perform the analysis internally and deliver connected prose.

## Develop the argument

### Establish a focused task need

Define the task and the capability needed to perform it. Use an application example only when it clarifies the later question. Narrow the background to the relevant input, prediction target, or operating condition.

For a proposed new setting, state what changes in the formulation and why existing objectives or assumptions do not already express the need. For a difficult condition within an existing task, explain why the task should handle that condition.

### Explain prior capability before its limit

Group relevant work by the operation or assumption needed for the argument. Describe what it does well. Introduce the strongest relevant counterexample before asserting what remains unresolved.

A citation list is not an explanation of how prior methods work. Broad claims such as all existing methods overlook this require support that a small set of examples cannot provide.

### Make the difficulty inspectable

Replace vague limitations with concrete relationships when the material supports them:

- **Insufficient fusion:** Identify the interacting representations, what information should pass between them, and the condition under which the operation is inadequate.
- **Weak generalization:** State what changes between training and evaluation, which behavior is observed, and what explanation remains hypothetical.
- **Missing fine-grained modeling:** Name the prediction and interaction units. Check whether the closest work already models the required unit and what assumption remains.
- **High computational cost:** Locate the cost in training, inference, data processing, or annotation. Use the relevant measurements rather than an unrelated proxy.
- **Limited prior attention:** Explain the unmet task requirement and its significance; lack of attention alone does not establish the problem.

### Examine the natural alternative

When a direct solution bears on the question, explain what it achieves and which actual cost, assumption, or remaining difficulty matters. Use existing comparisons if available. Without them, discuss the limitation as an assumption or open question rather than inventing a failed baseline.

### Separate observation, explanation, and design

Name the observed condition first, then explain the proposed dependency at the appropriate confidence level. State a design requirement before method names and implementation details.

A useful progression is:

> Task requirement -> existing capability -> concrete difficulty -> supported explanation or hypothesis -> design requirement -> actual operation -> evidence.

A task-first narrative can establish a new question before analyzing methods. A mechanism-first narrative can derive the question by inspecting an established operation. Use the route that matches the study.

### Connect components and close the argument

- **Parallel complementarity:** Explain the different difficulties and where the operations meet.
- **Sequential processing:** Explain the residual problem and actual dependency between steps.
- **Collaborative preservation:** Explain the capability being added and the information or structure being retained.

Each contribution should correspond to a question, design property, or finding already established. Contribution bullets are optional; their number follows the work. A module list alone does not explain the contribution.

## Match evidence to its role

| Available material | Supported role in the Introduction | Unsupported upgrade |
| --- | --- | --- |
| A task example or schematic | Make a condition, unit, or information path understandable | Prove prevalence, failure, or a causal mechanism |
| Subgroup evaluation | Establish behavior under the defined condition | Prove a unique explanation for the gap |
| A controlled change to a suspected factor | Support an explanation under the tested controls | Establish causality across every setting |
| Correlation analysis | Motivate or support an association | Demonstrate a general causal law |
| A component ablation | Show its task contribution in the tested configuration | Verify every mechanism implied by its name |
| Aggregate benchmark results | Support task-level performance claims under that protocol | Establish behavior on an unmeasured subgroup |
| Resource measurements | Support the measured cost-quality tradeoff under stated conditions | Equate parameter count, FLOPs, memory, and latency |
| An architectural constraint | Explain the intended information flow | Guarantee the intended learned behavior |

Use available figures and preliminary results where they advance the argument. An analogy can motivate an intuition but does not provide experimental validation. Writing support does not automatically require new experiments.

## Hypothetical revision example

A draft might say:

> Existing retrieval methods have insufficient interaction. We therefore introduce an adaptive module to improve performance.

Develop the argument using the actual study's facts:

- Identify what is compared or combined: for example, query features and candidate representations.
- Describe the relevant condition: for example, a change in the query's available information.
- State what the supplied evaluation observes, if anything.
- Separate the possible explanation from the result: for example, a fixed weighting rule may treat features as equally informative under both complete and incomplete inputs.
- State the requirement: adapt the combination to available evidence.
- Explain how the real implementation meets it and what completed evaluation supports.

When the explanation is a hypothesis, a motivation passage could read:

> Queries may provide different amounts of usable information. A fixed combination rule assigns the same feature weights across these conditions, raising the question of whether the weighting should depend on the information available in each query. We investigate this question through a query-conditioned combination rule and evaluate its behavior under the specified input conditions.

Use this only when those statements match the actual work. Add a measured limitation or result only when it has been supplied or verified. Do not use this passage to claim that all fixed-weight methods fail.

## Final revision check

- Does the opening reach the concrete computer science research object?
- Is the work framed as the kind of contribution actually made?
- Can the reader understand the closest prior method's operation and capability?
- Is the limitation tied to a defined condition or dependency?
- Is the observed behavior distinct from the proposed explanation?
- Does the design act at the identified point of difficulty?
- Do module relationships, training conditions, and inference behavior match the implementation?
- Do contribution and result statements stay within the evidence?
- Can repeated importance claims, redundant definitions, or unsupported priority language be removed?

Deliver coherent scientific prose with clear subjects and operations. Preserve the user's terminology, citations, factual uncertainty, and real limitations.
