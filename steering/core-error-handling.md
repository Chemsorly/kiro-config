# Error Handling
## Purpose
This rule standardizes error handling across all rules and operations.

## Instructions
- Log all errors to scratchpad.md with timestamp and context (ID: ERROR_LOG_TO_SCRATCHPAD)
- For tool failures: Retry once, then fallback to alternative approach (ID: ERROR_TOOL_RETRY)
- For rule conflicts: Document in scratchpad, apply rule-hierarchy.rule.md (ID: ERROR_RULE_CONFLICT_HANDLING)
- For acceptance criteria failures: Stop current task, fix issue, re-verify all criteria (ID: ERROR_ACCEPTANCE_FAILURE)
- For coverage failures: Add targeted tests, avoid generic tests (ID: ERROR_COVERAGE_FAILURE)

## Priority
High

## Error Recovery
- Always provide fallback solutions
- Document lessons learned for future prevention
- Update confidence levels after errors