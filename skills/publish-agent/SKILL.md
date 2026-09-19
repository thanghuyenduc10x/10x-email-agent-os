---
name: publish-agent
description: Package a solved workflow into a 10X Public Agent artifact, validate it, version it in GitHub, deploy the tested website, and report Definition of Done. Trigger on "Public Agent", "publish agent", "push GitHub", "publish website", or "public website".
---
# Publish Agent
Use the canonical source and `agent.yaml` as source of truth. Require seven website sections: Problem, Destination, System, Roadmap, Quick Start, Test & Definition of Done, Evolution. For `Public Agent`, run package → QA → GitHub → deploy → verify. For `push GitHub`, stop after version-control. For `publish website`, deploy only the tested version. Never publish secrets or private user data. Never report a deployment, domain, or push as successful without confirmation from the corresponding tool.
