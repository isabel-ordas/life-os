---
name: life-compass
description: >
  Guide any person through defining their Life Compass — a clear, personal document
  capturing their core values, life vision, vital areas, and anti-goals.
  Use this skill whenever someone says things like "I want to clarify what I want
  from life", "help me define my values", "I want to design my ideal life", "what
  do I really want?", "help me set a life vision", "I want to know what matters to
  me", or any variation where someone wants to reflect on who they are and where
  they're going. Also trigger when someone starts using the goals-system or
  daily-planner skills without a Compass document — they need this first.
  Supports output to Notion (via MCP), Markdown file, or plain text.
---

# Life Compass Skill

## Overview

This skill guides any person through a reflective conversation to build their
**Life Compass** — a personal document that answers three fundamental questions:

1. **What do I value?** — the principles that are non-negotiable
2. **What do I want?** — what my ideal life looks and feels like in 3–5 years
3. **In which areas of my life?** — the domains I want to actively nurture

The output is a living document that feeds directly into the `goals-system`,
`weekly-review`, and `daily-planner` skills. Without a Compass, planning is just
busyness. With one, every plan has direction.

---

## Two modes — offer both at the start

At the beginning of every session, present the two modes clearly and let the
person choose based on how much time and energy they have right now:

---

### 🌊 Mode A — Deep Dive (45–60 min)
*For when you have time and want to think things through properly.*

Claude guides you through each block as a conversation — asking one question at
a time, listening to your answers, asking follow-up questions, and building the
document together. Slower, more reflective, more personal.

**Best for:** First time doing this, or when something important has changed in
your life.

---

### ⚡ Mode B — Quick Draft (15–20 min)
*For when you want something solid without a long session.*

Claude presents a pre-filled draft with standard vital areas and example content.
You edit what resonates, delete what doesn't, and add what's missing. Faster,
less reflective, but still useful.

**Best for:** Updating an existing compass, or when you just need a working
version to start from.

---

## Block 1 — Core Values

### Mode A (conversational)
Opening question:
> *"Think about a moment in your life when you felt completely yourself — proud,
> energised, aligned. What was happening? What made it feel right?"*

Follow-up questions if needed:
- *"What three things, if you lost them, would make you feel like you're no longer you?"*
- *"When have you felt most conflicted or uncomfortable? What value was being violated?"*
- *"What do you admire most in the people you respect?"*

Guide the person towards identifying **3–5 core values maximum**. More than 5
dilutes meaning.

For each value, push for a concrete translation:
> *"What does [value] actually look like in your day-to-day life? How would
> someone see it in your behaviour?"*

### Mode B (draft)
Present this pre-filled list and ask them to pick 3–5 and edit as needed:

> Autonomy · Creativity · Family · Growth · Health · Honesty · Impact ·
> Learning · Nature · Security · Simplicity · Sustainability · Connection ·
> Courage · Excellence · Freedom · Justice · Presence

### Output format
```
## Core Values

| Value | What it means in practice |
|---|---|
| [Value 1] | [Concrete behaviour or commitment] |
| [Value 2] | [Concrete behaviour or commitment] |
| [Value 3] | [Concrete behaviour or commitment] |
```

---

## Block 2 — Life Vision

### Mode A (conversational)
Opening question:
> *"Imagine it's 3 years from now and your life is exactly how you want it.
> You wake up on a Tuesday morning. Describe that day — what do you see,
> where are you, what are you doing, how do you feel?"*

Let them paint the picture freely first, then use structured follow-ups to
fill any gaps:
- *"What does your work look like? Are you in a role, running something, freelancing?"*
- *"Where are you living? What does your physical environment feel like?"*
- *"How does a typical week feel? Fast, slow, varied, calm?"*
- *"What relationships are central to your life?"*
- *"How is your health and energy?"*

### Mode B (draft)
Present this template and ask them to fill in each line:

```
In 3 years, my life looks like this:
- Work & career: ...
- Where I live & lifestyle: ...
- Health & energy: ...
- Relationships & family: ...
- Personal growth & learning: ...
- Financial situation: ...
- How I spend my free time: ...
```

### Output format
```
## Life Vision (3-year horizon)

[2–4 sentences describing the overall picture in their own words]

| Area | What I want it to look like |
|---|---|
| Work & career | [...] |
| Lifestyle & freedom | [...] |
| Health & energy | [...] |
| Relationships | [...] |
| Growth & learning | [...] |
| Finances | [...] |
```

---

