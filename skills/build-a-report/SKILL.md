---
name: build-a-report
description: Turn connected business data into a report someone will actually read and trust - a weekly summary, a daily check, a one-page view of how things are going. Use when the user asks how the business is doing, wants to see their numbers, asks for a report or a dashboard, or says they want to know X every week.
argument-hint: "(optional) what the report should cover"
---

# Build a report

Getting numbers out is the easy half. A report people trust and act on is the
other half, and it's where most of these die.

## Find out what they actually want

Business owners ask for "a report". Nobody wants a report. They want to know
something. Get to the real question before building anything.

Ask:

1. **What decision does this help you make?** If there isn't one, it's a vanity
   report and it'll be ignored by week three.
2. **What would make you act?** That's the thing to put at the top.
3. **When will you read it, and on what?** Monday at the counter on a phone is a
   different report from Friday at a desk.
4. **What do you check today, by hand?** Start there. Automating something they
   already trust beats inventing something new.

## The shape that works

**One screen.** If it scrolls on a phone, it's too long. Cut until it isn't.

**The headline is a number and a direction.** Not a chart, not a table.
*"Takings $18,400, up 6% on last week."* They should be able to stop reading there.

**Everything compares to something.** A number alone means nothing. Against last
week, against the same week last year, against target — pick one and be consistent.

**One line for the exception.** The thing that's odd this week. *"Thursday was down
40%, everything else was normal."* This is the line people actually act on, and
it's the one most reports leave out.

**Say what it can't see.** Every report has a blind spot. Cash sales that bypass
the till. An invoice not raised yet. Name it in one line at the bottom, every
time, so nobody over-reads the number.

## Numbers that mislead, and what to do

Check every one of these before showing a figure:

**Before the table: two systems disagreeing is normal.** They measure different
things — taken, billed, reconciled — so never resolve a clash by deciding one
system outranks the others. Work out which one answers *this* question, say which
you used and what it counts, and tell the owner the other number exists and why
it differs. Treating one system as authoritative is how a report ends up
confidently wrong.

| Trap | What to do |
|---|---|
| Comparing unequal periods | Match the day count and the days of week. Four Saturdays beats five every time. |
| A system that updates late | Say so. "Last 3 days may be incomplete" stops a false panic. |
| A total hiding a mix | Per customer, per day, per staff member. Totals flatter and conceal. |
| A zero that isn't | A zero price can mean free, or paid another way. Find out which. |
| One outlier moving everything | Name it. "Includes one $4,200 function booking." |
| The same person, twice | A name is a hypothesis, not a match. Join on something nobody can type two ways — an ID, a phone number, an email — before treating two records as one person. |
| An empty screen read as an empty dataset | A blank view can be filtered, scoped to one location, or just the wrong screen. Check another way before reporting that something isn't there. |
| Two dates for one event | When something was *actioned* and when it *takes effect* are different dates, and they describe different people. Find out which one the report counts before trusting it. |

## Prove it before they rely on it

**Test it against a period they already know.** Pick a week they can verify from
memory or a printed report. If your number disagrees with theirs, your number is
wrong until proven otherwise.

Do this before showing it to anyone else. A report that's wrong once is never
trusted again, even after it's fixed.

## Stamp it

Every report carries, at the top:

- The period it covers, in full
- The date and time it was produced
- Where the numbers came from

So anyone looking at it later knows what they're holding.

## Then make it repeat

When it's right and they trust it:

- `schedule-something` to make it arrive on its own
- `make-a-skill` so it rebuilds the same way next time, and for the next business
- `build-a-dashboard` if they'd rather go and look at it than be sent it. A report
  is pushed to them; a dashboard is somewhere they go. Some people want one, some
  the other, plenty want both.

## What not to do

- Don't build a dashboard when an email would do. Nobody logs in to a dashboard.
- Don't add a number because it's available. Every extra line costs attention.
- Don't use a chart where a sentence is clearer. Most weekly numbers are a sentence.
- Don't make them ask for it. A report they have to go and get is a report they stop getting.
