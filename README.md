# grand-archive

A personal Obsidian-based knowledge archive for collecting, interpreting, and synthesizing high-signal sources.

This repo is designed as a living research assistant workspace.
It preserves raw source material, turns important sources into concise notes, and later combines related material into higher-level synthesis.

## Core idea

The archive currently follows a 3-layer model:

- raw
  immutable source captures from blogs, papers, social posts, GitHub, company research pages, and other sources
- produced
  brief interpreted notes that explain what a source is really saying and what it actually does
- synthesis
  higher-level reflections, topic maps, and personal research notes built from multiple sources

## Current structure

- `00_meta/`
  system notes, index, schema, operating rules, and log
- `01_profile/`
  personal taste, interests, seed sources, and source preferences
- `10_raw/`
  captured source material
- `20_produced/`
  concise source interpretations
- `30_synthesis/`
  cross-source synthesis and reflection

## Writing philosophy

Produced notes are intentionally concise.
They should focus on:
- what a source is trying to solve or say
- why it matters
- what it actually does
- the most important figure or image when useful
- what was truly validated

They should avoid:
- inflated concept dumping
- excessive setup detail
- decorative architecture explanation without evidence
- confusing proposed ideas with validated results

## Source policy

The archive prefers high-signal, primary, builder-oriented sources such as:
- impactful personal blogs
- GitHub repositories and profiles
- GitHub Pages essays and course pages
- X / Twitter threads
- arXiv papers
- newsletters
- podcasts and YouTube transcripts

Sources are added dynamically.
Folders for raw material are created when needed rather than fixed in advance.

## Image policy

When a figure or image is important for understanding a source:
- download it into a local asset folder when possible
- embed the local file instead of hotlinking when possible

## Repository purpose

This repository is not just a note dump.
It is meant to become a compounding personal archive that helps:
- track interests and taste over time
- preserve source provenance
- make future synthesis easier
- support question answering and research workflows inside Obsidian

## Next directions

- improve the produced-note pipeline
- localize important source images into asset folders
- add more source ingestion and synthesis workflows
- optionally simplify the top-level folder naming later
