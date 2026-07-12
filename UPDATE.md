# UPDATE — Solnest Cinematic Director (Claude reads this)

**You are Claude. The user pasted this repo's link and asked you to update their Solnest Cinematic Director. Do it FOR them, in plain language. Never paste a raw error at them.**

---

## Step 0 — Find their install

- macOS / Linux: `~/.claude/skills/solnest-cinematic-director/`
- Windows: `%USERPROFILE%\.claude\skills\solnest-cinematic-director\`

If that folder isn't there, they never installed it. Tell them to grab the zip from the Skool community and drag it in for a fresh install, and stop here.

## Step 1 — Check if they even need this

Compare `VERSION` in their install to `VERSION` in this repo. If they match, say so and stop:

> You're already on the latest version (`X.Y.Z`) — nothing to update. You're good.

## Step 2 — What to preserve

**Nothing inside the skill folder.** This skill runs on connected tools (Higgsfield, Firecrawl, Descript), and those connections live in Claude's own settings — not in here. The update doesn't touch them, and the user will **not** need to reconnect anything.

## Step 3 — Pull the latest

```bash
git clone --depth 1 https://github.com/Solnest-AI/solnest-cinematic-director.git /tmp/solnest-cinematic-director-update
```

No `git`? Download `https://github.com/Solnest-AI/solnest-cinematic-director/archive/refs/heads/main.zip` instead.

## Step 4 — Copy the new files over

Copy the fresh files into their skill folder, **file over file**. Don't delete the folder first — just overwrite what's changed.

## Step 5 — Confirm it landed

Check `SKILL.md` is still at the install path and `VERSION` now shows the new number.

## Step 6 — Tell them what changed

Read `CHANGELOG.md` from the fresh copy and give them two or three plain-English bullets for the **new version only** — not the whole file. Then:

> Updated to `X.Y.Z`. Nothing else to do — just use it like normal.

## If something goes wrong

Tell them in one friendly sentence. Nothing here is destructive — they can always reinstall from the Skool zip.
