# Demo video shot list — TriageLens, Lens Studio preview walkthrough

**Under 3 minutes, Public on YouTube. Screen recording of the Lens Studio
Interactive Preview ONLY — no slides, no screenshots assembled as video,
no harness, no stock footage. (User video rule: the video must show the
actual product working.) Target 2:00–2:50; hard limit 2:59.**

## Before pressing record

1. Lens built and LEAF tests run; all five done criteria checked in the
   preview at least once.
2. Preview open in Interactive Preview, camera at the user's standing
   position, checklist area in view.
3. Synthetic household labelled SYNTHETIC on screen — check it is readable
   before recording.
4. No secrets on screen: no tokens, keys, passwords, inboxes, or real
   patient data (there is none — the household is hard-coded synthetic).
5. Record with OBS Studio or Windows Game Bar (Win + G). One continuous
   take if possible; if a take breaks, re-record from the start rather
   than splicing.

## Shot list (in order, one continuous take)

1. **(0:00–0:20) The Lens open.** Lens Studio preview, the empty visit
   view. Say/show the one line: "TriageLens — hands-free field triage.
   The checklist lives where the health worker is already looking."
2. **(0:20–0:50) Household found.** Pinch the "Household found" button.
   The synthetic household loads and the danger-sign checklist appears
   at ~1 m, readable. Show the SYNTHETIC label. Name the three groups
   on screen: pregnancy, newborn, general.
3. **(0:50–1:40) Tick → escalate.** Pinch one danger-sign button. It
   shows as ticked; the large red "ESCALATE PER PROTOCOL" panel appears
   beside the checklist. Hold it in view long enough to read. Say the
   rule once: "A tick is the only thing that escalates. No free text,
   no diagnosis."
4. **(1:40–2:10) Visit complete.** Pinch "Visit complete". The checklist
   hides, the escalation panel clears, and "Households seen today"
   increases by one. (If time, load a second household and show the
   no-tick state: no escalation panel without a tick.)
5. **(2:10–2:40) Walk around it.** Move with WASD + mouse look to show
   the panels stay readable and in view from the user's position; nothing
   behind the shoulder, nothing stuck to the face.
6. **(2:40–2:55) Close on the checklist.** End on the checklist in view.
   One closing line: "The escalation is where her eyes already are."
   Stop the recording before 2:59.

## Honesty notes — do not hide or cut these

- The "Household found" button is a stand-in: the preview cannot
  recognise a real household. Show the button press as-is; do not imply
  the glasses recognised anything.
- The household is synthetic and labelled. Say so on camera or keep the
  label readable in frame.
- If a LEAF-tested interaction behaves differently live, show what
  actually happened — do not re-record to hide a stumble unless the take
  is unusable.

## After recording

- Watch the file back end to end, check duration is under 3:00, then
  upload to YouTube as Public and keep the link.
- Fill the video link into `submission/SUBMISSION_DRAFT.md` and tick the
  video checklist item there.
- Next step after the video: publish the repo (Lens Studio project folder
  with `devpost/` inside) and submit on Devpost before Tue 10 Nov 2026,
  03:30 IST (safe: Mon 9 Nov 20:00 IST).
