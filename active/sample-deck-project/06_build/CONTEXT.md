# Stage 06: Build

## What This Stage Does

Create the actual deck and matching speaker notes from the approved storyboard and design plan.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Build from scratch | `../04_storyboard/output/slide-storyboard.md`, `../05_design-system/output/design-plan.md`, approved sources as needed | Raw intake unless a dependency is unresolved | `output/YYMMDD_Presentation_Name.pptx`, `output/YYMMDD_Presentation_Name_Speaker_Notes.md` | Storyboard and design are approved |
| Build from template | Storyboard, design plan, template deck, brand guide | Unrelated templates and old drafts | Draft deck and notes using same naming convention | User provides a deck template |

## Process

1. **Discuss first.** Before building, confirm with the user:
   - Are the storyboard and design plan fully approved and ready to build from?
   - Are there any last-minute changes before touching the deck file?
   - Which build mode applies (scratch, template, existing deck, hybrid)?
2. Get explicit go-ahead before creating or modifying any deck file.
3. For template-based decks: copy `_skills/deck-boilerplate.py` into `06_build/build_deck.py` and populate from the storyboard.
4. Build slide-by-slide following the approved storyboard and design plan.
4. Draft speaker notes for each slide.
5. Run all speaker notes through the `/humanizer` skill before saving — notes must sound like a person talking, not AI copy.
6. Share the draft with the user before marking it ready for QA.

## Build Modes

- From scratch.
- From template.
- From existing deck.
- Hybrid using prior patterns.

## Acceptance Criteria

- `YYMMDD_Presentation_Name.pptx` exists.
- `YYMMDD_Presentation_Name_Speaker_Notes.md` exists and matches the slide flow.
- Deck follows storyboard and design plan.
- Claims, quotes, data, and logos preserve source attribution.
- Filenames use the presentation date (not build date) as the YYMMDD prefix.

## Approval Gate

Review required by: builder before QA.
Approved to proceed?: yes/no.

## What Not To Do

- Do not start building without explicit user approval to proceed.
- Do not silently drop slides or claims.
- Do not leave placeholder text.
- Do not create a text-only deck.
- Do not use speaker notes to smuggle in unsupported claims.
- Do not save speaker notes without running them through the humaniser first.
