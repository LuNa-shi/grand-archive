# Source Ingestion and Produced-Note Rules

## Folder policy
- The current numeric prefixes exist only for ordering and system structure.
- For raw-source subfolders, create them dynamically when a real source category appears.
- Do not create unnecessary empty folders.
- If the user later wants, the top-level numbered folders can be renamed to simpler names.

## Writing policy for produced notes
- Be brief and concise.
- Focus on what the source is trying to say and what it actually does.
- Do not over-explain every concept.
- Do not spend much space on setup details, model sizes, or exhaustive architecture details unless they are central.
- For papers, prioritize this order:
  1. what problem the paper is trying to solve
  2. why that problem matters / motivation
  3. what the method actually does
  4. what the main figure or architecture image shows
  5. what the experiments really validate
- Prefer validated contribution over claimed concept.
- If a source has useful images, diagrams, or figures, include the key one in the produced note whenever possible.
- When a key image matters, download it into a local asset folder and embed the local file instead of hotlinking when possible.
- The goal is readability, not completeness.

## Capture policy learned so far
- Use source-aware ingestion instead of blindly relying on generic web extraction.
- X/Twitter: browser-first capture.
- GitHub: browser-first capture when extraction is blocked.
- arXiv: abstract/HTML first, PDF only when necessary.
