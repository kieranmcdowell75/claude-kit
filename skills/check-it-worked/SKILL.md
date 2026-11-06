---
name: check-it-worked
description: Check the Claude setup is actually working and say in plain English what is wrong if it isn't. Use when the user says it's not working, something's broken, did that work, check my setup, or has just finished installing and wants to know they're ready.
---

# Check it worked

Turn "it didn't work" into a specific line someone can act on.

Run every check. Do not stop at the first failure — the whole point is one complete
picture rather than a dribble of problems.

## The checks

Work through all ten. For each, report one line: a tick or a cross, what it is in
plain words, and the actual finding.

**1. A folder is connected**
Is there a working folder? Name it. No folder is the single most common failure and
nothing else matters until it's fixed.

**2. The folder has house rules**
Is there a `CLAUDE.md` at the top of that folder? Say whether it looks filled in or
still has template placeholders in it.

**3. The reply format is installed**
Does `~/.claude/CLAUDE.md` exist and contain a "How to reply" section? If it's there
but replies haven't been following it, say so — that usually means the session
started before it was added.

**4. The kit's skills are present**
Look in `~/.claude/skills/`. Report which of these are there and which are missing:
`interview-me`, `connect-anything`, `build-a-report`, `schedule-something`,
`make-a-skill`, `handover`, `check-it-worked`, `build-a-dashboard`, `draft-a-reply`, `learn-my-documents`, `pressure-test`, `keep-it-awake`, `list-my-systems`, `run-a-promotion`. That's fourteen.

**5. Git is installed and knows who they are**
Check `git --version`, then `git config --global user.name` and `user.email`. Blank
name or email is a real failure — it stops work being saved later, with a confusing
message. Offer to set it.

**6. Node and Python are installed**
Check `node --version` and `python3 --version`. Node runs most connections; Python
is what scripts get written in. On a Mac, a Python that came only from Xcode's
command line tools is not enough — say so if that's all there is.

**7. A browser can be driven**
Try opening a page and reading it. Needed for any system without a ready-made
connection, which is plenty of them. If nothing can, say so and offer to install
Playwright — `connect-anything` has the command. Fixable in two minutes, and much
better known now than mid-connection.

**The app has its own browser, so on most machines this passes without anything
being installed.** If it doesn't, say so plainly rather than reporting it like a
fault they caused, and offer the Playwright install in the same breath.

**8. Something is actually connected**
List the systems this Claude can reach. If the answer is none, say so plainly —
the setup is complete but it can't see their business yet, and connecting is the
next job.

**9. Files can be written**
Write a small test file into the connected folder, read it back, delete it. If this
fails it's a permissions problem and nothing else will work.

**10. Memory is being kept**
Is there anything saved for this folder yet? On a fresh install the answer is no and
that's fine — say it's expected, not a fault.

## How to report it

Ten lines, then a verdict. No preamble.

```
✅ Working folder      Desktop/The Cafe
✅ House rules         CLAUDE.md found, filled in
❌ Reply format        not installed
✅ Skills              all 14 present
❌ Git identity        installed, but no name or email set
✅ Node and Python     v24.19.0 and 3.12.7
✅ Browser             can open and read a page
❌ Connected systems   none yet
✅ Writing files       fine
⬜ Memory              nothing saved yet (expected on a new setup)
```

Then:

- **If everything passed:** this is the moment it goes from installed to theirs,
  so land it properly. Say they're set up in a line, then **go straight into the
  systems list in this same session** — don't send them off to another one for a
  two-minute job:

  > *"You're set up. While we're here, let's take two minutes and get down what
  > your business runs on — then we can start connecting things one at a time."*

  Then follow `list-my-systems` and finish the job here. That skill ends by
  pointing them at their first connection, which is the right next session.

  No feature tour, no reading list.
- **If anything failed:** list only the failures, in the order they must be fixed,
  with what to do about each. Offer to fix the ones you can fix yourself.

## Then give them the copyable block

This is the part that makes the skill worth having. End with a block they can paste
to whoever is helping them:

```
SETUP CHECK — <date and time>
Computer: <Mac or Windows, and the version>
Claude: <app version if known>

<the ten lines exactly as above>

<on a run where something went wrong, add:
What I was doing when it went wrong:
<their own words, if they said; otherwise leave this line for them to fill in>>
```

**Leave that last line out entirely when every check passed.** A clean report that
ends with "what I was doing when it went wrong:" and nothing after it reads like
something got cut off.

No account names, no keys, no customer data in that block. It's a status report,
not an export.

**If you solved something that wasn't in `TROUBLESHOOTING.md`**, offer to write it
up as a known issue — `known-issues/README.md` says how. Then tell them, in one
line, that it's worth sending to whoever gave them the kit. A finished file gets
forwarded; a complaint doesn't.

**On a test build** — when there's a `report-to.txt` at the top of the kit — also
send this check's result there, as "Setup check result". Send the ten lines and
nothing else: no folder names, no connected account names, no figures. Mention it
the first time in a session, then do it quietly.

## Rules

- **Never say "it should work now" without re-running the checks.** Fix, then check
  again, then say so.
- **Don't bury a failure in reassurance.** A cross is a cross.
- **Plain English.** "Git doesn't know your name yet" beats "user.email unset".
