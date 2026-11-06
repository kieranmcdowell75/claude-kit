# Connector index

One line per product: which door worked, roughly how long, and the thing that
wastes twenty minutes if you don't know it.

**Read this before probing.** If the product is listed, start where the table says
rather than working through the doors from the top.

**This is deliberately not a set of step-by-step guides.** Click paths move when
vendors redesign; which door works for a product changes far more slowly. A short
index that stays true beats fifty guides that quietly rot.

## The rule that keeps it honest

**A "no API" row expires. A "works" row doesn't.**

If a row says something works and it's out of date, you try it and find out in two
minutes. No harm done.

If a row says there's no API and that's out of date, you spend hours going the hard
way when an easy route now exists. Vendors ship APIs all the time — being told
there isn't one is the costly kind of wrong.

So: **before accepting any row that says no API, no connector or browser-only,
check whether it's still true.** Takes a minute. Look at the vendor's developer or
integrations page, not your memory of it.

Any row over about six months old is worth a glance regardless. The date is in the
table for exactly that reason.

## How to use it

- **Product listed, positive row?** Go straight to that door and get on with it.
- **Product listed, negative row?** Check it's still true first, then proceed.
- **Not listed?** Work the doors in `SKILL.md`, then add a row.
- **Row turned out wrong?** Fix it, and change the date. A wrong row is worse than no row.

## The index

Effort is for someone who has done one before. First time, double it.

**Before using this table, search the app's own connector directory.** It holds
hundreds of ready-made connectors that connect with a button in the session, and it
is faster than anything below. Several rows here predate it and may now be easier
than they say — if the directory has the product, use that and update the row.

| Product | Door | Effort | Cost | The thing that would have saved twenty minutes | Checked |
|---|---|---|---|---|---|
| Xero | Official connector | 15 min | ~$10/mo **per company** | Billing is per organisation, so two companies is two fees. Pin the scopes the server asks for — leave them to default and it starts and then dies. Don't trust the vendor's own "connected" display; prove it with a real call. | Nov 2026 |
| Square | Official connector | 15 min | free | Pick the read-only tier on the consent screen. It does **not** give you one tool per endpoint — the whole API arrives as three general-purpose tools, so expect to look up the endpoint name rather than pick from a list. | Nov 2026 |
| GoHighLevel | Official connector | 15 min | free | Token lives at **Settings → Private Integrations**. It needs two headers, the token and the location id — one without the other silently returns nothing. It's **per sub-account**, so connecting one location is not connecting the business. On a reseller account that page can be slow rather than switched off — have the owner open it in their own browser before concluding anything. Make a new key per location; never revoke one you didn't create, since an agency or another computer may be living on it. | Nov 2026 |
| Meta Ads | Official connector | 30 min | free | It must run as the login that actually owns the ad account, which is often not the owner's. A "full access" invitation that was never accepted gives nothing, and looks identical to having access. Expect the sign-in to need the owner's own machine — it times out otherwise. | Nov 2026 |
| Slack | Community connector | 20 min | free | Read and search work; posting is a separate permission and a separate decision. | Oct 2026 |
| Email, calendar, docs | **Start with the app's own built-in connector** | 10 min | free | Almost everyone asking to "connect my email" wants reading, searching and drafting, and the desktop app has a built-in connector that does exactly that in minutes. **Check for it before offering anything heavier.** Its limit is that it drafts but doesn't send, which is usually what you want anyway. | Nov 2026 |
| Google Workspace, full | Own setup, needs a Google Cloud project | 1–2 hr | free | Only go here when the built-in connector genuinely isn't enough — writing to Sheets, Drive, Calendar, sending as them. It's the heaviest on this list and it's project setup, not a sign-in. A second account is a second everything: its own config and its own permission grant, inheriting nothing from the first. | Nov 2026 |
| Deputy | API key | 30 min | free | Each site is a separate install with its own address, login and token — one token is one site. The admin pages ignore scripted clicks entirely, so the token has to be made by hand. | Nov 2026 |
| Hapana | Plan-gated API, else browser | hours | free | Premium and above advertise self-service read-only keys; below that it's the browser. The sign-in is a non-persistent cookie living inside the running browser process, so it dies with the process and survives nothing. | Nov 2026 |
| ClassPass | **No API** for venues — browser | hours | free | The developer portal is for integrators, not venues. The dashboard's own JSON backend is the route, inside an already-signed-in browser, and it's one venue per login. Expect bot protection, so go slowly. | Nov 2026 |
| Canva | Official connector | 5 min | free | Nothing to configure — click Connect and sign in. **It arrives able to create, edit and comment, not just read**, so read-only is a choice you make in how you use it, not a setting on the sign-in. Design search mixes designs shared with you in with the business's own, so filter by ownership before assuming a design is yours. An empty Brand Kit list usually means no kit was ever set up, not a fault. | Nov 2026 |

### Worth knowing

- **Xero** — one connection per company. Two companies means two connections and
  two fees.
- **Square** — the connector is in beta. Tool names change between updates and it
  can time out intermittently. Usually their side, not yours.
- **Meta Ads** — needs an authorisation step the owner has to complete themselves.
- **Deputy** — the admin screens ignore scripted clicks. Generate the key by hand.
- **Email** — try the app's own built-in connector first. The full Google Workspace
  route is the heaviest thing on this list and most people never need it.
- **Google Workspace, full** — needs its own Google Cloud
  project before anything works. Budget an afternoon the first time.
- **Hapana** — drops its own session when the browser closes, so you sign in again
  every time however the profile is set up. Not a setup fault.
- **Hapana, ClassPass** — no self-serve API as at October 2026. **Check before you
  accept that** — both are the kind of vendor that could ship one. If they have,
  this row is wrong and worth fixing.

## Adding a row

Right after you connect something, while it's fresh:

> "Add a row to the connector index for [product]."

One line. If there's genuinely more worth saying — a click path that's hard to
find, a plan tier that catches people, a sequence that has to happen in order —
write a full skill with `make-a-skill` and point at it from Worth knowing.

## What a row must never contain

Account numbers, keys, logins, customer or staff names, or anybody's actual
figures. This is a map of which door opens, not a record of what was behind it.

## Doors, for reference

1. Official connector already exists
2. Public API
3. Scheduled export
4. Drive the browser
5. Not this way, not today — name the blocker

See `SKILL.md` for what each one involves.
