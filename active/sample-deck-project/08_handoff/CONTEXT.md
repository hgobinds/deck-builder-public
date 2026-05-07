# Stage 08: Handoff

## What This Stage Does

Package the finished deck so someone else can use it, and update pre-delivery workspace memory.

## What To Load

| Situation | Load | Skip These | Output | Trigger |
|---|---|---|---|---|
| Default | `../07_qa/output/qa-v1.md`, final deck files, speaker notes, source list, project `project-state.md`, `../run-retrospective.md` | Raw working files not needed for delivery | `output/` handoff package | QA is approved |

## Process

1. **Discuss first.** Before packaging, confirm with the user:
   - Who is receiving this and what do they need?
   - Should a PDF export be included?
   - Are there any last edits or additions before handoff?
2. Get sign-off on the package contents before finalizing.
3. Assemble the handoff package.
4. Update `project-state.md` and `run-retrospective.md`.

## Handoff Package

- Final `.pptx` — named `YYMMDD_Presentation_Name_Final.pptx`.
- Optional `.pdf` — named `YYMMDD_Presentation_Name_Final.pdf`.
- Speaker notes — named `YYMMDD_Presentation_Name_Speaker_Notes.md`.
- Source list for data, quotes, images, and claims.
- Change log from draft to final.
- Notes for future reuse.
- Archive-ready summary.

## Acceptance Criteria

- Final deck, optional PDF, speaker notes, source list, and handoff notes exist.
- `project-state.md` reflects final delivery status and next archive action.
- `run-retrospective.md` captures proposed lessons before durable files are changed.
- Recipient can present, edit, or reuse the deck without asking how it was built.

## Approval Gate

Review required by: deck owner.
Approved to proceed?: yes/no.

## What Not To Do

- Do not package handoff without confirming contents and recipients with the user.
- Do not move the project to archive before presentation is over.
- Do not promote one-off lessons directly into stable workspace rules.
- Do not hand off until delivery files and pre-delivery memory are updated.
