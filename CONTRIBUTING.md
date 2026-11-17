# Contributing

Thanks for contributing to `MonitorDeployPilot`.

Documentation follows the [QuantStrategyLab documentation style guide](https://github.com/QuantStrategyLab/.github/blob/main/docs/STYLE_GUIDE.md).

## Workflow

1. Branch from `origin/main` using a short prefix such as `docs/`, `feat/`, `fix/`, or `chore/`.
2. Run the local documentation check before pushing (with a sibling checkout of `QuantStrategyLab/.github` at the `policy-revision` configured in `.github/workflows/docs-check.yml`):

```bash
git clone https://github.com/QuantStrategyLab/.github ../.github
git -C ../.github checkout b4966bdd8780cad3ae5154ae50d8b98259a16dc6
python3 ../.github/scripts/check_style.py --root . --phase 2
```

3. Use English Conventional Commits with headers at most 72 characters, and fill in `.github/pull_request_template.md`.

## Security

See [SECURITY.md](SECURITY.md). Do not open public issues for security vulnerabilities or commit real Azure/GCP identifiers.
