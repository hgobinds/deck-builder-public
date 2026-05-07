# Stage 09: Archive

## What This Stage Does

After the presentation is over, close the project, capture what happened, preserve useful memory, and move the project from `active/` to `archive/YYYY/`.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Presentation complete | `../08_handoff/output/`, presentation outcome notes, `../run-retrospective.md`, `../project-state.md`, QA notes | Active drafts without reuse value | `output/archive-closeout.md`, archive package, registry updates | User confirms project is done |
| Project cancelled or paused | Project state, useful source/narrative/QA material, retrospective | Drafts with no future value | Archive package or paused closeout | User marks project cancelled, paused, or superseded |

## Process

1. **Discuss first.** Before archiving, confirm with the user:
   - Is the presentation over and the project fully closed?
   - What artifacts are worth preserving vs. discarding?
   - Are there lessons from this run worth promoting to stable workspace rules?
2. Get explicit confirmation before moving anything to `archive/`.
3. Execute archive actions below.

## Archive Actions

- Move or copy curated project artifacts into `archive/YYYY/client-topic-deck-YYYY-MM/`.
- Preserve final deliverables, source selections, saved webpages, source briefs, narrative, storyboard, design plan, speaker notes, QA notes, rendered slides, handoff notes, run retrospective, and archive closeout.
- Update archive `README.md`.
- Update `_registry/decks-index.md` and `_registry/archive-log.md`.
- Promote durable lessons from `run-retrospective.md` only when they matter for future deck work.

## Acceptance Criteria

- Presentation has ended, or the user has marked the project delivered, paused, cancelled, or superseded.
- Curated archive package exists.
- Archive README and `archive-closeout.md` are complete enough for a future agent to open cold.
- Registry and archive log are updated.
- Durable lessons from `run-retrospective.md` are promoted or explicitly left project-local.

## Approval Gate

Review required by: deck owner.
Approved to proceed?: yes/no.

## What Not To Do

- Do not archive without confirming the project is closed and the user has approved what to keep.
- Do not archive before the presentation is over unless the user explicitly closes the project.
- Do not preserve every working draft by default.
- Do not invent presentation outcomes.
- Do not leave a stale active project that looks current.
