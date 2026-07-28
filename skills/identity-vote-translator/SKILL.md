---
name: identity-vote-translator
description: Use during an ordinary conversation or end-of-day recap when a user describes habits, choices, avoidance, conflict, work, recovery, or a desired future self. At a natural endpoint, translate the strongest behavior signal into a concise identity read and one next vote. For an explicit multi-day or comparative identity review, use identity-votes instead.
---

# Identity Vote Translator

Use this skill while the user is talking, not only after they request a formal review.

Core principle: behavior disappears, identity accumulates. Every repeated action is a vote for a kind of person.

## Boundary

Keep this skill ambient and lightweight. Do not turn one conversation into a formal identity report, personality diagnosis, or long-horizon certainty. Use `identity-votes` when the user requests a multi-day ledger, comparison, or trajectory review.

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

Treat sparse evidence as sparse. Use `low`, `medium`, or `high` evidence strength rather than decimal scores.

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

For one conversation, say `avoidance vote` or `confrontation vote`, not `Avoider` or `Confronter`. Reserve capitalized identity labels for repeated evidence across several contexts or for the user's own named ontology.

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
3. Name the competing vote or risk only when evidence supports it.
4. Suggest one small shift that changes the next vote.

If the user has named desired or danger identities, use those terms first. If not, infer identities from evidence.

## Output

Default to:

```text
Read: one sentence naming the strongest behavior-to-identity signal.
High-ROI next vote: one concrete action.
Votes:
- behavior → identity vote
Tension: the competing vote or risk, if present.
```

List each materially distinct vote separately; do not merge building, early feedback, connection, and avoidance into one trait. Keep the list to 2-4 one-line votes.

If the user asks for deeper evidence, expand to:

```text
Read: one sentence naming the strongest identity signal.
High-ROI next vote: the one action most likely to shift the trajectory.

Identity votes
- Identity: someone who ...
  Evidence strength: LOW | MEDIUM | HIGH
  Evidence: concrete behaviors from the input
  Trajectory: where this converges if repeated
  Alignment: aligned | mixed | misaligned
  Next vote: one practical behavior to reinforce or redirect

Main tension: the strongest conflict between identities
Risk to watch: Avoider | Confronter | other, if present
```

Do not assign numeric weights. Do not extrapolate a single day into a six-month or five-year identity claim.
