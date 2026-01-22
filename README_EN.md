# n8n Workflow: ICP → SEO/GAIO Keywords → Google Sheets

This repository versions n8n workflows as JSON files.

![n8n](https://img.shields.io/badge/n8n-FF6C37?style=for-the-badge&logo=n8n&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)

---

## Workflow Architecture

![ICP → SEO/GAIO Keyword Automation](icp-seo-gaio-workflow.png)

---

## Contents

- `n8n/workflows/` – exported n8n workflows (JSON)
- optional: `docs/` – additional documentation / screenshots

---

## Workflow: ICP → SEO/GAIO Keywords → Google Sheets

### Purpose

- Accepts ICP data via a form (Form Trigger).
- Generates **exactly 20 SEO/GAIO keywords** (short-head & long-tail) using OpenAI.
- Writes **one row per keyword** to Google Sheets.

---

### Input (Form Fields)

- `branche`
- `target_role`
- `age`
- `target_goal`
- `target_pain`
- `target_land`
- `language`

---

### Output (Google Sheets – one row per keyword)

- Timestamp
- Industry
- Target role
- Age
- Target audience goals
- Target audience pain points
- Target audience country/region
- Keyword language
- Keyword (overall)
- Short-head (optional)
- Long-tail (optional)

---

## Import into n8n

1. Open n8n
2. Workflows → **Import from File**
3. Select the JSON file from `n8n/workflows/`
4. Reconnect credentials (OpenAI, Google Sheets)

---

## Important Notes (Security)

- **Do not commit secrets** (no tokens/keys in files).
- Credentials belong in n8n: **Settings → Credentials**
- For GitHub: use **Repo Settings → Secrets and variables**

---

## Recommended Repository Conventions

- Branches: `feature/...`, `fix/...`, `chore/...`
- Commits: `feat: ...`, `fix: ...`, `chore: ...`

---

## License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.
