# When something isn't working

Start here before asking anyone. Most of it is one of the things below.

## First, always

Open a session and type:

> /check-it-worked

Ten lines come back telling you what's working and what isn't. Anything with a
cross on it, say so in that same session and it'll fix what it can.

If that command does nothing at all, the skills didn't install — see the first
entry below.

---

## "I typed /check-it-worked and nothing happened"

The skills aren't installed, or you're in the session that installed them.

Skills only become available in a **new** session. Start a fresh one and try again.

Still nothing? Say to Claude:

> "Are the kit's skills in my skills folder? There should be fourteen. If any are
> missing, copy them out of the Claude Kit folder."

## "It's not talking to me the way it's supposed to"

The reply format went in after this session started. Start a new session — it'll pick it
up.

If it's still not following it, say:

> "Check my CLAUDE.md in my home folder for a 'How to reply' section. Is it there,
> and are you following it?"

## "I connected something and Claude can't see it"

New connections need the **whole app** restarted, not just a new session.

- **Mac:** press Cmd + Q, then reopen Claude from the dock.
- **Windows:** click the small arrow near the clock, right-click the Claude icon,
  choose Quit, then reopen.

## "It can't see my files"

Nothing is connected, or the wrong folder is.

Click the **+** below the session box and check which folder is listed. Claude can
only see inside the folder you've connected — everything outside is invisible to
it.

## "It's forgotten everything about my business"

You're in a different folder. Memory is saved against the folder you had connected
when it learned something.

Check the + below the session box. If you're in the wrong one, switch back.

## "It's gone stupid — repeating itself, losing the thread"

The session is full. Look bottom right: there's a circle that fills as a conversation
grows.

Type `/handover`, then start a new session and say *"read HANDOVER.md and carry on."*

Don't push through it. The last stretch of a full session costs more and gives worse
answers.

## "It's asking permission for everything" / "It's not asking me anything"

That's the mode selector below the session box.

- **Auto** handles the small decisions itself, asks about the ones that matter
- **Manual** asks before every single change
- **Accept edits** waves file changes through, still asks about everything else
- **Plan** can't change anything at all
- **Bypass permissions** asks nothing — switched off unless you enable it in settings

Your safety rules apply in all three, so even in Bypass it won't email a customer
or delete anything.

## "It says it can't connect to my software"

Sometimes true, sometimes not. Ask it directly:

> "Which of the ways in did you try, and what exactly happened with each one?"

The three common dead ends:

- **The plan doesn't include it.** Many systems lock access to higher tiers. That's
  a billing question, not a Claude one.
- **No route in that Claude could find.** That's not the same as impossible — it
  usually means no API on your plan, no export, and no sensible workaround *today*.
  Ask what specifically is blocking it and what would change that. Often it's a
  plan tier or a vendor still building one.
- **The account isn't yours.** If it's a head office or franchisor login, you may
  not have the rights.

## "It keeps making me sign in to the same system"

Check whether it's only that one. If everything else stays signed in, it's that
system, not your setup — some drop their session the moment the browser closes and
there's nothing on your end that changes it.

Ask Claude to note it in the connector index so it stops being a surprise.

## "A box appeared asking to access my Documents / Desktop / Downloads"

That's your Mac, not Claude, and it's normal. macOS asks the first time any app
reaches into one of those folders, and it keeps asking until you answer.

**Allow it if the work is in that folder.** Your business folder, the kit, a
spreadsheet you've asked about — those need access and nothing happens without it.

**Deny it if it isn't.** If you're working on the Desktop and it asks for Documents,
it doesn't need Documents. Denying is safe; you can always allow it later from
System Settings → Privacy & Security → Files and Folders.

**Either way, tell Claude what you chose** so it isn't left guessing why something
failed.

## "It's refusing to do something I think it should do"

Two different things, and it's worth knowing which.

**If it's asking permission**, just give it. Say what you want and that you're
happy for it to go ahead — it'll carry on.

**If it says it won't, because of a rule**, ask which rule and where that rule
came from:

> "Which rule is stopping you, and did I set it or did you decide it?"

The ones you set are in your CLAUDE.md and they're yours to change. **Anything it
decided itself and saved is not a rule** — it's a note from one conversation that
had half the picture, and it shouldn't be refusing on it:

> "That's a note you wrote, not a rule I set. Drop it and carry on."

It should then do the job and not argue. If a note like that is making it refuse
things, it's worth saying so to whoever gave you the kit — that's a fault in the
kit, not in your setup.

## "It worked for months and now it doesn't"

Usually the vendor changed something. Ask:

> "Has that site changed since last time? Tell me what's different and whether it
> affects what the numbers mean."

Claude can usually work around a moved button on its own. What it should **not** do
is guess at a renamed field — if it tells you it's stopped because something might
mean something different now, that's it working correctly, not failing.

## "The numbers look wrong"

Good instinct. Check it against a period you already know, and say so:

> "That doesn't match what I remember for [month]. Walk me through exactly where
> that number came from and what you counted."

Usually it's a definition difference, not a mistake — something counted differently
than you assumed. Worth finding out which.

---

## When none of this helps

Run `/check-it-worked`, copy the block it gives you at the end, and send that to
whoever gave you this kit along with:

- What you were trying to do
- What you expected
- What actually happened, word for word

Those four things together are usually enough to solve it without anyone looking at
your screen.

## Once it's solved, say this

Whatever the problem was, if it took real time to work out:

> "Write that up as a known issue."

Claude writes a short file into the `known-issues/` folder in the kit — what you
saw, why it happened, what fixed it. Send that file to whoever gave you the kit.

It takes you thirty seconds and it means the next person doesn't lose the same
afternoon. It's also how the kit gets better, and there's no other way it does.
