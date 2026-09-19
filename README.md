# True Margin

**A two-week reality check for people who can't change their fixed commitments.**

Chatathon 2026 · WHOOP Track · [Team name]

## The Problem

Knowledge workers carry a mix of fixed obligations — meetings, deadlines, client commitments — and variable day-to-day capacity. Generic wellness advice tells them to "protect focus time" or "start earlier," but their start time and meetings are fixed. They can't act on that advice.

True Margin surfaces what's actually controllable — movable tasks and open time — and flags when fixed commitments plus workload will compound into overload, two weeks before it happens.

## Who It's For

**The Constrained Professional**: a knowledge worker in finance, consulting, or tech with recurring meetings, deadlines, and capacity that varies day to day. They don't want to work less — they want their limited controllable time to go to the right things.

## How It Works

1. **Two-week dashboard** — a calendar view of the next two weeks with high-stress days flagged
2. **Deterministic rule engine** — flags a day when high-concentration task hours exceed the concentration-friendly open time available. No AI, no ML — transparent logic you can explain in one sentence
3. **Drill-down + recommendation** — click a flagged day to see why, and get a suggested reschedule for a movable task
4. **Accept, edit, or reject** — the tool recommends; the person decides
5. **AI-drafted delegation message (mockup)** — the one place AI appears: turning a flagged conflict into a respectful, editable message asking for help

## What This Is Not

Not a wellbeing surveillance tool. Not an employee scoring system. Not a mental-health diagnostic. Not an automatic calendar editor. It recommends; the employee decides.

## Running It

```
git clone https://github.com/khaitt135/chatathon-TrueMargin.git
cd chatathon-TrueMargin
npm install
npm run dev
```

Open http://localhost:3000. The dashboard loads with pre-loaded synthetic data — no API key, login, or setup required to see the core demo.

## What's Working (Demonstrated)

- Two-week dashboard with day-level overload flagging
- Deterministic rule engine matching movable tasks to open time
- Drill-down view explaining why a day is flagged
- Accept / edit / reject workflow on recommendations

## What's Simulated (For This Demo)

- Calendar events, tasks, and check-in history: pre-loaded synthetic data, not a live calendar connection
- AI-drafted delegation message: static mockup, not a live LLM call *(update this line if you built the live version — see Decision 2)*

## What's Planned (Post-Chatathon)

- Live Google Calendar / Outlook integration
- Manager task-assignment screen (real, interactive)
- Live, editable AI-drafted delegation messages
- Day-to-day ("today's adjustment") view

## Privacy

Individual check-in data — energy, meals, breaks, workload, confidence — is never shown to a manager, individually or in aggregate. The manager sees only the tasks they assigned.

## AI Agents Used to Build This

- **Cursor** (Composer + Agent mode) — scaffolding, UI, rule engine
- **Claude** — QA validation, documentation, PRD synthesis
- **GPT-4** — early ideation and spec discussion

## Team

[Team name] — [Team members]

Built at Chatathon 2026, Northeastern University · AINU · WHOOP Track
