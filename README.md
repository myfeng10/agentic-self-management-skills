# Agentic Self-Management Skills

Installable skills for agents that help people manage energy, identity, weekly trajectory, and long-term memory without adding more tracking overhead.

The shared point of view: users do not need another productivity menu. They need an agent that can read behavioral signals, make a clear call, and return one high-ROI next move.

## Skills

### Identity Vote Translator

Translates one ordinary conversation or end-of-day recap into distinct behavior votes and one next vote. It stays lightweight and does not turn sparse evidence into decimal scores or fixed personality labels. Use the standalone `identity-votes` skill for an explicit multi-day trajectory review.

Install:

```bash
npx skills add myfeng10/agentic-self-management-skills --skill identity-vote-translator
```

### Next Mode

`energy-decision-support` decides whether the user should push, switch modes, recover, or stop from general sleep, timeline, meeting, food, context-switching, and fatigue signals. It is distinct from the standalone `next-mode`, which specializes in hidden cognitive spend from AI-assisted work.

Install:

```bash
npx skills add myfeng10/agentic-self-management-skills --skill energy-decision-support
```

### Weekly Trajectory

Turns weekly logs, habits, energy patterns, identity movement, relationships, and commitments into a short operating review. Ends with a protect / try / avoid plan.

Install:

```bash
npx skills add myfeng10/agentic-self-management-skills --skill weekly-trajectory-review
```

### Living Archive

Preserves a project, realization, experiment, life period, or recurring thread as future-self context. Captures what happened, why it mattered, what changed, and what should not be forgotten.

Install:

```bash
npx skills add myfeng10/agentic-self-management-skills --skill living-archive-entry-builder
```

## Install All

```bash
npx skills add myfeng10/agentic-self-management-skills --all
```

Restart the agent after installing so the new skills are picked up.

## Actual before / after

All four skills were run on realistic scenarios in isolated Codex sessions.

| Skill | Before | After | Material effect |
|---|---:|---:|---|
| `energy-decision-support` | 10 | 10 | Kept its decisive general-capacity behavior; UI name now matches the skill. |
| `identity-vote-translator` | 8 | **10** | Replaced decimals and fixed labels with four distinct one-line behavior votes. |
| `living-archive-entry-builder` | 10 | 10 | Now drafts inline unless saving or editing a file was explicitly requested. |
| `weekly-trajectory-review` | 8 | **10** | Each Protect, Try, and Avoid item is now one atomic decision. |

See the [public evaluation note](https://github.com/myfeng10/myfeng10/blob/main/skills-evaluation.md#full-scorecard) for the frozen-suite method and full scorecard.
