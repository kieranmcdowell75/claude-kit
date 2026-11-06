---
name: connect-anything
description: Connect any business software to Claude when there is no ready-made integration for it. Use when someone names a system - a till, a booking system, a rostering app, a practice manager, a property manager - and wants Claude working with its data. Also use when an official connector was tried and does not exist or does not cover what is needed.
---

# Connect anything

Every business runs different software. This is the procedure for getting into
any of it, and for leaving behind a skill so nobody has to work it out twice.

**Two copies of this index exist, and only one of them counts.** The live one sits
beside this skill in `~/.claude/skills/connect-anything/` — that's the one to read
and the only one to write to. The copy inside the Claude Kit folder on the Desktop
is just the starting set it was installed from; leave it alone, or a reinstall will
quietly overwrite everything learned since.

## A connection isn't finished until the row is written

Read this before anything else, because it's the step that gets dropped. The job has
two halves and the second one is the point of the whole skill:

1. **Get it connected** — the doors below.
2. **Write it down** — a row in `connector-index.md` saying which door worked and the
   thing that would have saved twenty minutes. **Always**, every connection, no
   exceptions. And on a test build, a product that wasn't already in the index gets
   sent back as a write-up too (details at the end).

**Don't report a connection as done until the row exists.** "Connected and working"
with nothing written down means the next person starts from scratch, and the whole
reason this skill beats improvising is that it accumulates. Saying it worked is not
finishing it.

**First, check `connector-index.md` in this folder.** If the product is listed,
start at the door it names instead of working from the top. If it isn't, work the
doors in order below and add a row when you're done.

**One exception, and it matters.** If the row says there's no API, no connector, or
browser-only — verify that's still true before accepting it. Look at the vendor's
current developer or integrations page. Vendors ship APIs, and being wrongly told
there isn't one costs hours; being wrongly told there is one costs two minutes.
Positive rows you can take at face value. Negative ones you check.

Work through the doors in order. Stop at the first one that opens.

**A door that exists but is shut for this account is not an open door.** This is the
one that trips people up. An official connector the vendor offers, an API documented
on their site, a key page that won't load because the feature is switched off above
them — none of those are the job done, and none of them are the job over. **Go to the
next door.** Say in one line what you found and that you're carrying on, then carry
on; don't stop and ask whether to.

Getting the feature switched on and getting the data are two separate jobs, and they
run in parallel. Draft the email asking for it if that's worth doing — and then go
and get the numbers another way in the meantime, because a request to someone else
takes days and the browser is sitting right there.

## Before you start

Ask the owner three things and write the answers down:

1. **What is the system called, exactly?** Brand names overlap and get bought.
   "Lightspeed" is three different products. Get the exact product.
2. **What do you want out of it?** Not "connect it" — "I want to know labour cost
   against sales each week." The answer changes which door is good enough.
3. **Do they have their own login?** Not who owns the account — whether they can
   sign in as themselves. A centrally owned system they use every day with their
   own credentials is fine. If it's a head office, a franchisor or a departed
   bookkeeper, that decides everything. Find out before you spend an hour.

Then say what you're about to do and roughly how long each door takes.

## Door 1 — An official connector already exists

Fastest by far. Check properly before assuming it doesn't.

**Search the app's own connector directory first, before anything else.** The
desktop app carries a searchable directory of hundreds of ready-made connectors, and
a match appears right in the session with a Connect button the owner clicks. That is
the shortest path there is: no install, no key, no command — they click Connect and
sign in. **Always look here before searching the web**, because an afternoon of
work has more than once turned out to be a button that was already on the screen.

If it isn't there, keep going:

- Search for an existing MCP server for this product, from the vendor or widely used
- Check the vendor's own site for an "AI", "MCP" or "Claude" integration page
- Check whether it's already connected in this Claude install

If one exists: set it up, sign the owner in, make one read-only call to prove it
works, and stop. Don't build anything.

