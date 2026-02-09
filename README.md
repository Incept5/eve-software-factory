# Eve Software Factory (MVP)

AgentPack that implements a simple relay-chain "software factory":

PM -> Planner -> Coder -> Verifier -> PR

This repo is intended to be installed into an Eve project via `x-eve.packs`,
then used through chat routing (messages starting with `factory ...`).

## Install (local dev)

In your target repo's `.eve/manifest.yaml`, add:

```yaml
x-eve:
  packs:
    - source: ../eve-software-factory
```

Then re-sync:

```bash
eve agents sync --project <PROJECT_ID> --ref main --repo-dir . --allow-dirty --local
```

## What's Included

- `eve/pack.yaml`: pack descriptor
- `eve/agents.yaml`: four factory agents
- `eve/teams.yaml`: one relay team (`factory`)
- `eve/chat.yaml`: one route (`^factory\\b`)
- `eve/x-eve.yaml`: harness profiles + defaults
- `skills/`: OpenSkills `SKILL.md` instructions and templates

