---
source_note: "[[10_raw/companies/2026-04-17-company-physical-intelligence]]"
created: 2026-04-17
type: produced
---

# Physical Intelligence π0.7

## What problem this post is tackling
The post is tackling a concrete weakness of current robot foundation models: they can execute trained skills, but they do not reliably recombine those skills into new tasks. Physical Intelligence presents π0.7 as a step toward a model that can use richer conditioning to perform unseen tasks without task-specific fine-tuning.

## Why that problem matters
For a robot model, generalization is not just about recognizing more scenes. It means taking language, state, and task guidance and turning them into correct multi-step behavior on tasks that were not directly collected as demonstrations. Without that, a VLA model is still closer to a library of trained behaviors than to a general-purpose policy.

## What the system actually does
π0.7 is presented as a steerable VLA system built around multimodal conditioning.
The technical move is not just "more data" but better structured prompts.
The article says the model can condition on:
- task language
- subtask language
- episode metadata such as speed or quality
- control modality labels
- visual subgoals
- observation history / memory

The point of this design is practical: these extra conditioning channels let the system combine data from different robots, control schemes, human videos, and autonomous rollouts without collapsing everything into one ambiguous training signal.

## Main figure
![[../10_raw/companies/assets/physical-intelligence-pi07/pi07-main-figure-reference.png]]

This is the clearest main architecture figure for the source. It shows the full control stack around π0.7: a High-Level Policy proposes subtasks, a World Model predicts visual subgoals, and the central Vision-Language-Action Model consumes observation memory, task instruction, subtask instruction, subgoal images, and metadata before the action expert produces low-level actions.

The key technical point is that π0.7 is not driven by plain instruction text alone. The architecture makes multimodal steerability explicit: language, memory, subgoal images, and metadata jointly control execution, which is the mechanism the source uses to explain stronger compositional generalization.

## What the figure reveals technically
The figure is trying to explain a specific pipeline:
- training uses diverse language instructions, subgoal images, and metadata
- the central model consumes observation plus memory together with that prompt structure
- inference can use high-level policy outputs and world-model-produced subgoals
- outputs are evaluated by whether one model can produce specialist-level behavior across different tasks and embodiments

So the figure is not mainly a branding image. It is the post's compact explanation of how steerability is implemented.

## What was actually demonstrated
The strongest concrete claims in the post are:
- out-of-the-box dexterous performance without an extra task-specific fine-tune step
- appliance-following behavior with language coaching
- improved autonomous execution once a high-level policy generates language subtasks
- transfer across tasks, scenes, and robot setups

The evidence shown in the article is still mostly demo-driven and qualitative. So the solid takeaway is not "general robotics is solved," but rather: richer prompt structure appears to produce a more capable and controllable VLA policy than their earlier setup.

## What is technically solid here
More solid:
- the system uses explicit multimodal conditioning instead of only a single text prompt
- subgoal images and metadata are being treated as first-class control signals
- the article shows a clear systems idea for mixing heterogeneous data sources

Less solid from this post alone:
- how broadly the claimed compositionality survives outside curated demos
- how much comes from prompt design versus data scale and collection strategy
- whether the same gains hold under harder, more standardized evaluation

## Why this note matters for my archive
This source is useful because it exposes an actual systems design choice in frontier embodied AI:
- steerability through prompt structure
- subgoal-conditioned control
- memory-aware VLA execution

That is more useful than a vague "generalist robots are coming" story.

## Open questions
- What is the minimum conditioning set that actually drives the gain: language, metadata, subgoals, or all of them together?
- What benchmark would best separate real compositional generalization from strong prompt-assisted demos?
