# Public Agent Workflow V1

Trigger phrases: `Public Agent`, `publish agent`, `public website`, `push GitHub`.

## Public Agent
1. Resolve Agent name + canonical source.
2. Validate required sections: Problem, Destination, System, Roadmap, Quick Start, Test/DoD, Evolution.
3. Generate/update `agent.yaml`.
4. Render website from the canonical source/manifest.
5. QA HTML/JS, mobile layout, links and sensitive-data exposure.
6. Commit/push source to the Agent GitHub repository.
7. Deploy the exact tested version.
8. Verify production URL and return URL + commit/version + DoD status.

## push GitHub
Validate → commit → push only. Do not change site visibility or DNS.

## public website / publish website
Validate current build → ensure source is versioned → deploy exact version → verify URL. Public visibility/domain changes require explicit confirmation if they expose previously private content.

## Safety gates
Never publish secrets, tokens, personal email content, private customer data or credentials. Do not claim GitHub/domain/deployment succeeded without tool confirmation.
