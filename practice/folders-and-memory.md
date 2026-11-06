# Folders and memory

The single most important thing in this kit, and the one people skip.

## Connect a folder

Click the **+** below the session box, then **Add folder**.

The folder you connect is everything Claude can see. Files inside it can be read
and changed. Files outside it don't exist as far as Claude is concerned. With no
folder connected, Claude can't touch your files at all.

## One folder per business or project

Not per department. Not per location. Not per staff member.

The test: **if two things share the same systems and the same numbers, they belong
in the same folder.**

Two sites running on the same booking software go in one folder together. A
completely separate venture gets its own.

```
Desktop/
├── The Studios        ← both locations, same software, same numbers
├── Property           ← different systems entirely
└── Personal Money     ← nothing to do with the business
```

Never connect your whole Desktop, and never your home folder. Claude then sees
your entire life and everything it learns turns into a junk drawer.

## Memory is saved per folder

This is the part that surprises everyone.

Everything Claude learns about your business is filed against the folder you had
connected at the time. Open Claude on a different folder and none of it loads.
You get a blank slate.

So: **open Claude on the right folder before you start working.** Every time.

That's the trap. For what actually belongs in a memory and how to build one worth
having, see `memory.md`.

## Put house rules in each folder

Make a file called `CLAUDE.md` at the top of each business folder. Every session in
that folder reads it automatically, for you and for anyone on your team.

Don't write it yourself. Say to Claude:

> "Write me a CLAUDE.md for this folder. Ask me what the business is, what systems
> we use, what the common mistakes are, and what you must never do without asking
> me first. Then write it in plain English."

There's a template in this kit at `CLAUDE-md-template.md` if you'd rather start
from something.

## What belongs in house rules

The things that would make Claude confidently wrong if it didn't know them:

- What the business is and what the sites or brands are called
- What each system is actually for, and what each one actually holds
- The traps — the numbers that look right and aren't, and why
- What Claude must never do without asking you first

## Back it up — this is the bit that would actually hurt to lose

After a few months, the valuable things aren't the files. They're the rulings.
Your definitions, your traps, the corrections you've made, the skills you've built.
If your laptop died tomorrow, that's what you'd miss.

Three places hold it, and they're easy to miss because two are hidden:

| What | Where |
|---|---|
| Your business folders | wherever you put them — Desktop, usually |
| Your rules and skills | `~/.claude/` — your CLAUDE.md, your skills folder |
| What Claude remembers | `~/.claude/projects/` |

**The simplest thing that works:** turn on your computer's built-in backup — Time
Machine on a Mac, File History on Windows — and let it run. It covers all three
without you thinking about it.

If you'd rather be deliberate, ask Claude:

> "Make me a copy of my business folder and my Claude setup, somewhere safe, and
> tell me how to do it again."

Do it before any big change, and once a month otherwise.

## Don't confuse this with grouping your sessions

The folders in the left-hand sidebar of the app group your conversations. That's
tidiness. The connected folder is what Claude can actually reach. Different thing,
and the one that matters.
