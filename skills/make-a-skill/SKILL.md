---
name: make-a-skill
description: Turn something that just worked into a reusable skill, so it happens the same way next time without being worked out again. Use when the user says turn that into a skill, remember how to do that, write that up, or make that repeatable - and after any system is connected, any report is built, or any fiddly process is finally cracked.
argument-hint: "(optional) what the skill should cover"
---

# Make a skill

A skill is a short set of instructions Claude reads when a particular kind of job
comes up. It is how a thing that worked once becomes a thing that works every time.

## Only make one from something that actually happened

The good ones come from real work just completed, while the detail is still here in
the conversation. Go back through what was actually done — the wrong turns included.

If asked to write a skill for something that hasn't been done yet, say so. That
produces a plausible-sounding document that falls apart the first time it's used.

**Worth a skill:** a system connected, a report built, a process with an order that
matters, anything that took more than one attempt to get right.

**Not worth a skill:** a one-off question, something the software's own help page
covers, anything that'll be different next time anyway.

## The description is the hard part

Two parts to a skill. The body is what to do. The description decides whether it
ever gets read at all.

Write the description in **the words the user would actually say**, not the words a
technical person would file it under.

| Weak | Strong |
|---|---|
| "Xero integration utilities" | "Get at invoices, bills, contacts and the chart of accounts in Xero. Use when someone asks about money owed, money out, or what's in the accounts." |
| "Reporting module" | "Build the Monday numbers for the week just gone. Use when someone asks how last week went, or wants the weekly figures." |

Rules for it:

- Say **what it does** and **when to use it**, in one or two sentences
- Include the phrases someone would really type — "how did last week go", "who owes us money"
- Name the actual products, by their exact names
- No jargon the business owner wouldn't use themselves

## The body

Short. A procedure, not an essay. Someone should be able to follow it without
knowing anything about how it was worked out.

Include:

- **What this is for**, in a line
- **What has to be true first** — connected, signed in, on a particular plan
- **The steps, in order**, with the exact names of buttons, menus and pages
- **How to check it worked** — one specific thing to look at
- **The traps** — what looks right and isn't, what breaks, what to do about it
- **What this can't tell you** — every system has a blind spot, and naming it stops
  a confident wrong answer later

Leave out: the story of how it was figured out, anything already in the body of the
software's own documentation, and anything that'll be stale in a month.

## Never put in a skill

- Keys, tokens, passwords, or anything from an account
- Customer names, staff names, or any of the business's actual numbers
- Anything specific to one person's machine

A skill is the instructions. The data stays with the business it came from.

If an example genuinely helps, invent one. Never paste a real row.

## Where it goes

```
~/.claude/skills/<name>/SKILL.md
```

Lower case, hyphens, named after what it does — `connect-xero`, not `xero-utils`.

It's available in any new session. No app restart needed, just start a fresh session.

If the skill only makes sense for one business, put it in that business's folder
under `.claude/skills/` instead, so it doesn't fire for unrelated work.

## Test it before calling it done

Start a fresh session and say the thing a real person would say — the phrase from
the description. If the skill doesn't fire, the description is wrong, not the body.
Fix the description and try again.

Then follow it exactly as written, without the memory of having done it. Anywhere
you have to guess is a gap in the skill.

## When it breaks later

Don't write a second skill. Fix the first one, and add a line to its traps section
saying what happened. A skill that records its own failures gets better every time
it's used.
