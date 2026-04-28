NuGet generated data
===

This repository stores generated NuGet package statistics as checked-in JSON files.

- `/home/runner/work/nuget/nuget/nuget.json` is refreshed by `/home/runner/work/nuget/nuget/.github/workflows/nuget.yml`
- the workflow runs monthly and can also be triggered manually
- updates are pushed to `automation/nuget-update` and proposed through a pull request
- Mergify can merge automation PRs after your repository rules allow it

This fork does not maintain a custom `owners.json` list or external SponsorLink endpoint documentation. It is intended to be a generated-data repository only.
