# Debugging Workflow
## Purpose
Defines the sequence for debugging issues and failures.

## Instructions
- Step 1: Use sequential thinking for complex problem analysis (ID: DEBUG_THINK_FIRST)
- Step 2: Use visual testing (screenshots) for UI issues using playwright in docker (ID: DEBUG_VISUAL_UI)
- Step 3: Research error patterns using Context7/web-search (ID: DEBUG_RESEARCH_ERRORS)
- Step 4: Implement fixes using file operations (ID: DEBUG_IMPLEMENT_FIX)
- Step 5: Verify fix with comprehensive testing, use acceptance criteria. (ID: DEBUG_VERIFY_FIX)
- Step 6: Update lessons-learned to prevent recurrence (ID: DEBUG_DOCUMENT_LESSON)

## Workflow Chain
Sequential thinking → Visual testing (if UI) → Research → Fix → Verify → Document

## Iterative Development Support
- Allow returning to implementation workflow after debugging (ID: DEBUG_RETURN_TO_IMPLEMENTATION)
- Support debugging multiple issues in parallel with context tracking (ID: DEBUG_PARALLEL_ISSUES)
- Enable research workflow integration for complex debugging scenarios (ID: DEBUG_RESEARCH_INTEGRATION)
- Allow partial debugging with documented workarounds (ID: DEBUG_PARTIAL_RESOLUTION)

## Priority
Medium

## Error Handling
- If visual testing reveals unexpected behavior, investigate thoroughly
- If fix doesn't work, return to analysis step
- Always document root cause and solution