<!-- Run as a slideshow: reveal-md Lessons/05-MakeVoiP_and_Blog.md -w -->
# MakeVoiP and Blog About It

⭐️ **GOAL:** Leave with a Zoom or Discord product-improvement proposal your team can present, plus a short eng blog draft you can link that names challenge, approach, outcome, and one takeaway.

<!-- omit in toc -->
## ⏱ Agenda

- [[**5m**] Attendance &amp; Announcements](#5m-attendance--announcements)
- [[**15m**] ☀️ Warm Up](#15m-️-warm-up)
- [[**30m**] 📚 TT: Assumptions, Consults, and Short Posts](#30m--tt-assumptions-consults-and-short-posts)
- [[**10m**] 🌴 Break](#10m--break)
- [[**40m**] 💻 Activity 1: MakeVoiP Product Consult](#40m--activity-1-makevoip-product-consult)
- [[**35m**] 💻 Activity 2: Blog Workshop Draft](#35m--activity-2-blog-workshop-draft)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Spot shared failure signals between a founder story and an external post-mortem
1. Name product changes that fix a real pain for Zoom or Discord users
1. Draft a short eng post with challenge, approach, outcome, and one takeaway
1. Leave a linkable proposal doc and a linkable blog draft for the next session

<!-- > -->

## [**5m**] Attendance &amp; Announcements

Last stretch covered tickets and write-ups teammates can start from. Today splits into two deliverables: a **VoIP product consult** (Zoom or Discord) and a **short eng blog draft** about a project you already built.

Both share the same move: name the pain, then show the fix. Friendster first — then the consult — then the blog.

<!-- > -->

## [**15m**] ☀️ Warm Up

Friendster was an early social network that lost to Facebook. Two angles on the same failure:

- [Founder Jonathan Abrams on Friendster](https://mashable.com/2014/02/03/jonathan-abrams-friendster-facebook/)
- [Wired: Friendster autopsy](https://www.wired.com/2013/02/friendster-autopsy/)

Skim both for about eight minutes (or split the team: half on Mashable, half on Wired). Then jot:

```text
One claim both pieces agree on:
One place they disagree (or one side is quieter):
One assumption Abrams could have checked earlier:
```

Share one line in chat or unmute. You’re hunting **checked assumptions**, not blame.

> **📈 PROTIP:** If load time is slow, read the Wired section headers and the Mashable founder quotes first — enough to fill the three lines above.

<!-- > -->

## [**30m**] 📚 TT: Assumptions, Consults, and Short Posts

**Next action:** Friendster signals → consult framing for Zoom/Discord → blog craft that sticks.  
**Done when:** You can name one unchecked assumption from Friendster and one pain you’d pitch Zoom or Discord to fix.

### 1. Failure Signals Worth Keeping (~8m)

Product failures rarely fail for one reason. Friendster’s story mixes scale, relationships between users, timing, and leadership calls. The useful move for today: **what would you have verified before betting the roadmap?**

Typical signals that show up across both pieces:

| Signal | Looks like | Check earlier |
| --- | --- | --- |
| Scale debt | Growth outruns infra | Load tests against real traffic shapes |
| Relationship gap | Users don’t return to each other | Retention loops, not just signups |
| Competitor timing | A rival ships the missing piece | Weekly competitor notes, not quarterly |
| Founder blind spot | Story says “we were right” | Outside user interviews |

> **💬 ASK AUDIENCE:** Was Friendster mostly mismanagement, or a product that never locked user-to-user relationships — or both?

<details>
<summary>Answer</summary>

**Both show up.** Wired leans hard on technical and competitive pressure; Abrams’ own telling surfaces choices about growth and focus. The teachable move is the third question: which **assumptions** (scale, retention, feature race) went unchecked until it was expensive.

</details>

### 2. Consult Mode — Zoom vs Discord (~10m)

You’re a small consulting team pitching product changes to a VoIP / realtime-comms company. Two leads walked in:

- [Zoom — about / mission](https://zoom.us/about)
- [Discord — company / mission](https://discord.com/company)

Read the mission pages for flavor. Then pick **one** company for Activity 1.

A strong consult does four things:

1. Names a **pain** real users feel this week
1. Proposes a **change** (feature, UX, or policy) that attacks that pain
1. Shows **why this company** (mission fit, not a random wishlist)
1. Leaves a **doc a reader can open** without you narrating it live

Questions that surface good engineering problems:

- What do you wish was easier in daily use?
- What utility or API would change your day the most?
- What could you automate so the team gets more done?
- What would make a teammate’s day more useful (or less painful)?

> **💬 QUICK CHECK:** Your teammate pitches “add dark mode” to Zoom with no user pain named. Pitch or wishlist?

<details>
<summary>Answer</summary>

**Wishlist until the pain is named.** Dark mode can be real — but the consult needs who hurts (night-shift support? accessibility?), what they do today, and why Zoom’s mission makes this the right next bet vs Discord’s community focus.

</details>

> **‼️ BE AWARE:** Copying a competitor’s entire feature list. The session wants *your* unique problem plus a fix Zoom or Discord could release.

### 3. Why Short Eng Posts Still Matter (~7m)

Blogs today usually do one of two jobs:

1. Teach a reader how you solved something (so they don’t repeat the pain)
1. Put heat behind the work — portfolio, team, product

Examples worth skimming later:

- [Dan Morse on Medium](https://danielmorse.medium.com) — introspective / how-to eng posts
- [InsideBigData: AI under the hood (Jay Lowe)](https://insidebigdata.com/2021/06/17/ai-under-the-hood-object-detection-model-capable-of-identifying-floating-plastic-beneath-the-surface-of-the-ocean/) — project story in a public venue

Same outline as last session’s write-up lab:

```text
Challenge → Approach → Outcome → One takeaway
```

Loose technical outline:

```text
Peak traffic melted the app
Compared backend options that handle spikes
Picked XXX; implemented YYY (snippet optional)
Learned to budget for load earlier
Hope readers size capacity before launch day
```

> **💬 ASK QUESTION:** A draft opens with “I learned React and Postgres.” Is that a challenge?

<details>
<summary>Answer</summary>

**No.** That’s a stack list. Challenge sounds like: “Support tickets piled up because nobody could see which queue was stale.” Stack belongs under approach.

</details>

> **💬 YOUR TURN:** One sentence — challenge for a project you already built (portfolio, course project, or side tool). No framework names yet.

<details>
<summary>Answer</summary>

Anything that names a person + a pain works. “Hiring managers bounced because the README never said what problem the app solved” is a challenge. “Built with Next.js” is not.

</details>

> **📈 PROTIP:** Open with the pain, not the framework. The stack is secondary. The challenge is the story.

<!-- > -->

## [**10m**] 🌴 Break

Stretch. Reopen Zoom/Discord mission tabs and your blank proposal doc. After break: Activity 1 consult, then Activity 2 blog draft.

<!-- > -->

## [**40m**] 💻 Activity 1: MakeVoiP Product Consult

> **✅ DONE WHEN:** Your team has a Google Doc (or similar) with a share link that covers pain points, feature / product change recommendations, UX improvements, and at least one extra idea — ready to present for feedback in #general.

1. Form a small team (3–4). One person creates a blank Google Doc and shares edit access.
1. Agree on **Zoom** or **Discord** after a quick skim of the mission page.
1. Brainstorm from the solve questions (wish easier / high-impact utility / automate / make the day better). Capture concrete pain users feel this week.
1. Write the proposal with these sections:

    ```text
    Company (Zoom | Discord) + one-line mission fit
    Pain points (3+) with who feels them
    Feature / product change recommendations
    UX improvements
    Other ideas
    Open questions for the exec room
    ```

1. Paste the **share link** where the session tracks deliverables (channel thread or assignment path your facilitator names; skip any third-party grade portal).
1. Be ready for a short all-team present: each team intros one recommendation; peers leave feedback in #general.

> **📈 SHORTCUT:** Pick Zoom *or* Discord in the first two minutes. Switching mid-hour burns the proposal.

> **‼️ WATCH OUT:** “Make it cooler” without a named user. Every recommendation needs a who + a pain.

> **FINISHED EARLY?** Stress-test the proposal: “What would a skeptical eng manager ask first?” Add that Q&A section.

<!-- > -->

## [**35m**] 💻 Activity 2: Blog Workshop Draft

> **✅ SHIP WHEN:** You have a linkable doc (Google Doc, draft blog post, or README section) with **100–300+ words** covering challenge, approach, outcome, and one takeaway.

Prompts (use one, both, or a mix):

1. Looking back at a portfolio project you had to improve — what do you wish you’d scoped differently on day one? How will the next project change because of that?
1. What motivation did you pick up from iterative improvement work, and how will you bake that into the next build?

Fill these points in some form:

- What challenge pushed you to build this? (Assignment is fine — dig for the deeper need if it’s there.)
- How did you pick the tech that might fix it?
- Did the challenge get solved — why or why not?
- What eng or life lesson stuck?
- What’s the **one** thing you want a reader to keep?

1. Open a blank doc or your production blog draft.
1. Write 100–300 words (more is fine). Paragraphs or a bullet outline that hits the five points above both work.
1. Drop the **share link** in the same deliverable thread as Activity 1.
1. Optional 90s teammate swap: trade links; name one strong section and one missing section.

> **‼️ PITFALL:** Writing only for people who were in the session. If the draft needs you live-narrating it, it isn’t done.

> **📈 DO THIS:** If the project feels detached from any purpose, write that feeling into the draft — then say how you’ll pick the next project differently. Honest beats polished empty.

<!-- > -->

## [**5m**] Wrap Up

- **Tonight:** Finish any thin sections on the proposal or the blog draft so both links open clean for a reader who was not in the session.
- **Next session:** Pitch / validate — you’ll reuse today’s writing muscle on users and YC-style framing.
- **Optional:** Form a tiny accountability pair for one short post a week — same outline every time.
- **Stuck?** Re-open the Friendster jot lines: unchecked assumption → pain → fix. That chain is the whole day.

<!-- > -->

## Additional Resources

1. [Mashable — Jonathan Abrams on Friendster](https://mashable.com/2014/02/03/jonathan-abrams-friendster-facebook/)
1. [Wired — Friendster autopsy](https://www.wired.com/2013/02/friendster-autopsy/)
1. [Zoom — About](https://zoom.us/about)
1. [Discord — Company](https://discord.com/company)
1. [Dan Morse — Medium posts](https://danielmorse.medium.com)
1. [InsideBigData — AI under the hood (object detection / marine plastic)](https://insidebigdata.com/2021/06/17/ai-under-the-hood-object-detection-model-capable-of-identifying-floating-plastic-beneath-the-surface-of-the-ocean/)
1. [Write the Docs — docs principles](https://www.writethedocs.org/guide/writing/docs-principles/)

<details>
<summary>For Curriculum Authors</summary>

## For Curriculum Authors

### In Class

| | |
| --- | --- |
| **Next action** | Open this file → Agenda → GOAL → Warm Up (Friendster skim). |
| **Done when** | Each team has a linkable MakeVoiP proposal; each person has a 100–300 word blog draft link. |

```text
Feeling (1 word):
Behind | On track | Ahead:
Today's MVP: Zoom/Discord proposal doc + short eng blog draft (both linkable)
```

### Facilitator Notes

- **Teach from** the local dated draft; ship path: `Lessons/05-MakeVoiP_and_Blog.md` (PR #4 open on `lesson/makevoip-blog-fall2026`).
- Continuity: prior Writing Lab four-section outline (challenge → approach → outcome → takeaway). Reuse that language; don’t invent a new narrative shape.
- Gradescope paths from the legacy source are **retired** — collect Google Doc / blog share links in-channel or via the live assignment surface in the repo.
- Friendster articles: if Mashable/Wired are slow, split the team half/half and pool answers.
- MakeVoiP present: keep to one recommendation per team + #general feedback form/thread. High visibility is the point; timebox presents.
- Blog examples (Dan Morse / InsideBigData) are optional skim — not required reading before Activity 2.
- Voice: on-the-job builder. No classroom / roster language in the learner body.
- Behind at ~0:45? Cut TT §3 deep examples → jump to Activity 1 after the consult pulses.

### Expert Follow-Ups

1. **Deliverable surface** — confirm where share links land (Slack thread vs in-repo path) once Gradescope is fully off.
2. **Staff post examples** — Dan Morse / InsideBigData may age; keep two live eng-post examples (one reflective, one project spotlight).
3. **Session 8 handoff** — Pitch / YC / Blog should reuse today’s proposal + draft links without restarting from blank.
4. **Ship filename** — canonical `05-MakeVoiP_and_Blog.md`; local draft keeps date+version in the filename only.

</details>
