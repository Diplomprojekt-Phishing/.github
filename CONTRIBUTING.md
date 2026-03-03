# Contributing Guide

Dieses Dokument beschreibt die Regeln und Konventionen für alle Beiträge zu den Repositories der `Diplomprojekt-Phishing`-Organisation.

## Branch-Strategie

| Branch | Zweck |
|---|---|
| `main` | Produktionsstand – **nur via Pull Request**, direkte Pushes sind gesperrt |
| `dev` | Integrations-Branch für abgeschlossene Features |
| `feat/<beschreibung>` | Entwicklung neuer Features (Basis: `dev`) |
| `fix/<beschreibung>` | Behebung von Fehlern (Basis: `dev` oder `main`) |

**Beispiele für Branch-Namen:**
```
feat/tracking-composable
feat/abandon-endpoint
fix/cors-configuration
docs/update-readme
```

## Commit-Konvention

Alle Commits müssen dem [Conventional Commits](https://www.conventionalcommits.org/de/v1.0.0/)-Standard entsprechen:

```
<typ>: <kurze beschreibung>

[optionaler body]

[optionaler footer]
```

**Typen:**

| Typ | Wann verwenden |
|---|---|
| `feat` | Neues Feature |
| `fix` | Fehlerbehebung |
| `docs` | Dokumentationsänderung |
| `refactor` | Code-Umstrukturierung ohne Funktionsänderung |
| `chore` | Wartungsarbeiten (Dependencies, Config, Build) |
| `test` | Tests hinzufügen oder ändern |

**Beispiele:**
```
feat: add useTracking composable with focus time measurement
fix: resolve CORS error on /api/track/submit endpoint
docs: add API endpoint documentation to README
refactor: extract API calls into dedicated trackingApi service
chore: update tailwind to v4
```

## Pull Request Prozess

1. Feature-Branch von `dev` erstellen: `git checkout -b feat/mein-feature dev`
2. Änderungen committen (Conventional Commits beachten)
3. Branch pushen: `git push origin feat/mein-feature`
4. Pull Request gegen `dev` erstellen
5. Mindestens **1 Approval** eines anderen Teammitglieds einholen
6. Erst nach Approval mergen

## Code-Qualität

- Kommentare in deutschem Fließtext (für Diplomarbeit)
- Keine auskommentierten Code-Blöcke committen
- Keine `.env`-Dateien committen (nur `.env.example`)
- Keine `node_modules` committen