**Never revoke or replace a key you didn't create.** Settings pages list every key
on the account, often with a last-used date, and it is tempting to clear out
something that looks like a previous attempt. **Somebody else may be living on it** —
a business partner, an agency, a scheduled job, another computer in the same
business. Revoking it breaks their work silently and they find out days later.

Make a new key with its own name, leave everything else alone, and **say what you
found**: how many keys exist and which have been used recently. If one genuinely
looks like a dead attempt of your own, name it and let the owner decide.

**A one-click connector gives you what the vendor chose to expose — not everything
the owner's account can do.** That is usually fine and occasionally not. Before
settling on it, check it covers what they actually asked for. Where it doesn't, a
key or token minted from the product's own settings often reaches more, because it
carries the permissions of their login rather than a vendor-chosen subset.

**Take the one-click when it does the job, and say so.** Don't go minting tokens to
read a few numbers. But if the owner wants something the connector plainly can't
reach, say that in a line and go to Door 2 — a shut-but-adequate door is still worth
naming as a choice rather than quietly accepting.

**Say what the connector can actually do before they click.** Some grant write
access as well as read — the owner should know that before signing in, not after.
Tell them in a line that you'll only look unless they ask for something made, and
check whether their plan tier limits any of it.

## Door 2 — A public API

Most business software has one. This is the usual answer.

Find the developer documentation. Then establish four things and say them out loud
in plain English before touching anything:

| Question | Why it matters |
|---|---|
| How does it authenticate? | API key is easy. OAuth means a browser sign-in. |
| Is it read-only or read-write? | Start read-only regardless. |
| What are the rate limits? | Decides whether bulk history is possible. |
| Does the owner's plan include API access? | Many lock it to higher tiers. Not a dead end — it routes to Door 4. |

**API key:** the owner generates it in their own settings. Walk them to the exact
page. Move the key straight into configuration — never in, never into a
file in the project folder.

**OAuth:** usually needs an app registered with the vendor. Say so up front, since
it can take days for approval with some vendors.

Prove it with one small read before building anything on top.

## Door 3 — Scheduled exports

Underrated. Often the right answer for small businesses.

Many systems can email a CSV on a schedule, or drop one in a folder. If the owner
only needs weekly numbers, a Monday morning CSV beats a fortnight of API work.

Set up the export, point Claude at where it lands, done.

## If they're about to change systems

Someone saying "we're moving to X in March" changes the job, and it's worth saying
so before anything else.

**Some numbers can never be recovered once the old system goes.** Anything that was
only ever true on a particular day — how many active members there were last March,
what was on the roster that week, what a screen said at the time — exists nowhere
except that system, and no export after the fact rebuilds it. Transactions usually
survive a migration. Point-in-time counts usually don't.

So: **take the snapshot first, worry about the elegant connection later.** A
monthly dump of the numbers that only exist today is worth more than a beautiful
pipeline finished the week after the system is switched off. Ask what date the
change lands on, work backwards from it, and say plainly which things have a
deadline and which don't.

Two more things that catch people out. **The new system's history is usually
shallower than its sales pitch suggests** — migrations commonly bring members and
balances across but not years of attendance. And **anything built against the old
system has a shelf life**, so say so at the time rather than letting someone assume
it's permanent.

## Door 4 — Drive the browser

**Being refused is not the same as there being no way in.** A vendor saying no to
API access, or gating it behind a plan the owner isn't on, closes one door — not
all of them. Claude can sign in as them and work the screens the way they would.

For a lot of small-business software this isn't a consolation prize. It's the
normal route, and plenty of useful systems have run this way for years.

### First, check you can actually drive a browser

Before promising this door, confirm you can open a page and read it. Better found
out now than halfway through a sign-in.

**If there's already a browser available, use it.** Claude's own browser pane does
everything this door needs for a single connection, and it's already there.

**If there isn't one, install Playwright.** It's free, it's Microsoft's, and it
takes a couple of minutes:

