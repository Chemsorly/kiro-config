# .NET Core Rules
## Purpose
.NET-specific overrides and requirements for the core workflows.

## Instructions
- Follow Microsoft C# coding conventions (ID: DOTNET_CONVENTIONS)
- Apply DRY, SOLID, KISS principles (ID: DOTNET_PRINCIPLES)
- Use Context7 for NuGet packages, official .NET libraries, popular frameworks (Entity Framework, ASP.NET, etc.) (ID: DOTNET_CONTEXT7_SCOPE)
- Skip web-search for basic concepts: LINQ, async/await, basic C# syntax, common .NET types (ID: DOTNET_SKIP_BASIC)
- Always search for: new frameworks, complex algorithms, security implementations, performance optimizations and best practices (ID: DOTNET_ALWAYS_SEARCH)
- Consider checking documentation before using tools or responding (ID: DOTNET_CHECK_DOCUMENTATION)
- When checking documentation, always print the link to web-search being used (ID: DOTNET_PRINT_WEB_RESULT)
- Valid resources: `https://learn.microsoft.com/en-us/dotnet/`, `https://stackoverflow.com/`, `https://github.com/` (ID: DOTNET_VALID_RESOURCES)

## Package Evaluation
- Follow package evaluation criteria defined in packages.rule.md (ID: DOTNET_USE_PACKAGE_RULES)

## Priority
Medium

## Error Handling
- If no suitable package found, implement solution manually
- Document package evaluation decisions