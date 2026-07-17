---
title: Hub Cheat-Sheet
emoji: 🗺️
category: library
updated: 2026-07-17
---

## What a card is

A card is just a markdown file living in `content/` with a bit of frontmatter at the top:

```
---
title: <shows as the card title>
emoji: <shows next to the title>
category: tools | library
updated: <YYYY-MM-DD>
---
```

Everything below the frontmatter is the card body — plain markdown, rendered as-is.

## The two categories

- **tools** — things your AI runs or produces for you (a daily briefing, a scan, a report).
- **library** — things you save for reference (prompts, notes, DNA, this cheat-sheet).

Those are the only two values the Hub recognizes. Anything else won't show up.

## Scheduled tasks can write straight to the Hub

Any scheduled task can, as its last step, write its output as a card into `content/` and push it — so a task that runs while you're away still leaves something for you to find later, instead of only living in a chat you have to scroll back through.

- Daily/rolling output → `content/<name>-<YYYY-MM-DD>.md` (one card per day, history builds up).
- Always-current output → a fixed filename that gets overwritten each run (one card, always fresh).

## Ideas board → Wins

Drop a rough idea on the **Ideas** board whenever one crosses your mind. Once you've actually built and shipped it, move it over to **Wins** — a running record of what's gone from idea to real.

## What's next: starter ideas

Grounded in what's actually running for you today:

1. **Card-emit your Weekday Morning Brief.** It already runs every weekday at 6:01am pulling calendar and unread email — right now the output only lives in chat. Add one step so each run also writes a `tools` card (`daily-brief-YYYY-MM-DD.md`), and your mornings build a browsable history in the Hub.
2. **Card-emit James Clear Thursday.** Same idea for your Thursday 3-2-1 newsletter pull from Gmail — push it as a `library` card each week instead of letting it scroll away in chat.
3. **Build a "Newsletter Radar" task.** Bradford Tax Institute is landing in your inbox multiple times a week and Checkpoint/Thomson Reuters mail is landing on your modrakcpa.com address — both are exactly the kind of "routine newsletter" your current brief skips outright. A weekly scan that surfaces headlines from Bradford, Checkpoint, Accounting Today, and CPA Trendlines (even when the article's paywalled) as a `library` card means nothing important slips through silently.
4. **Build a "Tax Deadline Tracker."** As a CPA, a recurring task that checks your calendar plus known IRS filing/estimated-payment dates and writes a `tools` card of what's coming up would turn a mental checklist into something you can glance at.
5. **Use the `morning` skill for a styled brief.** It can render your daily brief as a proper HTML artifact instead of plain text — worth pairing with idea #1 so the card version looks as good as the chat version.
6. **A "Hub Setup Log" card.** Document the GitHub-repo-to-Lovable pipeline, where the token lives, and how pushes work — so the next time this needs troubleshooting (by you or a future Claude session), it's a five-second read instead of a rebuild-from-scratch investigation.
7. **A weekly "Inbox Triage" card.** Separate from the daily brief — a Friday-afternoon `library` card rounding up what got deferred all week across both your Gmail and modrakcpa.com inboxes, so nothing quietly falls off the end of the week.
