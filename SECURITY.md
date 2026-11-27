# Sikkerhed

## Meld et sikkerhedshul

**Opret ikke et offentligt issue eller en Discussion om et sikkerhedshul.** Et offentligt opslag viser angribere, hvor de skal angribe, før hullet er lukket.

Meld det i stedet privat:
1. Gå til det berørte repo → fanen **Security** → **Report a vulnerability**.
2. Beskriv hullet, hvordan man genskaber det, og hvad det kan bruges til.

Vi svarer så hurtigt som muligt og fortæller, når hullet er lukket. Først derefter beskriver vi det offentligt i ændringsloggen (*responsible disclosure*).

## Det gør vi selv for at holde systemet sikkert

- **Trivy** scanner vores Docker-images ved hver pull request og stopper dem, hvis der er kendte HIGH- eller CRITICAL-sårbarheder.
- **Dependabot** laver pull requests med opdateringer af Go-pakker, Docker-images, GitHub Actions og Playwright hver uge.
- **HTTPS** med Let's Encrypt, HSTS og security headers (CSP, X-Frame-Options m.fl.).
- **Passwords** gemmes som bcrypt-hashes. Hemmeligheder ligger i GitHub Secrets og på serveren, aldrig i Git.
- **Serveren** har firewall (kun port 22, 80 og 443), fail2ban og opdateres med sikkerhedsrettelser.

## Understøttede versioner

Kun den version, der kører på https://whoknows-gruppe2.dk (seneste commit på `main`), får sikkerhedsrettelser.
