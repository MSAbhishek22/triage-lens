# TriageLens — hands-free field triage for frontline health workers

**Learn AR with SPECS (Devpost) · $2,500 total — 1st $1,250, 2nd $750, 3rd $500
· Deadline: Mon 9 Nov 2026, 5:00 PM EST = Tue 10 Nov 2026, 03:30 IST
· Solo, India-eligible, free · Status: PREP DONE (brief + scaffold), BUILD NOT STARTED — Lens Studio runs on the user's Windows laptop, not in this Linux sandbox**

Nothing new. Something missing.

## The concept (one paragraph — why this Lens)

ClinicLink already proved the gap on the web: a frontline health worker sees a
danger sign in the morning, but the clinic only learns about it in the evening,
when she transcribes her paper register. The phone version closes that gap to
minutes — but in the field her hands are busy and her eyes must stay on the
household, so a phone means putting the register down. TriageLens moves the
same tick-only rule into her view: the danger-sign checklist (pregnancy,
newborn, general) floats at arm's length, she pinches a big button to tick a
sign, and the moment any sign is ticked a large red "ESCALATE PER PROTOCOL"
panel appears beside it. It is the same idea, the same rule, the same synthetic
households — but the escalation is unmissable where her eyes already are, and
her hands stay free. That is the whole Lens: one spatial moment, three big
interactions (household found → tick → visit complete), all standard pinch
buttons, all showable in the Lens Studio preview. The live code-review lens was
the alternative; it lost because code review is a screen task — a laptop does
it better, and glasses add nothing. The clinic lens wins because it uses all
three strengths of glasses at once: it shares her view, it draws in the world,
and it leaves her body free.

## Event facts (verified from the official Devpost page, 5 Nov 2026)

- Event: Learn AR with SPECS — https://learn-specs.devpost.com/
- Prizes: $2,500 — 1st $1,250, 2nd $750, 3rd $500.
- Deadline: Mon 9 Nov 2026, 5:00 PM EST = Tue 10 Nov 2026, 03:30 IST.
- Eligibility: solo verified (individuals at age of majority may enter);
  India verified eligible (excluded: Brazil, Russia, Crimea, Cuba, Iran,
  North Korea, US-sanctioned — India not listed). Free, no purchase necessary.
- What to build: a NEW Lens for SPECS glasses, planned with the Devpost Learn
  skill pack (`devpost/design-brief.md` in the repo) and built by an AI coding
  agent through Snap CLAD in Lens Studio. Old idea OK, old code not.
- No glasses needed: everything runs in the Lens Studio preview on a laptop.
- What to submit: demo video (public on YouTube, under 3 min, screen
  recording of the Lens Studio preview is perfect) + public repo with the Lens
  Studio project files and the `devpost/` folder + short description (what the
  Lens does, who it's for, what was learned). Reviewers won't clone or run the
  project, so the video has to show it working.
- Judging: Design / Technical Implementation / Innovation-Idea / Presentation.
- Skill pack: https://github.com/challengepost/learn-specs — install with
  `npx skills add challengepost/learn-specs --all -y`, then say `plan-lens`
  (20–30 min interview, writes `devpost/design-brief.md`).
- Winners announcement date: NOT verified in this prep — check the Devpost
  page before submitting; do not quote a date from here.

## Judging angles (how this Lens scores)

| Criterion | How TriageLens answers it |
|---|---|
| Design | One coherent moment, not a floating website: checklist anchored where the visit happens (~1 m, slightly below eye level), big forgiving targets, shows only when needed, red escalation inside the view. |
| Technical Implementation | Built with CLAD + SIK + UI Kit; every done criterion has a LEAF test run in the preview; stand-in ("Household found" button) is explicit and honest. |
| Innovation / Idea | A real problem for real frontline workers — the paper-register delay — solved where the worker's eyes already are. Not a demo gimmick; it adapts a working triage prototype (ClinicLink). |
| Presentation | Video is a screen recording of the preview showing the full flow end-to-end (household → tick → escalation → visit complete), with the synthetic label visible. |

## What's in this scaffold

- `devpost/design-brief.md` — the design brief the skill pack would produce
  (status: draft — approve it in the laptop `plan-lens` session before
  building). Follows the skill pack's template exactly, including its Build
  notes and After-the-build sections.
- `LAPTOP_STEPS.md` — the exact laptop checklist: install Lens Studio +
  CLAD + MCP, create the SPECS project, run `plan-lens`, build with CLAD,
  LEAF tests, record the video, publish the repo, submit.
- `submission/SUBMISSION_DRAFT.md` — title, one-liner, description text for
  the Devpost form, and the pre-send checklist.
- `submission/DEMO_VIDEO_SHOT_LIST.md` — the under-3-minute preview
  recording shot list.

## Honest limits (do not hide these)

- **Synthetic data only.** The demo household is hard-coded and labelled
  SYNTHETIC. No real patient data, no real household, no real recognition.
- **Stand-in, stated openly.** The Lens cannot recognise a real household in
  the preview; a "Household found" button loads the demo household. That is
  the skill pack's own stand-in pattern, and the brief says so.
- **No diagnosis, no treatment advice.** A tick only ever produces
  "escalate per protocol" — the clinic's own protocol, never a condition.
  There is no free-text input, so free text can never escalate.
- **Preview-proven only.** LEAF tests + preview walkthrough prove the logic;
  comfort over time, real hand tracking, and daylight readability are "feel
  unproven" until real glasses — label them that way in the submission.
- **Lens Studio is not in this sandbox.** The actual Lens build happens on
  the user's Windows laptop (see `LAPTOP_STEPS.md`). Nothing in this scaffold
  claims a Lens already exists.

## Free-only rule

Lens Studio, CLAD, the skill pack, Devpost, and YouTube upload are all free.
No card, no payment, no paid plan anywhere in this track. If any step asks
for a card or payment, stop and report it.
