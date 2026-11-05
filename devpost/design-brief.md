---
status: draft
---

# Design brief: TriageLens — hands-free field triage for frontline health workers

<!-- Filled in by plan-lens from the learner's interview. Use the learner's words. Mark any value they didn't choose as (default). -->
<!-- NOTE: this draft was prepared in advance from the delegated concept pick (ClinicLink adaptation) so the laptop plan-lens session starts from a complete draft. Run `plan-lens` on the laptop, confirm or change anything, and only then set status: approved. -->

## The one spatial moment
A frontline health worker stands in a household during a visit, hands busy with her paper register and kit. In front of her, at arm's length, floats the visit's danger-sign checklist — three groups (pregnancy, newborn, general). She pinches a big button to tick a sign. The moment any sign is ticked, a large red panel appears beside the checklist: "ESCALATE PER PROTOCOL" — the same rule as ClinicLink, now where her eyes already are.

## Why it belongs on glasses
- Uses: shares your view, draws in the world, leaves your body free (all three).
- Why it's better than the phone or laptop version: the worker's hands are busy and her eyes must stay on the household; a phone means putting the register down, unlocking it, and finding the form. The glasses keep the checklist where she looks, and the escalation is unmissable in her view instead of waiting for the evening transcription at the clinic.

## Product or overlay
- Type: overlay — it responds to the household visit in front of the worker.
- What the real version would sense: the household being visited and the danger signs the worker observes. The Lens never diagnoses from vision; the worker confirms each sign.
- Stand-in for the preview: a "Household found" button that loads a hard-coded synthetic demo household (labelled SYNTHETIC — no real patient data, ever). The checklist and the escalation that follow are built for real.

## Where things live
- Where the user is looking during the main task: at the household space in front of her, slightly below eye level, where a visit happens.
- Checklist panel: floating ~1 m away, a little below eye level, anchored in front of the user at start; ~40 cm wide, three groups with big tick targets.
- Escalation panel: appears to the right of the checklist, same distance, large red panel with "ESCALATE PER PROTOCOL" plus the ticked sign and "household flagged" text. Light text on red (the display is additive: black renders as transparent, so no black text).
- Counter chip: small chip above the checklist: "Households seen today: N". N counts "Visit complete" taps in the session (default).

## Hands and input
- Pinch to tick a danger sign (one big button per sign, highlights when aimed at).
- Pinch "Household found" to load the demo household (the stand-in).
- Pinch "Visit complete" to file the visit and advance the counter.
- Targets are big and highlight when aimed at.
- Voice (if any) and the button that does the same job: none — voice may not work in the preview, so every action has a button.

## When things show
- Checklist panel: shows when a household is loaded, hides when the visit is completed.
- Escalation panel: shows the moment any danger sign is ticked, stays until the visit is completed.
- Counter chip: shows whenever the checklist is visible.
- If something needs attention out of view: a short chime; the red panel sits next to the checklist, inside the view (never behind the shoulder).

## Done criteria
Each one can be checked in Lens Studio's preview.
1. In the preview, pinch "Household found" and the synthetic household's danger-sign checklist appears at ~1 m, readable from where the user stands.
2. Pinch one danger-sign button and it shows as ticked; the red "ESCALATE PER PROTOCOL" panel appears next to the checklist.
3. With no sign ticked, no escalation panel is shown (tick-only rule: there is no free-text input in this Lens, and free text could never escalate).
4. Pinch "Visit complete" and the checklist hides, the counter "Households seen today" increases by one, and the escalation panel clears.
5. Walk around the Lens (WASD + mouse) and the panels stay readable and in view during the main task; no panel sits behind the user or stuck to the face.

## Out of scope
- No real patient data, no real household recognition (stand-in only).
- No diagnosis or treatment advice — the Lens only flags "escalate per protocol" and never names a condition.
- No free-text notes, no phone sync, no ClinicLink backend connection. The Lens is a standalone demo of the field moment; ClinicLink remains the separate web prototype.
- No multi-person / shared Lens, no memory across sessions.

## Risks and open questions
- Real hand tracking on device vs mouse-driven pinch in the preview: feel unproven until real glasses; the demo uses only standard pinch buttons so the flow is preview-provable.
- The escalation panel's readability in bright daylight is only answerable on real glasses (additive display); in the preview, light-on-red text is used.
- Whether the worker would want the checklist anchored to the household doorway instead of floating in front: kept as floating in front (default) — the plan-lens session on the laptop can change this.

## Build notes for CLAD
- Build for SPECS so it runs and can be demonstrated in Lens Studio's preview. No SPECS device is available.
- Use Spectacles Interaction Kit (SIK) and UI Kit for all interactions, so they work with the mouse in Interactive Preview and with LEAF.
- Build any stand-in exactly as described above, and keep it obvious in the scene.
- Use real-world scale in centimeters. Keep content inside the user's view during the main task.
- The display is additive: black renders as transparent. Don't rely on black or very dark content to be seen; keep text light and readable from where the user stands.
- Get the basic flow working first, then add detail.
- Write LEAF scenarios for each done criterion, run them in preview, and report which pass. Say which criteria have no test.
- Don't record, identify, or follow people.

## After the build: judge it
This part is for you, after CLAD finishes.

1. **Does it work?** Ask your agent which LEAF tests passed and which done criteria have no test.
2. **Walk around it.** Open the preview in Interactive Preview. Use WASD to move, Q and E to go down and up, and right-drag (or hold Shift) to look around. Clicking acts as a pinch. Stand where a user would and look at the task.
3. **Ask the three questions.**
   - Does it use what I'm looking at?
   - Does it put something in my space, where it belongs?
   - Does it free my hands or let me keep my eyes up?
   - Would it be just as good on a phone? If so, what would make it need the glasses?
4. **Check comfort.**
   - Everything I need is in view while I do the task. Nothing sits at the edges, behind me, or stuck to my face.
   - Every control is within reach of someone standing there.
   - Text reads easily from where I stand. No dark UI disappearing.
   - Things show when needed and get out of the way.
5. **Label what you know.** Write "logic proven" next to anything the tests and preview show working, and "feel unproven" next to anything only real glasses could tell you (comfort over time, real hand tracking, real recognition).
6. **Fix with design notes, not code.** Tell your agent what to change in design terms, for example: "Move the step card 15 cm lower and next to the pan. Make the Next button twice as big. Re-run the tests." If a fix takes under a minute, like nudging a panel, do it yourself in the scene.
7. **Submit.** Record a video under 3 minutes of your Lens in the preview, public on YouTube. Make your repo public with your Lens Studio project and this `devpost/` folder. Details are on the hackathon site: https://learn-specs.devpost.com/resources
