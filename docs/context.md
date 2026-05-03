# Context: Documentation

## Purpose

Dokumentacja orchestratora: jak czyta konfigurację z hubu i jak planować workflowy.

## Boundaries

- Owns treści w `docs/` dotyczące orchestracji.
- Does not zastępuje `*-hub` jako źródła prawdy o URL-ach repo.

## Important Files

- `features/orchestrator-role.md`: rola repo `*-control`.
- `features/github-dispatch-outline.md`: szkic integracji GitHub (issue → dispatch).

## Local Commands

- `pwsh ./scripts/ci/Test-ChangeDocs.ps1` (z katalogu głównego repozytorium)

## Decisions

- Konwencja nazwy repo z provisioning: sufiks `control` (np. `myproj-control`).

## Child Contexts
