---
source: [[10_raw/social/2026-04-17-x-karpathy-llm-knowledge-bases]]
created: 2026-04-17
type: produced
---

# Karpathy on LLM Knowledge Bases

## What this source is saying
Karpathy is arguing that LLMs are already useful for building personal knowledge bases, not just writing code. His main idea is simple: collect raw source material, let the LLM compile it into a markdown wiki, then keep asking questions and filing the answers back into the archive so the knowledge base compounds over time.

## Why it exists
- Problem: research knowledge gets scattered across articles, papers, repos, and notes.
- Why it matters: if exploration does not accumulate, you keep re-doing the same reading and thinking.

## What it actually does
- Uses a raw/ folder to store source material.
- Uses an LLM to compile markdown wiki pages with summaries, backlinks, and topic pages.
- Uses Obsidian as the reading and viewing interface.
- Files outputs like markdown notes, slides, and figures back into the wiki.

## Main figure / picture to remember
There is no central research figure here.
The key mental picture is a loop:
raw sources -> compiled markdown wiki -> LLM questions and outputs -> results filed back into the wiki.

## What was actually validated
- Karpathy says this already works for him at the scale of roughly 100 articles / 400K words.
- He says the system is good enough for complex questioning without needing fancy RAG at this scale.
- The source is a practice report, not a formal benchmark.

## Why it matters to me
- It directly validates the archive structure I am building.
- It supports raw -> produced -> synthesis as a practical workflow.
- It suggests that accumulation and reuse are more important than one-off answers.

## Open questions
- At what scale does this workflow start to need stronger search or retrieval?
- What is the best linting routine for keeping the archive clean over time?
