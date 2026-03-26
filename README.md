# coretech-github-praxis

Kompaktes Test-Repository, um Git und GitHub über ein Remote-Setup zu verbinden sowie einfache Befehle praktisch zu testen und zu üben.

---

## Voraussetzungen

- [Git](https://git-scm.com/) ist lokal installiert
- Ein GitHub-Account ist vorhanden
- Git ist mit deinem GitHub-Account konfiguriert:

```bash
git config --global user.name "Dein Name"
git config --global user.email "deine@email.de"
```

---

## Projektstruktur

```
coretech-github-praxis/
├── README.md             # Projektdokumentation
├── notizen.txt           # Persönliche Notizen und Lernfortschritt
└── .gitignore            # Ausgeschlossene Dateien (z. B. .env, Logs)
```

---

## Wichtige Git-Befehle (Übersicht)

| Befehl | Beschreibung |
|---|---|
| `git init` | Lokales Repository initialisieren |
| `git remote add origin <URL>` | Remote-Repository verknüpfen |
| `git add .` | Alle Änderungen stagen |
| `git commit -m "Nachricht"` | Commit erstellen |
| `git push origin main` | Änderungen zu GitHub übertragen |
| `git pull` | Änderungen vom Remote holen und integrieren |
| `git clone <URL>` | Repository klonen |
| `git status` | Aktuellen Stand prüfen |
| `git log --oneline` | Commit-Historie anzeigen |

---

## Nächste Schritte

- [ ] Branches erstellen und Pull Requests öffnen
- [ ] Merge-Konflikte erkennen und lösen
- [ ] GitHub Actions / Workflows erkunden
- [ ] Zusammenarbeit mit anderen GitHub-Nutzern testen
