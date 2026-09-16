<!-- Run as a slideshow: reveal-md Lessons/writing-lab.md -w -->
# Writing Lab — Day 7

⭐️ **GOAL:** Leave with a project write-up draft you can link, shaped by peer feedback and patterns from strong eng posts.

<!-- omit in toc -->
## ⏱ Agenda

- [[**10m**] ☀️ Warm Up](#10m-️-warm-up)
- [[**35m**] 📚 TT: Write-Ups Others Can Use](#35m--tt-write-ups-others-can-use)
- [[**10m**] 🌴 Break](#10m--break)
- [[**25m**] 💻 Activity 1: Analyze Hacker News High Ranking Posts](#25m--activity-1-analyze-hacker-news-high-ranking-posts)
- [[**35m**] 💻 Activity 2: Draft Your Project Write-Up](#35m--activity-2-draft-your-project-write-up)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Name three patterns that show up in strong eng write-ups (and three that weaken them)
1. Turn peer feedback into concrete edits on a project narrative
1. Draft a project write-up with challenge, approach, outcome, and one takeaway
1. Leave a clear next-step note so next week’s final-project / demo work has a first cut

<!-- > -->

## [**10m**] ☀️ Warm Up

Last session: tickets a teammate can start from — story, requirements, business value, edges, ROAM. Tickets pass *work*. Today’s write-up passes *story* — why this project exists, what you tried, what stuck.

**Scene:** Someone pastes a project into a public channel:

```text
Built a cool app with React and Postgres.
It was hard but I learned a lot.
Link soon.
```

Three readers, three shrugs. No challenge. No decision. No lesson anyone else can reuse.

Think and jot (60s):

```text
One sentence on the challenge that forced this project:
One decision a new reader would care about:
One takeaway I want them to keep:
```

Say:

> “A project write-up passes context forward the same way a ticket does. You next quarter, a hiring manager, and a teammate onboarding later all need the same outline: challenge → approach → outcome → takeaway.”

**PROTIP:** if you cannot name the challenge in one sentence, you don’t have a write-up yet. You have a changelog.

<!-- > -->

## [**35m**] 📚 TT: Write-Ups Others Can Use

**Next action:** Patterns from strong posts → feedback that names a fix → four-section draft outline.  
**Done when:** You can mark a draft “ready to link” or “still needs work” and name the missing section.  

### 1. Why the Write-Up Exists (~6m)

Code alone rarely carries a decision. The write-up is how the *decision* reaches someone who wasn’t in the room — what broke, what you tried, what you’d do again.

On the job you’ll publish READMEs, RFC notes, postmortems, and “what we built” posts. Same outline every time. Fancy voice is optional. Clear sections are not.

**BE AWARE:** writing for people who already sat in the room. If the draft only works while you’re narrating it live, it isn’t a write-up yet.

<!-- -->

> **ASK AUDIENCE:** “Built a cool app with React and Postgres. Learned a lot.” — can a new reader decide whether to open the repo?

<details>
<summary>Answer</summary>

**No.** Missing: who it was for, what problem hurt, what you chose and why, what still fails, and the one lesson worth keeping. The first fix is one sentence of *challenge*, not another tech list.

</details>

### 2. What Strong Eng Posts Share (~12m)

Look at patterns in [HN favorites analysis (Observable)](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis) and skim live [Hacker News](https://news.ycombinator.com/) plus the [HN guidelines](https://news.ycombinator.com/newsguidelines.html). You’re hunting structure, not karma.

Common patterns in posts that hold up under a quick skim:

| Pattern | Looks like | Test |
| --- | --- | --- |
| **Concrete problem** | A person + a pain, not “I wanted to learn X” | A new reader nods before the stack appears |
| **Decisions, not diaries** | Tradeoffs you picked and what you refused | Someone could disagree with you in a comment |
| **Evidence** | Numbers, screenshots, failure modes, before/after | Claim without proof gets cut |
| **One takeaway** | The one sentence you’d keep | Not five morals and a shrug |
| **Respect the reader** | Short paragraphs, honest limits, no hype fog | Skimmable in under two minutes |

Anti-patterns that weaken trust:

- Tech list with no challenge named
- “It was hard” with no *what* was hard
- Victory lap with zero failure modes
- Secret jargon that only the team understands
- Links that promise a demo and deliver a 404

Say:

> “Skip writing for karma. Copy the *shape* of posts that respect someone who has two minutes.”

**PROTIP:** open with the pain, not the framework. The stack is secondary. The challenge is the story.

<!-- -->

> **ASK AUDIENCE:** A post titled “We rewrote our auth in Rust” with no latency, incident, or cost numbers — pattern or anti-pattern?

<details>
<summary>Answer</summary>

**Anti-pattern until evidence appears.** A rewrite claim without before/after (latency, error rate, cost, or a named incident) is a diary entry. Add one metric or one failure mode and it becomes a decision someone else can evaluate.

</details>

### 3. Peer Feedback That Becomes Edits (~8m)

Feedback that only says “looks good” doesn’t move the draft. Feedback that helps names a section.

Use this map when you read someone’s draft (or your own):

```text
Section that is strong:
Section that is missing or unclear:
One cut I would make:
One question a new reader would still ask:
```

On the job this is the same standard as ticket review applied to narrative. Same rule as tickets: if you can’t start from it without the author in Slack, send it back with the missing section named.

**BE AWARE:** rewriting their voice. Fix clarity and missing sections. Leave the personality unless they asked for a tone pass.

<!-- -->

> **ASK AUDIENCE:** Teammate says “tighten the middle.” Useful feedback — or incomplete?

<details>
<summary>Answer</summary>

**Incomplete.** Name the section: which part drifts, what claim lacks evidence, or which paragraph repeats the challenge. “Tighten” without a pointer is vague. “Cut the third paragraph — it restates the challenge without a decision” is feedback.

</details>

### 4. Four-Section Draft Outline (~9m)

Your draft needs four sections. Skip one and someone invents it.

| Section | Job | Prompt |
| --- | --- | --- |
| **Challenge** | Why this existed | What hurt? For whom? Why now? |
| **Approach** | What you tried and chose | Stack, cuts, tradeoffs, what you refused |
| **Outcome** | What changed | Works / partial / failed — with one piece of evidence |
| **Takeaway** | What a reader keeps | One sentence. Not five. |

Short worked example (threads feature from earlier sessions):

```text
Challenge:
Busy channels buried decisions. Teammates re-litigated the same call in standups.

Approach:
Released one-level thread replies with a stable URL. Refused infinite nest and emoji-only threads for v1.

Outcome:
Launch-week decisions lived in one URL. Notification fanout on mobile is still noisy — batched pushes are next.

Takeaway:
A thread without a URL is still a hallway conversation.
```

Reuse Slack notes, ticket language, and peer replies. Don’t start from a blank page if the channel already holds half the story.

Say:

> “Short draft first. Challenge + approach + outcome + one takeaway. Polish after the outline exists.”

<!-- -->

> **ASK AUDIENCE:** Which section is missing? “We used Postgres and Redis. Deployed Friday. Team is proud.”

<details>
<summary>Answer</summary>

**Challenge and takeaway are missing; outcome is light.** There’s a stack and a deploy date, but no pain, no decision, no evidence, and nothing a new reader should remember. Add who hurt, what you refused, one metric or failure mode, and one takeaway sentence.

</details>

<!-- > -->

## [**10m**] 🌴 Break

<!-- > -->

## [**25m**] 💻 Activity 1: Analyze Hacker News High Ranking Posts

> **DONE WHEN:** You have (1) three patterns you’ll reuse, (2) two anti-patterns you’ll avoid, (3) a feedback map on one draft section (yours or a teammate’s prior notes).

1. Open the [Observable HN favorites analysis](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis) and skim [HN](https://news.ycombinator.com/) for five minutes. Solo is fine.
1. Fill this card:

    ```text
    Patterns to reuse (3):
    Anti-patterns to avoid (2):
    One title/hook shape I want to try:
    ```

1. Pull one paragraph of project notes (Slack, README stub, or ticket “why”). Run the feedback map on it:

    ```text
    Section that is strong:
    Section that is missing or unclear:
    One cut I would make:
    One question a new reader would still ask:
    ```

> **PROTIP:** Stop at the card. Do not start the full essay until Activity 2. Pattern first, prose second.

> **FINISHED EARLY?** Rewrite one weak title into a challenge-first hook (no stack in the title).

<!-- > -->

## [**35m**] 💻 Activity 2: Draft Your Project Write-Up

> **DONE WHEN:** A draft you can link (Google Doc, Notion, or repo README) has all four sections filled — rough is fine; empty sections are not.

1. Create or open a doc titled with the *challenge*, not the stack.
1. Paste the four-section outline. Fill each section in order. Reuse channel notes and Activity 1 feedback.
1. Add one piece of evidence under Outcome (metric, screenshot note, or named failure mode).
1. End with a single takeaway sentence.
1. Prompts if a section stalls:

    ```text
    Challenge: What forced this — assignment pressure is allowed, but name the user pain too.
    Approach: Which technology did you pick, and what did you refuse?
    Outcome: Did the challenge move? Why or why not?
    Takeaway: What should a reader remember after they close the tab?
    ```

> **PROTIP:** Publish an ugly complete outline over a polished first paragraph. Next week’s final-project / demo work needs a story you can point at.

> **FINISHED EARLY?** Swap docs for 90 seconds — a teammate names one missing section only, then return to writing.


## [**5m**] Wrap Up

**GOAL check:** You can say, in one breath:

1. Write-ups pass story the way tickets pass work.
1. Strong posts: concrete problem, decisions, evidence, one takeaway.
1. Feedback names a section — “tighten” alone is incomplete.
1. Four sections: challenge → approach → outcome → takeaway.

**Optional wrap note:**

```text
Finished today (outline sections filled):
Section still unclear:
Tomorrow's first 15m (final-project / demo cut):
```

- Finish any empty section before next session
- One thing to try if stuck: rewrite *only* the challenge sentence — then stop
- Next week leans final project / demo — this write-up is the story you’ll point at if demos go sideways

<!-- > -->

## Additional Resources

1. **[HN favorites analysis (Observable)](https://observablehq.com/@tomlarkworthy/hacker-favourites-analysis)** — patterns across highly favorited HN posts (structure hunt, not karma chase).
1. **[Hacker News](https://news.ycombinator.com/)** — live front page for skimming hooks and titles.
1. **[HN guidelines](https://news.ycombinator.com/newsguidelines.html)** — what the community treats as substantive vs. fluff.
1. **[GitHub — About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)** — the same outline often shows up in the repo root.
1. **[Write the Docs — docs principles](https://www.writethedocs.org/guide/writing/docs-principles/)** — audience-first framing for technical narrative.

<details>
<summary>For Curriculum Authors</summary>

## For Curriculum Authors

### In Class

| | |
| --- | --- |
| **Next action** | Open this file → Agenda jump list → GOAL → Warm Up. |
| **Done when** | Room can mark a draft ready-to-link / still-needs-work and has a four-section outline in a linkable doc. |

```text
Feeling (1 word):
Behind | On track | Ahead:
Today's MVP (1 sentence): four-section project write-up outline in a linkable doc
```

### Facilitator Notes

- **Teach from** `Lessons/writing-lab.md` (canonical). Keep `Lessons/07-Writing-Lab.md` as a pointer so old bookmarks don’t 404.
- Continuity: Day 6 tickets / ROAM / short PRD. Reuse the threads (or own-project) example — do not invent a new product mid-session.
- Voice: short speakable blocks. On-the-job builder voice. No classroom / roster language in the body.
- Old source had breakouts + `spd-jr` channel validation. Small/remote rooms: Activity 1 is solo-capable; teammate swap in Activity 2 is optional 90s, never required.
- Keep all four ASK AUDIENCE pulses; they replace digressions.
- Behind at ~0:30? Cut Observable deep-skim — use HN front page titles only → jump to four-section outline → Activity 2.
- Live-model the threads write-up outline (TT §4) on a shared doc for four minutes. Then get out of the way.
- Observable may rate-limit some networks; HN front page + guidelines are the fallback pattern source.
- Projector spare: none required. This file is the teach-from.

### Expert Follow-Ups

Flag for follow-up (do not block the live session):

1. **Observable durability** — if `@tomlarkworthy/hacker-favourites-analysis` dies, replace with another public HN-corpus write-up; keep HN guidelines + front page as floor.
2. **Deliverable surface** — confirm whether final project wants Google Doc, README, or both; outline stays the same.
3. **Channel validation** — old `spd-jr` peer-response step retired for audience-dependence; restore only if a standing async channel prompt exists.
4. **Old numbered path** — keep `07-Writing-Lab.md` as a stub pointer to `writing-lab.md`.

</details>
