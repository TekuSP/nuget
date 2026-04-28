NuGet generated data
===

This repository stores generated NuGet package statistics as checked-in JSON files.

- `nuget.json` is refreshed by `.github/workflows/nuget.yml`
- the workflow runs monthly and can also be triggered manually
- updates are pushed to `automation/nuget-update` and proposed through a pull request
- Mergify approves generated-data PRs and can auto-merge validated Dependabot updates

This fork does not maintain a custom `owners.json` list or external SponsorLink endpoint documentation. It is intended to be a generated-data repository only.
