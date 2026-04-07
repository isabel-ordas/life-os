---
name: goals-system
description: >
  Guide any person through defining their quarterly goals, separated into
  Professional and Personal, following an OKR-style format. Use this skill
  whenever someone says things like "I want to set my goals for this quarter",
  "help me plan Q2", "what should I focus on this quarter", "help me define my
  OKRs", "I want to set my priorities for the next 3 months", or any variation
  where someone wants to translate their life vision into concrete quarterly
  objectives with key results and initiatives.
  If a Life Compass document exists (from the life-compass skill), always read it
  first to ensure goals are anchored to values and vital areas. If no Compass
  exists, the skill works standalone.
  Output is written to Notion (via MCP) following a fixed 3-level page hierarchy,
  or exported as Markdown / plain text if Notion is not available.
---

# Goals System Skill

## Overview

This skill guides any person through defining their **quarterly goals** in two
separate tracks:

- 🏢 **Professional** — career, work, learning, visibility
- 🏡 **Personal** — wellness, family, home, finances, growth

Each track follows a structured format with **Objectives** (or OKRs), **Key Results**
(measurable outcomes), and **Initiatives** (concrete actions).

The output is saved as a set of Notion pages that the `weekly-review` and
`daily-planner` skills can read to keep daily planning connected to real priorities.

---

## Step 0 — Read the Life Compass (if available)

Before starting, search Notion for a `🧭 Compass` page under LIFE OS.

**If Compass exists:**
- Read the Compass Summary at the top
- Extract: vital areas with gap indicators, life vision, core values
- Use gaps (🔴 areas) to suggest where goals are most needed
- Tell the user: *"I've read your Compass — I'll suggest goals aligned with your
  values and the areas where you have the biggest gaps."*

**If no Compass exists:**
- Proceed standalone
- Ask the user to briefly describe their current priorities in professional
  and personal life before starting

---

## Step 1 — Determine the quarter

Identify the current or upcoming quarter:
- Q1: January 1 – March 31
- Q2: April 1 – June 30
- Q3: July 1 – September 30
- Q4: October 1 – December 31

State clearly: *"We're building your goals for [Q / year] — [start date] to [end date]."*

If the quarter is already underway, acknowledge it:
*"Q2 has already started. We'll define goals for the remaining weeks and note
that this is a partial quarter."*

---

## Step 2 — Two modes, offer both at the start

### 🌊 Mode A — Guided session (45–60 min)
*Work through Professional and Personal track by track, one objective at a time.*

Claude asks questions for each objective, helps sharpen Key Results into measurable
outcomes, and ensures Initiatives are concrete enough to act on this week.

**Best for:** First time setting quarterly goals, or after a major life change.

---

### ⚡ Mode B — Quick draft (15–20 min)
*Claude proposes a draft structure based on the Compass (or a conversation summary).
The person edits, adds, removes.*

**Best for:** Updating goals for a new quarter when direction is already clear.

---

## Step 3 — Professional goals (🏢)

### Format: OKR style

```
## OKR N – [Objective title] [emoji]

### Key Results Q[X] (outcomes/resultados):
1. [Measurable outcome — what success looks like]
2. [Measurable outcome]
3. [Measurable outcome]

### Initiatives Q[X] (acciones):
- [Concrete action — what you will actually do]
- [Concrete action]
- [Concrete action]
```

### Guidance for each element

**Objective title:** Ambitious but clear. Describes what you're trying to achieve,
not how. Add an emoji that captures the energy of the goal.

**Key Results:** These are outcomes, not tasks. Ask:
> *"How will you know this OKR was successful? What will be measurably different
> at the end of the quarter?"*

