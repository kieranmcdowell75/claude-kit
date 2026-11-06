# Long jobs and handovers

How to stop a good session turning into a bad one.

## The problem

Every conversation has a limit. As it fills up, Claude gets worse — it repeats
itself, loses the thread, forgets what you agreed an hour ago. You'll feel it
before you see it.

There's a gauge for it. Bottom right of the window, next to the model name, there's
a circle that fills as the conversation grows.

## The rule

**When that circle is about three-quarters full, hand over to a fresh session.**

Don't push on to full. That last stretch is where it gets foggy, and you'll spend
more time correcting it than the fresh start would have cost.

## How to hand over

Two words, in the session you're in:

> /handover

It writes everything down into a file called `HANDOVER.md` at the top of your
folder — what you're doing, what's done, what's left, the decisions and why, the
dead ends, and the next thing to pick up.

Then start a new session on the same folder and say:

> "Read HANDOVER.md and carry on."

That's it. Nothing to copy, nothing long to paste, and it works the same every
time. The old handovers are kept, dated, in a `handovers/` folder in case you ever
want to look back.

The new session picks up where you left off, without the fog.

## The bit people get wrong

**Include the dead ends.** "We tried pulling this straight out of the booking system and their plan
doesn't allow it" is worth more than another paragraph about what worked. Without
it, the fresh session will cheerfully try the same thing again.

## Break big work into phases

For anything that'll take more than a sitting, plan it first, then ask:

> "Break that into phases I can build one at a time. Each one should finish with
> something that works."

Then do one phase per session. You get a working thing at each step, and each
session stays well clear of the limit.

## Plan mode

There's a mode selector below the session box. **Plan mode can't change anything on
your computer** — it can only talk the work through with you.

Use it when you're not sure what you want yet. Switch out of it when you've decided.

Two things worth doing in plan mode:

- **Make it interrogate you.** "Ask me whatever you need to understand this
  properly before you propose anything."
- **Never accept the first plan.** Say: *"Go back over that. What have we missed?"*
  The second version is reliably better than the first.
