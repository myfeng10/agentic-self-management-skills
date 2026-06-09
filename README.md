# Agentic Self-Management Skills

Installable skills for agents that help people manage energy, identity, weekly trajectory, and long-term memory without adding more tracking overhead.

The shared point of view: users do not need another productivity menu. They need an agent that can read behavioral signals, make a clear call, and return one high-ROI next move.

## Skills

### Identity Votes

Tracks identity votes while the user talks. Useful when a user describes their day, habits, conflict, procrastination, goals, routines, work, recovery, or repeated behavior. The agent quietly maintains a lightweight vote ledger and presents the strongest identity signal at a natural endpoint.

Install:

```bash
npx skills add myfeng10/agentic-self-management-skills --skill identity-vote-translator
```

### Next Mode

Decides whether the user should push, switch modes, recover, or stop based on sleep, timeline, meetings, food, context switching, and fatigue signals. The output is one decision, not a generic list of options.

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
