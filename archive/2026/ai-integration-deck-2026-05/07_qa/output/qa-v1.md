# QA Report: AI Integration Plan
# Reviewer: Claude Code | 2026-05-07

---

## Text Review

| # | Issue | Location | Severity | Fix |
|---|---|---|---|---|
| T1 | Photo placeholders `[ Photo ]` present | Slide 11 | Low | Intentional — no photos supplied. Leave as is or add headshots before presenting. |
| T2 | "version 4 went to the right person" | Speaker notes, Slide 4 | Low | Specific enough to be vivid, generic enough not to be wrong. Keep. |

No missing text, no broken formatting, no placeholder copy left unintentionally.

---

## Claim and Source Audit

Approved source: S1 — Consultant Tooling Proposal (internal). No external sources approved.

| Slide | Claim | Status | Note |
|---|---|---|---|
| 2 | "Other firms are using it in delivery right now" | Needs user confirmation | No external source approved. True in the market generally, but unverified here. Low risk for internal presentation — presenter should be prepared to name examples if asked. |
| 2 | "structuring client outputs, drafting communications, processing research" | Needs user confirmation | Same as above — general market claim, no source. |
| 4 | Operating layer vs judgment layer distinction | Supported | Directly from S1: "AI handles setup, routing, formatting, logging — consultant handles judgment, diagnosis, trust." |
| 5 | Consultant operating loop (5 stages) | Supported | Directly from S1 operating loop. Note: S1 has 5 stages shown on slide, source has 7-stage loop — stages are consolidated here. Acceptable simplification. |
| 6 | Four tools (Intake Brief Builder, Meeting Notes Processor, Review Gate, Handoff Package Builder) | Supported | All four are in S1 Phase 1 tool list. |
| 6 | "These aren't mockups. We're building them." | FLAG — needs user confirmation | S1 is a proposal document. The speaker notes claim active development. Is this accurate beyond the sample implementation sub-trial? If yes, keep. If the tools are still at proposal stage, soften to: "These are the first tools we're building." |
| 7 | Trial Participant A and Trial Participant B, Consultants, sample implementation trial, active | Supported | Confirmed by user in session. |
| 8 | "Phase 1: seven tools, intake through handoff — in trial now" | FLAG — overstated | The confirmed trial is a "sub-trial of a single-use toolkit for sample implementation projects" — not the full 7-tool Phase 1. The slide implies the whole Phase 1 is in trial. Recommend softening to: "Phase 1 tools are being trialled, starting with the sample implementation toolkit." |
| 8 | Phase 1/2/3 tool lists | Supported | Directly from S1 build sequence. |
| 9 | No factual claims — call to action only | Supported | N/A |
| 10 | "This deck was built with the toolkit this morning" | Supported | Factually accurate — built in this session. |
| 11 | No factual claims | Supported | N/A |

---

## Flags Requiring Resolution Before Presenting

### FLAG 1 — Slide 6, Speaker Notes: "These aren't mockups. We're building them."
**Risk:** Source document is a proposal. If the tools are not yet in active development beyond the sample implementation trial, this claim is inaccurate.
**Options:**
- Keep if active development is confirmed
- Change to: "These are the tools we're building out from the trial."
- Change to: "The trial is the first version of these tools in practice."

### FLAG 2 — Slide 8, Slide + Speaker Notes: "seven tools in trial now"
**Risk:** Overstates the trial scope. Only a sample implementation sub-trial is confirmed, not the full 7-tool Phase 1.
**Recommended fix — slide:** Change "Phase 1: Core Delivery [NOW]" to "Phase 1: Core Delivery [IN TRIAL]" and add note "Starting with sample implementation toolkit"
**Recommended fix — speaker notes:** Change "That's in trial now" to "That's what the sample implementation trial is testing."

---

## Visual Check

Cannot inspect rendered slides directly — visual QA should be done in PowerPoint before presenting. Check:
- [ ] ASCII diagrams render correctly in Courier New on all slides
- [ ] Slide 4 two-column layout is readable (operating vs judgment layer)
- [ ] Slide 11 photo placeholders are clearly marked and not confusing
- [ ] No text is cut off at slide edges
- [ ] Title slide date reads "8 May 2026"

---

## Overall Status

**Approved to proceed to handoff. Both flags resolved:**
1. Flag 1 — Confirmed by user: active development is underway beyond the sample implementation trial. No change needed.
2. Flag 2 — Fixed: slide 8 label updated to "IN TRIAL — sample implementation toolkit"; speaker notes updated to "That's what the sample implementation trial is testing."

Both are one-line changes. Neither affects the deck structure.
