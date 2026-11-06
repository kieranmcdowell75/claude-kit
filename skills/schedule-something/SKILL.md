---
name: schedule-something
description: Set up a job that runs on its own - a weekly report, a daily check, a Monday morning email - without anyone opening Claude. Use when the user says every Monday, each morning, automatically, on a schedule, send me this weekly, or asks for a report that arrives without them asking for it.
argument-hint: "(optional) what should run, and when"
---

# Schedule something

Turning a thing you asked for into a thing that arrives.

## Ask three things first

Don't guess any of these. Getting them wrong builds the wrong job.

1. **What exactly runs?** It must already work when run by hand. Never schedule
   something that has not produced a correct result at least once.
2. **When?** Day and time, in their words. "Monday morning" means asking whether
   that's 6am or 9am, because it changes whether the computer is awake.
3. **Where does the result go?** An email, a message, a file in the folder? "It
   runs" is not useful if nobody sees the output.

## The fork that decides everything

**Does this job need anything on this computer?** Their Xero connection, their
till, their browser sign-ins, files in their folder — any of it.

| | Needs this computer | Needs nothing local |
|---|---|---|
| Where it runs | On their machine | In the cloud |
| Computer must be on | **Yes** | No |
| Can reach their connected systems | Yes | No |
| Set up via | Routines → New routine → Local | Routines → New routine → Cloud |

Almost every useful business report needs the computer, because that's where the
connections live. Assume local unless it genuinely only needs the open internet.

## Say the awkward part out loud

If it runs locally, **the computer has to be awake at that time.** A closed laptop
is asleep, and a sleeping laptop runs nothing.

Say this before building, not after the first Monday it silently doesn't happen.

The realistic options, in order:

1. **Pick a time the machine is already on.** 9am on a workday beats 6am.
2. **Leave it plugged in and stop it sleeping.** Fine on a desktop or a laptop
   that lives on a desk. Use `keep-it-awake` — it sets this up properly, on-power
   only so it can't flatten a battery.
3. **An always-on machine.** An old Mac left running at the office or at home. The
   proper answer if the job really matters.

## Build it so it cannot fail quietly

The worst outcome is not a job that breaks. It's a job that breaks and nobody
notices for a month, while decisions get made on a report that stopped updating.

Three things, every time:

- **Say when it ran.** The output carries the date and time it was produced, at
  the top. Then a stale one is obvious.
- **Say when there's no data.** "No sales recorded for this period" is a result.
  A silent, empty report is a bug that looks like good news.
- **Fail loudly.** If it can't reach a system, it sends a short message saying so.
  Never nothing.

## Watch the first run

Set it for a few minutes from now and watch it go, before setting the real time.

Check: did it run, did it produce the right thing, did it arrive where it was
meant to. Only then set the real schedule.

Scheduling an untested job is the single most common way this goes wrong.

## Tell them how to change it later

Before finishing, in plain English:

- Where to find it — Routines, in the app
- How to pause it, and how to change the time
- What will make it stop working: the computer off, a system disconnected, or
  someone changing a password on an account it uses

## Then write it up

Use `make-a-skill` so the job is repeatable for the next business, and so there's
a record of what it does, what it needs, and what breaks it.
