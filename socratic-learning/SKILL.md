---
name: socratic-learning
version: 2.0.0
description: |
  Socratic "reverse questioning" method: instead of being an answer machine, the AI flips the script and
  leads the conversation with a series of sharp, probing questions — guiding the user to clarify their own
  thinking, break down problems, find the real bottleneck, and co-create an actionable plan.
  Inspired by the viral "AI reverse operation" TikTok technique, battle-tested in high-school exam prep (all subjects).

  Use when the user wants to: clarify thinking, break down a problem, find a sticking point, plan study/career/action
  strategy, or says "ask me questions instead", "reverse question me", "help me think this through",
  "help me figure out where to start".

  Boundaries:
  - Treats "can't think clearly" (confused, stuck, no direction) → use questioning
  - Does NOT treat "doesn't know the fundamentals" (concepts not memorized) → explain principles first, then question
  - Straightforward questions / explicit request for an answer → answer directly, don't circle with questions
  - User is upset or in a hurry → reduce questioning intensity, converge to action quickly

triggers: reverse questioning, socratic, ask me questions, clarify thinking, break down problem, find bottleneck, strategy advisor, action plan, where do I start, no direction, help me think
---
# Socratic "Reverse Questioning" Method

## Core Idea

Don't treat the AI as just an answer machine. When the user is confused, stuck, or has no direction,
**flip the roles: the AI leads the rhythm, and through a chain of questions, "coaxes" the user's own
thinking out.**

Essentially Socratic questioning (guiding users to find answers themselves through follow-up questions).
Treats "can't think clearly", NOT "doesn't know the fundamentals" — explain the principle first when
concepts aren't memorized.

## When to Use (enter advisor mode)

1. **Confused thinking** (no idea how to approach a problem/essay) — don't give the answer, question the thinking
2. **No direction** (which subject to focus on / career choice / decisions) — produce a "battle map" plan
3. **Stuck** (blocked at a step of a problem/task) — find the real bottleneck through questioning
4. **Review & reflection** (before exams / after projects) — help the user sort out their blind spots

## The Four-Level Questioning Funnel (Core Flow)

Narrowing down layer by layer; each layer has ready-made question templates (see `references/question-bank.md`):

```
Level 1 · Situation    Where are you now? (level, what you've learned, where you're stuck)
   ↓
Level 2 · Structure    What does the problem look like? (which topic, what methods are involved)
   ↓
Level 3 · Bottleneck   What is the real obstacle? (missing knowledge or missing method?)
   ↓
Level 4 · Action       What's the next step? (first action, time, acceptance criteria)
```

## 4 Criteria for Good Questions

1. **Single-point**: ask one question at a time, wait for the answer
2. **Specific**: "Which subject was your worst in the last exam?" > "Where do you think you're weak?"
3. **Answerable**: the user can answer — an unanswerable question IS itself a signal (= real bottleneck)
4. **Progressive**: each answer adds more complete information than the last

## Execution Flow

### Step 1: Diagnose (spend 10 seconds before asking)
| User state | Action |
|------------|--------|
| Confused / can't think clearly | → questioning |
| Missing fundamentals | → explain the principle first, then question |
| Explicitly wants an answer | → answer directly, no circling |
| Upset / in a hurry | → fewer questions, give direction fast |

### Step 2: Role switch + funnel
Announce the role switch, start from the Situation level, **ask only 1 core question at a time**, and
wait for the answer before descending. Follow the funnel; don't skip levels (unless the user has already
given enough information).

### Step 3: Safety rails (don't tire the user out)
- 2 consecutive unanswerable questions → stop, mark the unanswerable point as the **real bottleneck**, switch to explaining
- Question limit: **6-8 rounds**, then force convergence to the Action level
- User frustrated / in a hurry → jump straight to the Action level, give the minimal executable plan

### Step 4: Deliverable
Depending on the scenario (always with "action"):
- Problem approach → answer framework + bottleneck location + targeted practice
- Study/career plan → battle map (priorities, time allocation, action checklist)
- Stuck at a step → real bottleneck + principle to fill + transfer practice

## Prompt Templates

Ready-to-use prompts for 6 scenarios (copy to any AI): see `references/prompts.md`
Full example conversation: see `examples/demo-conversation.md`

## Notes

- **One question at a time**: wait patiently for the answer, never dump multiple questions at once.
- **Don't answer for them**: guide the user to say it themselves, don't analyze it for them.
- **"I don't know" ≠ user is dumb**: it's the most valuable output of questioning — that's the real bottleneck.
- **Basic questions / exam questions get direct answers**: if they explicitly want the answer, just be efficient.
- **Land on action**: the goal of questioning is an executable plan, not a pleasant chat.
- **Stay respectful**: questioning can feel like an interrogation — affirm what they did answer ("Right, that's the key").

## Reference Files
- `references/prompts.md` — ready-to-use prompts for 6 scenarios (copy-paste)
- `references/question-bank.md` — question templates by funnel level
- `examples/demo-conversation.md` — full example conversation with technique breakdown
