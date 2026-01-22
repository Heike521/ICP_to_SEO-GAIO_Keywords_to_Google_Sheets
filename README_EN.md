# n8n Workflow: ICP → SEO/GAIO Keywords → Google Sheets

This repository versions n8n workflows as JSON files.

## Contents

- `n8n/workflows/` – exported n8n workflows (JSON)
- optional: `docs/` – additional documentation / screenshots

## Workflow: ICP → SEO/GAIO Keywords → Google Sheets

### Purpose

- Accepts ICP data via a form (Form Trigger).
- Generates **exactly 20 SEO/GAIO keywords** (short-head & long-tail) using OpenAI.
- Writes **one row per keyword** to Google Sheets.

### Input (Form Fields)

- `branche`
- `target_role`
- `age`
- `target_goal`
- `target_pain`
- `target_land`
- `language`

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

## Import into n8n

1. Open n8n
2. Workflows → **Import from File**
3. Select the JSON file from `n8n/workflows/`
4. Reconnect credentials (OpenAI, Google Sheets)

## Important Notes (Security)

- **Do not commit secrets** (no tokens/keys in files).
- Credentials belong in n8n: **Settings → Credentials**
- For GitHub: use **Repo Settings → Secrets and variables**

## Recommended Repository Conventions

- Branches: `feature/...`, `fix/...`, `chore/...`
- Commits: `feat: ...`, `fix: ...`, `chore: ...`

## License

This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.
