# Stage 01: Intake

## What This Stage Does

Capture what the deck is for before any writing, design, or research begins.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Default | User request, `input/`, project `project-state.md`, root `CONTEXT.md`, `_config/deck-types.md` | Later stage outputs, archive folders | `output/deck-brief.md` | Starting or clarifying a deck |

## Process

1. **Discuss first.** Even if the user gives a one-line brief, do not start drafting. Explicitly invite them to add more context:
   - What is this deck for and who is the audience?
   - What decision or action do you want from them?
   - Do you have existing materials, prior decks, internal documents, or constraints?
   - When is this due and what format is needed?
   - Is there anything else you want me to know before I write the brief?
2. Wait for the user to confirm they have shared everything before drafting anything.
3. Identify audience, decision, deck type, and desired action.
4. Inventory run-specific inputs in `input/`.
5. Decide whether external source discovery is needed.
6. List constraints, out-of-scope items, and claims needing verification.

## Acceptance Criteria

- Audience, decision, deck type, success criteria, constraints, and source needs are explicit.
- Run-specific source material lives in the project folder, not `_references/`.
- Source discovery is marked needed, skipped, or lightweight.

## Approval Gate

Review required by: deck owner.
Approved to proceed?: yes/no.

## What Not To Do

- Do not draft the brief before discussing with the user.
- Do not treat a one-line brief as sufficient — always invite more context explicitly.
- Do not start narrative or build work from a vague brief.
- Do not put one-off user files in `_references/`.
- Do not assume external sources are needed; decide based on the deck brief.
