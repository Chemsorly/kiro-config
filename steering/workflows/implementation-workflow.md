---
inclusion: manual
---

# Implementation Workflow
## Purpose
Defines the sequence for implementing features after research is complete.

## Instructions
- Step 1: Code implementation using file operations (ID: IMPL_CODE_FIRST)
- Step 2: Run tests to verify functionality (ID: IMPL_TEST_VERIFY)
- Step 3: Check acceptance criteria for language-specific requirements (ID: IMPL_ACCEPTANCE_CHECK)
- Step 4: Validate coverage and quality metrics (ID: IMPL_COVERAGE_VALIDATE)
- Step 5: Update project documentation (memories, lessons-learned) (ID: IMPL_DOCUMENT)

## Workflow Chain
Code → Test → Acceptance criteria → Coverage validation → Documentation

## Iterative Development Support
- Allow returning to research workflow if implementation reveals knowledge gaps (ID: IMPL_RETURN_TO_RESEARCH)
- Support incremental implementation with partial feature completion (ID: IMPL_INCREMENTAL_DEVELOPMENT)
- Enable context switching between multiple implementation tasks (ID: IMPL_CONTEXT_SWITCHING)
- Allow debugging workflow integration at any step (ID: IMPL_DEBUG_INTEGRATION)

## Priority
Medium

## Error Handling
- If tests fail, fix issues before proceeding
- If acceptance criteria not met, address gaps before completion
- Document any deviations or compromises made