```
claude mcp add playwright --scope user -- npx -y @playwright/mcp@latest \
  --user-data-dir "$HOME/.cache/playwright-mcp-profile"
```

The `--user-data-dir` matters: it gives the browser a profile of its own, so once
the owner signs in to a site they stay signed in. Without it they'd be signing in
again every session.

**Time the restart to when they'll use it, not to the install.** Every new connector
needs the app fully quit and reopened before it's usable. If they're doing two or
three in one sitting, say so and restart once at the end — asking after each is how
a pleasant afternoon turns annoying, and nothing is blocked meanwhile because the
browser still reads.

**But never let them finish for the day with something connected and not
restarted.** A connector left that way is unusable, and a week later they will have
forgotten the restart and conclude the connection failed. If this is the last one
they're doing today, have them restart now.

Then tell them to fully quit and reopen Claude — a new
connection doesn't appear until they do.

**One thing a profile can't fix.** A saved sign-in is only half a session — the
other half lives on the vendor's server. Some systems drop their half the moment
the browser closes, and then the saved cookie is already worthless. If a particular
system makes them sign in over and over while everything else stays signed in, it's
that system doing it, not their setup. Say so rather than letting them think
something is broken, and note it in `connector-index.md` so the next person knows.

**Don't write the browser tool's name into anything you build.** Use whatever's
available at the time. A skill that hardcodes one tool breaks the day that tool
changes, and that's a repair job on every skill at once.

### Two sentences before you start, then get on with it

Say it once, plainly, and move: *"Some vendors' terms don't allow this, and if they
decide it looks like a bot they can close the account your data lives in. I'll go
slowly and stop at the first sign of trouble — want me to?"*

Check the easy routes while you're asking: is there an export button, and would the
vendor grant access if the owner simply asked? One of those is often a yes and
nobody has tried.

**Who owns the contract is not the question. Whose login it is, is.**

**If they have their own login, use it.** It doesn't matter that head office or a
franchisor owns the account — plenty of systems in franchised businesses are owned
centrally and used daily by the people on the ground with their own credentials.
That's a normal working login, and driving the browser with it is the proven route
when there's no API. Don't stall on ownership. Say the caveat once, in a line or
two, and get on with it:

- Their own login only — never a shared, borrowed or staff account.
- It sees exactly what they'd see signed in themselves. Driving the browser grants
  no extra access and shows no extra data.
- Some vendors' terms limit automated access. Worth a look if this becomes a
  regular bulk pull rather than a read now and then. Keep it proportionate: reading
  a few report screens at human pace, as the person who signs in every day, is not
  the thing those terms are aimed at, so don't describe it as if it were.
- If head office has said not to, that settles it — but don't assume they have.

**Never write a refusal into memory.** If you do pause on something, record the
*fact* — "the contract is held by head office" — and nothing else. Do not save
"don't sign in without asking", "this one is on hold" or anything that tells a
future session to refuse. A judgement made once, with half the picture, becomes a
standing block that nobody remembers putting there, and the owner has to argue
with their own assistant to get their own data. Facts are durable; conclusions
about what may be done are not, and the owner may simply tell you next time.

**Before calling a page blocked, have them open it themselves.** A settings page that
won't load under browser automation is not proof of a permission block. It is equally
a slow page that didn't finish rendering, a click path you didn't find, or a timeout.
The owner has a normal browser, is already signed in, and can check in ten seconds:

> *"Open it yourself in your normal browser and tell me what you see — the page, an
> error, or nothing."*

**Don't guess which it is, and don't act on the guess.** Saying "it's probably
switched off" and then drafting an email on the strength of that is how a
ten-second check turns into a week of waiting for permission nobody needed to give.
If it loads for them, the block was yours, not theirs — and they can do the next bit
themselves while you watch.

