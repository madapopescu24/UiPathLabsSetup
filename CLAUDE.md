# CLAUDE.md — UiPath Labs Setup

Read automatically every Claude Code session in this repo. Apply all rules below.

## Project purpose

A GitHub Pages–hosted MkDocs site that walks workshop participants through
**setting up their UiPath Labs environment**, and nothing else:

1. **Before You Start** — the VM details and the workshop account details they receive.
2. **Connect to Your VM** — Remote Desktop (recommended) and Azure Bastion tabs, clipboard check.
3. **Sign In** — UiPath sign-in with the workshop account, check that both workshop tenants are in the Tenant picker.
4. **Troubleshooting** — symptom → cause → fix for the steps above.

It's a companion to the workshop courses (for example *UiPath Agentic Testing with
Coding Agents*), which link here for setup. **Scope is deliberately narrow:** no
exercise content, no product lessons. Keep anything workshop-specific (a scenario,
a solution name, test data) out of these pages.

## Rules

- **Environment values come from `main.py`** (mkdocs-macros): `{{ training_url }}`,
  `{{ training_authority }}`, `{{ training_org }}`, `{{ training_tenant }}`, `{{ agentic_tenant }}`,
  `{{ env_label }}`. Never hardcode a URL, organization, or tenant in a page.
  The only profile is `prod`: cloud.uipath.com/tpenlabs, tenants `AgenticTestingWorkshop` (`training_tenant`) and `AgenticWorkshop` (`agentic_tenant`).
- **No staging references**, no personal usernames, no internal URLs (Bastion host
  names, VM IDs), and no screenshots that show them, faces, or real names.
- **Never put passwords or credentials in pages or prompts.**
- **Two languages:** English `docs/<page>.md`, Simplified Chinese `docs/<page>.zh.md`
  (`mkdocs-static-i18n`, suffix structure, Chinese under `/zh/`). When you change an
  English page, make the same change in its `.zh.md`, with the same headings in the
  same order. Every Chinese heading ends with the English anchor
  (`## 🔌 选择连接方式 { #choose-how-to-connect }`). Chinese tab
  names are `nav_translations` in `mkdocs.yml`. Keep code blocks, prompts, UI labels,
  and product names in English.
- **Style:** same as the course. Second person, short sentences. Orange `eyebrow`
  label, an emoji in every heading. Prefer the components in
  `docs/stylesheets/extra.css` (`feature-grid`, `circles`, `fix-grid`, `link-grid`)
  over tables. Fenced code blocks with a language. Each step page ends with a
  `!!! success` check. See `Master/` for the shared authoring rules.

## Local preview

```bash
pip install -r requirements.txt
COURSE_ENV=prod mkdocs serve      # http://127.0.0.1:8000/UiPathLabsSetup/
COURSE_ENV=prod mkdocs build      # release-equivalent check, run before committing
```
