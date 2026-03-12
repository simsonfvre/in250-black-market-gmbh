# Branching-Strategie

## Gewählte Strategie

Für dieses Projekt verwenden wir **Trunk-Based Development** mit einer geschützten Hauptbranch `main` und kurzen, thematisch klaren Arbeits-Branches.

## Ziel der Strategie

Diese Strategie wurde gewählt, weil sie:

- einfach verständlich ist
- wenig Verwaltungsaufwand erzeugt
- Merge-Konflikte reduziert
- eine saubere und stabile Hauptbranch ermöglicht
- gut für kleine bis mittelgroße Projekte geeignet ist

## Branches

### `main`

Die Branch `main` ist die zentrale und stabile Hauptbranch.

Regeln:

- `main` soll jederzeit in einem lauffähigen Zustand sein
- direkte Commits auf `main` sollen vermieden werden
- Änderungen gelangen nur über Pull Requests nach `main`

### Arbeits-Branches

Neue Arbeiten werden in separaten Branches durchgeführt. Diese Branches werden von `main` abgezweigt und nach dem Merge wieder gelöscht.

Namenskonventionen:

- `feat/...` für neue Funktionen
- `fix/...` für Fehlerbehebungen
- `docs/...` für Dokumentation
- `chore/...` für Wartung, Aufräumarbeiten oder Konfiguration

Beispiele:

- `feat/login`
- `fix/input-validation`
- `docs/readme-update`
- `chore/github-actions`

## Arbeitsablauf

1. Von `main` wird ein neuer Branch erstellt.
2. Änderungen werden in diesem Branch umgesetzt.
3. Die Änderungen werden in sinnvollen Commits gespeichert.
4. Anschließend wird ein Pull Request erstellt.
5. Nach Prüfung und erfolgreichen Tests wird der Branch in `main` zusammengeführt.
6. Danach kann der Arbeits-Branch gelöscht werden.

## Vorteile dieser Strategie

- klare Trennung von stabiler Version und laufender Arbeit
- einfache Zusammenarbeit im Team
- bessere Nachvollziehbarkeit von Änderungen
- gute Grundlage für Code Reviews und automatisierte Tests

## Nachteile

- bei sehr vielen parallelen Releases ist diese Strategie weniger geeignet
- diszipliniertes Arbeiten mit kleinen Branches ist wichtig

## Warum nicht Gitflow?

Gitflow ist für größere Teams oder komplexe Release-Prozesse sinnvoll. Für dieses Projekt wäre Gitflow jedoch eher zu aufwendig, da zusätzliche Branches wie `develop`, `release` und `hotfix` den Prozess unnötig komplizieren würden.

## Fazit

Für dieses Projekt ist **Trunk-Based Development mit kurzer Lebensdauer von Feature-Branches** die sinnvollste Wahl. Die Strategie ist einfach, übersichtlich und unterstützt einen stabilen Entwicklungsprozess.