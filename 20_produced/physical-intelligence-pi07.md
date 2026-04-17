---
source: [[10_raw/companies/2026-04-17-company-physical-intelligence]]
created: 2026-04-17
type: produced
---

# Physical Intelligence π0.7

## What this source is saying
This post is saying that robotic foundation models should not just memorize trained skills or rely on fine-tuning. π0.7 is presented as an early step toward a real generalist robot model that can recombine known skills, follow new instructions, and work across tasks and robots.

## Why it exists
- Problem: current VLA / robotic foundation models still struggle to generalize compositionally.
- Why it matters: a real generalist robot should solve unseen tasks by combining known skills instead of needing per-task specialization.

## What it actually does
- Trains one steerable VLA model with diverse multimodal prompts.
- Adds richer conditioning beyond plain task language: metadata, control-mode labels, and visual subgoals.
- Uses this prompt structure to mix broader data sources and make training more controllable.
- At inference time, the model can use instructions plus additional guidance such as desired strategy or subgoal imagery.

## Main figure / picture to remember
![](https://www.pi.website/_next/image?url=%2Fimages%2Fpi07%2Fsubgoal_1.png&w=3840&q=75)

The main architecture idea is not the tiny image itself but the pipeline described around it:
- broad multimodal prompt in
- VLA model with memory in the middle
- action generation out
- optional world-model-produced visual subgoals at inference time

What matters is the claim that better conditioning, not just more data, is what unlocks better generalization.

## What was actually validated
- They show specialist-level dexterity without fine-tuning.
- They claim early compositional generalization on unseen tasks, such as new appliances.
- They claim stronger transfer across robots, scenes, and tasks than prior models.

## Why it matters to me
- It sits exactly at the intersection of my interests: VLA, robotics, memory, long-horizon behavior, and generalization.
- It is a strong example of American frontier embodied-AI work.
- It suggests that controllable prompting and subgoal structure may matter as much as raw scale.

## Open questions
- How much of the gain comes from prompting structure versus data breadth?
- How robust is the claimed compositional generalization outside curated demos?
