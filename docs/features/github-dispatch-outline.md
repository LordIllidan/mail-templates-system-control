# Szkic integracji GitHub (issue → dispatch)

## Wzorzec

1. Issue w `*-control` opisuje epik (zakres, kryteria).
2. Workflow w `*-control` mapuje zakres na listę docelowych repo (na podstawie `*-hub` / `config/solutions/*.json`).
3. Dla każdego celu: `repository_dispatch` z payloadem `{ "issue_url": "...", "slug": "..." }`.
4. Docelowe repo ma workflow `on: repository_dispatch` wykonujący pracę (lub odpala lokalnego agenta na runnerze).

## Uwagi

- Uprawnienia PAT: minimalny zakres pod `contents/workflow` w repo docelowych + `actions:write` jeśli uruchamiasz workflowy.
- Długie sesje agentów: rozważ **self-hosted runner** przypięty do `*-control` lub do repo docelowych.
