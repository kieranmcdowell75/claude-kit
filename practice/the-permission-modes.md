# The permission modes

Below the session box there's a mode selector. It decides how much Claude can do
without stopping to ask you. There are five. You'll live in one or two of them.

## Auto

**Claude handles the permission decisions itself**, and stops you for the ones that
matter. You'll still see boxes — just not for every single step.

This is the default, and it's the right one for almost everything. Fast enough to
get work done, and it still comes back to you before anything consequential.

## Manual

**Always asks before making a change.** A box for everything.

Use it when you want to watch every move — a job you don't trust yet, or someone
else's computer. It is genuinely slow. Nobody stays here.

## Accept edits

**File changes go through without asking; everything else still asks.**

Good for a long editing job where you've already agreed what's being changed and
you don't want fifty boxes about it.

## Plan

**Claude cannot change anything on your computer.** It can read, think and talk the
work through. That's all.

Use it when you don't yet know what you want. Scoping a job, thinking out loud,
working out whether something is even possible.

Two things worth doing while you're in it:

- **Make it interrogate you.** *"Ask me whatever you need to understand this
  properly before you propose anything."*
- **Never accept the first plan.** *"Go back over that. What have we missed?"* The
  second version is reliably better.

## Bypass permissions

**Nothing is asked. Claude just does it.**

This is where most people end up, and that's fine — but earn it in Auto first.

**The signal to switch:** when the boxes stop telling you anything. Early on each
one is information — you're learning what Claude does and what normal looks like.
After a week or two you're clicking allow without reading, and at that point the
box isn't protecting you, it's just slowing you down. That's the moment.

It's switched off until you turn it on: **Settings → Claude Code**, then the mode
appears in the selector. It's deliberately a deliberate act.

**What it does and doesn't do.** Bypass turns off the *app's* prompts. It does not
touch your safety rules — those live in your `CLAUDE.md` and hold in every mode:
nothing goes out to another person, nothing gets deleted, nothing is sent on your
behalf. The app stops asking; the rules still apply. That's exactly why switching is
reasonable rather than reckless.

**Go back to Auto for anything you'd want to watch** — a job on someone else's
computer, a first run of something unfamiliar, anything touching money. The mode is
per session, so switching costs nothing.

## Which one, when

```
don't know what you want yet  ──▶  Plan
normal work, starting out     ──▶  Auto        ← the default; start here
want to watch every step      ──▶  Manual
a long agreed editing job     ──▶  Accept edits
boxes stop teaching you things ──▶  Bypass permissions  (turn on in Settings)
```

Setup runs in **Auto**. Not Plan — Plan can't change anything, so the setup
couldn't run at all.
