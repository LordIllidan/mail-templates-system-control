# Rola orchestratora (`*-control`)

## Po co osobne repo

- **Hub (`*-hub`)** trzyma kanoniczną mapę URL-i repozytoriów (JSON).
- **Orchestrator (`*-control`)** jest **portem wykonania**: issue, etykiety etapów, workflowy dispatch, komentarze agentów — bez mieszania z plikami konfiguracyjnymi hubu.

## Minimalny następny krok (poza szablonem)

Dodać workflow w `.github/workflows/`, który:

1. Czyta profil z hubu (np. checkout jako `resource` albo `curl` raw JSON z `main`).
2. Na issue (lub label) uruchamia `gh workflow run` / `repository_dispatch` w docelowych repo zgodnie z zakresem.

To jest intencja szablonu — implementacja zależy od projektu.
