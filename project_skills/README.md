# Project Local Skills

This folder contains project-local operating skills for the Grand Archive.
These are not global Hermes skills.
They are compact reusable procedures for this vault's recurring work.

## Why this exists
The archive is becoming a small software system made of reusable functions:
- search
- ingest
- produce concise technical notes
- synthesize across many sources

The goal is to separate:
- source-specific preprocessing
- normalized raw capture
- produced-note generation
- higher-level synthesis

## Core idea
Every future workflow should pass through a normalization layer.
That means each source, no matter where it comes from, should first be turned into a stable local raw artifact.
Only after that should the system generate produced notes or syntheses.

## Local skills in this folder
- search.md — recurring search / monitoring workflow
- ingest.md — convert a source into normalized raw + produced note
- deepen.md — second-pass upgrade for important notes with more figures, sharper framing, and stronger technical interpretation
- synthesize.md — answer questions or generate higher-level ideas from normalized local sources
- source-preprocessing.md — platform-specific rules for turning any source into a normalized local artifact
- blog-block-quality.md — what makes a concise but technically useful produced note

## Seed-source proof
The current seed sources already demonstrated working pipelines across:
- blogs / GitHub Pages / course pages
- X / Twitter
- arXiv papers
- GitHub repositories and profiles
- company research sites
- business portals

See: `../30_synthesis/seed-source-multi-platform-demonstration.md`

## Design principle
Think of each skill here as a project function.
A source comes in, gets routed through preprocessing, then becomes raw, then produced, then synthesis.
