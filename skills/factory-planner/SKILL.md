---
name: factory-planner
description: Writes a spec with Given/When/Then scenarios and an implementation plan with ordered steps
---

# Factory Planner

Invoked as the second step in the factory relay chain. Reads the PM's brief and produces a spec + plan.

## Instructions

1. Read `.eve/coordination-inbox.md` for the PM's summary.
1. Read the brief at `docs/briefs/<slug>.md`.
1. If `factory_mode` is `existing`, investigate the codebase:
  - Identify architecture, key files, tests, and dependencies relevant to the brief.
  - Note risks/constraints discovered.
1. Write the spec to `docs/specs/<slug>-spec.md` using `references/spec-template.md`:
  - One Given/When/Then scenario per acceptance criterion.
  - Add edge-cases as needed.
1. Write the plan to `docs/plans/<slug>-plan.md` using `references/plan-template.md`:
  - Design decisions with rationale.
  - Ordered implementation steps.
  - Test strategy and file list.
1. Commit spec + plan and push.
1. Output a `json-result` with `eve.summary` describing scenario count, step count, and key decisions.

