# Submission draft — TriageLens (DO NOT SEND until the checklist is green)

Event: Learn AR with SPECS (Devpost) — https://learn-specs.devpost.com/
Track: single track, $2,500 (1st $1,250, 2nd $750, 3rd $500)
Team: Solo
Status 2026-11-05: PREP ONLY. Design brief + scaffold written; Lens NOT built
yet (Lens Studio runs on the user's Windows laptop — see LAPTOP_STEPS.md).
Nothing registered, nothing submitted.

## Title
TriageLens — hands-free field triage for frontline health workers

## One line
A SPECS Lens that puts the danger-sign checklist where a health worker is
already looking: tick a sign with a pinch, and a red "ESCALATE PER PROTOCOL"
panel appears in her view — no phone to hold, no evening transcription wait.

## What to paste (after the Lens + video + repo exist)
- Repo: TBD — publish the Lens Studio project folder (with `devpost/`
  inside it) as a public GitHub repo. Suggested name: `triage-lens`.
  Do NOT invent a repo URL before it exists.
- Demo video: TBD — public on YouTube, under 3 minutes, screen recording
  of the Lens Studio preview only.
- What it does: a frontline health worker opens a household visit in the
  Lens; the danger-sign checklist (pregnancy, newborn, general) floats at
  arm's length; she pinches to tick a sign; any tick raises a large red
  "ESCALATE PER PROTOCOL" panel beside the checklist; "Visit complete"
  files the visit and advances the "Households seen today" counter.
- Who it's for: frontline health workers doing household visits, whose
  hands are busy and whose eyes must stay on the household.
- What was learned: (fill in after the build — one or two sentences on
  what the preview taught you about designing for glasses: placement,
  big targets, showing things only when needed).
- How it was built: planned with the Devpost Learn skill pack
  (`devpost/design-brief.md`), built by Snap CLAD agents in Lens Studio
  with SIK + UI Kit, LEAF tests run for each done criterion in the preview.
- What is NOT claimed: the demo household is hard-coded and labelled
  SYNTHETIC — no real patient data, no real recognition (a "Household
  found" button is the stand-in, stated openly). The Lens never diagnoses
  and never gives treatment advice; a tick only ever means "escalate per
  protocol". Comfort over time, real hand tracking, and daylight
  readability are "feel unproven" until real glasses.

## Pre-send checklist (all must be true)
- [ ] Lens built in Lens Studio and working in the preview (all five done
      criteria checked; LEAF test results recorded in the brief)
- [ ] Synthetic household labelled SYNTHETIC on screen; stand-in button
      visible and honest
- [ ] Demo video recorded from the preview, under 3:00, watched back,
      Public on YouTube
- [ ] Public repo with the Lens Studio project files + `devpost/` folder
- [ ] Short description written (what it does, who it's for, what was
      learned)
- [ ] Submitted on https://learn-specs.devpost.com/ before Tue 10 Nov 2026,
      03:30 IST (safe: Mon 9 Nov 20:00 IST)

## Side notes
- Reviewers won't clone or run the project — the video has to show it
  working end to end.
- Winners announcement date was NOT verified in this prep — check the
  Devpost page; do not quote a date from here.
- Free-only: no card, no payment anywhere in this track.
