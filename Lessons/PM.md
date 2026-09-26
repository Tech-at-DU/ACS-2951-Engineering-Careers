<!-- Run as a slideshow: reveal-md Lessons/Lesson05-PMs.md -w -->
# PMs & Communication

⭐️ **GOAL**: Walk out able to say what a PM owns, write one answer-first stakeholder pitch, and push back on scope with a real tradeoff.

<!-- omit in toc -->
## ⏱ Agenda

- [[**15m**] ☀️ Warm Up](#15m-️-warm-up)
- [[**45m**] 📚 TT: Working with PMs without getting steamrolled](#45m--tt-working-with-pms-without-getting-steamrolled)
- [[**10m**] 🌴 Break](#10m--break)
- [[**50m**] 💻 Activity](#50m--activity)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this class, you'll be able to&hellip;*

1. Explain what a PM owns (**what/why**) vs what eng owns (**how**) vs who owns **when**
1. Write one feature pitch aimed at one stakeholder, answer first
1. Protect sprint time with a clear tradeoff

<!-- > -->

## [**15m**] ☀️ Warm Up

Last time: leadership under pressure — styles, candor, serving the team. Today is the same pressure on the product side.

**Scene:** Friday. Launch Monday. Sales wants a banner. Design wants polish. A founder DMs: “can we also do dark mode?” Three days of work. Two days left.

Panic answers: yes (and ship garbage) or no (and sound difficult).

Third move: make the cost visible. “We can pull dark mode in. Then X slips, or we cut Y. Which outcome matters more?”

That’s not attitude. That’s engineering with a calendar.

```text
One “just one more thing” moment:
What you felt:
What you did:
What you’d say next time (tradeoff, not yes/no):
```

<!-- > -->

## [**45m**] 📚 TT: Working with PMs without getting steamrolled

| Min | Beat |
| --- | --- |
| 0–7 | Why this matters |
| 7–15 | What a PM actually optimizes for |
| 15–24 | Ownership, using threaded messages |
| 24–32 | One feature, four audiences |
| 32–39 | Tools you’ll touch anyway |
| 39–45 | Scripts + live model |

<aside class="notes">
Primary deck: https://docs.google.com/presentation/d/1cK3U9-87ysDcjOVdVOhJNniNiO77FZtIrUixGYonxKU/edit
</aside>

### 0–7 · Why this matters

A lot of career advice treats product people like another species. That’s how you lose scope fights.

Friday before launch, the asks pile up. If all you know is how to write code, all you’ve got is panic answers. If you understand the PM’s job, you answer with a tradeoff: what ships, what slips, and what metric that serves.

You don’t need the PM title. You need enough product language that scope stops turning into a personality contest.

### 7–15 · What a PM optimizes for

Strip it down: ship the right thing for the right reason.

Not bossing engineers. Not winning Slack. Not handwriting every ticket.

They own **what** you’re building — and what you’re not — and **why** it matters now.  
You own **how**: design, architecture, quality, honest estimates.  
Someone owns **when**: timeline, dependencies, launch checklist. At a small company that’s often the same PM wearing two hats. Separate the questions anyway.

A PM’s day is mostly collisions — eng, eng manager, execs, CS, marketing, design, QA, sales. They’re a translation layer. Bad translation means thrash.

Two traps:

1. Ticket fairy — “just tell me what to build.”
1. Enemy mode — “PMs don’t get eng.”

Both make you weaker on teams and in interviews. The PM owns outcomes. You own a system that can survive those outcomes.

### 15–24 · Ownership · threaded messages

Running example: threaded messages in a chat product.

| Role | Owns | Threads question |
| --- | --- | --- |
| PM | What / Why | Does this cut noise enough to move retention or seats? |
| Engineer | How | Reply graph, notifications, mobile, migrations, perf |
| Timeline | When | Can it land this quarter without slipping search? |

“Can we ship threads?” is not “are you smart?” It’s “is the why worth eng weeks?”

In that conversation, bring three things:

1. Cost — weeks, risk, complexity
1. Coupling — what else has to wait
1. Cut line — what’s a thin MVP

“My internship PM told us how” — small companies blur roles. You still own how. If they’re deciding architecture for you, that’s a smell — not a reason to check out.

### 24–32 · One feature, four audiences

Same feature. Different emphasis. Match the metric they care about — not lies.

**Founders / execs** — As the company grows, channels get unreadable. Threads keep decisions moving and cut meeting tax. Pitch the business outcome, not the UI chrome.

**Engineers** — MVP is reply-to-message, one-level nest, notification batching. Out of scope for v1: infinite nest, emoji-only threads, moving threads across channels. Call out fanout and mobile early.

**Customer Success** — People @-spam or DM just to keep context. Threads give “the bug thread” a URL. Less archaeology.

**Sales / Marketing** — Buyers already know this pattern. Demo line: “Your deal channel stays readable when twelve people join.”

Before you answer a scope ask, name the audience. Lead with their metric. Eng-only truth makes “no” sound arbitrary upstairs.

### 32–39 · Four tools you’ll touch anyway

1. **Issue tracking** — what’s actually in the sprint. Drive-by Slack asks either land here or they don’t count.
1. **Timeline** — dependencies get visible. Dark mode isn’t free if it blocks launch item four.
1. **Analytics** — if nobody defined the event, you can’t prove the feature worked. Day one: what are we measuring?
1. **A thin PRD** — one screen. Problem, why now, solution, use case, out of scope, success metric. Collaborate on it; don’t ghost it. (Skeleton is in the Activity.)

### 39–45 · Scripts + live model

Chain of command breaks. People DM you. Keep a spine.

1. **Tradeoff** — “We can pull that in before Friday. Then launch item X slips, or we cut Y. Which matters more?”
1. **Priority** — “Is this higher than anything already in the sprint? If yes, what comes out?”
1. **Metric** — “What moves: retention, tickets, conversion? If we don’t know, maybe this isn’t Friday work.”
1. **Redirect** — “I’ll estimate. Drop it in the tracker, or confirm with the PM, so it doesn’t ghost the plan.”

Minto when stakes are high: answer first, then two or three reasons, details only if asked.

**Model:**

> Should we ship threaded messages next sprint?  
> **Answer:** Yes for a thin MVP — not full parity.  
> **Why:** Channel noise already slows decisions, and one-level threads give CS a single URL.  
> **Limit:** Notification fanout and mobile wait for v1.1.  
> **Ask:** If this takes two eng weeks, what exits the sprint?

Clarity under pressure is the same muscle as leadership earlier this term. Protecting time serves the team. It isn’t about winning Slack.

<!-- > -->

## [**10m**] 🌴 Break

<!-- > -->

## [**50m**] 💻 Activity

### Worked example (Founders pitch)

```text
Audience: Founders
Answer: Ship a thin threaded-messages MVP this sprint.
Why: Unreadable channels slow decisions; threads cut meeting tax.
Why: CS needs one URL for “the bug thread,” not archaeology.
Limit: One-level nest; mobile polish waits.
Ask: If this takes two eng weeks, what exits?
```

### PRD skeleton (copy into your doc)

```text
Feature:
Problem (1–2 sentences):
Why now:
Solution (3–5 sentences):
Primary user + one use case:
Out of scope:
Success metric:
Open eng questions:
```

### Build

1. Copy the PRD skeleton above.
1. Pitch A — Founders or Execs, answer first.
1. One tradeoff sentence for a mid-sprint “dark mode” DM.
1. Fill the PRD skeleton for the same feature (threaded messages or your pick).
1. If time: Pitch B — Engineers or CS.
1. Stretch: remaining pitches + one day-one analytics event.

| Pace | Done looks like |
| --- | --- |
| Floor | Pitch A + tradeoff sentence |
| On track | Floor + PRD skeleton filled |
| Ahead | Floor + PRD + Pitch B (or four pitches) |

If stuck: write only the Founders answer line — one sentence — then fill Problem / Why now on the PRD.

**Before Mon Sep 14:** four stakeholder pitches + finished PRD skeleton. Optional: one paragraph — do you want a PM-track role? Why or why not.

<!-- > -->

## 📚 Additional Resources

1. [PMs & Communication deck](https://docs.google.com/presentation/d/1cK3U9-87ysDcjOVdVOhJNniNiO77FZtIrUixGYonxKU/edit)
1. [05. PMs & Communication](https://drive.google.com/drive/folders/1HRr5fEK-moO3IWdxZni4178U52EqQ0Hn)
1. [ACS 2951 course folder](https://drive.google.com/drive/folders/1BT-2RYJtEsvSe4xwhHNPrHc9yF2kiC6L)
1. [How to Write a Self-Paced Lesson](https://docs.google.com/document/d/16O2xGeNSayfQ1cC03fwMKzBA25c5yrnMrrQ5QfKyY50)
