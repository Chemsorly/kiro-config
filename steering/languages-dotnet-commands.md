# Command Standardization
## Purpose
Defines the exact command format to use when the agent intends to execute these common operations. This ensures consistency and minimizes context usage through minimal verbosity.

## Instructions
- ALWAYS check this list before executing any command listed here (ID: COMMANDS_CHECK_STANDARD)
- If you intend to use a command listed here, use EXACTLY the specified format (ID: COMMANDS_USE_EXACT_FORMAT)
- Use minimal verbosity options by default to reduce context usage (ID: COMMANDS_MINIMAL_VERBOSITY)
- Only use verbose options when explicitly needed for debugging or troubleshooting (ID: COMMANDS_VERBOSE_WHEN_NEEDED)
- Commands not listed here can be used freely with appropriate flags as needed (ID: COMMANDS_UNLISTED_FLEXIBLE)

## Standardized Commands

### .NET Build & Test
```powershell
# Build
dotnet build

# Test on Windows
dotnet test

# Test on Linux
docker run --rm -v "${PWD}:/app" -w /app mcr.microsoft.com/dotnet/sdk:10.0 dotnet test
```
(ID: COMMANDS_DOTNET_RUN)

## User-Requested Variations
If the user explicitly requests a different format or additional flags:
1. Use the user's requested format
2. Optionally note in scratchpad.md if it's a common variation worth standardizing
3. Continue using the standardized version for future executions unless told otherwise

## Validation Checklist
Before executing any command:
- [ ] Is this command in the standardization list?
- [ ] If yes, am I using the exact standardized format?
- [ ] If user requested specific flags, am I using their format?

## Priority
Critical

## Error Handling
- If uncertain whether a command should be standardized, use the most common/simple form
- Document frequently used variations as candidates for adding to this list