# Change: Init PLDC Orchestrator template

## Summary

Dodano szablon repozytorium orchestratora PLDC (`*-control`) — osobne repo od hubu konfiguracyjnego, z tymi samymi bramkami dokumentacji co Project Docs.

## Verification

- `pwsh ./scripts/ci/Test-ContextDocs.ps1`
- `pwsh ./scripts/ci/Test-ChangeDocs.ps1`

## Context Updates

- `context.md`
- `docs/context.md`
