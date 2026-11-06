---
name: build-a-dashboard
description: Build a one-page view of a business from whatever is connected, and grow it into more pages only when one page stops being enough. Use when someone asks for a dashboard, a screen with their numbers on it, somewhere to see how the business is going, or wants their reports in one place.
argument-hint: "(optional) what the dashboard is for, or who it's for"
---

# Build a dashboard

A report answers a question. A dashboard is where someone goes to look. Different
job, and it fails differently — a report nobody trusts gets corrected, a dashboard
nobody opens just quietly dies.

**Start with one page.** Always. However much data is connected.

## Before building anything

**Use `build-a-report` for the numbers themselves** — getting to the real question,
the five traps, testing against a period they already know. That work doesn't change
because it's on a screen. Don't repeat it here; do it there first.

Then three questions:

1. **What do you look at now, and where?** A spreadsheet, a report in their booking
   system, a number they ask someone for. Start from what they already check, not
   from what's available to show.
2. **When would you open this?** Monday morning, before a meeting, every day at the
   counter. That decides what goes at the top and how much fits.
3. **What would make you do something?** If a number changes and nothing happens,
   it's decoration. Decoration is what makes dashboards die.

## The one page

**It fits on one screen.** If it scrolls on a laptop, it's too long. On a phone,
allow one scroll and no more.

**Top left is the thing they came for.** One number, big, with its direction.
*Takings this week $18,400, up 6%.* They should be able to stop there.

**Four to six things, not twenty.** Every extra tile costs attention and nobody
reads the twelfth one. If something hasn't been looked at in a month, take it off.

**Everything compares to something.** A number alone means nothing — against last
week, the same week last year, or target. Pick one and be consistent across the page.

**One line of plain English saying what changed.** *"Thursday was down 40%,
everything else normal."* This is the part people actually read, and most
dashboards don't have it.

**Stamp it.** The period covered and when it was last refreshed, somewhere visible.
A stale dashboard that looks live is worse than no dashboard.

**Say what it can't see**, once, at the bottom. Cash that bypasses the till, an
invoice not raised yet. One line stops someone over-reading the whole page.

## Build it as a file they can open

A single HTML file in their business folder they can double-click. No server to
run, no login, no site to host. It works offline and it keeps working if nothing
else does.

If `dashboard-design-kit` is installed, use its templates and tokens — the design
work is already done. If not, keep it plain: system font, lots of white space, one
accent colour, and no chart where a number would do.

**Refreshing:** they say *"refresh the dashboard"* and it rebuilds from the
connected systems. When they trust it, `schedule-something` makes it rebuild on its
own.

## When one page becomes several

Not before. A second page is earned, and there are only three good reasons:

- **Different people want different things.** The owner wants money, the manager
  wants today. That's two pages, not one crowded one.
- **Different time horizons.** What's happening today versus how the year is
  tracking. They get looked at in different moods.
- **The page is full.** More than six or seven things and nobody reads the bottom.

When you split, split by **subject** — what it's about — not by where the data came
from. "Sales" and "Retention" are pages. "Xero" and "Square" are not; nobody thinks
in software names.

Keep one page as the front door with the two or three numbers that matter most, and
let the others sit behind it.

## What kills dashboards

- **Built from what's available** rather than what gets looked at
- **Too many numbers**, so the important one is buried
- **No comparison**, so nothing means anything
- **Stale without saying so** — the fastest way to lose trust completely
- **Pretty before it's right.** Check the numbers against something known first.
  A beautiful wrong dashboard gets abandoned and never comes back

## When it's built

Show them, and ask one question: **"Would you open this on Monday?"**

If they hesitate, it's wrong — and the fix is almost always fewer things, not more.
