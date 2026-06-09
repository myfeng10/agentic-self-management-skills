---
name: weekly-trajectory-review
description: "Use when a user wants a short weekly operating review from logs, habits, energy, identity, relationships, or commitments. Finds the main pattern and returns a decisive next-week plan: protect, try, avoid."
---

# Weekly Trajectory Review

Use this skill for a Sunday-style review that converts the week's logs into self-management decisions.

The purpose is not reflection for its own sake. The purpose is calibration: predict, observe, adjust.

## Who This Is For

Use this for people building a self-management practice around energy, attention, identity, relationships, and commitments. The output should feel like a useful weekly operating review, not a diary summary.

## Trigger Phrases

- "Review my week."
- "What patterns showed up this week?"
- "Plan next week from my logs."
- "How did my energy and identity move?"
- "What should I protect next week?"

## Inputs

Use whatever the user has:

- Daily memory files
- Energy logs
- Habit tracker rows
- Calendar summaries
- Relationship/social notes
- Project notes
- Identity analysis entries

If local files are available, read recent logs before asking questions. Ask only for missing information that would materially change next week's plan.

## Review Lenses

Analyze the week through five lenses:

- Energy: sleep, high-load work, crashes, recovery, best work windows.
- Attention: context switching, mind flow, external breaks, drift.
- Identity: Builder, Reflector, Executor, Consumer, Connector, Recoverer, or custom identities present in the evidence.
- Relationships/environment: people, weather, workspace, roommate or colleague effects.
- Commitments: what the user promised vs what capacity actually allowed.

## Decision Style

The review must end in choices, not observations. Pick the highest-leverage protection, experiment, and avoidance for next week.

Be gentle about the user's week, but decisive about the plan. Do not offer a menu of possible improvements unless the user asks.

## Output

Return:

```text
Week signal
One paragraph naming the week's actual pattern.

Energy pattern
- Best capacity window:
- Main depletion source:
- Recovery that worked:

Identity movement
- Rising:
- Falling:
- Mixed:

Self-management lesson
One concrete lesson the user should remember.

Next week plan
- Protect:
- Try:
- Avoid:
- One calibration question:
```

Keep recommendations small enough to execute. Do not create a grand life plan unless the user asks.

## Persistence

If the user asks to save the review, write a concise entry to the appropriate memory or review file. Separate raw facts from interpretation.
