# Agentic Self-Management Skills

Four installable skills that turn ordinary conversation into one useful self-management decision or durable artifact.

The shared point of view: you should not need another tracker or productivity menu. Give the agent the context you already have and get back something you can act on.

## Choose the moment

| If you are thinking… | Use | What comes back |
|---|---|---|
| “What did today's ordinary choices vote for?” | [`identity-vote-translator`](#identity-vote-translator) | A lightweight behavior read and one next vote. |
| “Given my sleep, meetings, food, and workload, what is safe now?” | [`energy-decision-support`](#energy-decision-support) | One capacity-based decision and a bounded fallback. |
| “What should I protect, try, and avoid next week?” | [`weekly-trajectory-review`](#weekly-trajectory-review) | One week signal and exactly three decisions. |
| “How do I preserve why this project or period mattered?” | [`living-archive-entry-builder`](#living-archive-entry-builder) | A future-self archive entry returned inline. |

## Identity Vote Translator

**Use it when:** one ordinary conversation or end-of-day recap contains useful behavior signals, but a formal identity review would be too heavy.

**Returns:** two to four distinct behavior votes, one overall read, and one high-ROI next vote—without turning a single day into a personality diagnosis.

### Actual user case

> I turned a vague idea into a small demo, asked a teammate for feedback before it was polished, delayed a five-minute expense form for the third day, and called my sister instead of continuing to work. I want to become someone who ships, stays connected, and handles small obligations before they become noise. What pattern am I reinforcing?

### What the skill returns

> **Read:** You're reinforcing someone who turns ideas into artifacts, invites feedback early, and protects relationships—but also casts an avoidance vote when small, dull obligations lack urgency.
>
> **High-ROI next vote:** Submit the expense form before starting tomorrow's work.
>
> **Votes:**
>
> - Vague idea → small demo: someone who ships.
> - Asked for early feedback: someone who builds openly instead of hiding behind polish.
> - Called your sister: someone who stays connected and recognizes that stopping work can be aligned.
> - Delayed the expense form again: someone who trades five minutes of action for days of background noise.
>
> **Tension:** Your aspirational identity is already visible in the meaningful choices. The weak point is mundane closure—not motivation or ambition.

### Try it

```text
Use $identity-vote-translator to turn this end-of-day recap into one identity read and one next vote.
```

### Install

```bash
npx skills add myfeng10/agentic-self-management-skills --skill identity-vote-translator
```

Use the standalone [`identity-votes`](https://github.com/myfeng10/identity-votes) skill when you want an explicit multi-day trajectory review.

## Energy Decision Support

**Use it when:** you need one capacity-based decision from ordinary signals such as sleep, meetings, food, movement, timing, and accumulated work.

**Returns:** one safe next action, a risk point, and one bounded fallback.

### Actual user case

> I slept 6 hours. I wrote from 8 to 10, ran errands until noon, had a high-stakes interview from 1 to 2, and handled admin from 2:30 to 4. I ate, drank water, and took a 20-minute walk. It is 4:30 and I am considering a two-hour strategy session. What should I do next?

### What the skill returns

> **Decision:** Defer the two-hour strategy session and end demanding work for today.
>
> - **Current capacity:** LOW
> - **Generative budget remaining:** 0–0.5 hours
> - **Safe mode:** RECOVERY
> - **Risk point:** Starting open-ended strategy work at 4:30 after an interview and multiple context switches
>
> **Primary action:** Take the next hour fully off—no planning, admin, or consequential decisions.
>
> **Fallback:** If you must continue, spend 20 minutes capturing strategy questions and facts only, then schedule the actual session after a full night's sleep.
>
> **Why:**
>
> - Six hours of sleep reduced today's starting capacity.
> - Writing and a high-stakes interview both consumed generative and socially evaluative energy.
> - Errands and admin added sustained effort and several context switches.
> - Food, water, and walking helped stabilize you, but they did not restore enough capacity for two hours of sound strategy work.
>
> **Confidence:** HIGH—caffeine is unknown, but it would not materially change the recommendation.

### Try it

```text
Use $energy-decision-support to choose one safe next action from my sleep, timeline, recovery, and current decision.
```

### Install

```bash
npx skills add myfeng10/agentic-self-management-skills --skill energy-decision-support
```

This is the general-capacity skill. Use standalone [`next-mode`](https://github.com/myfeng10/next-mode) when the hard-to-see cost came specifically from supervising AI, judging outputs, debugging tools, and holding project context.

## Weekly Trajectory Review

**Use it when:** a week contains mixed sleep, work, meetings, relationships, and unfinished commitments—and you need three decisions, not a diary summary.

**Returns:** one week signal, the energy and identity patterns underneath it, and exactly one Protect, Try, and Avoid decision.

### Actual user case

> Mon/Tue: 7.5h sleep, protected morning build blocks, shipped core feature. Wed: three meetings, no deep work, evening crash. Thu: 6h sleep, tried to recover with admin but kept context-switching. Fri: worked from a cafe with a friend, finished a hard bug and felt steady. I promised five major deliverables and completed two. Give me a decisive next-week plan.

### What the skill returns

> **Week signal**
>
> Your capacity was strong when sleep, protected mornings, and a steady environment aligned. The problem wasn't effort; it was planning for five major deliverables when the week realistically supported two, then using fragmented admin as recovery after overload.
>
> **Energy pattern**
>
> - Best capacity window: Protected morning build blocks after 7.5 hours of sleep.
> - Main depletion source: Meeting-heavy days followed by insufficient sleep.
> - Recovery that worked: A lunch walk restored steadiness.
>
> **Identity movement**
>
> - Rising: Builder.
> - Falling: Executor, because commitments exceeded capacity.
> - Mixed: Connector—meetings depleted you, while working beside a friend helped you persist through a hard bug.
>
> **Self-management lesson**
>
> Plan from demonstrated capacity, not aspirational capacity: two major deliverables completed under protected conditions is the reliable baseline.
>
> **Next week plan**
>
> - **Protect:** Reserve Monday and Tuesday mornings for uninterrupted work on the week's top deliverable.
> - **Try:** Commit to only two major deliverables for the entire week.
> - **Avoid:** Do not use fragmented admin work as recovery.
> - **One calibration question:** By Friday, did limiting the week to two major deliverables increase completion without causing an evening crash?

### Try it

```text
Use $weekly-trajectory-review on these logs. Give me one week signal and exactly one Protect, Try, and Avoid decision.
```

### Install

```bash
npx skills add myfeng10/agentic-self-management-skills --skill weekly-trajectory-review
```

## Living Archive Entry Builder

**Use it when:** a project, realization, or period mattered and you want future you to recover what happened, what changed, and why it was worth remembering.

**Returns:** a complete archive entry inline. It only writes or edits a file when you explicitly ask.

### Actual user case

> In July 2026 I built a tiny context-health overlay after repeatedly losing the thread in long AI coding sessions. At first I blamed model quality; the real problem was that neither the agent nor I could see the stale context accumulating. It changed how I think about AI UX: systems should expose when their own state becomes unreliable. Future me should remember that the useful product came from noticing my own confusion instead of hiding it.

### What the skill returns

> **Title:** When Context Became Visible
>
> **Time period:** July 2026
>
> **Thread:** Making hidden system state legible
>
> **Pull:** I kept losing the thread during long AI coding sessions. I initially blamed model quality, but the deeper problem was shared blindness: neither the agent nor I could see how much stale context had accumulated.
>
> **Blocks:**
>
> I built a tiny context-health overlay that made repeated reads and context saturation visible. When the session became unreliable, it offered a clean-start handoff instead of asking us to keep pushing through degraded context.
>
> - Repeated reads became a signal rather than background noise.
> - Saturation became something I could notice before the session unraveled.
> - Starting fresh became a continuation strategy, not a failure.
>
> The project changed how I think about AI UX. Systems should expose when their own state is becoming unreliable. The most useful part of the product came from treating my confusion as evidence instead of hiding it.
>
> **Future-self note:** When I repeatedly lose the thread, do not assume I need a better model or more discipline. Look for the invisible condition shaping the interaction. Confusion can be an instrument.

### Try it

```text
Use $living-archive-entry-builder to turn this project story into a draft future-self archive entry. Return it inline.
```

### Install

```bash
npx skills add myfeng10/agentic-self-management-skills --skill living-archive-entry-builder
```

## Install All

```bash
npx skills add myfeng10/agentic-self-management-skills --all
```

Restart the agent after installing so the new skills are picked up.
