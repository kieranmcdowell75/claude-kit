---
name: handover
description: Write a complete handover into the project folder as HANDOVER.md, so a fresh session can pick the work up with one sentence. Use when the context gauge is filling up, when a session has gone foggy or circular, when picking the work back up tomorrow, or any time the user says handover, hand over, or wrap this up for a new session.
argument-hint: "(optional) what the next session should focus on"
---

# Handover

Write a handover file the next session can read, so the work continues where this
one is — not where it began.

## Where it goes

Write it to **two places in the connected project folder**, with the same content:

1. `handovers/<YYYY-MM-DD-HHMM>.md` — the dated copy, kept forever
2. `HANDOVER.md` at the folder root — always the newest, overwritten each time

Create the `handovers/` folder if it isn't there.

The first line of the file is always:

```
Written <day, date, time>. Folder: <full path>
```

So that anyone opening it later can see straight away whether it's still current.

Because `HANDOVER.md` is always the latest, the user's next session only ever needs
one sentence: *"Read HANDOVER.md and carry on."* Never ask them to copy the body of
the handover.

If there is no connected folder, fall back to putting the whole thing in the session
as a copyable block and say that's what you've done, and why.

**Re-read this conversation before writing.** Do not write from a vague sense of
what happened. Go back through it. The specifics are the point.

**Be specific or leave it out.** "We set up the connection" is worthless.
"Connected the accounting system; the main company works, the second one is a
separate org and is not connected" is a handover.

**The dead ends matter as much as the wins.** Without them the next session will
cheerfully repeat them.

**Never include secrets.** No keys, tokens, passwords, or customer and staff
details. Say "the API key is in the config" — never the key.

**Plain English.** Someone non-technical has to be able to read it.

If the user passed an argument, treat it as what the next session is for, and bias
the detail towards that.

## The shape

Use exactly these headings. Drop any section that would genuinely be empty — never
pad one.

```
HANDOVER — <short project name, the same one used in this session>
Open this folder: <the full folder path to connect>

WHAT WE'RE DOING
Two or three lines. The goal, and why it matters. Not a history.

WHERE IT'S UP TO
✅ <done, specific>
✅ <done, specific>
⬜ <not done yet>
⬜ <not done yet>

DECISIONS WE MADE
- <what was decided> — because <the reason>
- <what was decided> — because <the reason>
Include decisions the user made, not just technical ones.

TRIED AND RULED OUT
- <what was attempted> — <what actually happened, and why we stopped>
If nothing was ruled out, say "Nothing ruled out yet."

THINGS THAT WILL BITE YOU
- <trap, quirk, or thing that looks right and isn't>
The numbers that lie, the system that logs you out, the report that runs late.

FILES AND WHERE THINGS LIVE
- <full path> — <what it is>

STILL OPEN
- <question we could not answer, and who or what would answer it>

NEXT ACTION
One concrete thing, specific enough to start on without asking anything.
```

## What to show in the session

Not the whole thing. Five lines at most:

1. That it's written, and the path to `HANDOVER.md`
2. The two or three biggest things it captured
3. The next action
4. Anything genuinely unresolved they personally need to decide
5. The exact sentence to start the next session with:
   **"Read HANDOVER.md and carry on."**

Nothing else. They can open the file if they want the detail.

## Quality check before you send it

Ask yourself: **if I had only this block and no memory of the conversation, could I
pick the work up?**

If the answer is no, the usual reasons are:

- Vague verbs — "looked into", "worked on", "explored". Say what was found.
- Missing paths. If a file matters, give its full path.
- No next action, or one that needs a decision first.
- The dead ends left out because they felt like failures. They're the most
  valuable part.
