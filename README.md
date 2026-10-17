# Trinity Studio — Architecture Seed

Planning and architecture for a proposed local-first management layer around TrinityCore.

**Stage: planning.** This repository contains documentation and project instructions; it does not contain a runnable Studio, installer, package manifest or application tests.

## Proposed first milestone

A small read-only CLI with `status`, `doctor`, `scan` and `config` commands. Keep TrinityCore as an external dependency. Use local tools and optional Ollama assistance, with no required cloud account or subscription.

Later build/start/stop actions and any desktop UI require explicit implementation, authority boundaries and validation. They are not current features.

## What remains

- Define the CLI contract and local workspace/configuration format.
- Implement read-only discovery and dependency diagnostics.
- Add focused tests, a package manifest and CI with the first executable code.
- Verify Linux installation and a real TrinityCore workspace before declaring alpha readiness.

See [AGENTS.md](AGENTS.md) for constraints and component boundaries. [AgentFoundry TrinityCore Studio](https://github.com/HenricHuntsman/AgentFoundry-TrinityCore-Studio) is a separate placeholder, not an implemented component.

Updated 18 October 2026.
