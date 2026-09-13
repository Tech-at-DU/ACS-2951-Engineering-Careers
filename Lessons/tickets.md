<!-- Run as a slideshow: reveal-md Lessons/Lesson1.md -w -->
# Ticket Writing

⭐️ **GOAL:** Walk out able to write a feature ticket a teammate can start from, ROAM a known risk, and file a bug with repro plus current vs expected.

<!-- omit in toc -->
## ⏱ Agenda

- [[**10m**] ☀️ Warm Up](#10m-️-warm-up)
- [[**40m**] 📚 TT: Tickets a teammate can start from](#40m--tt-tickets-a-teammate-can-start-from)
- [[**10m**] 🌴 Break](#10m--break)
- [[**25m**] 💻 Activity 1](#25m--activity-1)
- [[**30m**] 💻 Activity 2](#30m--activity-2)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Split one feature into tickets a teammate can start without a hallway conversation
1. Judge whether a ticket has enough to start — story, requirements, why, edges, risks
1. Write a feature ticket with a user story, requirements, business value, edge cases, and a ROAMed risk
1. Write a bug ticket with a summary, diagnostics, repro steps, and current vs expected behavior

**How you’ll know:** Activity 1 produces a feature ticket with those five parts and a named MVP cut line. Activity 2 produces a bug ticket a teammate could pick up tomorrow.

<!-- > -->

## [**10m**] ☀️ Warm Up

Last session: what a PM owns, one answer-first pitch, a thin PRD. That doc is the *why*. Tickets are how the work actually enters the sprint.

**Scene:** Monday standup. “Can someone pick up deletion?” The ticket says:

```text
Title: Allow true deletion
Description: We never actually delete data — we just flip flags.
Please make it so we can really delete records from the database.
Due Friday.
```

Three engineers, three different products. One hard-deletes user rows. One adds a purge job and bricks billing. One spends two days asking questions that should have been in the ticket.

That’s not a process failure. That’s a missing ticket.

Think and jot (60s):

```text
First question I would ask before starting:
What I would refuse to guess:
What “done” even means on Friday:
```

Say:

> “A ticket is a handoff across time. The person who wrote it will be in another meeting — or gone — when you start. If the ticket only makes sense while they’re on Slack, it isn’t a ticket yet.”

**Rookie tip:** if you cannot name the user, the cut line, and one risk, you don’t have a ticket. You have a vibe.

<!-- > -->

## [**40m**] 📚 TT: Tickets a teammate can start from

**Next action:** Bad ticket → five-part feature ticket → split the feature → ROAM → bug shape.  
**Done when:** You can mark a ticket “startable” or “not yet” in one sentence, and say which part is missing.  
**≤2m next after TT:** Open Activity 1; copy the feature skeleton.

### 1. Why tickets exist (~6m)

Vague tickets create silent product forks. Nobody argues in the room. Everyone implements a different story, then argues in the PR.

A ticket is not bureaucracy. It’s how you hand work across timezones, PTO, and a Tuesday three months from now when nobody remembers the hallway conversation.

You will *receive* tickets long before you own the backlog. The same checklist tells you what to ask for — and when to send a ticket back instead of guessing.

**Rookie trap:** starting from “we need threads” or “just delete it” because you don’t want to look difficult. Asking “what’s the MVP cut line?” is the job.

<!-- -->

> **ASK AUDIENCE:** “Allow true deletion. We just flip flags today. Friday.” — can a teammate start tomorrow without you in Slack?

<details>
<summary>Answer</summary>

**No.** Missing: which records, who is allowed, what happens to billing / exports / legal hold, soft vs hard delete, which environment, how you test, and why now. The first question is “what does delete mean for *which* resource — and what must still exist after?”

</details>

### 2. Feature ticket anatomy (~12m)

A startable feature ticket has five parts. Skip one and someone will invent it.

| Part | Job | Test |
| --- | --- | --- |
| **User story** | Who, what, why for the *user* | You can name a persona and an end goal |
| **Requirements** | What it is and how it behaves | States, access, where it lives, what it does |
| **Business value** | Why the *company* pays for it | A non-technical reader gets why now |
| **Edge cases** | Known weird / extreme paths | You wrote what happens, not “handle errors” |
| **Risks** | What can go wrong + how you’ll ROAM it | Named owner or a conscious accept |

**User story** — one line, this shape:

> As a `[persona]` I want to `[do the thing]` so that I can `[end goal]`.

Restaurant example (journey, not the database):

> As a restaurant owner, I want to message customers who leave reviews so that I can follow up and serve them better.

That’s the *user*. It is not the business case. “Reviews drive repeat bookings” belongs under business value.

**Requirements** — what you’re building and how it behaves. Capture:

- Behavior in each state (empty, success, blocked, deleted)
- Who has access
- Where it lives (screen, API, job)
- What is *out* of scope for this ticket

**Business value** — one or two sentences. An exec should understand it. Not “we should use Postgres triggers.”

**Edge cases** — extreme, known, specific. Example: the owner sees a review headline, the reviewer deletes it, the owner clicks a link that now goes nowhere. What does the product do?

**Risks** — next beat. Don’t skip the heading because “we’ll be careful.”

Worked example — thin **threaded messages** MVP from last session:

```text
Title: One-level thread replies in channel

User story:
As a teammate in a busy channel, I want to reply in a thread
so the main channel stays readable and the decision has a URL.

Requirements:
- Reply-to-message opens a one-level thread
- Thread has a stable URL
- A reply notifies thread participants
- Out of scope: infinite nest, moving threads, emoji-only threads

Business value:
Unreadable channels slow decisions and create meeting tax.
One-level threads keep launch-week decisions in one place.

Edge cases:
- Original message is deleted after replies exist
- Reply from someone who left the channel
- Empty / whitespace-only reply

Risks:
- Notification fanout on mobile
  ROAM: Mitigate — batch pushes. Own — [name] checks payload size before ship.
```

<!-- -->

> **ASK AUDIENCE:** “As a teammate I want threads so channels stay readable.” — user story or business value? What’s missing?

<details>
<summary>Answer</summary>

**User story (almost).** Persona + want are there. Tighten the *so that* into a user goal (“so I can find the decision later without scrolling”). “Cuts meeting tax / saves CS archaeology” is **business value** — keep it in that field, not stuffed into the story.

</details>

### 3. Split the feature — MVP, then iterate (~8m)

One feature is often several tickets. A ticket should not feel like a novel. If it does, it isn’t one ticket.

The deletion prompt is a quarter if you treat it as one line:

| Ticket | MVP cut |
| --- | --- |
| 1 | Define “deleted” for *one* resource (what the flag means today) |
| 2 | Add a purge path for that resource only, with an undo window |
| 3 | Billing / export / legal-hold checks before hard delete |
| Later | Other resources, admin UI, cross-region purge |

Same move on threads: reply + URL + one-level nest this ticket. Fanout polish, mobile parity, infinite nest — later tickets.

Say:

> “Skateboard, then car. One wheel is not a product. A fully spec’d car in ticket one is how Friday slips to next month.”

**Rookie trap:** bundling “also dark mode” onto a ticket because the founder DMed. That’s a scope fight, not a requirement. Last session’s move still holds: name the tradeoff, then write a *separate* ticket or it doesn’t count.

### 4. ROAM the risks you already know (~6m)

If you can see the risk, write it down and pick a letter. Surprise risks still happen. *Known* risks with no owner are how you ship a page and a fire.

| Letter | Meaning | Looks like |
| --- | --- | --- |
| **R**esolve | Answered, avoided, or eliminated | “We will not hard-delete; purge is undoable for 30 days.” |
| **O**wn | A named person is responsible | “Sam owns legal-hold check before purge runs.” |
| **A**ccept | Eyes open; we will not act | “First week we accept slower exports. Noted.” |
| **M**itigate | Shrink impact or likelihood | “Batch notifications; cap 50 recipients on v1.” |

Accept is a decision. “We’ll see” is not Accept. Own without a name is not Own.

<!-- -->

> **ASK AUDIENCE:** “We might blow the notification service. Nobody owns it. We shipped anyway.” — which ROAM letter did they skip?

<details>
<summary>Answer</summary>

They skipped **Own** (no name) and did not really **Accept** (no written decision). “Shipped anyway” is hope, not a letter. Minimum fix: name an owner *or* write “Accept: v1 may drop pushes; we will watch error rate.” Better: **Mitigate** with a batch/cap, **Own** the check.

</details>

### 5. Bug tickets — five parts, no novel (~6m)

A bug ticket is how someone reproduces your Tuesday afternoon. “It’s broken” is a Slack message, not a ticket.

| Part | Job |
| --- | --- |
| **Summary** | 1–2 sentences. What failed, where. |
| **Diagnostics** | Platform, OS, browser / app version, env, role, build. |
| **Repro steps** | Numbered. Start from a clean state. |
| **Current behavior** | What you see. Not what you wish. |
| **Expected behavior** | What the product should do. |

Worked example:

```text
Title: Thread reply sends two push notifications

Summary: Replying in an existing thread delivers two identical pushes ~1s apart.

Diagnostics:
- iOS 18.6 · app 4.2.1 · production
- Role: channel member (not admin)
- Thread with 3 existing replies

Repro:
1. Open #launch
2. Reply in an existing thread with one word
3. Lock the phone and wait for push

Current: two identical pushes about one second apart.
Expected: one push per reply (or one batched summary).
```

**Rookie trap:** filing current *or* expected, not both. “Wrong” is not a behavior. Two sentences — what happened, what should have.

If you can’t repro it twice, say so. “Saw once, cannot repro” is still a ticket — mark it. Guessing a root cause in the title (“Redis is down”) is not.

### 6. Bridge into practice (~2m)

Say:

> “Activity 1: write one startable feature ticket — threads MVP or a feature you actually shipped. Activity 2: file a real-shaped bug and run the checklist on your own ticket. Break first.”

<!-- -->

> **ASK AUDIENCE:** What is the done-state for Activity 1?

<details>
<summary>Answer</summary>

A feature ticket with all five parts filled, a named **MVP cut / out of scope** line, and **one risk with a ROAM letter** (and a name if the letter is Own). Title + user story pasted as the visible checkpoint.

</details>

<!-- > -->

## [**10m**] 🌴 Break

Stand up. Leave the bad deletion ticket on screen if you want — Activity 2 can rewrite it.  
**≤2m next when back:** open Activity 1; copy the skeleton; don’t invent a new tracker.

<!-- > -->

## [**25m**] 💻 Activity 1

**Write one startable feature ticket.** Solo · visible checkpoint · artifact.

| | |
| --- | --- |
| **Next action** | Copy the skeleton. Pick **threaded-messages MVP** (from last session) *or* one small feature you have actually shipped. |
| **Done when** | Five parts filled, MVP cut / out of scope named, one risk ROAMed. |
| **Artifact** | A doc, issue, or markdown file you can paste from. |
| **Checkpoint (visible)** | Paste **title + user story** in chat or notes when asked. |

### Skeleton (copy)

```text
Title:

User story:
As a  I want to  so that I can

Requirements:
-
-
- Out of scope:

Business value:
(1–2 sentences a non-technical reader would accept)

Edge cases:
-
-

Risks (ROAM):
- Risk:
  Letter (R/O/A/M):
  Owner or written accept:
```

### Steps

1. Pick the feature. Smaller is better. “The whole app” is not a ticket.
2. Write the user story in one sentence. If you need a paragraph, the feature is still too big — split, then write ticket one.
3. List requirements as behavior, not architecture. Who, where, what happens.
4. Write business value last if you’re stuck — *why now* for the company, not the stack.
5. Add two edge cases that have actually bitten you, or would. For threads, start with “original message deleted.”
6. ROAM one risk. If the letter is Own, put a name (yours is fine).

| Pace | Done looks like |
| --- | --- |
| Floor | Story + requirements + out of scope |
| On track | Floor + business value + one edge + one ROAMed risk |
| Ahead | On track + a second ticket that is *explicitly* “not this MVP” |

If stuck: write only the user story and the out-of-scope line, then fill requirements.

**Rookie tip:** the restaurant story is a template, not the assignment. Don’t invent a restaurant unless that’s the product.

<!-- > -->

## [**30m**] 💻 Activity 2

**File a bug a teammate can reproduce — then stress-test a ticket.** Same tracker. Less scaffolding.

| | |
| --- | --- |
| **Next action** | Write a bug ticket (real or the thread-push scenario). Then run the checklist on *your* Activity 1 ticket. |
| **Done when** | Bug ticket has summary, diagnostics, numbered repro, current, and expected. You can say one thing you changed on the feature ticket after the checklist. |
| **Artifact** | Bug ticket + a one-line note: “Changed ___ because ___.” |
| **Checkpoint** | Paste the bug **title + expected** line. |

### Bug skeleton (copy)

```text
Title:

Summary (1–2 sentences):

Diagnostics (OS / browser or app / version / env / role):

Repro:
1.
2.
3.

Current behavior:

Expected behavior:
```

### Path A — you have a real bug

Use something you hit this month. If diagnostics are fuzzy, write “unknown — saw on ___” rather than inventing a build number.

### Path B — use the thread scenario

Title: `Thread reply sends two push notifications`  
Fill diagnostics and expected as if you just saw it on a phone. Repro must be numbered.

### Then: checklist on the feature ticket (10m)

Read your Activity 1 ticket as if you were *not* in the meeting.

- [ ] A teammate can name the user and the end goal
- [ ] Requirements say how it behaves, not “make it work”
- [ ] Out of scope is written (MVP cut line)
- [ ] Business value would survive an exec skim
- [ ] At least one edge case says what the product *does*
- [ ] One risk has a ROAM letter (and a name if Own)
- [ ] This is one ticket, not a quarter

Change one thing. That’s the point.

If someone nearby can read it, great — ask them only: “Could you start tomorrow? What’s missing?” You do not need a partner. The checklist is the review.

### Stretch (only if MVP is green)

Rewrite the Warm Up deletion ticket into **two** startable feature tickets (purge-for-one-resource vs legal-hold / billing). Same five parts. Don’t write the novel.

### Hard no for this activity

- Do not file “it’s broken” with no repro.
- Do not put the root cause in the title unless you measured it.
- Do not depend on a live drawing game or a full room to finish.

<!-- > -->

## [**5m**] Wrap Up

**GOAL check:** You can say, in one breath:

1. A ticket is a handoff. If it only works while you’re in Slack, it isn’t done.
1. Feature tickets: story, requirements, business value, edges, ROAMed risks.
1. One feature, several tickets. MVP first. A novel is a smell.
1. ROAM is a decision: Resolve, Own (named), Accept (written), Mitigate.
1. Bugs need repro + current + expected. “Wrong” is not a behavior.

**≤2m wrap sticky (optional):**

```text
Shipped today:
Ticket I would send back:
Tomorrow's first 15m:
```

- Finish the feature ticket if the five parts are thin
- File the bug ticket if you only have a Slack paragraph
- One thing to try if stuck: rewrite the deletion ticket’s *user story* only — one sentence — then stop

<!-- > -->

## Additional Resources

1. **[Ticket Writing slides](https://docs.google.com/presentation/d/1ELpW7E9ccpW3rDtMEEaq57dvix00ca0GB2dxhrleJOY/edit#slide=id.p)** — older deck (same beats: feature parts, bugs, ROAM). Teach from this file; use the deck as a projector spare.
1. **[Ticket Writing — How to Write Requirements and Not Flip a Table](https://docs.google.com/presentation/d/1hbLIYsSZjO8upXxiEfxEn4T91GDK5ILKUwEEoXE1vaw/edit)** — alternate copy of the same lesson slides.
1. **[ROAM risk management (SAFe)](https://content.intland.com/blog/agile/safe/roam-risk-management-under-safe)** — Resolve / Own / Accept / Mitigate background.
1. **[Atlassian — user stories](https://www.atlassian.com/agile/project-management/user-stories)** — persona / want / so-that shape.
1. **[GitHub — writing issue bodies](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/creating-an-issue)** — a tracker-shaped place to paste today’s skeletons.

<details>
<summary>For curriculum authors</summary>

### In Class

| | |
| --- | --- |
| **Next action** | Open this file → skim the Agenda jump list → start at the GOAL, then Warm Up. |
| **Done when** | The room can write a five-part feature ticket, ROAM one risk, and file a bug with repro + current vs expected. |
| **≤2m next** | Optional sticky in notes: Feeling / Behind\|On track\|Ahead / Today’s MVP. |

```text
Feeling (1 word):
Behind | On track | Ahead:
Today's MVP (1 sentence): write one startable feature ticket; file one bug a teammate can repro
```

### Facilitator notes

- **Teach from this file** (`Lessons/tickets.md`). `Lessons/06-tickets.md` is a pointer only.
- **Do not run Telephone / Gartic Phone.** The old deck opens with a drawing-spec game. Same learning (detail prevents silent forks) is the Warm Up deletion ticket + ASK AUDIENCE #1. Audience-dependent games fail remote / thin rooms.
- Voice: write-like-you-talk. Short blocks. GOAL first. On-the-job, not classroom.
- Continuity: last session is PMs / thin PRD / threaded-messages pitch. Use that feature as the default Activity 1. Own-project path is the fallback.
- Live-model the threads ticket (TT §2) on a shared doc for five minutes. Then get out of the way.
- Keep all four ASK AUDIENCE pulses; they replace digressions.
- Behind at ~0:35? Skip the restaurant aside — jump to ROAM → bug shape → Activity 1.
- Solo activities by design. Optional 60s “could you start?” swap after the checklist — never required.
- Have one extension ready: deletion-ticket split (Activity 2 stretch).
- Projector spare: slides linked under Additional Resources. Do not send people to the deck for the teach-from.

### Expert follow-ups

Flag for follow-up (do not block the live block):

1. **Tracker of record** — GitHub Issues, Linear, Jira? Skeletons are tracker-agnostic on purpose.
2. **PRD vs ticket** — confirm the prior session still assigns a thin PRD; Activity 1 should *not* rewrite the whole PRD.
3. **ROAM depth** — SAFe article is background only; four letters + a name is the live floor.
4. **Old numbered path** — keep `06-tickets.md` as a stub so old bookmarks don’t 404.

</details>