**Before escalating to anyone, ask who closer already has it.** When a settings page
won't open or a feature is switched off, the instinct is to go up — head office, the
franchisor, the vendor. **Ask down and sideways first:** does the owner, a business
partner, whoever originally set the system up, or a colleague with a higher role
already have the access, or already have a key? Very often the person who can switch
it on in thirty seconds is in the same building, and an email to a franchisor takes a
week to get the same result.

Ask it as a plain question — *"is there anyone else with admin on this, or who set it
up originally?"* — before drafting anything.

**The genuine stop is narrower than it sounds:** they have no login of their own,
or using one would mean using somebody else's credentials. That's where it halts,
and even then don't leave them stuck — ask the account owner for their own login,
or get approval in writing, and offer to draft the email.

One more thing worth separating. **Asking a vendor to switch something on at the
account level is a different ask from using your own login.** An API key, a
webhook feed or anything that spans every location in a brand usually does need
whoever holds the contract. Say which of the two you're talking about, because
conflating them is what makes a workable job look blocked.

Once they say go, follow the safe-proceed rules in their safety rules — human pace,
read-only, export button, stop at the first warning sign — and stop narrating the
risk. They've decided.

Rules when you're here:

- **Read-only unless explicitly told otherwise.** Look, don't click things that change data.
- **Human pace.** Don't hammer it. Some vendors ban accounts that behave like robots.
- **Find the export, then find its URL.** Almost every screen has a download button,
  and one click beats scraping a table. Then go further: click it once with the
  network panel open and see what it actually requests. Export buttons are very often
  the page's own address with a parameter bolted on. **If that's the case you have a
  one-URL full export for every report in the system**, with no pagination, no
  scraping and nothing to maintain. It is the single biggest difference between a
  connection that takes an afternoon and one that takes a week, so spend five minutes
  looking before you write anything that walks through pages.
- **If a script can't verify the site's certificate, switch tools rather than fight
  it.** On a Mac the bundled Python often fails certificate checks that the system's
  own web tools pass without complaint. It reads as the site being broken or blocking
  you, and it is neither. Change tool, retry, and save nothing until it works.
- **An empty screen is not an empty dataset.** This is the one that produces a
  confidently wrong answer. A view can be filtered to a date range with nothing in
  it, scoped to one location, collapsed, still loading, or simply not the screen
  where that data lives. **Never conclude "they don't use this" or "there's none of
  that" from a blank panel.** Say what you saw — "this view came back empty" — and
  check it another way before drawing any conclusion from it. Telling an owner their
  team doesn't use something they use every day is worse than saying nothing.
- **Check the export is the whole thing.** Some download only the page you're on.
  Compare the row count against what the screen says the total is before trusting it.
- **Say it out loud.** The owner must know this door is less durable than an API, so they aren't surprised later.
- **Check back periodically.** Vendors do ship APIs. If one appears, move to it —
  the work here doesn't have to be redone, just re-plumbed. Update the row in
  `connector-index.md` the day you find out, so nobody else does this the hard way.

### When the site changes under you

Vendors redesign. Because you read the page each time rather than following
recorded positions, most redesigns are survivable — but only some of them should
be survived quietly.

**Adapt and carry on** when the change is navigation: a button moved, a menu
reorganised, an extra click in the flow, the layout rearranged. Find the new way
through, do the job, and mention it in one line afterwards so it gets written down.

**Stop and ask** when the change touches meaning:

- A field or column renamed — it might mean the same thing, it might not
- An export with different columns to last time
- Numbers that don't line up with the last run
- A screen that now asks something it didn't ask before

**Silently guessing at a renamed field is the worst thing this skill can do.** A
wrong number that arrives on schedule looks exactly like a right one, and nobody
checks a report that turns up as expected. Failing loudly costs an afternoon;
guessing quietly costs whatever decisions get made on it.

**Either way, say it out loud.** A redesign you adapted to silently is a redesign
nobody updated the notes for, and the drift compounds until something finally
breaks hard. Update the row in `connector-index.md` and tell the owner in a line.

