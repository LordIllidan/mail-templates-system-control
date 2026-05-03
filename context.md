# Context: PLDC Orchestrator

## Purpose

Repozytorium **sterujące** procesem PDLC dla jednego rozwiązania: issue jako wejście, integracja z GitHub Actions i (opcjonalnie) agentami, bez trzymania w nim mapy kodu — ta jest w hubie.

## Boundaries

- Owns workflowy orchestracji, szablony issue i dokumentację procesu w tym repo.
- Does not own kanoniczną mapę repozytoriów — to `*-hub` (`PdlcTemplatePLDCHub`).

## Important Files

- `docs/context.md`: kontekst dokumentacji orchestratora.
- `docs/features/`: opis ról i integracji z hubem.
- `.github/workflows/`: docelowe miejsce na dispatch / joby agentowe (do rozbudowy).

## Local Commands

- `pwsh ./scripts/ci/Test-ContextDocs.ps1`
- `pwsh ./scripts/ci/Test-ChangeDocs.ps1`

## Decisions

- Orchestrator jest **osobnym** repo od hubu, żeby nie mieszać konfiguracji statycznej z ciężkim lifecycle agentów.

## Child Contexts

- `docs/context.md`
