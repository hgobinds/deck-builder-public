# Stage 02: Source Discovery

## What This Stage Does

Gather external evidence, market context, examples, benchmarks, data points, quotes, and source links before shaping the deck argument.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| External evidence needed | `../01_intake/output/deck-brief.md`, `../01_intake/input/`, project `project-state.md` | Build, QA, handoff, archive | `output/source-candidates.md`, `output/source-selection.md`, `output/source-brief.md` | Brief requires current facts, sources, examples, or citations |
| Sourcing skipped | `deck-brief.md`, user-provided sources | Web search unless user requests it | `output/source-brief.md` noting skipped research | Deck is internal or user supplied all sources |

## Process

1. **Discuss first.** Before searching anything, ask the user:
   - Do you have documents, reports, or internal material to contribute?
   - What kinds of external sources would be useful (research, case studies, data, quotes)?
   - Should we search at all, or is internal material sufficient?
2. Agree on a source plan. Only proceed once the plan is clear.
3. Collect user-provided documents into `input/` and index them.
4. If external search is agreed, turn the deck brief into specific research questions and run web search.
5. Save relevant webpages or clean markdown snapshots into `saved-pages/`.
6. Create `output/source-candidates.md` listing all sources (user docs + any found).
7. Ask the user which sources should be used.
8. Record choices in `output/source-selection.md`.
9. Produce `output/source-brief.md` using approved sources only.

## Saved Page Format

Saved webpage files should use `YYYY-MM-DD-source-slug.md` and include title, URL, publisher, published date, accessed date, relevant extract, possible deck use, and reliability notes.

## Acceptance Criteria

- Source candidates are saved and summarized.
- The user has approved, rejected, or marked candidate sources undecided.
- `source-brief.md` uses approved sources only.
- Claims to avoid or qualify are explicit.

## Approval Gate

Review required by: deck owner or source reviewer.
Approved to proceed?: yes/no.

## What Not To Do

- Do not run web searches without first discussing the source plan with the user.
- Do not assume external search is needed — user documents may be sufficient.
- Do not use rejected or undecided sources as support for deck claims.
- Do not summarize sources without saving links, dates, and access dates.
- Do not let research sprawl into a full report.
