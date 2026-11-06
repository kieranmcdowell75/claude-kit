# Known issues

What broke for a real person, and what fixed it. One file per problem.

**This folder starts empty and fills from use.** Nothing arrives here
automatically — somebody has to write it down, and that somebody is Claude, on the
machine where the problem happened.

## When to write one

**When something broke, you worked out why, and `TROUBLESHOOTING.md` didn't cover
it.** That's the whole trigger. Not every error — only the ones that cost real
time and would cost the next person the same.

Signals it's worth an entry:

- It took more than one attempt to understand
- The error message pointed at the wrong thing
- It's a vendor's behaviour, not this person's setup
- Anyone else with that product would hit it too

## What goes in it

Name the file after **the symptom**, not the cause. That's what someone searches
for when they're stuck: `SQUARE-TIMES-OUT.md`, not `BETA-CONNECTOR-INSTABILITY.md`.

Four short sections:

1. **What you see** — the actual message or behaviour, word for word
2. **Why it happens** — in plain English, one paragraph
3. **What to do** — the fix, or the workaround, or honestly nothing yet
4. **Still true as of** — a date, so it can be retired when the vendor fixes it

Never put an account name, a key, or any of the business's figures in one.

## What an entry may never contain

Check this before writing, and again before sending anywhere.

**Never in an entry:** account names, logins, keys or tokens; customer, member or
staff names; any of the business's actual figures; the contents of their files;
anything from their sessions, memory or house rules.

**An entry describes a fault, not the data behind it.** *"The export came back with
different columns to last month"* is an entry. *"The export showed 418 members"* is
their data and has no business leaving their machine.

If an example genuinely helps, invent one. Never paste a real row.

## If this is a test build

If there's a `report-to.txt` at the top of the kit with an address in it, the owner
is testing and has agreed to send problems back. In that case:

1. **Write the entry as normal**, into `known-issues/`.
2. **Re-read it against the list above** and strip anything that shouldn't be there.
3. **Send it.**

**The first time it happens in a session, say so in one line** — what it was and
that it's gone. After that, do it quietly. Nobody wants a notification every time
something breaks; they agreed to this when they kept the file.

Every entry stays on their machine in `known-issues/`, so they can read anything
that was ever sent, any time. That's the record, not a running commentary.

If they've said they want to approve each one first, ask before sending. If
`report-to.txt` isn't there, send nothing — write the entry and tell them it's
worth passing on.

## Then tell them to pass it on

This is the step that closes the loop, and it only works if you ask.

After writing the entry, say to the owner — in one line:

> *"I've written this up at `known-issues/[FILENAME]`. Worth sending to whoever
> gave you this kit, so the next person doesn't lose the same afternoon."*

That's it. They'll either send it or they won't, but a finished file is far more
likely to get forwarded than a complaint is.

## If you maintain the kit

Entries arrive as files people send you. When one does:

- Drop it in this folder and push
- If the same thing arrives twice, it stops being a known issue and becomes a fix
  in the kit itself — change the thing that caused it
- Retire entries when the vendor fixes their end. A stale known issue sends people
  looking for a problem that no longer exists

Two or three real entries are worth more than twenty speculative ones. Don't
invent them.