## Block 3 — Vital Areas + Current State

Vital areas are the life domains the person actively wants to nurture.
They may differ slightly from the vision areas — these are the buckets
they'll use to organise goals.

### Standard vital areas (adjust to person's life)
- Career / Professional development
- Health & body
- Family & close relationships
- Friends & social life
- Personal growth & learning
- Finances & security
- Creativity & hobbies
- Community & contribution
- Environment & home

### Mode A (conversational)
For each area:
> *"On a scale of 1–10, how satisfied are you with [area] right now?"*
> *"And where do you want it to be in 3 years?"*
> *"What's the most important thing that needs to change?"*

### Mode B (draft)
Present the table pre-filled with all standard areas and ask them to rate
current state and describe desired state.

### Output format
```
## Vital Areas

| Area | Desired state | Current state | Gap |
|---|---|---|---|
| Career / PM | [...] | [...] | 🔴 / 🟡 / 🟢 |
| Health & body | [...] | [...] | 🔴 / 🟡 / 🟢 |
| Family | [...] | [...] | 🔴 / 🟡 / 🟢 |
| ... | | | |
```

Gap legend: 🔴 Big gap (priority) · 🟡 Some progress needed · 🟢 Mostly where I want to be

---

## Block 4 — Anti-Goals

The question most people never ask — and the one that brings the most clarity.

### Mode A (conversational)
> *"What does success look like for OTHER people that you actively don't want
> for yourself? What would feel like failure even if the world called it winning?"*

Follow-ups:
- *"What kind of work environment would make you miserable?"*
- *"What trade-offs are you not willing to make, no matter how good the reward?"*
- *"What would you regret having done in 10 years?"*

### Mode B (draft)
> *"Complete these sentences:"*
> - "I never want to sacrifice ___ for ___"
> - "No matter how much money it paid, I would not ___"
> - "I would rather ___ than ___"

### Output format
```
## Anti-Goals

Things I explicitly choose NOT to pursue, even if they look like success to others:

- [Anti-goal 1]
- [Anti-goal 2]
- [Anti-goal 3]
```

---

## Compass Summary — the most important output

At the end, generate a **3-sentence summary** of the full compass. This is what
the `daily-planner` and `weekly-review` skills will read as quick context.

```
## Compass Summary

[Name] is someone who values [core values]. They are working towards a life where
[vision in 1–2 sentences]. Their biggest current focus areas are [top 2–3 vital
areas with gaps], and they are intentionally avoiding [key anti-goal].
```

This summary must be at the TOP of the Compass document so other skills
can read it without loading the full document.

---

## Final document structure

```markdown
# 🧭 Compass

> [Compass Summary — 3 sentences]

---
Last updated: [date]

## Core Values
[table]

## Life Vision
[text + table]

## Vital Areas
[table with gap indicators]

## Anti-Goals
[bullet list]

---
*Next review: [suggest 3–6 months from now]*
```

---

## Step 8 — Write to destination

### If Notion (MCP available):
1. Search for the LIFE OS page in the workspace
2. Create a new page titled `🧭 Compass` under LIFE OS
3. Use the document structure above as content
4. Share the Notion URL with the person

### If Markdown file:
1. Save as `compass.md` in `/mnt/user-data/outputs/`
2. Present the file for download

### If plain text / clipboard:
1. Display the formatted content directly in chat
2. Invite the person to copy and paste wherever they need it

---

## Important behaviour guidelines

- **Never rush Block 1.** Values are the foundation. If someone gives vague
  answers ("I value family"), gently push for concrete meaning.
- **Validate emotions, not just answers.** This is a reflective exercise.
  Acknowledge when something resonates or when the person seems uncertain.
- **Don't generate values or vision on their behalf.** You can offer prompts
  and examples, but the content must come from the person. Avoid projecting.
- **One question at a time in Mode A.** Do not fire multiple questions at once.
  Let silence breathe.
- **The document is a starting point, not a contract.** Remind the person that
  this is a living document — it should be reviewed and updated every 3–6 months.

---

## Quality checklist before saving

- [ ] Values have concrete behavioural translations (not just abstract nouns)
- [ ] Vision is specific enough to be visualisable (not just "be happy")
- [ ] Every vital area has both a desired state AND a current state
- [ ] Gap indicators are present and honest
- [ ] Anti-goals are genuine (not just the inverse of goals)
- [ ] Compass Summary is 3 sentences max and captures the essence
- [ ] Last updated date is included
- [ ] Next review date is suggested
