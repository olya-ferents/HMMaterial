- **Суддя:** `claude-haiku-4-5` / `anthropic`.
- **Прогони:** `clean`,`lesson-01``lesson-02`
- **Активні дефекти:** 
lesson-01:D01, D02, D03. D04, lesson-02:D05, D16, D19, D20, D25.

## Команди

```sh
docker compose run --rm eval \
  --profiles lesson-02 \
  --runs 1 \
  --only C-03,C-04,C-06,C-08,C-12 \
  --metrics hallucination,faithfulness
```

```sh
docker compose run --rm eval --runs 3
```

```sh
docker compose run --rm eval --profiles clean
```
