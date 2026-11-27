# Sådan bidrager du

Tak, fordi du vil hjælpe. Sådan arbejder vi i alle repos i **devops-gruppe-2**.

## 1. Start med et issue
- Find eller opret et issue, der beskriver opgaven eller fejlen. Brug skabelonerne (*Bug report* eller *Feature request*).
- Større valg (fx database eller deployment-strategi) diskuteres først i **Discussions**, så alle kan se, hvorfor vi valgte, som vi gjorde.

## 2. Lav en branch
Arbejd aldrig direkte på `main`. Navngiv branchen efter typen af ændring:

| Præfiks | Bruges til |
|---|---|
| `feature/` | Ny funktion, fx `feature/search-log` |
| `fix/` | Fejlrettelse, fx `fix/nginx-1.30.7` |
| `docs/` | Kun dokumentation |
| `chore/` | Vedligehold, fx afhængigheder |

## 3. Før du laver en pull request
- Kør linteren lokalt (`prek run --all-files`), og kør testene (se README).
- Skriv ændringen i `docs/aendringslog.md`: hvad var galt, hvad er ændret, hvorfor, og hvordan man ser, at det virker.
- Opdater README, hvis noget skal køres eller sættes op på en ny måde.
- Ingen passwords, nøgler eller tokens i koden. De hører hjemme i GitHub Secrets eller i `.env` på serveren.

## 4. Pull request
- Udfyld PR-skabelonen, og link issuet (fx `Closes #12`).
- Alle krævede checks skal være grønne: `lint`, `test`, `e2e`, `build` og `trivy`.
- Brug **squash merge**, så `main` har én commit pr. ændring.

## 5. Efter merge
- CD deployer automatisk. Tjek, at deployet er grønt, og at siden virker.
- Hold øje med Grafana-dashboardet, hvis ændringen påvirker brugerne.
