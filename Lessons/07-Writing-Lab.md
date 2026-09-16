<!-- Run as a slideshow: reveal-md Lessons/writing-lab.md -w -->
# Writing Lab — Day 7

⭐️ **GOAL:** Leave with a shareable project write-up draft that uses peer feedback and patterns from high-signal eng posts — not a stack dump with no problem statement.

<!-- omit in toc -->
## ⏱ Agenda

- [[**10m**] ☀️ Warm Up](#10m-️-warm-up)
- [[**35m**] 📚 TT: Write-ups that travel](#35m--tt-write-ups-that-travel)
- [[**10m**] 🌴 Break](#10m--break)
- [[**25m**] 💻 Activity 1](#25m--activity-1)
- [[**35m**] 💻 Activity 2](#35m--activity-2)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Name three patterns that show up in high-signal eng write-ups (and three that kill them)
1. Turn peer feedback into concrete edits on a project narrative
1. Draft a shareable project write-up with challenge, approach, outcome, and one takeaway
1. Leave a clear next-step note so next week’s final-project / demo work has a first cut

**How you’ll know:** Activity 1 produces a pattern list + feedback map. Activity 2 produces a shareable doc with all four sections filled (even if rough).

<!-- > -->

## [**10m**] ☀️ Warm Up

Last session: tickets a teammate can start from — story, requirements, business value, edges, ROAM. Tickets hand off *work*. Today’s write-up hands off *story* — why this project exists, what you tried, what stuck.

**Scene:** Someone pastes a project into a public channel:

```text
Built a cool app with React and Postgres.
It was hard but I learned a lot.
Link soon.
```

Three readers, three shrugs. No challenge. No decision. No lesson anyone else can steal.

Think and jot (60s):

```text
One sentence on the challenge that forced this project:
One decision a stranger would care about:
One takeaway I want them to keep:
```

Say:

> “A project write-up is a handoff across time — same as a ticket. Future-you, a hiring manager, and a teammate onboarding next quarter all need the same spine: challenge → approach → outcome → takeaway.”

**Rookie tip:** if you cannot name the challenge in one sentence, you don’t have a write-up yet. You have a changelog.

<!-- > -->

## [**35m**] 📚 TT: Write-ups that travel

**Next action:** Patterns from high-signal posts → feedback that lands → four-section draft spine.  
**Done when:** You can mark a draft “shareable” or “not yet” and name the missing section.  
**≤2m next after TT:** Open Activity 1; skim the HN / Observable list with one review goal.

### 1. Why the write-up exists (~6m)

Code alone rarely travels. The write-up is how the *decision* travels — what broke, what you tried, what you’d do again.

On the job you’ll ship READMEs, RFC notes, postmortems, and “what we built” posts. Same spine every time. Fancy voice is optional. Clear sections are not.

**Rookie trap:** writing for people who already sat in the room. If the draft only works while you’re narrating it live, it isn’t a write-up yet.

<!-- -->

> **ASK AUDIENCE:** “Built a cool app with React and Postgres. Learned a lot.” — can a stranger decide whether to open the repo?

<details>
<summary>Answer</summary>

**No.** Missing: who it was for, what problem hurt, what you chose and why, what still fails, and the one lesson worth stealing. The first fix is one sentence of *challenge*, not another tech list.

</details>

### 2. What high-signal eng posts share (~12m)

Look at patterns in [HN favorites analysis (Observable)](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis) and skim live [Hacker News](https://news.ycombinator.com/) plus the [HN guidelines](https://news.ycombinator.com/newsguidelines.html). You’re hunting structure, not karma.

Common patterns in posts that travel:

| Pattern | Looks like | Test |
| --- | --- | --- |
| **Concrete problem** | A person + a pain, not “I wanted to learn X” | A stranger nods before the stack appears |
| **Decisions, not diaries** | Tradeoffs you picked and what you refused | Someone could disagree with you in a comment |
| **Receipts** | Numbers, screenshots, failure modes, before/after | Claim without evidence gets cut |
| **One takeaway** | The one sentence you’d keep | Not five morals and a shrug |
| **Respect the reader** | Short paragraphs, honest limits, no hype fog | Skimmable in under two minutes |

Anti-patterns that kill trust:

- Stack dump with no problem statement
- “It was hard” with no *what* was hard
- Victory lap with zero failure modes
- Secret jargon that only the team understands
- Links that promise a demo and deliver a 404

Say:

> “You’re not writing for HN points. You’re stealing the *shape* of posts that respect a busy engineer’s time.”

**Rookie tip:** open with the pain, not the framework. The stack is secondary. The challenge is the story.

<!-- -->

> **ASK AUDIENCE:** A post titled “We rewrote our auth in Rust” with no latency, incident, or cost numbers — pattern or anti-pattern?

<details>
<summary>Answer</summary>

**Anti-pattern until receipts appear.** A rewrite claim without before/after (latency, error rate, cost, or a named incident) is a diary entry. Add one metric or one failure mode and it becomes a decision someone else can evaluate.

</details>

### 3. Peer feedback that becomes edits (~8m)

Feedback that only says “looks good” doesn’t ship. Feedback that lands names a section.

Use this map when you read someone’s draft (or your own):

```text
Section that is strong:
Section that is missing or foggy:
One cut I would make:
One question a stranger would still ask:
```

On the job this is PR review energy applied to narrative. Same rule as tickets: if you can’t start from it without the author in Slack, send it back with the missing section named.

**Rookie trap:** rewriting their voice. Fix clarity and missing sections. Leave the personality unless they asked for a tone pass.

<!-- -->

> **ASK AUDIENCE:** Teammate says “tighten the middle.” Useful feedback — or incomplete?

<details>
<summary>Answer</summary>

**Incomplete.** Name the section: which part drifts, what claim lacks a receipt, or which paragraph repeats the challenge. “Tighten” without a pointer is vague. “Cut the third paragraph — it restates the challenge without a decision” is feedback.

</details>

### 4. Four-section draft spine (~9m)

Your shareable draft needs four sections. Skip one and someone invents it.

| Section | Job | Prompt |
| --- | --- | --- |
| **Challenge** | Why this existed | What hurt? For whom? Why now? |
| **Approach** | What you tried and chose | Stack, cuts, tradeoffs, what you refused |
| **Outcome** | What changed | Works / partial / failed — with one receipt |
| **Takeaway** | What a reader steals | One sentence. Not five. |

Worked thin example (threads feature from earlier sessions):

```text
Challenge:
Busy channels buried decisions. Teammates re-litigated the same call in standups.

Approach:
Shipped one-level thread replies with a stable URL. Refused infinite nest and emoji-only threads for v1.

Outcome:
Launch-week decisions lived in one URL. Notification fanout on mobile is still noisy — batched pushes are next.

Takeaway:
A thread without a URL is still a hallway conversation.
```

Reuse Slack notes, ticket language, and peer replies. Don’t start from a blank page if the channel already holds half the story.

Say:

> “Thin write-up first. Challenge + approach + outcome + one takeaway. Polish after the spine exists.”

<!-- -->

> **ASK AUDIENCE:** Which section is missing? “We used Postgres and Redis. Deployed Friday. Team is proud.”

<details>
<summary>Answer</summary>

**Challenge and takeaway are missing; outcome is thin.** There’s a stack and a ship date, but no pain, no decision, no receipt, and nothing a stranger should remember. Add who hurt, what you refused, one metric or failure mode, and one takeaway sentence.

</details>

<!-- > -->

## [**10m**] 🌴 Break

<!-- > -->

## [**25m**] 💻 Activity 1

**Done when:** You have (1) three patterns you’ll steal, (2) two anti-patterns you’ll avoid, (3) a feedback map on one draft section (yours or a teammate’s prior notes).

1. Open the [Observable HN favorites analysis](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis) and skim [HN](https://news.ycombinator.com/) for five minutes. Solo is fine.
1. Fill this card:

```text
Patterns to steal (3):
Anti-patterns to avoid (2):
One title/hook shape I want to try:
```

1. Pull one paragraph of project notes (Slack, README stub, or ticket “why”). Run the feedback map on it:

```text
Section that is strong:
Section that is missing or foggy:
One cut I would make:
One question a stranger would still ask:
```

**Rookie tip for on-the-job success:** stop at the card. Do not start the full essay until Activity 2. Pattern first, prose second.

If you finish early: rewrite one weak title into a challenge-first hook (no stack in the title).

<!-- > -->

## [**35m**] 💻 Activity 2

**Done when:** A shareable doc (Google Doc, Notion, or repo README draft) has all four sections filled — rough is fine; empty sections are not.

1. Create or open a shareable doc titled with the *challenge*, not the stack.
1. Paste the four-section spine. Fill each section in order. Reuse channel notes and Activity 1 feedback.
1. Add one receipt under Outcome (metric, screenshot note, or named failure mode).
1. End with a single takeaway sentence.

Prompts if a section stalls:

- Challenge: What forced this — assignment pressure is allowed, but name the *user* pain too.
- Approach: Which technology did you pick, and what did you refuse?
- Outcome: Did the challenge move? Why or why not?
- Takeaway: What should a reader remember after they close the tab?

**Stretch:** swap docs for 90 seconds — a teammate names one missing section only, then return to writing.

**Rookie tip:** ship an ugly complete spine over a polished first paragraph. Next week’s final-project / demo work needs a story you can point at.

<!-- > -->

## [**5m**] Wrap Up

**GOAL check:** You can say, in one breath:

1. Write-ups hand off story the way tickets hand off work.
1. High-signal posts: concrete problem, decisions, receipts, one takeaway.
1. Feedback names a section — “tighten” alone is incomplete.
1. Four sections: challenge → approach → outcome → takeaway.

**≤2m wrap note (optional):**

```text
Shipped today (spine sections filled):
Section still foggy:
Tomorrow's first 15m (final-project / demo cut):
```

- Finish any empty section before next session
- One thing to try if stuck: rewrite *only* the challenge sentence — then stop
- Next week leans final project / demo — this write-up is the story you’ll point at when demos wobble

<!-- > -->

## Additional Resources

1. **[HN favorites analysis (Observable)](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis)** — patterns across highly favorited HN posts (structure hunt, not karma chase).
1. **[Hacker News](https://news.ycombinator.com/)** — live front page for skimming hooks and titles.
1. **[HN guidelines](https://news.ycombinator.com/newsguidelines.html)** — what the community treats as substantive vs. fluff.
1. **[GitHub — About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)** — same spine often lands in the repo root.
1. **[Write the Docs — docs principles](https://www.writethedocs.org/guide/writing/docs-principles/)** — audience-first framing for technical narrative.

<details>
<summary>For curriculum authors</summary>

## For curriculum authors

### In Class

| | |
| --- | --- |
| **Next action** | Open this file → Agenda jump list → GOAL → Warm Up. |
| **Done when** | Room can mark a draft shareable/not-yet and has a four-section spine in a shareable doc. |
| **≤2m next** | Optional note: Feeling / Behind|On track|Ahead / Today’s MVP (four sections filled). |

```text
Feeling (1 word):
Behind | On track | Ahead:
Today's MVP (1 sentence): four-section project write-up spine in a shareable doc
```

### Facilitator notes

- **Teach from** `Lessons/writing-lab.md` (canonical). Keep `Lessons/07-Writing-Lab.md` as a pointer so old bookmarks don’t 404.
- Continuity: Day 6 tickets / ROAM / thin PRD. Reuse the threads (or own-project) example — do not invent a new product mid-block.
- Voice: short speakable blocks. On-the-job builder voice. No classroom / roster language in the body.
- Old source had breakouts + `spd-jr` channel validation. Thin/remote rooms: Activity 1 is solo-capable; teammate swap in Activity 2 is optional 90s, never required.
- Keep all four ASK AUDIENCE pulses; they replace digressions.
- Behind at ~0:30? Cut Observable deep-skim — use HN front page titles only → jump to four-section spine → Activity 2.
- Live-model the threads write-up spine (TT §4) on a shared doc for four minutes. Then get out of the way.
- Observable may rate-limit some networks; HN front page + guidelines are the fallback pattern source.
- Projector spare: none required. This file is the teach-from.

### Expert follow-ups

Flag for follow-up (do not block the live block):

1. **Observable durability** — if `@tomlarkworthy/hacker-favourites-analysis` dies, replace with another public HN-corpus write-up; keep HN guidelines + front page as floor.
2. **Deliverable surface** — confirm whether final project wants Google Doc, README, or both; spine stays the same.
3. **Channel validation** — old `spd-jr` peer-response step retired for audience-dependence; restore only if a standing async channel prompt exists.
4. **Old numbered path** — keep `07-Writing-Lab.md` as a stub pointer to `writing-lab.md`.

</details>
