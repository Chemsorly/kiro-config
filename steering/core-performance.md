# Performance
## Purpose
Defines performance optimization guidelines, monitoring requirements, and resource management strategies.

## Instructions
- Optimize for large directory operations with efficient file system access patterns (ID: PERFORMANCE_LARGE_DIRECTORIES)
- Use thread-safe collections (ConcurrentDictionary) for concurrent access scenarios (ID: PERFORMANCE_THREAD_SAFE_COLLECTIONS)
- Implement automatic cleanup mechanisms for in-memory collections to prevent memory leaks (ID: PERFORMANCE_MEMORY_CLEANUP)
- Use background services with reasonable timeouts (30 minutes) for long-running operations (ID: PERFORMANCE_BACKGROUND_TIMEOUTS)
- Use efficient path normalization for cross-platform file operations (ID: PERFORMANCE_PATH_NORMALIZATION)
- Implement proper disposal patterns (IDisposable, DisposeAsync) for resource cleanup (ID: PERFORMANCE_RESOURCE_DISPOSAL)

## Memory Management
- Use hosted background services with timer-based cleanup for temporary data (ID: PERFORMANCE_TIMER_CLEANUP)
- Clean up temporary test files and resources after completion (ID: PERFORMANCE_TEST_CLEANUP)

## Cross-Platform Performance
- Optimize for both Windows and Linux file system differences (ID: PERFORMANCE_CROSS_PLATFORM_FS)
- Use platform-appropriate path handling and command execution (ID: PERFORMANCE_PLATFORM_COMMANDS)

## Priority
High

## Error Handling
- Document performance issues and solutions in lessons-learned
- Document performance trade-offs and optimization decisions during development