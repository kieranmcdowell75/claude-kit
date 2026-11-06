---
name: scope-an-email-agent
description: Work out which emails an agent should draft replies to, and which it must leave alone, by measuring the business's own mailbox. Use when Kieran asks "can it handle these emails too", "what else should it draft", "should the agent reply to this one", when an email agent is being built or widened, or when a drafted reply turns out to state a rule wrongly.
---

# What an email agent should draft, and what it must not

The question is never "can a model write this reply". It can write anything. The
question is whether the business has answered this kind of email enough times,
consistently enough, for a draft to be right rather than plausible.

That is a measurement, not a judgement. Do the measurement.

## What has to be true first

The mailbox is already mined into a local store, with inbound and outbound in
the same table so a request can be matched to the reply it got. Without the
outbound half none of this works: you can count what people ask, but not what
the business does about it.

## The order

### 1. Strip the mailbox down to real member mail

Most of an inbox is not work. On one studio's mailbox, 94 inbound in a week came
down to 52 once marketing and internal threads were removed. A page that counts
the other 42 is lying about somebody's morning.

Three filters, cheapest first, none of which needs a model:

- **the mail provider's own category labels.** Gmail's promotions label caught
  every piece of marketing in the sample and nothing else. It is free and better
  than any rule you would write.
- **internal senders** — anyone on the business's own domain.
- **automated senders** — `no-reply`, `notifications`, `mailer`, `bounce`. Match
  on the sender address, not the subject. Do NOT include `support` or `alerts`:
  a customer writing from `support@their-own-business.com` is rare and real, and
  a silently dropped request is the worst failure this kind of system has.

### 2. Count the categories, and count the replies

For each kind of request, two numbers: how many times it came in, and how often
the business actually answered it. A category nobody answers is not a category
you can learn from.

```
                        times   replied
late cancel               229       87%
new enquiry                49       96%
booking problem            24       88%
gift card                  11      100%
failed payment              6      100%
```

The right-hand column is a trap on its own. 100% of six is not a pattern.

### 3. Draw the line, and say where it is

Three tiers, not two:

| | |
|---|---|
| **drafted** | enough examples, consistent handling, and the facts are readable from a system |
| **listed** | real mail, needs a person, shown so nobody has to work two places |
| **never shown** | marketing, internal, automated |

Roughly fifty examples is where a pattern becomes trustworthy. Below twenty,
don't. **Money is a separate test, not a volume one**: refunds, double charges
and failed payments stay listed however many there are, because a confident
wrong answer about somebody's money is a different size of wrong.

**Say why, on the page, for every email you did not draft.** "Only 11 of these
in 18 months, which is not enough to copy how the team answers them" teaches the
reader what the agent is for. A blank space teaches them it is unreliable.

### 4. Find where the policy actually lives

**It is almost never in the replies.** Twice now the real rule was in an email
the business sends to every new customer, and both times the replies alone gave
a wrong answer.

Search the whole corpus, outbound included, for the policy language: the fee
amount, "policy", "window", "within", "notice", "per month". Read the clause,
not the summary.

### 5. Check practice against the policy before writing the rule down

Count how often the stated rule is actually applied, by year. If practice and
policy disagree, **do not pick for them and do not assume drift.** Read the
clause again first.

A worked example of getting this wrong, twice in an hour:

> A studio's policy said one free late cancellation per calendar month. The team
> waived it every single time somebody emailed, and never once mentioned the
> allowance. That looked like a year of drift.
>
> It was not. The clause charged a fee for cancelling *without telling anyone*.
> Everybody who emails has told someone, so the fee never applied to them. The
> monthly allowance was a cushion for the silent ones. Two mechanisms, read as
> one, and the "correction" was worse than the original.

If it still conflicts after reading the clause properly, that is an owner's
decision. Put both readings in front of them with the counts.

### 6. Write the rule where a person can argue with it

A plain-language rules file, marked clearly as not ratified until the people who
do the job have read it. Include the open questions you could not answer, by
name. The ones you cannot answer from the mailbox are usually the ones that
matter.

## How to check it worked

Take the biggest drafted category and read ten real replies the business sent.
If the agent's draft would have passed for one of them, the scope is right. If
it reads like a template and theirs do not, measure the similarity between their
own replies before templating anything: a sample of seven from one week can look
identical when 212 across two years have a median overlap of 25%.

## The traps

- **A sample from one week is one person in one mood.** Both scoping mistakes in
  the worked example above came from reading seven recent replies.
- **High reply rate on low volume means nothing.**
- **"We always do X" is a claim to test, not a rule to encode**, including when
  the owner says it.
- **The courtesy reply is not work.** "Thanks!" on a finished thread will look
  like an unanswered request unless you check for a prior reply from the
  business. Strip signatures and quoted tails before measuring length, or a
  one-word thank-you with a corporate footer reads as a substantial email.
- **Check the real mailbox, not the local copy**, for whether something was
  answered. A reply sent before the window you downloaded looks like no reply.

## What this cannot tell you

- **The channel you cannot see.** If the business also takes these by text,
  phone or DM, the mailbox shows one slice and cannot tell you how big it is.
  Ask, and write the answer down.
- **The people who never write in.** Everyone in an email corpus self-selected
  by contacting the business. The ones who silently absorb a charge are invisible
  and are often the fairness question worth asking.
- **Informal arrangements.** Exemptions a departed staff member granted by hand
  leave no trace in any system. Expect to find one, and expect it to be
  unrecorded.
