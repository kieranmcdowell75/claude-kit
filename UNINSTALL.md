# Removing it, or resetting a machine

Two reasons you'd be here: you've tested on a machine and want it clean again for
someone else, or you want Claude off a computer entirely.

## Before you delete anything

**Check whether the person already had Claude.** If they did, their own work is in
the same folders and you'd be deleting that too.

Ask Claude on that machine:

> "Is there anything in my Claude setup that was here before today? Check my
> CLAUDE.md, my skills folder and my saved memory, and tell me what you find
> before I delete anything."

If it finds anything that isn't from the kit, stop and move it somewhere safe first.

## Resetting a machine for someone else to try

This puts it back to never-had-Claude, which is what you want before a second
person tests it.

**1. Remove Claude's settings, skills and memory.** All of it lives in one hidden
folder. Ask Claude:

> "Delete the whole .claude folder in my home directory. I've checked there's
> nothing in it I need."

That takes out the house rules, the fourteen skills, and everything it remembered.

**2. Delete the business folder** that the setup created — wherever you told it to
put one. Drag it to the bin.

**2b. Check Downloads for a leftover installer folder.** An older build left the
Node and Python installers behind in a folder called something like `claude-setup`.
They're just installer files — nothing of yours, nothing the setup needs any more.
Bin the folder. (Current builds delete them automatically, so you'll only see this
on a machine set up before that.)

**3. Sign out of the Claude app.** Click your name, bottom left, then sign out. The
next person signs in as themselves.

**4. Re-unzip the kit** onto the Desktop, fresh.

**Your old sessions will still be listed down the left, and that's normal.** That
list belongs to the app and your account, not to the kit — signing out and back in
brings it straight back. **It does not mean the wipe failed.** A new session won't
read any of them, so it changes nothing; archive them if the clutter bothers you.

**What proves the wipe worked** is the three things the kit actually installed. Ask:

> "Check whether anything from a previous Claude setup is still here: a CLAUDE.md in
> my home folder, anything in my skills folder, and any saved memory. Tell me exactly
> what you find."

Clean looks like: no CLAUDE.md, no skills, no memory. Anything with content in it
and the reset didn't take.

**What stays, and why it's fine:** Node and Git remain installed. They're harmless
background tools. The only difference is the next person's run will skip that step,
so you won't be testing it twice — worth knowing, not worth undoing.

## Removing it completely

Steps 1 to 3 above, then:

- **Delete the Claude app** — drag it from Applications to the bin
- **Delete the Claude Kit folder** from the Desktop
- **Cancel the subscription** if there is one, in your account settings on the web.
  Deleting the app does not cancel anything.

## What you can't delete from here

Anything that was connected to Claude stays connected until you remove it at the
other end. If you joined it to your accounting, your till or your email, go into
each of those and revoke the access.

Ask before you start:

> "List everything this Claude was connected to, so I know what to disconnect at
> the other end."

Do that **before** deleting the `.claude` folder, or you'll lose the list.
