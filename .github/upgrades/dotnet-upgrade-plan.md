# .NET10.0 (PREVIEW) Upgrade Plan

## Execution Steps

Execute steps below sequentially one by one in the order they are listed.

1. Validate that an .NET10.0 SDK required for this upgrade is installed on the machine and if not, help to get it installed.
2. Ensure that the SDK version specified in global.json files is compatible with the .NET10.0 upgrade.
3. Upgrade Stocks.csproj

## Settings

### Excluded projects

Table below contains projects that do belong to the dependency graph for selected projects and should not be included in the upgrade.

| Project name | Description |
|:-----------------------------------------------|:---------------------------:|


### Aggregate NuGet packages modifications across all projects

NuGet packages used across all selected projects or their dependencies that need version update in projects that reference them.

| Package Name | Current Version | New Version | Description |
|:---------------------------------------------|:---------------:|:-------------------------------:|:--------------------------------------------------------------------|
| Microsoft.Extensions.Hosting |8.0.0 |10.0.0-rc.2.25502.107 | Replace package with the10.0.0-rc runtime package recommended for .NET10 (per analysis). |
| Microsoft.Extensions.Logging.Console |8.0.0 |10.0.0-rc.2.25502.107 | Replace package with the10.0.0-rc runtime package recommended for .NET10 (per analysis). |


### Project upgrade details

This section contains details about each project upgrade and modifications that need to be done in the project.

#### Stocks.csproj modifications

Project properties changes:
 - Target framework should be changed from `net8.0` to `net10.0`

NuGet packages changes:
 - `Microsoft.Extensions.Hosting` should be replaced: `8.0.0` -> `10.0.0-rc.2.25502.107` (*recommended replacement for .NET10*)
 - `Microsoft.Extensions.Logging.Console` should be replaced: `8.0.0` -> `10.0.0-rc.2.25502.107` (*recommended replacement for .NET10*)

Feature upgrades:
 - No automatic code-breaking change instructions were discovered by analysis. After project build, address any compiler errors or API-breaking changes reported.

Other changes:
 - Verify compatibility of `Microsoft.Orleans.Server`8.0.0 with .NET10. If incompatible, plan to update or replace it accordingly.

