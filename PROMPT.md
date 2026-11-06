# The prompt

This is the no-download route. The person installs the Claude app, opens Claude
Code, connects their Desktop, and pastes the block below. Claude fetches the kit
itself and runs the setup. No zip, no unzipping, no file handling.

**Deliberately short.** It downloads the kit and then follows `START-HERE.md`,
rather than restating the setup steps. One source of truth — if the steps change,
this prompt doesn't need touching.

Send them the five lines above the block, then the block.

---

Before you paste this: install the Claude desktop app, create an account and pick
a plan (Pro is enough to start), switch the toggle at the top left from Chat to
Claude Code, make a new folder on your Desktop called **Claude**, open it with **Choose** in the bar along the bottom
then **Open folder** (and click **Trust workspace** when it asks), and set the mode just
below the session box to **Auto**.

Then copy everything between the lines and paste it in.

---

I'm setting up Claude for my business. I am not technical.
Talk to me in plain English and do the work yourself rather than handing me
commands to run. Tell me what you're doing as you go.

**If some of this is already on the machine, carry on anyway.** Re-pasting this
prompt is how the kit gets updated — it is the normal, supported thing to do, not
a mistake to be protected from. Download the kit again and replace the kit folder,
and replace those two sections of my CLAUDE.md in place. **Never skip a step
because something is already there, and don't stop to ask whether to proceed.**

What is safe to replace: the `Claude Kit` folder itself, the two sections of my
home CLAUDE.md that this kit installs, and this kit's skills.

What you must never touch: any other folder inside `Claude`, any business notes or
CLAUDE.md in those folders, my saved memory, my connected systems, and anything
else in my home CLAUDE.md. Replacing the kit does not disturb any of it.

Afterwards, tell me what you replaced and what was already up to date.

**Before you download anything, check there is a folder called `Claude` on my
Desktop.** Write that check so it can't report a failure — a step labelled
*Failed* reads as something being broken, even when the next line says it's fine. If there isn't, stop and tell me to make it and connect it — don't
create it yourself and don't download into somewhere else. A download into a
folder that isn't there fails quietly and looks like it worked.

**First, get the kit.** Download and unpack it into the `Claude` folder on my
Desktop:

- Mac or Linux: `curl -sSL https://github.com/kieranmcdowell75/claude-kit/archive/refs/heads/main.tar.gz | tar -xz -C ~/Desktop/Claude` then rename `claude-kit-main` to `Claude Kit`
- Windows: download `https://github.com/kieranmcdowell75/claude-kit/archive/refs/heads/main.zip`, expand it into the `Claude` folder on my Desktop, and rename the expanded folder to `Claude Kit`

Use a hard timeout of sixty seconds so a dead download fails loudly instead of
hanging, and check the unpacked files are actually there afterwards rather than
trusting the command's exit code — piping curl into tar hides tar's failures. Tell me before you start that it may look frozen when it isn't.

If the download fails, stop and tell me plainly — don't carry on with a half-built
kit. The likely causes are no internet, or wifi that's struggling.

**Then check I have `Claude/Claude Kit` on my Desktop with a `START-HERE.md`
inside it.** Say so when you do.

**Then read `START-HERE.md` and do exactly what the instruction block inside it
says** — the part between the two lines of dashes, steps 0 through 6, including
the checks at the end. That block is the real setup; treat it as if I had pasted
it myself. Follow its stopping instruction: don't ask me about my systems and
don't connect anything.

---

## What they should see

- A `Claude Kit` folder appears on their Desktop
- House rules go into their `CLAUDE.md`
- Fourteen skills installed
- Git, Node and Python installed, Git told their name
- A folder made for their business
- A five-line verify list, all passing
- One last instruction: start a new session and say *"I've just finished setting up,
  check everything's working."*

## If the download is blocked

Some corporate networks block GitHub. Fall back to sending them
`Claude Kit.zip` and the longer setup document, which assumes a file rather than
a download.
