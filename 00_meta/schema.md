# Grand Archive Schema

## Purpose
This vault is a personal knowledge base and personal information-grasping system for the user.
It has three layers:
1. raw = immutable source captures from the web and other inputs
2. produced = interpreted notes for each source in a consistent format
3. synthesis = higher-level combinations, reflections, and research notes built from related materials

## Core principles
- raw files are append-only and treated as read-only after capture
- every produced note should point back to one or more raw sources
- every synthesis note should point back to relevant produced notes and, when useful, raw notes
- the system should learn the user's taste, interests, habits, and curiosities over time
- the user's personal taste profile is a living note and should be updated whenever new durable preferences are discovered
- broad sources are encouraged: blogs, interviews, books, papers, Twitter/X threads, newsletters, forums, videos, transcripts

## Directory layout
- 00_meta/ = system notes and navigation
- 01_profile/ = personal taste, habits, curiosity map
- 10_raw/ = immutable source captures
- 20_interpreted/ = one note per source, interpreted in a standard template
- 30_synthesis/ = multi-source reflections, topic maps, essays, personal research papers

## Naming conventions
- folders use numeric prefixes for ordering
- files use lowercase kebab-case where practical
- date prefix format: YYYY-MM-DD
- raw source filenames should include date + source + short slug
- produced filenames should usually mirror the raw source slug
- synthesis filenames should describe the combined topic or research question

## Raw-source policy
- never overwrite a raw source file once captured
- if a source must be corrected, create a new version note or add correction metadata elsewhere
- include source URL, capture date, source type, author if known, and tags
- recommended raw subfolders:
  - 10_raw/blogs/
  - 10_raw/social/
  - 10_raw/books/
  - 10_raw/papers/
  - 10_raw/newsletters/
  - 10_raw/videos/
  - 10_raw/other/

## Produced-note format
Every produced note should include:
- what the source is
- the source's main point
- key claims / arguments / ideas
- why it may matter to the user
- links to related produced and synthesis notes
- open questions triggered by the source

## Synthesis-note format
Synthesis notes can include:
- combined thesis
- agreements / tensions between sources
- what seems most aligned with the user's taste
- the user's own reflections or questions
- next reading directions

## Operating rule for Hermes
At the start of future work in this vault, Hermes should first read:
- 00_meta/schema.md
- 00_meta/index.md
- 00_meta/log.md (recent entries)
- 01_profile/personal-taste.md

## Change management
- every major change should be appended to 00_meta/log.md
- new top-level notes should be added to 00_meta/index.md
