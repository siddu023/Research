# RS Fuels Flagship — Agent Team Workspace

Cost-planning workspace for the RS Fuels flagship station (gas + c-store + express tunnel wash + vacuums + EV), run by a Claude Code agent team: **architect, planner, procurement, auditor**.

## Files

- `CLAUDE.md` — the project brief every agent reads automatically
- `.claude/settings.json` — enables the experimental agent-teams feature
- `.claude/agents/` — the four specialist definitions
- `work/` — each agent writes its working file here
- `FLAGSHIP-PLAN.md` — the final deliverable (created by the team)

## How to run it from your phone

1. Push this folder to a GitHub repo (see below).
2. Claude app → **Code** tab → **New Session** → pick this repo, `main` branch.
3. Paste the kickoff prompt below and start the session. Check in whenever; answer questions when agents ask.

## Kickoff prompt (copy-paste)

```
Read CLAUDE.md. Set up an agent team using the four definitions in
.claude/agents/ (architect, planner, procurement, auditor).

Phase 1 — parallel research: architect, planner, and procurement each
produce their work/ file per their definitions, web-verifying every
number. Auditor starts independently re-pricing the ten largest cost
drivers and building the comps bridge (QT/7-Eleven listings vs
ground-up replacement cost).

Phase 2 — challenge round: auditor posts line-by-line challenges;
each agent must defend with dated sources or revise. Argue in the
shared task list until each item is resolved-by-evidence or logged
as an open risk. No silent averaging.

Phase 3 — synthesis: produce FLAGSHIP-PLAN.md per the deliverable
spec in CLAUDE.md, including the final all-in ex-land range, equity
check, comps bridge table, value-engineering menu, schedule, financing
plan, and honest open-risk list.

If agent teams isn't available in this environment, run the same
three phases using the four agents as subagents, with you (the lead)
routing the auditor's challenges to each agent for rebuttal until
resolved.
```

## Getting this onto GitHub from your phone

- github.com in your phone browser → New repository → `rs-fuels-flagship` (private)
- Easiest upload path: in the new repo, "uploading an existing file" → upload the zip's contents (GitHub's web uploader can't take a zip directly, so upload the files/folders from the extracted zip; the GitHub mobile app or a Files-app Git client also works)
- Note: folders starting with `.` (like `.claude/`) can be finicky in the web uploader — if it skips them, create the files manually with "Add file → Create new file" and type the path `.claude/settings.json` etc., pasting the contents.

## Cost warning

Agent teams runs multiple Claude instances and uses several times the tokens of a normal session — expect it to consume a meaningful chunk of your plan's usage limits in one run. The subagent fallback is significantly cheaper.
