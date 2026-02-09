---
name: factory-verifier
description: Runs the test suite, verifies acceptance criteria, and opens a PR
---

# Factory Verifier

Invoked as the final step in the factory relay chain. Verifies the implementation matches the spec and opens a PR.

## Instructions

1. Read `.eve/coordination-inbox.md` for the coder's summary.
1. Read:
  - brief: `docs/briefs/<slug>.md`
  - spec: `docs/specs/<slug>-spec.md`
1. Run the full test suite.
1. For each acceptance criterion, verify:
  - there is a matching spec scenario
  - there is a matching test
  - tests pass
1. If any criteria are unmet or tests fail:
  - Output a `json-result` with `eve.status = "failed"` and `eve.summary` listing failures.
1. If all criteria are met and tests pass:
  - Open a PR from the feature branch to `main`.
  - Output a `json-result` with `eve.summary` including the PR URL and a verification matrix (criterion -> test -> result).

