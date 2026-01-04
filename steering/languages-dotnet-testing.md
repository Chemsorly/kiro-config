# .NET Testing Rules
## Purpose
.NET-specific testing and coverage requirements.

## Instructions
- Use the command `dotnet test` to test on Windows. (ID: DOTNET_TEST_WINDOWS)
- Use the command `docker run --rm -v "${PWD}:/app" -w /app mcr.microsoft.com/dotnet/sdk:10.0 dotnet test` to test on Linux (ID: DOTNET_TEST_LINUX)
- No compiler warnings or errors (ID: DOTNET_NO_WARNINGS)
- Line coverage targets: Complex business logic (90%), Standard logic (80%), Generated/boilerplate code (60%) (ID: DOTNET_LINE_COVERAGE)
- Branch coverage targets: Critical paths (90%), Standard paths (80%), Error handling (70%) (ID: DOTNET_BRANCH_COVERAGE)
- UI components require visual testing with Playwright screenshots (ID: DOTNET_UI_VISUAL_TESTING)
- Clean up temporary test files after completion (ID: DOTNET_TEST_CLEANUP) 

## Cross-Platform Testing
- All tests must pass on both Windows and Linux platforms (ID: DOTNET_CROSS_PLATFORM_TESTS)
- Use Docker containers for consistent cross-platform testing environments (ID: DOTNET_DOCKER_CONSISTENCY)
- Mock external dependencies (system tools) to ensure platform-agnostic tests (ID: DOTNET_MOCK_DEPENDENCIES)
- Use platform-appropriate commands (/bin/echo vs cmd.exe) in tests (ID: DOTNET_PLATFORM_COMMANDS)
- Handle path differences (forward vs backslash) in cross-platform tests (ID: DOTNET_PATH_HANDLING)
- Test fallback mechanisms when platform-specific tools are unavailable (ID: DOTNET_FALLBACK_TESTING)
- Use persistent containers for complex testing scenarios, avoid --rm flag during debugging (ID: DOTNET_PERSISTENT_CONTAINERS)
- Implement visual testing with Playwright in containerized environments (ID: DOTNET_VISUAL_TESTING_CONTAINERS)

## Coverage Exceptions
- Auto-generated files, simple DTOs, one-line properties can be excluded with justification (ID: DOTNET_COVERAGE_EXCEPTIONS)

## Priority
Critical

## Error Handling
- If coverage below threshold, prioritize adding tests over other tasks
- If tests fail on either platform, fix before proceeding
- Document any coverage exceptions with clear justification
- Document test failures and cross-platform issues in lessons-learned
- Implement proper test retry mechanisms for flaky tests
- Address container and environment setup issues promptly