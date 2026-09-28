<!-- Run as a slideshow: reveal-md Lessons/BehavioralInterviewing.md -w -->
# Behavioral Interviewing (STAR)

⭐️ **GOAL:** Leave with three STAR outlines drafted and one answer delivered out loud that signals Position, Culture, or Mission Fit.

<!-- omit in toc -->
## ⏱ Agenda

- [[**10m**] ☀️ Warm Up](#10m-️-warm-up)
- [[**30m**] 📚 TT: Framing Behavioral Interviews](#30m--tt-framing-behavioral-interviews)
- [[**20m**] 💻 Activity 1: Draft Three STAR Outlines](#20m--activity-1-draft-three-star-outlines)
- [[**10m**] 🌴 Break](#10m--break)
- [[**30m**] 💻 Activity 2: Deliver One Answer Out Loud](#30m--activity-2-deliver-one-answer-out-loud)
- [[**15m**] 💻 Activity 3: Rewrite One Answer for Value and Risk](#15m--activity-3-rewrite-one-answer-for-value-and-risk)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Explain why interviewers ask behavioral questions and what they listen for
1. Outline an answer using STAR (Situation, Task, Action, Result) with Action as the longest section
1. Name which Fit your story signals: Position, Culture, or Mission
1. Revise an answer from feedback to raise perceived value and lower perceived risk

<!-- > -->

## [**10m**] ☀️ Warm Up

Quick progress check before new material. Think about your job search and interview prep since last session: portfolio fixes, applications sent, a coding challenge you tried, a README you cleaned up.

Paste this into Zoom chat:

```text
Built:
Verified:
Blocked by:
Next (this week):
```

Then read prompt #8 from the [common behavioral interview questions](https://github.com/Tech-at-DU/ACS-2951-Engineering-Careers/blob/master/Assignments/common-bi-questions.md) and jot your first instinct in one line. Keep it private for now. You'll come back to it.

> *Describe a time you had to do something you didn't expect or that was outside of your job role. How did it go?*

📈 **PROTIP:** "Blocked by" gets more useful when it names a thing (a failing test, a missing API key, a teammate reply you're waiting on). "Busy" isn't a blocker anyone can help with.

<!-- > -->

## [**30m**] 📚 TT: Framing Behavioral Interviews

### 1. Information Asymmetry (~6m)

Here is an answer interviewers hear every week:

```text
Q: Tell me about yourself as a teammate.
A: I'm a hard worker and a team player. I always give 110%.
```

The core problem in any interview is information asymmetry. You know a lot about yourself; the employer doesn't. The employer knows a lot about the company; you don't. An interview is both sides trying to close that gap.

A behavioral question is how the interviewer closes that gap on their side. They ask for a past situation because past behavior is the best evidence they can get in 45 minutes. Your answer is a *signal*: a short, efficient way to show something they can't check directly.

> **💬 ASK AUDIENCE:** What did "hard worker, team player, 110%" prove to the interviewer?

<details>
<summary>Answer</summary>

Nothing they can check. Every candidate says it, so it carries no information. A signal needs a specific story: a time, a problem, what you did, and what changed.

</details>

### 2. What the Interviewer Is Listening For (~8m)

The employer's frame is "hire the best people," and in practice "best" usually means best **Fit**. They gather evidence two ways:

- **Answers:** what you say
- **Observables:** what you do (on time, camera framing, how you handle a question you don't know, whether you ask them anything)

Fit has three parts:

| Fit | What it means | Sounds like in a story |
| --- | --- | --- |
| Position | You can do the work this role needs | "I traced the failure to a version bump and pinned it" |
| Culture | You work well with the people there | "I wrote up the fix so the next person didn't hit it" |
| Mission | You want this job and care about what the team is building | "Our users were blocked, and that bothered me" |

One story can touch all three. Pick **one** to lead with so the interviewer walks away with a clear signal.

‼️ **BE AWARE:** Interviewers are not allowed to ask about protected categories such as race, age, religion, disability, pregnancy, gender, sexual orientation, or medical history. If a question drifts there, you can redirect to the role: "I'd like to focus on how I'd handle this job. Here's a relevant example." We skip the deep-dive on this today; the EEOC link is in Additional Resources.

> **💬 ASK AUDIENCE:** Which Fit do you usually forget to signal: Position, Culture, or Mission?

<details>
<summary>Answer</summary>

Most engineers over-index on Position (skills, stack, debugging) and skip Culture (how you worked with people) or Mission (why the work mattered to you). Watch for that in Activity 2.

</details>

### 3. STAR, Worked Example (~10m)

STAR is the outline:

| Section | Job | Length |
| --- | --- | --- |
| **S**ituation | Where and when; just enough context | One or two sentences |
| **T**ask | What you were responsible for, or what fell to you | One sentence |
| **A**ction | What *you* did, step by step | The longest section |
| **R**esult | What changed, with evidence | One or two sentences, plus what you'd do next time |

Rough answer to prompt #8:

```text
Yeah so on our final project the deploy wasn't working and nobody
really knew why. We all kind of jumped in and figured it out and it
worked out fine in the end. I think it shows I'm a team player.
```

Same story, outlined with STAR:

```text
S: Two days before our final demo, our deploy started failing. Four
   of us on the team, and nobody owned the build pipeline.
T: I was on frontend. The deploy wasn't my job, but no deploy meant
   no demo URL.
A: I read the last ten build logs and found the failures started
   right after a Node version bump. I pinned the version in the build
   config and tested the deploy on a branch before merging. Then I
   posted a short note in our team channel: what broke, the fix, and
   how to check it next time.
R: The deploy passed that evening and we demoed on time. The note
   became the Troubleshooting section of our README. On my next
   project I set up a build check on day one.
Fit: Position (debugging a system I didn't own)
```

Spoken, that's about 90 seconds.

📈 **PROTIP:** Result is where most answers fade out. End on something checkable (a date, a number, a file that still exists, a habit you changed) instead of "it went well."

> **💬 ASK AUDIENCE:** Look at the rough version again. Which STAR sections are missing or too thin to count?

<details>
<summary>Answer</summary>

Task is missing (whose job was it?). Action is all "we" with no steps. Result is "worked out fine" with no evidence. The Situation is there but vague. The last line claims a trait instead of showing it.

</details>

### 4. Raise Value, Lower Risk (~6m)

The candidate's frame mirrors the employer's. You're trying to:

1. Put your best foot forward
1. Maximize perceived value (what you'd add)
1. Minimize perceived risk (what might go wrong if they hire you)
1. Show Fit

Read each line of your answer and ask whether it raises value or lowers risk. If it does neither, it's just taking up time. Cut it.

‼️ **BE AWARE:** Blaming a teammate raises risk even when the story is true. "A teammate broke the build" makes the interviewer wonder how you'd talk about them. "The failures started after a Node version bump" names the cause without naming a person.

> **💬 ASK AUDIENCE:** Two Result lines for the same story. Which one lowers perceived risk, A or B?
>
> - A: "It went great and everyone was really happy with how it turned out."
> - B: "The deploy passed that night, we demoed on time, and the fix is still documented in our README."

<details>
<summary>Answer</summary>

**B.** The interviewer can check it: it says when it happened and where the fix lives now. A asks them to take a feeling on faith.

</details>

<!-- > -->

## [**20m**] 💻 Activity 1: Draft Three STAR Outlines

> **✅ DONE WHEN:** You have three outlines, each with first-person Action bullets and a named Fit signal.

1. Open the [common behavioral interview questions](https://github.com/Tech-at-DU/ACS-2951-Engineering-Careers/blob/master/Assignments/common-bi-questions.md). Pick **three** prompts that ask about a specific time or situation. Prompts #2, #3, and #6 through #13 work well for STAR. If you pick #14, answer it as: *Tell me about your education. Why did you choose your program?*
1. Solo, fill one card per prompt (about 4 minutes each):

    ```text
    Prompt #:
    S:
    T:
    A: (2-3 bullets of what *I* did)
    R: (outcome + one piece of evidence)
    Fit signal: Position | Culture | Mission
    ```

1. Post just your three prompt numbers in Zoom chat. If you see heavy overlap with others, consider swapping one so you practice a prompt fewer people picked.

> **📈 PROTIP:** Pull stories from the last 12 months: MakeVoiP, ticket writing, the writing lab, portfolio work, a job or volunteer role. Recent stories come with details you still remember.
> **‼️ BE AWARE:** "We" stories bury your Action. Rewrite every Action bullet so it starts with "I."

<!-- > -->

## [**10m**] 🌴 Break

<!-- > -->

## [**30m**] 💻 Activity 2: Deliver One Answer Out Loud

> **✅ DONE WHEN:** You have delivered one full answer out loud and have a filled feedback card, from a teammate or from your own playback.

1. Listen to a live model answer to prompt #8 (5m). While you listen, write down the one Fit signal you hear. Working without a live session? Read the STAR example from TT §3 out loud instead and note its Fit.
1. In breakout rooms of two (20m, 10m per person):
    - Speaker: deliver one answer from Activity 1, aiming for under two minutes.
    - Listener: fill this card while they talk, then read it back:

    ```text
    Prompt #:
    Fit signal I heard:
    Strongest Action detail:
    One vague or risky line to cut:
    ```

1. Swap roles and repeat.
1. Back in the main room (5m): a couple of volunteers deliver their answer. Feedback from the room sticks to the card: Fit heard and strongest Action detail. Working on your own? Skip this step and start Activity 3.
1. No teammate free? Record a 90-second voice memo, play it back, and fill the same card for yourself.

> **FINISHED EARLY?** Deliver a second outline, and have your teammate guess the Fit before you name it. If they guess wrong, that's useful data for Activity 3.

<!-- > -->

## [**15m**] 💻 Activity 3: Rewrite One Answer for Value and Risk

> **✅ DONE WHEN:** One answer is written in full prose, runs under two minutes out loud, has Action as its longest section, and has one line you changed because of feedback.

1. Open the feedback card from Activity 2 and the outline you delivered.
1. Delete or rewrite the line flagged as vague or risky.
1. Expand Action to two or three concrete moves in first person.
1. Add one piece of evidence to Result.
1. Read it out loud with a timer running. Over two minutes? Trim Situation first.
1. Add this note under the answer:

    ```text
    Changed because of feedback:
    Still unsure about:
    ```

> **📈 PROTIP:** Two minutes spoken is roughly 250 to 300 words. If your draft runs longer, Situation and Task are usually carrying extra weight.
> **FINISHED EARLY?** Take a second outline and rewrite it to lead with a different Fit than the first one.

<!-- > -->

## [**5m**] Wrap Up

Paste in Zoom chat:

```text
STAR story title (3-5 words):
Fit I signaled:
Prompt # I still can't answer:
```

Before next session:

1. Write all three STAR answers in full prose in a doc you can link.
1. Rehearse one out loud at least once.
1. Next session covers live online interviews and take-home projects. Skim the [Live Coderpad Interviews and Take-Home Projects deck](https://docs.google.com/presentation/d/1WTwYSz6z5PHdS3_AAlu9UbWFmEd5VwqaCtTLMUoTqOw/edit) if you have time.

Missed today, or only got one outline done? Start with one Activity 1 card. One outline is enough to rejoin next session.

‼️ **BE AWARE:** Memorizing an answer word for word makes it sound like a script, and one interruption can throw you off. Memorize the outline, then tell it fresh each time.

<!-- > -->

## Additional Resources

1. **[Framing Behavioral Interviewing (slides)](https://docs.google.com/presentation/d/1vZrYeFYLg4OBFOtQRBs1lFt62fx53qhp-Ju5YNgwQFA/edit)**: signaling, the three kinds of Fit, and the candidate frame.
1. **[Common Behavioral Interview Questions](https://github.com/Tech-at-DU/ACS-2951-Engineering-Careers/blob/master/Assignments/common-bi-questions.md)**: the prompt list for today and practice afterward.
1. **[MIT CAPD: The STAR Method for Behavioral Interviews](https://capd.mit.edu/resources/the-star-method-for-behavioral-interviews/)**: a short walkthrough of each STAR section.
1. **[The Muse: STAR Interview Method](https://www.themuse.com/advice/star-interview-method)**: more example answers across different prompts.
1. **[Tech Interview Handbook: Behavioral Interviews](https://www.techinterviewhandbook.org/behavioral-interview/)**: how software companies run behavioral rounds.
1. **[Tech Interview Handbook: Behavioral Interview Questions](https://www.techinterviewhandbook.org/behavioral-interview-questions/)**: a longer prompt bank grouped by theme.
1. **[Amazon Leadership Principles](https://www.amazon.jobs/content/en/our-workplace/leadership-principles)**: an example of a company publishing exactly what its behavioral rounds look for.
1. **[EEOC: Prohibited Employment Policies/Practices](https://www.eeoc.gov/prohibited-employment-policiespractices)**: what US employers can't base hiring decisions on.

<details>
<summary>For Curriculum Authors</summary>

## For Curriculum Authors

### In Class

MVP (15 minutes or less): one STAR outline with first-person Action and a named Fit signal.

| Elapsed | Time (ET) | Section |
| --- | --- | --- |
| 0-10m | 1:00-1:10 | Warm Up: progress check-in in chat, first read of prompt #8 |
| 10-40m | 1:10-1:40 | TT: Framing Behavioral Interviews (deck + worked example) |
| 40-60m | 1:40-2:00 | Activity 1: three STAR outlines |
| 60-70m | 2:00-2:10 | Break |
| 70-100m | 2:10-2:40 | Activity 2: model answer, pairs, main-room delivery |
| 100-115m | 2:40-2:55 | Activity 3: rewrite one answer |
| 115-120m | 2:55-3:00 | Wrap Up + next-session preview |

- Before session: open Zoom, the Framing Behavioral Interviewing deck, and the question list. Paste the question list into chat so the room can pick without switching tabs.
- Behind at ~1:40? Drop TT §4 to its pulse only and fold the blame BE AWARE into Activity 3.
- Behind at ~2:40? Cut main-room delivery in Activity 2 and give Activity 3 the full 15 minutes.

### Facilitator Notes

- Model answer in Activity 2: use the deploy story from TT §3 or a real story of your own for prompt #8. Keep it around 90 seconds so the room hears the target length.
- The deck's original timing (5-minute switch, 25-minute interview-story groups, 15-minute answer analysis) is compressed here. Pull slides for signaling, Fit, and the candidate frame; skip the group interview-story round unless the room is ahead.
- Main-room delivery stays volunteer-only. Keep feedback on the card fields (Fit heard, strongest Action detail) so it stays about the answer.
- Anyone still catching up on the earlier STAR homework can treat Activity 1 as that catch-up.
- Prompts #1, #4, and #5 aren't story-shaped. They're fine for warm practice later; steer Activity 1 picks toward the STAR-friendly range. Prompt #14 works as STAR when asked as "Tell me about your education. Why did you choose your program?" (the lesson body uses that wording).

### Expert Follow-Ups

1. **Deck access:** the Framing Behavioral Interviewing deck and the Coderpad / take-home deck sit in a faculty shared drive. Anonymous requests redirect to Google sign-in, so learners outside that drive will likely see a request-access page. Set link sharing to "anyone with the link can view," or export a PDF into the repo.
1. **Schedule + sidebar:** Session 9 in the README schedule links only the question list. Add this lesson to the schedule row and `_sidebar.md` once it's published.

</details>
