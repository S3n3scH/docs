# Über GitHub Advanced Security

GitHub Advanced Security (GHAS) erweitert die Sicherheitsfunktionen von GitHub und hilft Entwicklungs‑ und Sicherheitsteams dabei, Schwachstellen in ihrem Code, in Abhängigkeiten und in der Lieferkette frühzeitig zu entdecken und zu beheben.

## Wichtige Funktionen
- Code-Scanning: Automatisierte statische Analyse (z. B. CodeQL), die potenzielle Sicherheitslücken im Quellcode erkennt.
- Secret-Scanning: Erkennung von hartkodierten Zugangsdaten und Geheimnissen in Repositorys.
- Dependency Review / Dependabot: Prüfung und Automatisierung für Abhängigkeiten sowie Hinweise zu bekannten Sicherheitsproblemen in Bibliotheken.
- Supply-Chain-Security: Unterstützung für Signaturen, Prüfpfade und Policies zur Absicherung der Softwarelieferkette.
- Sicherheits-Insights: Berichte und Dashboards für Risikoübersicht und Priorisierung.
- Policies & Automatisierung: Möglichkeit, Sicherheitsprüfungen in CI/CD‑Pipelines zu erzwingen und Befunde automatisch zu verwalten.

## Verfügbarkeit
GitHub Advanced Security ist für GitHub Enterprise Server (Versionen wie 3.22) und GitHub Enterprise Cloud verfügbar. Je nach Plattform und Lizenz können einzelne Funktionen variieren.

## Aktivieren und Verwenden
1. Prüfen Sie die Lizenz- und Infrastruktur-Anforderungen für GHAS in Ihrer Enterprise‑Umgebung.  
2. Aktivieren Sie die gewünschten Features (z. B. Code-Scanning, Secret-Scanning) in den Repository- oder Organisationseinstellungen.  
3. Konfigurieren Sie Workflows (z. B. GitHub Actions) oder CI-Integrationen, um Scans automatisch bei Pull Requests und Commits auszuführen.  
4. Nutzen Sie Befund‑Workflows und Policies, um Probleme zu priorisieren und zu beheben.

## Weitere Informationen
- Detaillierte Anleitungen zur Einrichtung und Konfiguration finden Sie in der GitHub-Dokumentation: https://docs.github.com/de/enterprise-server@3.22/get-started/learning-about-github/about-github-advanced-security.md

(Erweitern Sie diesen Text gerne mit organisationsspezifischen Anweisungen, Beispiel-Workflows oder Links zu internen Richtlinien.)