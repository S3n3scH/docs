# GitHub Advanced Security einrichten

Dieser Leitfaden zeigt eine einfache Vorgehensweise, um GitHub Advanced Security (GHAS) in einer Organisation oder einem Repository zu aktivieren.

## 1. Vorbedingungen prüfen

Stellen Sie sicher, dass:

- die passende GitHub-Edition oder Lizenz aktiviert ist
- Sie über die erforderlichen Rechte in der Organisation oder im Repository verfügen
- die gewünschte CI-Umgebung bereits konfiguriert ist

## 2. Funktionen aktivieren

In den Repository- oder Organisationseinstellungen können Sie die gewünschten Sicherheitsfunktionen aktivieren, zum Beispiel:

- Code-Scanning
- Secret-Scanning
- Abhängigkeitsprüfung

## 3. Workflow für Pull Requests einrichten

Ein typischer Workflow prüft bei Änderungen automatisch den Code und meldet Sicherheitsprobleme direkt im Pull Request.

```yaml
name: security-scan

on:
  pull_request:
  push:
    branches:
      - main

jobs:
  codeql:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Initialize CodeQL
        uses: github/codeql-action/init@v3
        with:
          languages: javascript
      - name: Autobuild
        uses: github/codeql-action/autobuild@v3
      - name: Analyze
        uses: github/codeql-action/analyze@v3
```

## 4. Risiken priorisieren

Nach der Aktivierung sollten Sie die Meldungen regelmäßig prüfen:

- kritische Sicherheitslücken zuerst beheben
- sensible Änderungen in Pull Requests dokumentieren
- betroffene Abhängigkeiten nachverfolgen und aktualisieren

## 5. Organisationale Richtlinien festlegen

Für größere Teams empfiehlt sich eine klare Sicherheitsstrategie:

- Verantwortlichkeiten definieren
- Automatisierung standardisieren
- Sicherheitswarnungen in den Entwicklungsprozess integrieren

## Fazit

Mit GHAS können Sicherheitsprobleme bereits im Entwicklungsprozess erkannt werden. Dadurch sinkt das Risiko für unentdeckte Schwachstellen und Sicherheitslücken im produktiven Betrieb.
