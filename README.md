# True Margin

**A two-week reality check for people who can't change their fixed commitments.**

Chatathon 2026 · WHOOP Track · Oracle Platform Engineering prototype

## The Problem

Knowledge workers carry a mix of fixed obligations — meetings, deadlines, client commitments — and variable day-to-day capacity. Generic wellness advice tells them to "protect focus time" or "start earlier," but their start time and meetings are fixed. They can't act on that advice.

True Margin surfaces what's actually controllable — movable meetings, open time, and private check-ins — and flags when fixed commitments plus workload will compound into overload, two weeks before it happens.

## Who It's For

**The Constrained Professional**: a knowledge worker in finance, consulting, or tech with recurring meetings, deadlines, and capacity that varies day to day. They don't want to work less — they want their limited controllable time to go to the right things.

This demo is set in **Oracle · Platform Engineering**. The manager, Priya, plans the fortnight for her team. Each person still owns their own check-ins.

## How It Works

1. **Two-week dashboard** — this week and next week, with each day marked Clear, At risk, or Overloaded
2. **Capacity from private check-ins** — energy, meals, breaks, demand, and confidence stay on the employee screen. The manager sees only a 1–5 capacity band derived from them
3. **Deterministic rule engine** — flags a meeting when its concentration demand exceeds the person's capacity in that block. No AI, no ML — transparent logic you can explain in one sentence
4. **Drill-down + recommendation** — click a flagged day to see the hour-by-hour view and a suggested move, cancel, shorten, or cover
5. **Apply, edit, or leave it** — the tool recommends; the manager decides
6. **Editable message draft** — the one place generation appears: a labelled template (or live Claude, if it responds) the manager can edit before sending

## What This Is Not

Not a wellbeing surveillance tool. Not an employee scoring system. Not a mental-health diagnostic. Not an automatic calendar editor. It recommends; the person decides. Raw check-in answers never appear in the manager view.

## Running It

```
git clone https://github.com/khaitt135/chatathon-TrueMargin.git
cd chatathon-TrueMargin
open index.html
```

Or serve it locally:

```
python3 -m http.server 8000
```

Then open http://localhost:8000. The dashboard loads with synthetic data (seed **4821**) — no API key, login, or setup required.

## Demo seed (4821)

| What you click | What you should see |
|---|---|
| Amara Okafor | Senior Developer, 5 of 10 days need a decision |
| Thu 8 | Overloaded — Architecture deep dive at 14:00 |
| Recommendation | Move to Fri 9 Oct, 10:30 |
| Apply | Calendar updates; message draft stays editable |
| View as employee | Private Pulse Ritual + check-in table for that day |

## What's Working (Demonstrated)

- Two-week dashboard with day-level overload flagging
- Team roster with per-person flagged counts
- Deterministic rule engine matching meeting demand to derived capacity
- Drill-down view explaining why a day is flagged
- Apply / move / cancel / leave-it workflow on recommendations
- Employee Pulse check-in that writes back into capacity
- Privacy split: manager sees 1–5 capacity only; employee sees the five answers

## What's Simulated (For This Demo)

- Calendar events, tasks, and check-in history: generated from the seed, not a live calendar connection
- Message draft: a local template is always available. The page tries a live Claude call and labels the result `template draft` or `drafted by Claude`

## What's Planned (Post-Chatathon)

- Live Google Calendar / Outlook integration
- Live, editable AI-drafted messages through a server-side API
- Day-to-day ("today's adjustment") view
- Manager task-assignment that is more than due-date flags on synthetic tasks

## Privacy

Individual check-in data — energy, meals, breaks, demand, confidence — is never shown to a manager, individually or in aggregate. The manager sees only the derived capacity band (1–5) and the calendar they already manage.

## AI Agents Used to Build This

- **Cursor** (Composer + Agent mode) — scaffolding, UI, rule engine
- **Claude** — QA validation, documentation, PRD synthesis
- **GPT-4** — early ideation and spec discussion

## Team

Built at Chatathon 2026, Northeastern University · AINU · WHOOP Track