Good KR: "Achieve 3 first-round interviews"
Bad KR: "Apply to jobs" (that's an initiative, not a result)

Push for numbers where possible (%, counts, specific milestones).
3 Key Results per OKR maximum.

**Initiatives:** Concrete actions that drive the Key Results.
Be specific: "Apply to 30 PM positions (~4/week)" is better than "Apply to jobs".

### How many OKRs?
Recommend **2–4 OKRs** for the Professional track.

### Mode A questions (one OKR at a time)

Opening:
> *"Let's start with your professional goals. What's the most important thing
> you want to achieve or move forward in your career this quarter?"*

For each OKR:
> *"What would success look like at the end of [quarter]? How would you know
> you achieved this?"* → Key Results

> *"What are you actually going to do to make this happen?"* → Initiatives

> *"Is there another professional goal that feels important this quarter?"*
> → Next OKR or move to Personal

---

## Step 4 — Personal goals (🏡)

### Format: Objective style

```
# OBJECTIVE N: [Title]
*"[A sentence describing the desired feeling or state — why this matters]"*

### Q[X] Key Results:
1. [Measurable outcome]
2. [Measurable outcome]
3. [Measurable outcome]

### Q[X] Initiatives:
1. ✅ [Concrete action]
2. ✅ [Concrete action]
3. ✅ [Concrete action with sub-items if needed]
   - [Sub-action]
   - [Sub-action]
```

### Key differences from Professional format

- Use **OBJECTIVE** (not OKR) as the heading (H1, not H2)
- Include a **motivational framing sentence** in italics after the title
- Initiatives use **✅ checkboxes** — personal goals have more granular steps
- Sub-items welcome for complex initiatives

### Motivational framing sentence

Ask:
> *"Complete this sentence: I want to work on [objective] because I want to
> feel or experience... what?"*

Example: *"Feel energized, strong, confident, and beautiful by caring for my
body, mind, and appearance."*

### How many Objectives?
Recommend **3–5 Objectives** for the Personal track. Common areas:
- Wellness (health, body, mental health)
- Family & relationships
- Home & environment
- Finances
- Personal growth & learning

### Mode A questions (one Objective at a time)

Opening:
> *"Now let's look at your personal life. What area most needs your attention
> this quarter?"*

For each Objective:
> *"Why does this matter to you right now? How do you want to feel at the
> end of the quarter?"* → Framing sentence + Key Results

> *"What specific things are you going to do to make this happen?"* → Initiatives

---

## Step 5 — Quality check before saving

Review the full set of goals with the person:

**Professional:**
- [ ] 2–4 OKRs
- [ ] Each OKR has 2–3 Key Results (measurable outcomes, not tasks)
- [ ] At least one KR per OKR has a number or specific milestone
- [ ] Initiatives are specific enough to act on this week

**Personal:**
- [ ] 3–5 Objectives
- [ ] Each Objective has a motivational framing sentence
- [ ] Key Results are outcomes (not just "do X more")
- [ ] Initiatives include ✅ markers and sub-items where needed
- [ ] Nothing feels like a "should" — goals should feel meaningful

Ask: *"Does anything feel unrealistic for 90 days? Is anything important missing?"*

---

## Step 6 — Write to Notion

Create the following hierarchy under LIFE OS:

```
📁 LIFE OS
└── 🎯 Goals
    └── [Q2 2026 (Apr–Jun)]       ← quarter page
        ├── 🏢 Professional        ← sub-page with all OKRs
        └── 🏡 Personal            ← sub-page with all Objectives
```

**Finding the parent:**
1. Search for `🎯 Goals` under LIFE OS
2. If found: create the quarter page as its child
3. If not found: create `🎯 Goals` under LIFE OS first

**Quarter page title format:** `Q2 2026 (Apr–Jun)` or append `✓ Current` if active

**Quarter page content:** Simple index — just the two child page links, no other content.

**Professional page:** OKR format from Step 3. Separate OKRs with `---` dividers.

**Personal page:** Objective format from Step 4. Separate Objectives with `---` dividers.

---

## Step 7 — If Notion is not available

Generate two Markdown sections (Professional and Personal) following the same
format, saved as `Q[N]-[year]-goals.md` in `/mnt/user-data/outputs/`.

---

## Format consistency note

This skill is designed to produce output **identical in structure** to the
existing quarterly goals format in Notion:

- Professional: `## OKR N –` headings (H2), bulleted Initiatives
- Personal: `# OBJECTIVE N:` headings (H1), numbered ✅ Initiatives
- Key Results always numbered list
- Each goal separated by `---`
- Motivational sentence in italics on Personal page only

Do not deviate from this format — consistency across quarters makes
retrospectives and comparisons much easier.
