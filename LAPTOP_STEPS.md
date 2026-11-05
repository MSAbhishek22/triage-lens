# Laptop steps — TriageLens (Learn AR with SPECS)

**Do these on the Windows laptop. Lens Studio does not run in the Linux
sandbox. Estimated: setup 1–2 h, interview 20–30 min, build 30+ min,
video + submit ~1 h. Deadline: Tue 10 Nov 2026, 03:30 IST.**

Free-only: Lens Studio, CLAD, the skill pack, Devpost, and YouTube are all
free. If anything asks for a card or payment, stop and report it.

## 0. Before you start (10 min, in the browser)

- [ ] Watch the short concept video at the top of
      https://learn-specs.devpost.com/ — it covers the design ideas the
      judges look for.
- [ ] Open the Quick Start on the Resources tab:
      https://learn-specs.devpost.com/resources

## 1. Install Lens Studio (Windows)

- [ ] Download and install Lens Studio from Snap.
- [ ] If Lens Studio **5.24** will not sign you in to the developer
      platform, use **Lens Studio 5.23.2** instead (link on the Resources
      tab: ar.snap.com). Do not fight the sign-in — 5.23.2 is the documented
      fallback.

## 2. Install CLAD for your coding agent

- [ ] Follow Snap's setup guide for your agent:
      - Claude Code: https://developers.specs.com/docs/clad/setup/setup-ai/claude-code-setup
      - Codex: https://developers.specs.com/docs/clad/setup/setup-ai/codex-setup
      - Cursor: https://developers.specs.com/docs/clad/setup/setup-ai/cursor-setup
- [ ] Confirm CLAD shows up in your agent (names like
      `specs-experience-builder`, `verify-preview`, `specs-leaf-...`).
      If it won't show up, see
      https://developers.specs.com/docs/clad/troubleshooting/troubleshoot-lens-studio-plugin

## 3. Create the SPECS project

- [ ] In Lens Studio choose **SPECS**, then **Base Template**, then
      **File > Save As**. Lens Studio saves it as its own folder (with the
      `.esproj` file and `.mcp.json` inside). Remember this folder — it
      becomes the public repo.
- [ ] Copy this scaffold's `devpost/design-brief.md` into that project
      folder, at `devpost/design-brief.md` (create the `devpost/` folder).
      It is a draft — the interview below confirms or changes it.

## 4. Start your agent in the project folder + install the skill pack

- [ ] Start your coding agent IN the project folder (the one with the
      `.esproj` and `.mcp.json` files), with Lens Studio open. That is
      where the Lens Studio tools load.
- [ ] Check the Lens Studio MCP is connected (`/mcp` in Claude Code
      should show `lens-studio`). If not, restart the agent in this folder
      and approve the `lens-studio` MCP server when asked. Troubleshooting:
      https://developers.specs.com/docs/clad/troubleshooting/troubleshoot-lens-studio-mcp
- [ ] Install the skill pack in the same folder:
      ```
      npx skills add challengepost/learn-specs --all -y
      ```

## 5. Run the interview (20–30 min)

- [ ] Say `plan-lens`. Answer its questions; the draft brief you copied
      in is the starting point — confirm what is right, change what is
      wrong. It writes/updates `devpost/design-brief.md`.
- [ ] When the brief looks good, say so clearly — that approves it
      (status: approved). Do not build from a draft you have not approved.

## 6. Build with CLAD

- [ ] Keep Lens Studio open with this project. In Claude Code, `/mcp`
      should show `lens-studio` connected and `/plugin` should list CLAD.
- [ ] Clear the chat (`/clear`) or start a new chat in the same folder.
- [ ] Paste exactly:
      > Read devpost/design-brief.md and build it for SPECS. Follow the
      > brief closely. Get the basic flow working first, then add detail.
      > Write and run LEAF tests for each done criterion, and tell me
      > which pass.
- [ ] A full build can take 30 minutes or more. When it is done, ask
      which LEAF tests passed and which done criteria have no test.

## 7. Judge it in the preview (the brief's After-the-build section)

- [ ] Open Interactive Preview. Walk with WASD, Q/E to go down/up,
      right-drag (or hold Shift) to look around. Clicking acts as a pinch.
- [ ] Check the five done criteria in the brief, one by one, in the
      preview. Label each "logic proven" or "feel unproven".
- [ ] Fix with design notes, not code (e.g. "Move the checklist 15 cm
      lower. Make the tick buttons twice as big. Re-run the tests.").
- [ ] Confirm the synthetic household is labelled SYNTHETIC on screen.

## 8. Record the demo video (under 3 minutes)

- [ ] Record a screen recording of the Lens Studio preview — OBS Studio
      or Windows Game Bar (Win + G). Follow
      `submission/DEMO_VIDEO_SHOT_LIST.md`. One continuous take if
      possible; no slides, no screenshots assembled as video.
- [ ] Watch the recording back end to end. Check: under 3:00, the full
      flow is visible (household → tick → escalation → visit complete),
      the synthetic label is readable.
- [ ] Upload to YouTube as **Public** (the hackathon requires a public
      video). Keep the link.

## 9. Publish the repo + submit

- [ ] Publish the Lens Studio project folder — with `devpost/` inside it
      — as a **public** GitHub repo. Suggested name: `triage-lens`.
- [ ] Fill the Devpost submission from `submission/SUBMISSION_DRAFT.md`
      (title, description, repo link, video link).
- [ ] Submit on https://learn-specs.devpost.com/ before
      **Tue 10 Nov 2026, 03:30 IST** (event ends Mon 9 Nov, 5:00 PM EST).
      Safe target: Mon 9 Nov, 20:00 IST.
- [ ] After submitting, confirm the Devpost page shows the entry, and
      record the submission link + time in `submission/SUBMISSION_DRAFT.md`.

## If something blocks you

- Lens Studio sign-in fails → use 5.23.2 (step 1).
- MCP not connected → restart the agent in the project folder, approve
  the server (step 4).
- CLAD not visible → re-run its setup guide for your agent (step 2).
- Build stalls or a done criterion fails LEAF → shrink to the basic flow
  first (household → tick → escalation), add detail only after that
  passes. Do not add features to fix a failing core.
- Anything asks for a card/payment → stop, do not pay, report it.
