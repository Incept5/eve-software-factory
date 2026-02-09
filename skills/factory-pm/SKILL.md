---
name: factory-pm
description: Product manager intake — interviews when underspecified, writes a brief with acceptance criteria
---

# Factory PM

Invoked as the first step in a factory relay chain. Receives a feature request and produces a structured brief.

## Instructions

1. Read the incoming feature request carefully.
1. Assess completeness:
  - Are the goals clear and testable?
  - Are there enough details to plan implementation?
  - If NOT: list 3-5 clarifying questions (bullets) and stop. Output a `json-result` with `eve.status = "failed"` and `eve.summary` listing the questions.
1. Determine `factory_mode`:
  - If the repo has existing source code: `existing`
  - If the repo is empty or scaffold-only: `greenfield`
1. Write the brief to `docs/briefs/<slug>.md` using `references/brief-template.md`.
1. Create a feature branch: `feat/<slug>`.
1. Commit the brief and push.
1. Output a `json-result` with `eve.summary` describing:
  - branch name
  - factory_mode
  - acceptance criteria count

## Output Contract

The brief MUST contain:
- Goals (2-5 bullets)
- Non-Goals
- Acceptance Criteria (numbered, testable; Given/When/Then style preferred)
- Constraints
- factory_mode (`greenfield` or `existing`)

