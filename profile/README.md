# DevOps-gruppe 2

Vi er en gruppe fra faget **DevOps på EK**. Vi har taget en gammel Python-søgemaskine, **¿Who Knows?**, og skrevet den om til **Go**, med en DevOps-kæde rundt om, så hver ændring bliver testet, sikkerhedsscannet, deployet og overvåget automatisk.

🌐 **Siden:** https://whoknows-gruppe2.dk
📈 **Monitoring:** [Grafana-dashboard](https://dreamycaravan440.grafana.net/public-dashboards/37e50f266f314afa9bb21bf85f9115dc)
📦 **Kode:** [search-engine](https://github.com/devops-gruppe-2/search-engine)

---

## Sådan arbejder vi

| | |
|---|---|
| **Planlægning** | Opgaver på [projekt-boardet](https://github.com/orgs/devops-gruppe-2/projects/1). Beslutninger tages offentligt i [Discussions](https://github.com/devops-gruppe-2/search-engine/discussions) |
| **Kode** | Feature branches og pull requests. `main` er beskyttet og kræver grøn CI |
| **Kvalitet** | golangci-lint, Hadolint, unit-, integrations- og E2E-tests (Playwright) |
| **Sikkerhed** | Trivy scanner Docker-images, Dependabot opdaterer afhængigheder, HTTPS og security headers |
| **Levering** | GitHub Actions bygger, tester og deployer automatisk til en DigitalOcean-droplet |
| **Overvågning** | Prometheus og Grafana med fokus på, hvordan brugerne bruger søgemaskinen |
| **Dokumentation** | Hver ændring står i [ændringsloggen](https://github.com/devops-gruppe-2/search-engine/blob/main/docs/aendringslog.md) med hvad, hvorfor og hvordan den testes |

## Teknologi

Go · Gin · PostgreSQL · Docker Compose · Nginx · GitHub Actions · DigitalOcean · Let's Encrypt · Prometheus · Grafana · Playwright · Trivy

## Gruppen

- [@elaf0016](https://github.com/elaf0016)
- [@hawraalmomen](https://github.com/hawraalmomen)

Vil du bidrage eller melde en fejl? Læs [CONTRIBUTING.md](https://github.com/devops-gruppe-2/.github/blob/main/CONTRIBUTING.md). Sikkerhedshuller meldes som beskrevet i [SECURITY.md](https://github.com/devops-gruppe-2/.github/blob/main/SECURITY.md).
