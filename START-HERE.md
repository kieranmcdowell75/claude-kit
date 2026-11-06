# Start here

However you got here — you unzipped the kit yourself, or Claude downloaded it for
you — the kit is now a folder called **Claude Kit**, inside a folder called
**Claude** on your Desktop. Leave it there. You'll point Claude at that outer
folder in a minute, and you'll come back to the kit later for the guides.

**If Claude downloaded this for you, the setup is already running** and you can
stop reading. It's working through the steps below on your behalf. Come back to
the guides when it's finished.

## Before you paste anything

1. **Install the Claude desktop app.** Always use the app, never the website.
   - Mac: https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect
   - Windows: https://claude.ai/api/desktop/win32/x64/setup/latest/redirect
   - Either link playing up, or on a Windows ARM machine: go to
     https://claude.com/download and it picks the right one.

2. **Create an account and pick a plan.** Pro at $20/month is enough to start and
   includes everything you need. You'll most likely outgrow it on your first real
   build and want Max — but start on Pro and find out for yourself.

   **What this will cost you, all in:** the Claude plan, and nothing else to begin
   with. Some connections have their own small fee — a few business systems charge
   for access, usually around $10 a month — and Claude will tell you before you commit
   to any of them. You do not need to buy anything else to start.

3. **Open Claude Code, not Chat.** Top left of the app there's a toggle. Claude
   Code is the one with `</>` on it. That's where you'll live from here.

4. **Make a new folder on your Desktop called `Claude`**, put this Claude Kit
   folder inside it, then open it: in the bar along the bottom of the
   session box, click **Choose**, then **Open folder**, then pick the `Claude`
   folder — the outer one, not the kit. (A "Choose a folder to work in" card also
   appears on a new session; either works, the bottom bar is more reliable.)

   **A box will ask "Trust this workspace?"** It says Claude may read, write or
   execute files in that folder. That is what you want, and it is why the folder
   exists. Click **Trust workspace**, and **Allow** if your Mac then asks for
   permission to the folder.

   Open that rather than your whole Desktop. The folder you open is everything
   Claude can see, and your Desktop probably has things on it that are none of its
   business. Everything Claude does for you will live in here.

