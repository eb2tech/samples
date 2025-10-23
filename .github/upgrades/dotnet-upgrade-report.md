# .NET10 Upgrade Report

## Project target framework modifications

| Project name | Old Target Framework | New Target Framework | Commits |
|:-----------------------------------------------|:-----------------------:|:----------------------------:|:---------------------------:|
| Stocks.csproj | net8.0 | net10.0 | a0152030, c9b4df76 |

## NuGet Packages

| Package Name | Old Version | New Version | Commit Id |
|:------------------------------------|:-----------:|:-----------:|:-------------------------------------------|
| Microsoft.Extensions.Hosting |8.0.0 |10.0.0-rc.2.25502.107 |3b6103b5 |
| Microsoft.Extensions.Logging.Console |8.0.0 |10.0.0-rc.2.25502.107 |3b6103b5 |

## All commits

| Commit ID | Description |
|:-----------------------|:-------------------------------------------|
| a0152030 | commit upgrade plan |
| c9b4df76 | Update Stocks.csproj to target .NET10.0 |
|3b6103b5 | Update package versions in Stocks.csproj |

## Project feature upgrades

### Stocks.csproj

- Initial upgrade completed: Target framework updated to net10.0 and NuGet package references for `Microsoft.Extensions.Hosting` and `Microsoft.Extensions.Logging.Console` were updated to `10.0.0-rc.2.25502.107`.

## Next steps

- Build the solution and address any compilation or API-breaking issues.
