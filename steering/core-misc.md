# Miscellaneous Rules
## Purpose
General development guidelines and constraints that don't fit into other rule categories.

## Instructions
- Do not call system specific binaries (cmd, powershell, bash) or third party tools (7z) (ID: NO_SYSTEM_BINARIES)
- Use no logging unless debugging (ID: MINIMAL_LOGGING)

## Priority
High

## Error Handling
- If system binaries are needed, use abstraction layers or dependency injection
- If extensive logging is required, document the debugging purpose