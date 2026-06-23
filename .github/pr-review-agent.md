# PR review contract

This repository is enrolled in the estate-wide PR review flow.

## Primary goal
Review each PR for:
- correctness
- regressions
- security
- test adequacy
- maintainability
- cross-repo impact when shared contracts or critical paths change

## Review rules
- Prioritize real bugs and security failures over style theater.
- Separate blockers/high-risk findings from nits.
- Cite file/line evidence whenever possible.
- If a changed API, auth flow, payment flow, event contract, schema, or shared package could affect other repos, add a short **cross-repo impact** section.
- If evidence is incomplete, say what is missing instead of guessing.
- Do not spam low-value comments.

## Related repositories
- `AchilleasDrakou/artemis`
- `AchilleasDrakou/command-center`
- `AchilleasDrakou/context`

## Domain notes
- Treat runtime, session, agent orchestration, and tool execution changes as system-sensitive.
- Prefer root-cause fixes over local patches when multiple agents or runtimes share the same path.

## Critical paths
- `auth/**`
- `payments/**`
- `billing/**`
- `infra/**`
- `migrations/**`
- `doc/spec/**`
- `src/runtime/**`
- `src/agents/**`
