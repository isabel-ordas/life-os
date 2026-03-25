# 🧠 life-os

A personal operating system built with Claude skills — to design an intentional life
and manage time towards the goals and lifestyle you want.

**Not a productivity hack. A thinking system.**

---

## What is this?

`life-os` is a collection of Claude skills that guide you through:

- Clarifying **who you are and what you want** from life
- Translating that into **concrete goals** by life area
- Mapping your **real available time and energy**
- Planning each **week and day** with intention

Each skill is a structured instruction file (`SKILL.md`) that tells Claude exactly
how to run a session with you — what questions to ask, in what order, and where to
save the results (Notion, Markdown files, or plain text).

---

## System structure

```
LAYER 1 — VISION
  🧭 life-compass       Who am I? What do I want my life to look like?

LAYER 2 — GOALS
  🎯 goals-system       What do I want to achieve? (by area, by quarter)

LAYER 3 — AVAILABILITY        ← you are here (Phase 1)
  🗓️ weekly-availability  When am I available? What's my energy like?

LAYER 4 — PLANNING
  📋 weekly-review      What happened this week? What matters next week?
  📅 daily-planner      What did I do today? What's the plan for tomorrow?
```

Each layer feeds the next. The `daily-planner` is powerful because it knows
your vision, goals, and available time — not just your task list.

---

## Skills

### ✅ [weekly-availability](./skills/weekly-availability/) — Phase 1
Guides any person through building a realistic **Weekly Availability map**.
Not a rigid timetable — an honest picture of fixed commitments, energy patterns,
and available windows that Claude can use to plan intelligently.

**Output:** Notion page, Markdown file, or plain text.

---

### ✅ [life-compass](./skills/life-compass/) — Phase 2
Guides any person through a reflective conversation to define their **Life Compass**:
core values, life vision, vital areas with current vs desired state, and anti-goals.
Offers a Deep Dive mode (45–60 min) and a Quick Draft mode (15–20 min).

**Output:** Notion page, Markdown file, or plain text.

---

### 🔜 goals-system — Phase 2
Translates your vision into concrete objectives by life area and quarter.
Connects to `weekly-availability` so planning always serves real goals.

---

### 🔜 weekly-review — Phase 3
A guided Sunday/Monday session: what happened, what moved forward,
what to prioritise next week. Writes a structured entry to Notion.

---

### 🔜 daily-planner — Phase 4
The evening routine: 10 minutes to review the day and build tomorrow's plan.
Reads from `weekly-availability` + Google Calendar + active goals.

---

## How to use these skills

### Option A — Claude Code (recommended)
```bash
git clone https://github.com/your-username/life-os.git
```
Point your Claude Code config to the `skills/` folder.
Skills trigger automatically when you describe what you want.

### Option B — Claude Projects
Copy the contents of any `SKILL.md` into a Claude Project's custom instructions.
Start a conversation — the skill guides the session from there.

### Option C — Paste directly
Copy the `SKILL.md` content into any Claude conversation as context.
Works in Claude.ai without any setup.

---

## Notion structure

This system writes to a `LIFE OS` section in Notion:

```
📁 LIFE OS
├── 🧭 Compass              ← values, life vision, vital areas
├── 🎯 Goals                ← objectives database by area + quarter
├── 🗓️ Weekly Availability  ← energy and time map ✅
└── 📅 Planning
    ├── Weekly Reviews      ← one entry per week
    └── Daily Plans         ← daily log
```

Skills also support Markdown files and plain text if you don't use Notion.

---

## Related repos

- [`pm-ai-skills`](https://github.com/your-username/pm-ai-skills) — Claude skills
  for product management: CV generation, job search tracking, PM frameworks.

---

## Roadmap

- [x] `weekly-availability` — Phase 1
- [x] `life-compass` — Phase 2
- [ ] `goals-system` — Phase 2
- [ ] `weekly-review` — Phase 3
- [ ] `daily-planner` — Phase 4

---

## License

MIT — use freely, adapt as needed, credit appreciated.
