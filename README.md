# PdlcTemplatePLDCOrchestrator

Szablon repozytorium **orchestratora PLDC** (wariant **B**): osobne repo od **hubu konfiguracyjnego** (`*-hub`). Tu zgłaszasz **issue** sterujące pracą (epiki, dispatch do FE/API/GitOps), a **mapa repozytoriów** żyje w `*-hub` (`config/solutions/*.json`).

## Relacja do innych repo

| Repo | Rola |
|------|------|
| `*-hub` | Konfiguracja rozwiązania — linki do `fe`, `api`, `db`, `gitops`, `docs`, `control` (to repo). |
| `*-control` (to) | Wejście ludzi/agents: issue → workflow / skrypty → `repository_dispatch` lub PR w docelowych repo. |
| `*-fe` / `*-api` / … | Implementacja — zmiany kodu. |

## Po utworzeniu z Project Managera

1. W `*-hub` sprawdź, że w profilu jest `repos.orchestrator` wskazujący na to repo (`…-control`).
2. Dodaj sekrety PAT / `GITHUB_TOKEN` zgodnie z planowanymi workflowami (minimalny zakres pod konkretne dispatch).
3. Rozwijaj workflow w `.github/workflows/` (szablon zawiera tylko CI dokumentacji — miejsce na Twój orchestrator).

## Szablon Project Manager

Ten template jest wpisany w `LordIllidan/PdlcTemplateProjectManager` (`config/templates.json`) i **provisionuje się** razem z pozostałymi repo projektu.