5. **Set the mode to Auto** for this first run. It's just below the session box,
   and it's usually already selected. Auto means Claude handles the small
   permission decisions itself and stops you for the ones that matter — so expect
   some boxes, not one for every step. That's normal.

   (If you'd rather approve literally everything, **Manual** does that. It's much
   slower and setup will take a while, but nothing is wrong with choosing it.)

   (There's a guide to all five modes in this kit. Don't use Plan mode for this
   first run — Plan mode can't change anything on your computer, so the setup
   below wouldn't be able to run.)

## What the setup will install

So nothing surprises you. Claude will put three free background tools on your
computer if they aren't already there:

- **Node** — a lot of the connections to accounting and booking systems are built
  on it. Without it, those won't run later.
- **Git** — keeps track of changes to your files so you can go back to how
  something was last week. It'll ask for your name and email, because it won't save
  anything until it knows who you are.
- **Python** — what Claude writes in when it needs to work through your data. Macs
  come with a cut-down version that isn't enough; this installs a proper one.

You never open any of them. They sit in the background. All three are free, all
three are standard, and all three are things a developer would have had on day one
— you just haven't needed them until now.

Downloads can take a few minutes and look frozen when they aren't.

## Then paste this

Copy everything between the lines in and press enter.

---

I'm setting up Claude for my business for the first time. I am not technical.
Talk to me in plain English and do the work yourself rather than handing me
commands to run.

You have the Claude Kit folder available — either connected directly, or sitting
inside a folder that is. Find it, then read these files from inside it first:

- house-rules/reply-format.md — how I want you to talk to me
- house-rules/safety-rules.md — the rules you must always follow
- practice/folders-and-memory.md — how folders and memory work
- practice/the-permission-modes.md — what each permission mode does

The rest of the kit is for later — don't read it now.

Then do this, one step at a time, telling me what you're doing as you go:

0. First, two quick checks so nothing surprises us later.

   **Write these so they can't report a failure.** A check whose honest answer is
   "no" must still finish successfully — if a step shows up labelled *Failed* I
   read that as something being broken, even when you tell me in the next line
   that everything's fine. Have the command report what it found and finish
   cleanly, rather than exiting on a negative answer.

   **How fast is the connection, really?** Not whether the sites answer — **how
   many megabytes a second actually arrive.** Pull a few megabytes from one of the
   places this setup downloads from, time it, and tell me the speed. Hard timeout
   of ten seconds so the check itself can't hang.

   A site answering in a tenth of a second says nothing about throughput: you can
   have a fast ping and a slow pipe, and then a reassuring internet check is worse
   than none. **Don't call the connection healthy on the strength of a ping.**

   Then turn it into a number I can plan around: at that speed, roughly how long
   the Apple developer tools download will take — it's the big one, well over a
   gigabyte. Under about 2 MB/s, say plainly that it will be a long wait, that my
   phone's hotspot is often faster than home wifi, and that it runs in the
   background either way. Then carry on.

   **Then start the long download, before anything else.** Check whether Apple's
   command line developer tools are already on this Mac, or already installing —
   the box often appears on its own when the app is first installed, and I may have
   clicked Install already. If it's running, say so and leave it. **If they aren't
   there and nothing is running, trigger that install now** — it's the one slow thing in the whole setup, over a gigabyte,
   and it's where Git comes from. Starting it first means it downloads while you do
   everything else, instead of being the thing I wait on at the end.

   A box will appear from Apple. Tell me in one line to click **Install** on it, that
   it's the slow one starting early on purpose, that it runs in the background, and
   **not to press Stop**. Then leave it alone and carry on — don't wait for it, and
   don't mention it again until the final checks.

   If they're already installed, say so — that's the single biggest time saving
   there is, and most Macs that have ever run a developer tool already have them.

   **Is anything already here?** Look at my CLAUDE.md, my skills folder and my
   saved memory, and tell me what you found. **Finding an earlier install is not a
   reason to stop** — re-running this is how the kit gets updated. Carry straight on
   and replace this kit's own files and sections. The only thing to be careful of is
   anything that isn't this kit's: other sections of my CLAUDE.md, my business
   folders and their notes, my memory and my connections all stay as they are.

1. Install the reply format AND the safety rules into my CLAUDE.md file at the top
   level of my home folder, exactly as those two files say. If a section with that
   name is already there, replace just that section and leave everything else
   alone. Tell me when it's done, and follow both from your very next reply.

2. Install this kit's skills so I can actually use them. **Describe the result you
   need, then verify it** — this copy has gone wrong twice, both times by putting the
   files from inside each skill folder into `~/.claude/skills/` rather than the
   folders themselves.

   **What correct looks like:** `~/.claude/skills/` contains fourteen *folders*, one
   per skill, and each of those folders contains its own `SKILL.md`. A loose
   `SKILL.md` sitting directly in `~/.claude/skills/` means it went wrong.

   **So after copying, count it.** Fourteen directories, fourteen `SKILL.md` files
   one level down, nothing loose at the top. If it's wrong, clear it out and do it
   again — and tell me only the final result, not the attempts.

   Tell me which ones landed. They become available in a new session — no app
   restart needed.

3. Now ask me the only two things you need, **both in one message**:

   - my full name and email, for Git — it's a label on saved work, nothing more
   - my business name, and what it does in a sentence

   In that same message, tell me what's about to be installed. **Name all three
   separately** — not two of them bundled together:

   - **Git** — already downloading since step 0, in the background. Just say where
     it's up to in a few words; nothing for me to do but leave it running
   - **Node** — about 70 MB from nodejs.org; my Mac will ask for my password
   - **Python** — about 70 MB from python.org; my Mac will ask for my password
     again

   Skip any that are already installed, and say which you're skipping. Then finish
   with one line: once I reply, you'll install them.

   **This is a heads-up, not a request for permission.** I already agreed by
   pasting this prompt. Don't ask whether to install them.

4. Once I've replied, install whatever's missing and set my name and email in Git.

   **Apple's developer tools are already downloading from step 0.** Don't start
   them again and don't wait on them.

   **One download at a time.** Don't pull Node and Python while the Apple one is
   still going — they share the same pipe, so everything gets slower and every
   countdown gets less honest. Do the work that needs no download first, then fetch
   Node and Python once the big one is through, or straight away if Apple's tools
   were already installed. If Git still isn't there by
   the end, set my name and email the moment it arrives and carry on without it —
   nothing else in this setup needs it.

   On a Mac the built-in Python is a cut-down one — if that's all there is, install
   a proper version. Don't install Homebrew just to get one of these — download the
   tool directly. Homebrew is a big thing to add for a small reason, and plenty of
   Macs don't have it.

   **Never ask me for my password, and never take it in the chat.** It goes in my
   Mac's own box, nowhere else. If a box is waiting for me and I haven't noticed,
   say so.

   **Don't tell me to ignore a box you'll later need me to click.** If Apple's
   developer tools box is already open, that's the one Git needs — say so the first
   time you mention it, not after telling me to leave it alone.

   **On Windows:** after installing something, this session won't know it's there
   until the PATH is refreshed — refresh it and check the version in the same
   command, because a new shell loses the refresh. If it still isn't found, have
   me fully quit and reopen Claude, and I'll tell you when I'm back.

   Downloads can take minutes and look frozen when they aren't — tell me that's
   normal before you start.

   **Clean up after yourself.** When the installers have run, delete the files you
   downloaded. Don't leave them in my Downloads and tell me I can bin them — that's
   handing me a job, which is the one thing this kit is supposed to stop.

5. Make the folder for my business **inside the same `Claude` folder, beside the
   kit** — so I end up with `Claude/Claude Kit` and `Claude/<my business>`. Create
   it now while this kit is still connected. Tell me where you put it.

   Putting it beside the kit rather than somewhere else means you can still read
   the kit's guides later, when I'm working in my business folder.

   Put a short `CLAUDE.md` in it with just what you know so far: the business
   name, what it does, and a note that the rest gets filled in later. Don't
   interview me now — that's a separate conversation and setup should finish fast.

6. That's your work done. Now give me the last step, as **one instruction** — but
   only after the checks below have passed.

   Tell me to start a brand new session, and **before I type anything**, to open my
   business folder the same way I opened the Claude folder: **Choose** in the bar
   along the bottom, then **Open folder**, then pick it.

   **Not the + beside the message box.** That attaches a folder to one message as
   something to look at; it doesn't change which folder the session is working in.
   The bottom bar is the one that does, and it's the one that matters — the check's
   first question is which folder is open, and memory is saved against it.

   **Say clearly: don't send a message until the folder is picked.** If it isn't
   set first, the check runs against the wrong place and the answers come back
   confusing. Also warn me that picking a folder doesn't appear to do anything —
   that's normal, there's nothing to wait for.

   Then tell me to paste this and press enter:

   *"I've just finished setting up, check everything's working."*

   Explain the two files while you're at it: the CLAUDE.md in my home folder is how
   you behave everywhere; the one in my business folder is about this business.
   Two files, same name, different jobs.

   **Warn me that it will ask me one question at the end of that check**, if this
   is a test build with a `report-to.txt` in the kit folder: whether to send the
   check result back to whoever gave me the kit. Say yes. It asks once because the
   report carries my name and goes to an outside address, and that is worth a
   human yes the first time. Nothing is broken — tell me now so I'm not surprised
   by it later.

   The skills you installed in step 2 only wake up in a new session, so you can't
   run that check yourself from this one. Tell me that's the last thing I do, and
   what a good result looks like — ten lines, mostly ticks. The two blanks are the
   things that really are empty on a new setup: nothing connected yet, nothing
   saved to memory yet.

Before you tell me you're done, check your own work and show me the list:

- the reply format and the safety rules are both in my CLAUDE.md, once each
- all fourteen skills are in my skills folder
- Node and Python answer when you ask their version
- Git either answers, **or is still installing** — if Apple's developer tools are
  still downloading, say so plainly and treat that line as fine. Git isn't needed
  for anything else in this setup or for connecting my systems; it's for file
  history later. Don't hold setup open waiting for it
- Git knows my name and email (or will, the moment Git finishes installing)
- my business folder exists, with a short CLAUDE.md in it
- **nothing you installed contradicts anything else you installed** — read back the
  house rules you put in my CLAUDE.md against each other and against any other file
  this setup created, and tell me if two of them pull opposite ways. A rule that
  quietly cancels another is the one fault I'd never find by using it

**Anything that doesn't pass, fix it with me now rather than mentioning it and
moving on.** No limit on attempts. Don't tell me setup is complete while a line is
still failing.

Stop there. **Don't ask me about my systems and don't connect anything** — that's
the next session, not this one. Don't install anything else and don't go looking for
extra tools.

---

## What happens next

You'll have Claude talking to you properly, a folder set up for your business, and
a plan for connecting your systems.

**One thing to know about the folders.** By the end of setup, Claude will be
pointed at your *business* folder, not this kit. That's correct — that's where your
work happens.

The guides in this kit are files for **you** to read, not Claude. They're sitting
in the Claude Kit folder, inside the Claude folder on your Desktop — open them
the way you'd open any
document. Nothing needs to be connected for that.

Start with `practice/where-to-start.md`. It's what to connect and in what order,
then what to build first — with the prompts to use, grouped by which systems each
one needs.

If you ever want Claude to read one of them with you, point it at the file and it
will.

The fourteen skills are now installed. You don't need to learn them — they fire when
they're relevant. The one worth remembering is `/handover`, for when a session gets
long and you want to carry on in a fresh one.

## If you get stuck

Paste the exact error back in and ask what's going wrong and what the
options are. If it's stuck twice on the same thing, start a fresh session and say
what you already tried.

There's a `TROUBLESHOOTING.md` in this kit covering what usually goes wrong. Worth
a look before asking anyone.
