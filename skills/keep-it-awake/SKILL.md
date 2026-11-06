---
name: keep-it-awake
description: Stop the computer sleeping through a scheduled job or a long task, and set up simple on/off commands for it. Use when a scheduled report didn't run, when someone asks why nothing happened overnight, before setting up anything that runs on a schedule, or when a long job needs to survive them walking away.
---

# Keep it awake

A sleeping computer runs nothing. This is the single most common reason a
scheduled job silently doesn't happen, and people usually blame the job.

## Say the three-tier reality first

Most people think "sleep settings" is one switch. It's three situations, and only
two of them are fixable.

| | What happens | Can it be fixed |
|---|---|---|
| **Plugged in** | Sleeps on a timer unless told otherwise | Yes, and it's the one to set up |
| **On battery** | Sleeps within minutes of going idle | Yes, but only on purpose and temporarily |
| **Lid closed** | Always sleeps | **No.** Not on a laptop without an external display |

**Say the lid one out loud.** Someone who closes their laptop and expects a 7am
report is going to be disappointed, and no amount of settings will change it.

## Set it up

**1. Two commands, so it's one word either way.**

Write two small scripts into their `~/.local/bin`:

- One that keeps the machine awake until told otherwise, taking an optional
  duration — an hour, ninety minutes, until they stop it
- One that undoes it

Make the "undo" one **narrow**. It should stop only the general keep-awake, never
a long job that wrapped itself in its own keep-awake. Killing someone's two-hour
job because they wanted their screen to dim is a bad afternoon.

Tell them the two words. That's the whole interface.

**2. The plugged-in guarantee, set once and forgotten.**

A login item that keeps the machine awake **only while on power**. On a Mac that's
a small file in `~/Library/LaunchAgents` — no password needed, and Claude can do
it directly.

**Only while on power matters.** An always-on keep-awake will flatten a battery in
a bag. On-power-only can't.

**3. The bit Claude can't do.**

Changing the operating system's own sleep settings needs their password. Point them
at it rather than trying:

- **Mac** — System Settings → Battery → Options, and Lock Screen for display timing
- **Windows** — Settings → System → Power, set "plugged in" to never sleep

Tell them exactly which toggle and why, then let them do it.

## When a scheduled job didn't run

Check in this order, because it's almost always the first one:

1. **Was the computer awake?** Lid closed, or on battery, or shut down.
2. **Was it on?** Different from asleep, and people forget they shut it down.
3. **Did the job itself fail?** Only worth looking once the first two are ruled out.

## Say when this isn't the answer

If something genuinely has to run while the computer is off, keeping it awake is
the wrong fix and they should hear that plainly. The options then:

- **Move the job somewhere that's always on.** An old laptop or a small machine
  left running at home or the office is the usual answer and costs nothing beyond
  the power.
- **Run it in the cloud instead**, if the job doesn't need anything on this
  computer — no local files, no connected systems, no sign-ins. That rules out
  most business reporting, which is exactly why it usually ends up local.
- **Accept it runs when they open the laptop** rather than at a set time. Often
  completely fine for a weekly report.

## Pair it with scheduling

When `schedule-something` sets up a recurring job, this is the step that makes it
actually happen. Doing one without the other is how people end up with a report
that works on Tuesdays and not Mondays.
