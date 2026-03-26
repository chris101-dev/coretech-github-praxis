# Workflow-Notizen: Git & GitHub Synchronisation

---

## 1. Remote-Repository verbinden

- Neues Repository auf GitHub unter https://github.com/new angelegt
- Lokal einen Ordner erstellt und darin Git initialisiert:
  ```bash
  git init
  ```
- Remote-URL mit dem lokalen Repository verknüpft:
  ```bash
  git remote add origin https://github.com/<username>/coretech-github-praxis.git
  ```
- Verbindung geprüft:
  ```bash
  git remote -v
  ```

---

## 2. Änderungen zu GitHub übertragen (Push)

- Dateien zum Staging-Bereich hinzugefügt:
  ```bash
  git add .
  ```
- Commit mit beschreibender Nachricht erstellt:
  ```bash
  git commit -m "docs: README und .gitignore hinzugefügt"
  ```
- Commits ins Remote-Repository übertragen:
  ```bash
  git push origin main
  ```

---

## 3. Änderungen von GitHub lokal integrieren (Pull)

- Repository in einen zweiten Ordner geklont:
  ```bash
  git clone https://github.com/<username>/coretech-github-praxis.git github-remote-praxis-klon
  ```
- Im geklonten Repository Commit-Historie geprüft:
  ```bash
  git log --oneline
  ```
- Im Original-Repository Änderungen gepusht, danach im Klon aktualisiert:
  ```bash
  git pull
  ```
- Beide Arbeitsstände anschließend identisch → Synchronisation erfolgreich

---

## 4. Merge-Konflikt erkannt

- Neuen Branch erstellt und eine Zeile in der README.md geändert:
  ```bash
  git checkout -b feature-notizen-update
  ```
- Branch zu GitHub übertragen und Pull Request geöffnet
- Dieselbe Zeile auch im `main`-Branch geändert und gepusht
- GitHub zeigte im Pull Request den Status **"Can't automatically merge"**
- Lokal erkennbar durch `git merge` → Ausgabe **"CONFLICT"** in der betroffenen Datei
- Im Konflikt-Bereich in der Datei sichtbar:
  ```
  <<<<<<< HEAD
  (lokale Änderung)
  =======
  (Remote-Änderung)
  >>>>>>> feature-notizen-update
  ```
- Konflikt manuell gelöst, Datei gespeichert und mit `git add` + `git commit` abgeschlossen
