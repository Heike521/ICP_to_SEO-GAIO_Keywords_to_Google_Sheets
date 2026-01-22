# n8n Workflow: ICP → SEO/GAIO Keywords → Google Sheets

Dieses Repository versioniert n8n-Workflows als JSON-Dateien.
![n8n](https://img.shields.io/badge/n8n-FF6C37?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

---

## Workflow ArchiArchitektur

![ICP → SEO/GAIO Keyword Automation](icp-seo-gaio-workflow.png)

---

## Inhalt

- `n8n/workflows/` – exportierte n8n-Workflows (JSON)
- optional: `docs/` – zusätzliche Doku / Screenshots

## Workflow: ICP → SEO/GAIO Keywords → Google Sheets

### Zweck

- Nimmt ICP-Daten über ein Formular entgegen (Form Trigger).
- Generiert **exakt 20 SEO/GAIO Keywords** (Short-Head & Long-Tail) via OpenAI.
- Schreibt **pro Keyword eine Zeile** in Google Sheets.

### Eingabe (Formularfelder)

- `branche`
- `target_role`
- `age`
- `target_goal`
- `target_pain`
- `target_land`
- `language`

### Ausgabe (Google Sheets – pro Keyword eine Zeile)

- Zeitstempel
- Branche
- Zielgruppenrolle
- Alter
- Ziele der Zielgruppe
- Ängste der Zielgruppe
- Land/Region der Zielgruppe
- Sprache der Keywords
- Keyword (Gesamt)
- Short-Head (optional)
- Long-Tail (optional)

## Import in n8n

1. n8n öffnen
2. Workflows → **Import from File**
3. JSON aus `n8n/workflows/` auswählen
4. Credentials neu verbinden (OpenAI, Google Sheets)

## Wichtige Hinweise (Sicherheit)

- **Keine Secrets committen** (keine Tokens/Keys in Dateien).
- Credentials gehören in n8n: **Settings → Credentials**
- Für GitHub: Secrets in **Repo Settings → Secrets and variables**

## Empfohlene Repo-Konventionen

- Branches: `feature/...`, `fix/...`, `chore/...`
- Commits: `feat: ...`, `fix: ...`, `chore: ...`

## Lizenz

Dieses Projekt ist unter der MIT-Lizenz lizenziert. Weitere Informationen
findest du in der Datei [LICENSE](LICENSE).
