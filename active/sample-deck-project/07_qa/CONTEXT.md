# Stage 07: QA

## What This Stage Does

Catch visual, textual, structural, source, and hallucination problems before handoff.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Default | `../06_build/output/YYMMDD_Presentation_Name.pptx`, `../06_build/output/YYMMDD_Presentation_Name_Speaker_Notes.md`, `../02_source-discovery/saved-pages/`, `../02_source-discovery/output/source-selection.md`, `../02_source-discovery/output/source-brief.md` | Unrelated references and rejected drafts except when checking misuse | `output/YYMMDD_Presentation_Name_QA.md` | Draft deck exists |

## Process

1. **Discuss first.** Before running QA, confirm with the user:
   - Are there specific slides or claims you want checked most carefully?
   - Are there known issues to look for?
   - Should QA cover speaker notes as well as slides?
2. Get alignment on QA scope before starting the audit.
3. Run the full audit against required artifacts.
4. Present findings to the user before marking QA complete.

## Required QA Artifacts

- Text extraction from the deck.
- Slide thumbnails or rendered images.
- Claim/source audit against saved pages, `source-selection.md`, and `source-brief.md`.
- QA notes with fixes.
- Final pass after fixes.

## Hallucination Audit

- Re-open saved webpages or source snapshots for any slide with a factual claim.
- Mark each claim as `supported`, `unsupported`, `overstated`, `source mismatch`, or `needs user confirmation`.
- Do not accept a claim solely because it appears in `source-brief.md`.
- Flag rejected or undecided sources if they appear in the deck.

## Acceptance Criteria

- Text extraction has been reviewed.
- Slide thumbnails or rendered images have been visually inspected.
- Claim/source audit has checked the deck against approved saved sources.
- Required fixes are made or explicitly tracked.

## Approval Gate

Review required by: QA reviewer or deck owner.
Approved to proceed?: yes/no.

## What Not To Do

- Do not begin QA without discussing scope with the user first.
- Do not approve a deck that has not been visually inspected.
- Do not skip source verification for factual slides.
- Do not treat a clean first pass as proof QA was deep enough.
