# Trinity Studio Architecture

**Status: planning and architecture seed — not a runnable application.**

This repository defines a proposed local-first management layer for TrinityCore development and server operations. The default branch currently contains documentation only; it has no application source, package manifest, installer or test suite.

## Intended direction

- Work offline by default, with no cloud account or telemetry requirement.
- Integrate local Ollama models optionally, without granting automatic privileged execution.
- Keep TrinityCore as a separately maintained upstream dependency.
- Build a small Linux-first CLI before attempting a desktop interface.
- Keep credentials, player data, databases and generated binaries out of Git.

## Proposed components

| Component | Intended responsibility | Status |
| --- | --- | --- |
| core-adapter | Discover TrinityCore source, builds and configuration | Proposed |
| workspace | Local profiles and paths | Proposed |
| doctor | Dependency, database, port and permission checks | Proposed |
| runner | Explicit, confirmed server and build operations | Proposed |
| ui | Optional desktop presentation | Proposed |
| ai | Optional local Ollama assistance | Proposed |

## Next verified milestone

Create a minimal CLI exposing `status`, `doctor`, `scan` and `config` commands. Add a manifest, minimal tests and CI together with the first executable implementation.

## CI and historical branches

The current default branch has no runnable build. Older failed pull-request workflows do **not** establish that the default branch's proposed architecture has been implemented or tested. Review any historical PR code before bringing it forward.

See [AGENTS.md](AGENTS.md) for repository constraints and contribution discipline.

## Related work

- [TrinityCore](https://github.com/HenricHuntsman/TrinityCore) — separate upstream-derived codebase; preserve its upstream attribution.
- [AgentFoundry TrinityCore Studio](https://github.com/HenricHuntsman/AgentFoundry-TrinityCore-Studio) — separate early-stage repository.

**No release or functional compatibility is claimed yet.**
