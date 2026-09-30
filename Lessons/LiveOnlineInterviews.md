<!-- Run as a slideshow: reveal-md Lessons/LiveOnlineInterviews.md -w -->
# Live Online Interviews & Take-Homes

⭐️ **GOAL:** Leave with a short list of strategies for live online coding interviews and take-home projects, and one paired CoderPad-style drill done in both roles.

<!-- omit in toc -->
## ⏱ Agenda

- [[**15m**] ☀️ Warm Up](#15m-️-warm-up)
- [[**25m**] 💻 Activity 1: Compare Live Online and Whiteboard Interviews](#25m--activity-1-compare-live-online-and-whiteboard-interviews)
- [[**10m**] 📚 TT: Strategies for Live Online Interviews](#10m--tt-strategies-for-live-online-interviews)
- [[**45m**] 💻 Activity 2: CoderPad Drill in Pairs](#45m--activity-2-coderpad-drill-in-pairs)
- [[**10m**] 🌴 Break](#10m--break)
- [[**10m**] 💻 Activity 3: Plan for Take-Home Projects](#10m--activity-3-plan-for-take-home-projects)
- [[**5m**] Wrap Up](#5m-wrap-up)

<!-- > -->

<!-- omit in toc -->
## 🏆 Objectives

*By the end of this session, you'll be able to&hellip;*

1. Compare a live online coding interview with a whiteboard interview
1. Set up a shared coding pad and check how it runs code and shows errors before the clock starts
1. Solve an easy or medium problem out loud in a pad: restate, list edge cases, code, and test with a print or two
1. Plan a take-home project so the asked scope is done first and every line is one you can explain

<!-- > -->

## [**15m**] ☀️ Warm Up

One more behavioral rep before the technical work. Use STAR from last session (Situation, Task, Action, Result), plus the Fit you want the interviewer to hear.

> *Tell me about a time you were working on multiple projects. How did you prioritize?*

1. Solo (8m): write a five-line outline.

    ```text
    S:
    T:
    A: (2-3 things *I* did)
    R:
    Fit: Position | Culture | Mission
    ```

1. In pairs (7m): each person tells the story in about 90 seconds. The listener names only the Fit they heard. No other feedback this round.

You're done when you have one outline and you've said it out loud once.

📈 **PROTIP:** A prioritization story works when Action names the rule you used to pick: a deadline, how many users it touched, who was blocked waiting on you. "I was really busy and juggled it" doesn't tell anyone how you think.

<!-- > -->

## [**25m**] 💻 Activity 1: Compare Live Online and Whiteboard Interviews

> **✅ DONE WHEN:** You've answered all three prompts with a teammate and the room has a shared list of strategies to use in the next section.

1. Think (3m). Jot quick answers to these:

    ```text
    1. Live online interviews I've done (real or mock):
    2. Same as a whiteboard interview:
       Different from a whiteboard interview:
    3. One strategy I'd recommend for prep or during the call:
    ```

1. Pair (15m). Compare notes in a breakout room. Haven't done a live online interview yet? Answer #1 with the closest thing you have, like a mock or a timed coding challenge.
1. Share (7m). Back in the main room, two or three pairs share one difference and one strategy. Add yours to the shared note or Zoom whiteboard so the list is there for TT.

> **📈 TIP:** "Different" answers that name a specific thing (autocomplete is off, you can run the code, the interviewer sees every typo live) are easier to turn into a strategy than "it felt more stressful."

<!-- > -->

## [**10m**] 📚 TT: Strategies for Live Online Interviews

Most of these came up in the share-out, probably in different words. Here's the short version, grouped by when you'd use it.

### 1. Before the Call (~2m)

- Use an internet connection you trust. Plug in, or sit close to the router.
- Wear headphones. Laptop speakers feed back into the mic, and the interviewer ends up hearing their own voice.
- Explore the pad early. Once you have the link, change the theme if it's hard to read, run a line on purpose, and break one on purpose so you know what an error looks like in that tool.

### 2. In the Pad (~6m)

A whiteboard gives you a few square feet. A pad gives you unlimited space for notes, so use the same interview framework you've practiced (restate the question, name inputs and outputs, list edge cases) and write it down as comments.

- Ask clarifying questions, then write the answers into the code as comments.
- Ask whether prints or console logs are OK before you lean on them.
- Change input values live to show how the code behaves.

Here's what the top of a pad looks like for "given an array `a` and a target `t`, find two numbers that sum to `t`" from the problem bank:

```python
# Input: list of ints `a`, target int `t`
# Output: a pair (x, y) where x + y == t, or None
# Asked: can a number pair with itself? -> No, must be two different positions
# Asked: are prints OK? -> Yes
# First edge case to test: empty list -> None

def two_sum(a, t):
    seen = set()
    for x in a:
        if t - x in seen:
            return (t - x, x)
        seen.add(x)
    return None

print(two_sum([2, 7, 11, 15], 9))  # (2, 7)
print(two_sum([], 9))              # None
```

📈 **DO THIS:** Before any code, leave a comment at the top with inputs, outputs, and the edge case you'll test first. If you freeze halfway through, you and the interviewer can both read where you were headed.

> **💬 QUICK CHECK:** You want a third `print` that proves the "can't pair with itself" answer. What input would you use, and what should it print?

<details>
<summary>Answer</summary>

Something like `two_sum([3], 6)`. It should print `None`, because the only 3 can't be used twice. The code checks `seen` *before* adding `x`, which is what makes that work. Showing it with a print is stronger than saying it.

</details>

### 3. Off the Pad (~2m)

- Keep paper nearby for diagrams. If a drawing would help, offer to hold it up to the camera.
- Ask whether looking up reference docs is OK. It can help online, but some interviewers count it against you, so ask first.

Honestly, we're not covering every pad tool's keyboard shortcuts today. Ten minutes poking around the pad before the call covers most of it.

> **💬 ASK AUDIENCE:** Look at the full list above. Which one do people skip when they're nervous?

<details>
<summary>Answer</summary>

Usually the clarifying questions and the edge-case comments. Under stress, most people start typing right away. Writing two or three comment lines first is slower by a minute and usually saves more than that later.

</details>

<!-- > -->

## [**45m**] 💻 Activity 2: CoderPad Drill in Pairs

> **✅ DONE WHEN:** Each person has been the candidate once and the interviewer once, on two different prompts, and each candidate has run their code with at least one test.

1. Set up one shared pad (about 3m): a [CoderPad](https://coderpad.io/) sandbox, a [Replit](https://replit.com/), or [VS Code Live Share](https://learn.microsoft.com/en-us/visualstudio/liveshare/). Use whichever one opens first for both of you. Fighting local setup eats the round.
1. Pick who goes first as candidate. The interviewer opens the [Mock Technical Interview Problems](https://docs.google.com/document/d/1Zq8wQ35Y5ynM4JLRxsLmoDESkD1Yr2MVj0zkaeKedkQ/edit) doc, chooses an Easy or Medium prompt, and pastes it into the pad. Good starting picks from the Computer Science section:
    - Easy: given an array `a` and a target `t`, find two numbers that sum to `t`
    - Medium: given a paragraph of text, find the most common word (`"A cat in a hat is a feline wearing a fedora"` => `"a"`)
    - Doc won't open? Use City Rain from the [Technical Interview Question Bank](https://docs.google.com/document/d/1RtuWkZhRBJr_tAOEBnSErC4Kr7E0eSJ8bfq4UYSuncE/edit): an array of building heights, return how much rainwater pools between them (`[4, 2, 3, 4]` => `3`, `[3, 5, 2, 3]` => `1`). Or paste a LeetCode Easy such as [Two Sum](https://leetcode.com/problems/two-sum/) or [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/).
1. Run round 1 (about 20m):

    | Role | Job |
    | --- | --- |
    | Interviewer | Paste the prompt, answer clarifying questions, give a nudge if the candidate is stuck for a while, and call time |
    | Candidate | Restate the prompt, write examples and edge cases as comments, talk through the plan, code out loud, then test with a print or two |

1. In the last two minutes of the round, the interviewer fills this card and reads it back:

    ```text
    Clarifying question they asked:
    Edge case they tested:
    Where the narration dropped off:
    ```

1. Switch roles and run round 2 (about 20m) with a **different** prompt.
1. On your own? Pick one Easy prompt, set a 25-minute timer, and talk out loud anyway. When time's up, paste your final function and one test case into Zoom chat.

> **‼️ BE AWARE:** Twenty or thirty seconds of quiet thinking is fine. Typing a wall of code without saying what it's for is the part that hurts. Say the plan in one sentence, then type.
> **FINISHED EARLY?** Take a follow-up from the doc on the prompt you just solved: solve it another way, give the time complexity, or handle the edge case the interviewer asked about.

<!-- > -->

## [**10m**] 🌴 Break

<!-- > -->

## [**10m**] 💻 Activity 3: Plan for Take-Home Projects

> **✅ COMPLETE WHEN:** You've shared one take-home experience or plan with a teammate and picked the strategy from the list below you'll use first on this week's homework.

1. With a teammate (5m): share any take-home project you've done. No take-home yet? Talk through how you'd split a three-hour budget on the homework below. What helped you prepare, and what would you do differently?
1. Read through these strategies (5m) and mark the one you'll use first:
    - Match the company's linter or style guide if they share one.
    - Finish the asked scope first. Then add extras such as tests and polish.
    - Pace yourself. Start early instead of the night before.
    - Ask clarifying questions when you're stuck, within whatever rules the company gave you.
    - Be ready to walk through every line you submit. A follow-up call often asks you to.
    - Have a quiet place and working internet ready for that follow-up call.
    - Finishing fast and correct can help. Fast and sloppy doesn't.

> **‼️ WATCH OUT:** Code you copied and can't explain is a risk on the follow-up call. If a snippet came from docs or an example, make sure you can say why it's there.

<!-- > -->

## [**5m**] Wrap Up

Paste in Zoom chat:

```text
Live online tip I'll actually use:
Take-home tip I'll actually use:
Problem I still want reps on:
```

Before next session:

1. Finish any drill prompt you didn't get through today, on your own, with a timer.
1. Complete the [Take Home Project Assignment](https://docs.google.com/document/d/1bdFJksH9QuOjxk51aJOi6mxsvPY5AXkwNOMIcjgU6NM/edit). Pick the track that matches your concentration (Mobile, Front End, Back End, or Data Science). Aim for under three hours and write down how long it actually took.
1. Send your finished homework to your instructor in a Slack DM. That's the only submission step, whatever the doc's Requirements list says.
1. Next session is a technical interview challenges lab, so the pad setup from today carries straight over.

📈 **PROTIP:** Put the time you spent at the top of your README. Many companies ask for it, and a real number with a note like "skipped styling to finish tests" shows how you made tradeoffs.

<!-- > -->

## Additional Resources

1. **[Mock Technical Interview Problems](https://docs.google.com/document/d/1Zq8wQ35Y5ynM4JLRxsLmoDESkD1Yr2MVj0zkaeKedkQ/edit)**: Easy, Medium, and Hard problems for Frontend, Backend, Computer Science, and Mobile.
1. **[Technical Interview Question Bank](https://docs.google.com/document/d/1RtuWkZhRBJr_tAOEBnSErC4Kr7E0eSJ8bfq4UYSuncE/edit)**: City Rain, mobile questions, and a list of practice sites.
1. **[Take Home Project Assignment](https://docs.google.com/document/d/1bdFJksH9QuOjxk51aJOi6mxsvPY5AXkwNOMIcjgU6NM/edit)**: this week's homework prompt for each track.
1. **[Live "Coderpad" Interviews & Take Home Projects (slides)](https://docs.google.com/presentation/d/1WTwYSz6z5PHdS3_AAlu9UbWFmEd5VwqaCtTLMUoTqOw/edit)**: the session deck. If it asks you to request access, everything you need for today is on this page.
1. **[CoderPad](https://coderpad.io/)**: the pad many companies use for live coding rounds.
1. **[VS Code Live Share](https://learn.microsoft.com/en-us/visualstudio/liveshare/)**: edit the same file together from your own editors.
1. **[Tech Interview Handbook: Coding Interview Cheatsheet](https://www.techinterviewhandbook.org/coding-interview-cheatsheet/)**: what to do before, during, and after a coding round.
1. **[OpenWeatherMap API](https://openweathermap.org/api)**: the API behind the Mobile, Front End, and Back End homework tracks.
