# Skills

A skill is a short set of instructions Claude reads when a particular kind of job
comes up. You don't learn them or call them by name — they fire when they're
relevant.

Fourteen come with this kit:

| Skill | What it's for |
|---|---|
| `interview-me` | getting to know a business properly, and writing its house rules from the answers |
| `list-my-systems` | a two-minute inventory of what the business runs on |
| `connect-anything` | getting into any business software, when there's no ready-made integration |
| `build-a-report` | turning numbers into something you'll actually read and trust |
| `build-a-dashboard` | one page you go and look at, growing into more only when earned |
| `schedule-something` | making a job run on its own, like a Monday morning email |
| `keep-it-awake` | stopping the computer sleeping through a scheduled job |
| `make-a-skill` | capturing something that worked, so it repeats |
| `draft-a-reply` | answering a customer, with the facts already looked up |
| `handover` | carrying a long conversation into a fresh one without losing the thread |
| `learn-my-documents` | turning your policies and handbooks into something Claude can answer from |
| `run-a-promotion` | running a sale by text or email, so staff only have to press send |
| `pressure-test` | stress-testing a decision before you commit to it |
| `check-it-worked` | proving the setup is right, and saying exactly what isn't |

The install step copies these into `~/.claude/skills/`, which is where Claude looks
for them. They become available in a new session — no app restart needed.

**The only one worth remembering by name is `/handover`.** The rest take care of
themselves.

## Adding your own

Every system you connect and every report you build should leave a skill behind, so
the next time takes minutes instead of an afternoon. Say:

> "Turn what we just did into a skill."

The `make-a-skill` skill handles the rest.
