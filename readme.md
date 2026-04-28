NuGet Contribution Graph
===

Generates and updates the nuget.json file containing all active nuget packages, their associated repositories and contributors.

> An active nuget package has at least 200 downloads per day in aggregate across the last 5 versions.

The static [nuget.json](nuget.json) file (updated once a month via a [workflow](.github/workflows/nuget.yml)) can be used in shields.io badges.
The workflow updates generated files in a pull request so it can work with protected, PR-only default branches.
The following are generated from the latest version, entirely server-less:

![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.packages&style=social&logo=nuget&label=packages)
![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)

Source:

```
![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.packages&style=social&logo=nuget&label=packages)

![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2Fnuget.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)
```

Additional package owners can be added via [owners.json](owners.json) so that all package stats can be collected for 
the given accounts. Static badges can then be used for those, such as: 

[![NuGet Packages](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2FDevlooped.json&query=%24.summary.packages&style=social&logo=nuget&label=devlooped%20packages)](https://www.nuget.org/profiles/devlooped)
[![Daily Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fgithub.com%2Fdevlooped%2Fnuget%2Fraw%2Frefs%2Fheads%2Fmain%2FDevlooped.json&query=%24.summary.downloads&style=social&logo=nuget&label=daily%20downloads
)](https://www.nuget.org/profiles/devlooped)

## Workflow notes

- The workflow uses the built-in `GITHUB_TOKEN`; no extra bot identity or personal access token is required.
- Generated `*.json` updates are pushed to an automation branch and proposed through a pull request instead of pushing to the default branch directly.
- Static shields.io badges can point at the generated JSON files in this repository; no external SponsorLink endpoint is required.
