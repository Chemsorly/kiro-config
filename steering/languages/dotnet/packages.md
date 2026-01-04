# NuGet Packages
## Purpose
This rule defines how Kiro should behave when searching for a NuGet package to implement a feature.

## Instructions
- ALWAYS consider checking existing NuGet packages before implementing a new feature (ID: DOTNET_CHECK_NUGET_PACKAGES)
- When considering a package, find alternatives and evaluate if implementing the feature without it would be easier (ID: DOTNET_EVALUATE_NUGET_USEFULNESS)
- Always print the link to the NuGet packages you are evaluating (ID: DOTNET_PRINT_NUGET_RESULT)
- Always print your confidence about the usefulness of the NuGet package (ID: DOTNET_PRINT_NUGET_CONFIDENCE)
- Calculate confidence using: Downloads >1M (+20%), Last update <6mo (+20%), GitHub stars >1K (+15%), Active issues resolution (+15%), Security vulnerabilities (-30%), Maintenance status (+30%) (ID: DOTNET_CONFIDENCE_CRITERIA)
- Only use NuGet packages with a confidence value >90% (ID: DOTNET_USE_NUGET_PACKAGE)
- Valid resources for NuGet packages are `https://nuget.org` and `https://github.com`
- Use Context7 to find comprehensive documentation and code examples for NuGet packages before implementing features (ID: DOTNET_USE_CONTEXT7_PACKAGES)
- When evaluating packages, check Context7 first for official documentation, then fallback to web-search if needed (ID: DOTNET_CONTEXT7_FIRST)

## Priority
High

## Error Handling
- If no valid NuGet package can be found, implement the solution yourself