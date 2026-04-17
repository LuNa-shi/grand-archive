# Hermes Best Practices For This Vault

## Main role
Hermes should behave as a personal research assistant and archive maintainer.

## Best-practice workflow
1. Capture first.
   When the user asks Hermes to ingest a source, preserve the source in 10_raw before interpretation.
2. Interpret second.
   Create one note in 20_interpreted for each important source using a consistent summary format.
3. Synthesize third.
   Create notes in 30_synthesis only when there is enough overlap, tension, or thematic relation across sources.
4. Update the user profile continuously.
   Durable habits, tastes, and interests should be reflected in 01_profile/personal-taste.md and Hermes memory.
5. Keep provenance clear.
   Every produced or synthesis note should link back to source notes.
6. Prefer breadth of sources.
   Mix blogs, newsletters, papers, books, social posts, transcripts, and other formats.
7. Ask before large synthesis jumps.
   If a new synthesis note would significantly reinterpret the user's worldview or create many derived notes, ask first.
8. Use scheduled collection carefully.
   Daily collection should focus on likely-interest sources and avoid flooding the archive with low-value material.

## Practical Hermes features to use
- memory: store durable user preferences and long-term habits
- cron jobs: run daily collection or digestion workflows
- skills: keep reliable workflows for ingestion and note production
- session search: recall previous discussions when the user references past work

## Personal operating rules learned from failure
- Do not trust web_search or web_extract as the first path for every public source in this environment.
- When a source is important, prefer a source-aware strategy instead of blindly trying generic extraction first.
- Prefer local-first capture: preserve a durable local artifact in raw before summarizing whenever possible.
- For paper-like sources and technical posts, check first whether a clean PDF or HTML version exists; use that before browser screenshot workflows.
- For website captures, PDF export first, clean HTML second, browser/screenshot fallback third.
- For X/Twitter pages: use browser capture first and extract visible post text from the page.
- For GitHub profiles and repositories: use browser capture first if generic web extraction is blocked.
- For arXiv papers: prefer the arXiv abstract page first, then follow links to HTML or PDF only if needed.
- For general docs/blog pages: if web extraction fails once, switch quickly to browser-based capture instead of repeating the same failure path.
- For main figures in PDFs, direct page rendering plus cropping is usually better than rebuilding from webpage slices.
- When capture succeeds through a workaround, record that lesson in memory and in this vault so future ingestion is more reliable.

## Notes on web research
I attempted web search for Hermes best practices, but the current web-search endpoint returned errors in this session.
So this note is based on Hermes' installed skills and documentation already available in the environment.
During source ingestion, generic web extraction was also blocked for several public pages, so browser-based capture became the more reliable default for X, GitHub, and some other sources.
