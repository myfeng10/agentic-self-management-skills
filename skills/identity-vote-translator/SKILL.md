---
name: identity-vote-translator
description: Use when a user talks about their day, habits, routines, choices, goals, procrastination, conflict, work, recovery, or repeated behavior. Track identity votes during the conversation and, at a natural endpoint, show what identity they are reinforcing and the highest-ROI next vote.
---

# Identity Vote Translator

Use this skill while the user is talking, not only after they request a formal review.

Core principle: behavior disappears, identity accumulates. Every repeated action is a vote for a kind of person.

## Core Advantage

The agent can notice identity votes during normal conversation, maintain a lightweight vote ledger, and present the pattern at the end. The user does not need to open a tracker, fill out a form, or remember to ask for analysis.

High ROI: catch the pattern while the user is already explaining their life, then convert it into one next action.

## Who This Is For

Use this for people who want behavior-level self-awareness without vague personality analysis. Especially useful for users with ADHD or scattered attention: they can talk naturally, and the agent extracts the identity signal.

The skill should be usable by any person. Do not assume Michelle's private ontology unless the user provides it.

## Trigger Phrases

- "What identity am I reinforcing?"
- "What am I becoming?"
- "Analyze my routine."
- "Turn this day into identity votes."
- "What pattern does my week show?"
- "Am I becoming the person I want to be?"

## Implicit Triggers

Also use this skill when the user casually describes:

- a repeated routine or habit loop
- avoidance, procrastination, or drifting
- conflict, confrontation, or emotional escalation
- a good day or bad day with concrete behaviors
- a desired future self
- a mismatch between stated goals and actual actions
- a sequence of choices across work, relationships, body care, learning, or rest

Do not interrupt every time. Track the votes quietly and surface them when the conversation reaches a decision point, recap, end-of-day moment, weekly review, or "what should I do?" moment.

## Inputs

Accept any of:

- Daily routine logs
- Calendar summaries
- Journal reflections
- Weekly activity summaries
- Messy notes about habits, relationships, work, learning, recovery, or consumption

Do not require rigid formatting. If duration is available, use it. If duration is missing, weigh by intentionality, effort, emotional salience, and repetition.

## Vote Ledger

During conversation, maintain a temporary ledger:

```text
Behavior observed:
Identity vote:
Direction: reinforces | weakens | redirects
Strength: low | medium | high
Evidence:
Next vote candidate:
```

Only present the ledger if useful. Usually summarize the top 2-4 votes instead of showing everything.

## Identity Lens

Prefer grounded identity types over generic traits. Examples:

- someone who builds original systems from internal curiosity
- someone who protects capacity through physical stabilization
- someone who expands through low-pressure social contact
- someone who converts reflection into visible artifacts

Avoid praise. Avoid productivity scores. Avoid inventing a flattering identity when the evidence is mixed.

## Danger Identities

Name danger identities when evidence supports them, but do not shame the user.

- Avoider: someone who protects short-term comfort by delaying, blurring, or escaping the next clear action.
- Confronter: someone who seeks intensity, argument, or forceful collision when calibration, timing, or softer repair would work better.

These are not labels for the person. They are trajectories being reinforced by repeated behaviors.

When a danger identity appears, give one concrete "next vote" that redirects it. Keep the tone direct: identify the pattern, name the cost, and prescribe the smallest corrective action.

## ADHD-Friendly Delivery

- Put the strongest read in the first line.
- Use short labels and concrete verbs.
- Avoid long trait explanations.
- Give one high-ROI next vote, not five options.
- If the user is overwhelmed, skip the full analysis and give only: pattern, risk, next vote.

## Analysis Method

For each strong pattern:

1. Identify the behavior evidence.
2. Name the identity being reinforced.
3. Explain the trajectory if repeated for 6 months to 5 years.
4. Mark whether this identity aligns with the user's stated future self.
5. Suggest one small shift that changes the next vote.

If the user has named desired or danger identities, use those terms first. If not, infer identities from evidence.

## Output

Return:

```text
Read: one sentence naming the strongest identity signal.
High-ROI next vote: the one action most likely to shift the trajectory.

Identity votes
- Identity: someone who ...
  Weight: 0.00-1.00
  Evidence: concrete behaviors from the input
  Trajectory: where this converges if repeated
  Alignment: aligned | mixed | misaligned
  Next vote: one practical behavior to reinforce or redirect

Main tension: the strongest conflict between identities
Risk to watch: Avoider | Confronter | other, if present
```

If the input covers more than one week, include trajectory movement: rising, falling, or stable.
