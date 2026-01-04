# Acceptance Criteria
## Purpose
Defines quality gates and completion requirements for all tasks.

## Assumptions
1. The IDE is running in Windows, so windows tests can run directly and linux needs to utilize docker.

## Instructions
1. All code must compile without warnings or errors (ID: ACCEPTANCE_COMPILE_CLEAN)
2. All tests must pass on windows platform (ID: ACCEPTANCE_TESTS_PASS_WINDOWS).
3. All tests must pass on linux platform Use docker commands if running tests for linux (ID: ACCEPTANCE_TESTS_PASS_LINUX). 
4. Coverage thresholds must be met per language-specific rules (ID: ACCEPTANCE_COVERAGE_MET)
5. Code must follow language-specific conventions and principles (ID: ACCEPTANCE_CODE_STANDARDS)
6. Documentation must be updated (memories, lessons-learned) (ID: ACCEPTANCE_DOCS_UPDATED)
7. No breaking changes without explicit user approval (ID: ACCEPTANCE_NO_BREAKING_CHANGES)

## Validation Process
1. Compile and build verification
2. Test execution and results validation
3. Coverage analysis and threshold checking
4. Code quality and standards review
5. Documentation completeness check

## Priority
Critical

## Error Handling
- If any criteria fails, stop current task and address the failure
- Document the failure reason and resolution approach
- Re-validate all criteria after fixes