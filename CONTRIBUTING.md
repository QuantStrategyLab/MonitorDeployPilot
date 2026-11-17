# Contributing

Thanks for contributing to `MonitorDeployPilot`.

Documentation follows the [QuantStrategyLab documentation style guide](https://github.com/QuantStrategyLab/.github/blob/main/docs/STYLE_GUIDE.md).

## Workflow

1. Branch from `origin/main` using a short prefix such as `docs/`, `feat/`, `fix/`, or `chore/`.
2. Run the local documentation check before pushing:

```bash
python3 ../.github/scripts/check_style.py --root . --phase 2
```

3. Use English Conventional Commits with headers at most 72 characters, and fill in `.github/pull_request_template.md`.

## Security

See [SECURITY.md](SECURITY.md). Do not open public issues for security vulnerabilities or commit real Azure/GCP identifiers.