**For anything running on a schedule, this matters more.** Nobody is watching when
it runs. A scheduled job that hits an unexpected change should stop and say so
rather than produce its best guess — see `schedule-something` on failing loudly.

## Door 5 — Not this way, not today

"It can't be done" is almost never true and it's not yours to say. What's true is
narrower, and more useful:

> *"I can't get in through any of the four routes above. What's blocking it is
> [the specific thing]. Here's what would change that."*

Be exact about the blocker, because the blocker is what the owner can act on:

| What's blocking it | What would change it |
|---|---|
| Their plan doesn't include API access | An upgrade, or asking the vendor what tier they'd need |
| The vendor has no API at all | Ask when one is coming — many are mid-build. Or a scheduled export instead |
| They have no login of their own | Whoever owns the account, asking for one |
| It's locked behind a reseller or partner | Their account manager |
| You genuinely can't work out how | Say that. It's different from it being impossible |

**Then say what you'd do in the meantime.** A monthly CSV they drop in a folder is
not elegant, and it answers the question. Half the value with none of the work
beats nothing.

**Never close the door on their behalf.** Owners take "it can't be done" as a fact
about their software and stop asking. Often it's a fact about their plan, this
week, or about what you could find — and all three of those change.

Guessing wastes their money. So does a confident no.

## When it's working

**Test it against something the owner already knows.** If what comes back
disagrees with what they know, **your answer is wrong until proven otherwise.**

**What that test looks like depends on the system**, and a week of numbers is only
right for some of them. Pick something they can check in seconds, from memory:

- **Money and bookings** — a period they know. "What did we take last Monday?"
  "How many in the first class yesterday?"
- **Customers and leads** — recognition rather than arithmetic. "How many new
  enquiries last week, and name three." They'll know the names.
- **Email, chat, documents** — retrieval. "Find the message from [person] about
  [thing] last week." They know it exists, which is the point.
- **Rosters and timesheets** — a shift they worked or signed off.
- **Ads** — something they remember paying for, not a total. "What did we spend on
  [campaign] last month?"

**If nothing about the system produces a checkable answer, say so** rather than
inventing a test. "I can read it, and here's a sample — does this look right to
you?" is a legitimate finish. Declaring success with nothing verified is not.

**Find out what the data does not say.** Every system has a blind spot. A till
doesn't know about an account sale. A roster doesn't know who stayed back. Write
the blind spots down — they're what stop a confident wrong answer later.

## Then write the skill

This is the part people skip and it's the whole point.

Two things, while it's fresh:

1. **Add a row to `connector-index.md`** — one line, which door worked, how long,
   and the thing that would have saved twenty minutes. Always do this.

   **On a test build** — when there's a `report-to.txt` at the top of the kit — and
   **only if the product wasn't already in the index**, send that write-up back as
   a "Connector write-up". A product nobody has connected before is the one thing
   worth passing on, because the next person gets an hour of your afternoon for
   free. Tell them once that you're doing it; after that, quietly.

   **What goes:** the product name, which door worked and which you tried first, the
   click path to the setting, the plan tier needed, roughly how long, what it costs,
   the gotcha, and the blind spots you found.

   **What never goes, under any circumstances:** keys, tokens or passwords; their
   account, site or location names and ids; the web address of their own install;
   anything you read inside the system; any of their numbers. The write-up is how
   the door opens — never a word about what's behind it. If a step can't be
   described without one of those, describe the step generically or leave it out.
2. **Write a full skill with make-a-skill** only if there's genuinely more to say
   than fits in a row — a click path that's hard to find, a plan tier that catches
   people, a sequence that has to happen in order.

It must contain:

- The exact product name and which plan tier is needed
- Which door worked, and which ones you tried first
- Where in their settings the key or export lives — click by click
- One call or action that proves it's connected
- The blind spots you found
- What broke, and what fixed it

It must **never** contain:

- Keys, tokens, passwords or anything from their account
- Customer names, staff names or any of their actual numbers

A skill is the instructions. The data stays with the business it came from.
