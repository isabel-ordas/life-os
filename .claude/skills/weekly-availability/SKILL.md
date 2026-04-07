---
name: weekly-availability
description: >
  Generate a personalised Weekly Availability map for any person who wants to organise
  their time more realistically. Use this skill whenever the user says things like
  "help me organise my week", "I want to plan my time better", "create my availability
  map", "set up my weekly schedule", "I want a time management system", or any variation
  where someone wants to capture their real available windows, fixed commitments, and
  energy patterns. Always use this skill even if the user has not heard the term
  "Weekly Availability" — trigger on intent, not on exact wording.
  Supports output to Notion (via MCP), Markdown file, plain text, or clipboard-ready format.
---

# Weekly Availability Skill

## Overview

This skill guides any person through building a **realistic Weekly Availability map** —
not a rigid timetable, but an honest picture of:

1. **Fixed commitments** — non-negotiables that never move
2. **Energy patterns** — when their brain and body are at their best
3. **Available windows** — real, usable time slots by day
4. **Household / life budget** — time reserved for life admin and home tasks

The output is a structured document that a Time Manager skill (or the person themselves)
can use each evening to plan the following day intelligently.

---

## Philosophy: Availability Map vs Timetable

> A timetable says *"Monday 10–11: do X"* — and creates guilt when life intervenes.
> An availability map says *"Monday morning: 3.5h available, high energy"* — and lets
> priorities fill those windows flexibly each day.

Always frame this to the user as an **energy and availability map**, not a schedule.

---

## Step 0 — Choose output destination

Ask the user where they want to save their Weekly Availability:

| Option | When to suggest |
|---|---|
| **Notion page** (via MCP) | User has Notion connected and already uses it |
| **Markdown file** (.md) | User uses Obsidian, VS Code, or any local note system |
| **Plain text / clipboard** | User wants to paste it anywhere (Google Docs, Notion manually, etc.) |

If Notion MCP is available and the user uses Notion, suggest it as the default.
If uncertain, ask.

> For Notion: search for an existing AREAS or personal section to place the page under.
> If none found, create it at workspace root.

---

## Step 1 — Gather fixed commitments

Ask the user about their **non-negotiable recurring commitments**. Cover:

- **Children / dependants**: school drop-off and pick-up times, care responsibilities
- **Exercise / health**: recurring classes, gym, sport (include prep + shower time)
- **Work or learning sessions**: fixed calls, classes, language sessions, recurring meetings
- **Recurring personal commitments**: associations, volunteering, community groups
- **Temporary commitments**: anything with an end date (note the date explicitly)

Collect: commitment name, day(s) of week, start time, end time, and whether it has an end date.

> Tip: for exercise blocks, always add 30 min for shower/transition unless the user says otherwise.

---

## Step 2 — Capture energy patterns

Ask the user to describe how their energy typically flows through the day.
Use friendly, non-technical language. Suggested prompts:

- *"Are you more of a morning person or do you hit your stride later in the day?"*
- *"Is there a time of day when you feel sharpest for focused work?"*
- *"Do you get a second wind in the evenings, or do you wind down early?"*
- *"Is there a post-lunch dip you always feel?"*

Map answers to these standard energy zones:
- 🟢 **High focus** — deep work, strategic thinking, complex tasks
- 🟡 **Medium focus** — research, emails, lighter creative work
- 🔴 **Low energy** — admin, reading, planning, passive tasks

---

## Step 3 — Calculate available windows

From Step 1 data, calculate the real available windows for each day:

```
For each day:
  all_hours = 06:00 to 23:59
  subtract: fixed commitments (with buffer if needed)
  subtract: family/care time (school pick-up to bedtime, etc.)
  remaining = available windows
  label each window with energy level from Step 2
```

Present the results to the user for confirmation before writing to their chosen destination.
Ask if anything looks wrong or unrealistic.

---

## Step 4 — Life & household budget

Ask: *"How much time per week do you want to set aside for household tasks and life admin
(groceries, cleaning, errands, appointments)?"*

Split into:
- Weekday budget (distributed across Mon–Fri)
- Weekend budget (Sat + Sun combined)

Note this as a budget, not fixed slots — the Time Manager skill will allocate it dynamically.

---

## Step 5 — Weekend availability

Ask separately about weekends:
- *"Do you have any recurring commitments on weekends?"*
- *"How many hours of focused personal time can you realistically carve out on Saturday
  and Sunday?"*

Weekends are often more fluid — capture them as a total available block rather than
fixed windows.

---

## Step 6 — Seasonal or expiring changes

Ask: *"Is there anything in your current schedule that changes soon — a course ending,
a commitment starting, a period that's busier than usual?"*

Document these with explicit dates so the Time Manager skill can adjust automatically.

---

## Step 7 — Generate the Weekly Availability document

Build the document with these sections:

```markdown
# 🗓️ Weekly Availability

## Purpose
[1-sentence description of what this document is for]

---

## ⚠️ Fixed Commitments (non-negotiables)

| Commitment | Days | Time | Notes |
|---|---|---|---|
| [name] | [days] | [HH:MM–HH:MM] | [end date if temporary] |

---

## ⚡ Energy Patterns

- **[Time zone label]:** [Energy level] — [best task types]
- ...

---

## 📅 Available Windows by Day

| Day | Window 1 | Window 2 | Evening | Total focus time | Notes |
|---|---|---|---|---|---|
| Monday | [time] | [time or —] | [time or —] | [Xh] | [energy note] |
| ...

---

## 🔄 Seasonal Changes

- [Change description] *(until/from [date])*

---

## 🏠 Life & Household Budget

- Weekdays: ~[X]h/week total
- Weekends: ~[X]h/weekend total
- Monitor: [note on whether this is expected to be enough]

---

## 📝 Notes for Time Manager

1. Always check calendar integration for same-day appointments before generating plan
2. Prioritise deep work in [highest energy windows]
3. Reserve [best day] as the "big task" day whenever possible
4. Evening slots ([time]) suitable for: [low-energy task types]
5. Never schedule demanding tasks during [protected family/rest time]
```

---

## Step 8 — Write to destination

### If Notion (MCP available):

1. Search for the user's preferred parent page (AREAS, Personal, or similar)
2. Create a new page titled `🗓️ Weekly Availability`
3. Use the structure from Step 7 as page content
4. Confirm with the user and share the Notion URL

### If Markdown file:

1. Save as `weekly-availability.md` in `/mnt/user-data/outputs/`
2. Present the file for download

### If plain text / clipboard:

1. Display the formatted content directly in the chat
2. Invite the user to copy and paste wherever they need it

---

## Iteration & updates

After the document is created, offer the user the ability to:
- **Update a commitment** (e.g., a class time changed)
- **Add a seasonal change** (e.g., a new course starting)
- **Adjust the household budget** based on real experience
- **Export to a different format** if they want to share with someone else

---

## Quality checklist before finalising

Before writing to the destination, verify:

- [ ] Every fixed commitment has a day, start time, and end time
- [ ] Exercise blocks include transition/shower time
- [ ] Temporary commitments have an explicit end date noted
- [ ] Available windows don't overlap with fixed commitments
- [ ] Total weekly focus hours feel realistic (not overpromising)
- [ ] Household budget is split between weekdays and weekend
- [ ] Notes for Time Manager include at least one instruction about calendar integration
- [ ] Energy labels are present for at least morning and evening windows
