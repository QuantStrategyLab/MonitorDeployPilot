# AGENTS.md

Rules for AI assistants and maintainers in `MonitorDeployPilot`. Reusable PR governance lives in `Pigbibi/PrGovernance`.

## What this repository is

Isolated pilot demonstrating a reusable GitHub Actions workflow and an Azure Container Apps Jobs deployment adapter using a manual import-check job with no access to production state or schedules.

## Local checks

```bash
python3 scripts/test_style.py
python3 scripts/check_style.py --phase 2
```

## Naming and documentation

- English is default; `.zh-CN.md` siblings exist only when needed. Use lowercase kebab-case filenames (`README.md`, `AGENTS.md`, `CLAUDE.md`, `SECURITY.md` keep standard casing) and update links on rename.
- Update `README.md` / `README.zh-CN.md` only when user-visible behavior, CLI, or configuration changes; never append PR narration (`this PR`, `remains unchanged`), phase headings, or sections after `## License`.
- Keep working plans, handoffs, and internal audits out of Git.

<!-- repository-files:begin -->
- Public repositories (with `LICENSE`) include `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, and issue/PR templates (underscored filenames: `pull_request_template.md`); private ones require `SECURITY.md`.
- Public `SECURITY.md` covers disclosure only; never mix private rotation procedures into public files.
<!-- repository-files:end -->

## Do not

- Do not connect pilot workflows to production subscriptions, live state stores, credentials, or schedules.
- Do not bypass `pr-governance` or commit internal notes or real identifiers.

<!-- content-boundary:begin -->
- Public material carries no real resource names or accounts: use `gs://<bucket>/...`, `<account-id>`, and synthetic examples.
- Read bucket names, accounts, and hostnames from `vars.*`, env, or protected config; never commit hashes or identifiers that resolve to private objects.
- Judge whether a change is clean by `git diff` and `git ls-files`; `.gitignore` affects untracked files only.
<!-- content-boundary:end -->

## Commits and pull requests

- Use English Conventional Commits (`feat`, `fix`, `docs`, `refactor`, `test`, `chore`, `perf`, `ci`) with headers <= 72 chars; fill `.github/pull_request_template.md` sections (`AI assistance`, `What changed`, `How verified`, `Why`, `Risk`).
- R2 paths require green CI, `ai-review` on the exact head SHA, and one clearing label (`agent-approved` after checks pass, or `owner-approved` only on explicit owner confirmation; never add/remove `owner-approved` yourself).
- Never push directly to `main`, force-push reviewed branches, lower branch protection, or use `gh pr merge --admin`; merge strictly through normal checks.
