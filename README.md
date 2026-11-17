# MonitorDeployPilot

Isolated example of a reusable GitHub Actions workflow and an Azure Container Apps Jobs deployment adapter.

## Status

Experimental pilot. The workflow uses a manual dispatch trigger, runs only an import check, and has no access to production state, schedules, or trading accounts.

## What this is

A minimal reference repository for testing OIDC-based job deployment workflows in isolation before broader adoption.

## What this is not

It is not a production deployment target, does not connect to broker accounts, and does not manage live infrastructure.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) and [AGENTS.md](AGENTS.md).

## Security

See [SECURITY.md](SECURITY.md). Do not open a public issue for a vulnerability.

## License

MIT License. See [LICENSE](LICENSE).
