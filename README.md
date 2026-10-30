# UiPath Labs Setup

A small MkDocs site that walks workshop participants through setting up their
**UiPath Labs** environment: the VM, the workshop account, and the tenant. English and Simplified Chinese.

## Structure

| Path | Purpose |
|------|---------|
| `docs/*.md` | English pages, one per tab |
| `docs/*.zh.md` | Simplified Chinese pages, served under `/zh/` |
| `docs/images/` | Screenshots (no personal usernames or internal URLs) |
| `docs/stylesheets/extra.css`, `docs/javascripts/extra.js` | Shared styles and scripts, copied from the course |
| `hooks/` | MkDocs hooks: two-column shorthand, emoji-free table of contents |
| `main.py` | Environment values (organization, tenant, URLs) for the pages |
| `mkdocs.yml` | Site config, navigation, and languages |
| `Master/` | Shared authoring rules |

## Local preview

```bash
pip install -r requirements.txt
COURSE_ENV=prod mkdocs serve      # http://127.0.0.1:8000/UiPathLabsSetup/
COURSE_ENV=prod mkdocs build      # release-equivalent check
```

## Changing the environment

The organization, tenant, and URLs come from the `prod` profile in `main.py`.
Change them there, not in the pages.

## Publishing to GitHub

The deploy workflow (`.github/workflows/deploy.yml`) runs `mkdocs gh-deploy` on
every push to `main`, which creates the `gh-pages` branch. Then turn on GitHub
Pages for that branch.

```bash
gh repo create madapopescu24/UiPathLabsSetup --public --source=. --push
gh api -X POST repos/madapopescu24/UiPathLabsSetup/pages -f "source[branch]=gh-pages" -f "source[path]=/"
```
