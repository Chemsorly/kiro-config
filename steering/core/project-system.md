# Project System Rules
## Purpose
Core workflow and mode system for task execution control.

## Instructions
- Maintain project files: memories.md, lessons-learned.md, scratchpad.md (ID: PROJECT_MAINTAIN_FILES)
- ALWAYS use .kiro/steering/project/scratchpad.md - never create temporary scratchpad files elsewhere (ID: PROJECT_SCRATCHPAD_LOCATION)
- ALWAYS update scratchpad.md before starting any multi-step task (ID: PROJECT_MANDATORY_SCRATCHPAD)
- Use scratchpad for task tracking, progress updates, and status management (ID: PROJECT_SCRATCHPAD_TRACKING)
- Use sequential-thinking for complex problems (ID: PROJECT_USE_THINKING)
- Follow workflows: research-workflow → implementation-workflow → debugging-workflow (ID: PROJECT_FOLLOW_WORKFLOWS)
- Check acceptance criteria after task completion (ID: PROJECT_CHECK_ACCEPTANCE)
- Update lessons-learned when learning occurs (ID: PROJECT_UPDATE_LESSONS)
- Ask questions if unsure, provide confidence value for everything (ID: PROJECT_CONFIDENCE_TRACKING)
- Keep all code comments, add descriptive inline comments for long-term memory (ID: PROJECT_PRESERVE_COMMENTS)
- Follow established patterns from memories for context (ID: PROJECT_FOLLOW_PATTERNS)

## Mode System

### Plan Mode (trigger: "plan")
1. Repeat the instructions listed above and follow them.
2. MANDATORY: Update scratchpad.md with session details:
```
# Mode: PLAN 🎯
Current Task: [specific task from user input]
Understanding: [requirements and constraints]
Questions: [numbered list, minimum 3]
Confidence: [percentage based on unknowns]
Next Steps: [bullet points]
```
3. Generate clarifying questions until 95%+ confidence
4. Update scratchpad with each response and confidence change
5. Track all decisions and reasoning in scratchpad

### Agent Mode (trigger: "agent")
**Activation Requirements:**
- Confidence ≥ 95%
- All questions answered
- Tasks defined and tracked in scratchpad
- No blocking issues
- Scratchpad updated with current status

**Pre-Activation Checklist:**
1. Repeat the instructions listed above and follow them.
2. Verify all dependencies are understood
3. Confirm implementation approach is clear
4. Check acceptance criteria are achievable
5. Validate no conflicting requirements exist
6. MANDATORY: Update scratchpad with "READY FOR AGENT MODE" status
7. Create task breakdown with status tracking in scratchpad

**During Agent Mode:**
- Update scratchpad after each major step completion
- Track progress with status markers: [X], [-], [ ], [!], [?]
- Document decisions and changes in scratchpad
- Maintain confidence levels and blockers in scratchpad

## Task Management

### Scratchpad Format
```
Current Phase: [PHASE-X]
Mode Context: [FROM_MODE_SYSTEM]
Status: [Active/Planning/Review]
Confidence: [percentage]
Last Updated: [version]

Tasks:
[ID-001] Description
Status: [X/[-]/[ ]/[!]/[?]] Priority: [High/Medium/Low]
Dependencies: [blockers]
Progress Notes: [version] details
```

### Status Markers
- `[X]` Completed
- `[-]` In Progress
- `[ ]` Planned
- `[!]` Blocked
- `[?]` Needs Review

## Documentation Protocol

### Memories Format
- `[Version] Development:` Exhaustive description of changes, decisions, implementation details, outcomes
- `[Version] Manual Update:` (when user uses "mems" keyword) Planning discussions, requirements, strategic decisions

### Lessons Learned Format
- Format: `Category: Issue → Solution → Impact`
- Categories: Component Development, Error Resolution, Performance, Security, Accessibility, Code Organization, Testing

## Mode Types
1. **Implementation**: New features - Plan → 95% confidence → Agent
2. **Bug Fix**: Issue resolution - Plan → Chain of thought → Agent

## Escape Hatches (Stop Conditions)

### Mandatory Stops - ALWAYS halt and report:
- Confidence < 95% → STOP, list unknowns, ask clarifying questions (ID: ESCAPE_LOW_CONFIDENCE)
- Acceptance criteria cannot be met → STOP, explain blockers, propose alternatives (ID: ESCAPE_ACCEPTANCE_BLOCKED)
- Breaking changes required → STOP, get explicit user approval (ID: ESCAPE_BREAKING_CHANGES)
- Tests failing after changes → STOP, enter debug mode, fix before proceeding (ID: ESCAPE_TEST_FAILURES)
- Conflicting requirements detected → STOP, document conflict, request resolution (ID: ESCAPE_REQUIREMENT_CONFLICT)

### Conditional Stops - Halt if condition met:
- Missing dependencies or unclear architecture → STOP, research or ask (ID: ESCAPE_MISSING_DEPENDENCIES)
- Security concerns identified → STOP, document risk, get approval (ID: ESCAPE_SECURITY_CONCERNS)
- Cross-platform compatibility uncertain → STOP, verify approach (ID: ESCAPE_PLATFORM_UNCERTAINTY)
- Package evaluation < 90% confidence → STOP, find alternatives or implement manually (ID: ESCAPE_LOW_PACKAGE_CONFIDENCE)

### Output Requirements for All Stops:
```
🛑 STOP CONDITION TRIGGERED
Reason: [escape hatch ID and description]
Confidence: [current %]
Blockers: [numbered list]
Questions: [what needs clarification]
Proposed Solutions: [alternatives if any]
```

## Time Management
- When determining the current time, use appropriate system commands for the platform (ID: PROJECT_TIME_GET_CURRENT)
- When timestamps are needed for logging or documentation, use ISO format (ID: PROJECT_TIME_ISO_FORMAT)
- When comparing times or calculating durations, ensure consistent timezone handling (ID: PROJECT_TIME_CONSISTENT_TIMEZONE)
- For time-sensitive operations, always verify the current time before proceeding (ID: PROJECT_TIME_VERIFY_BEFORE_ACTION)

## Memory Management
- Create topic-based memory files when memories.md exceeds 500 lines: memories-testing.md, memories-refactoring.md, memories-features.md (ID: PROJECT_MEMORY_TOPIC_BASED_SPLIT)
- Keep the topic-based memory files in a subfolder `.kiro/steering/memories` (ID: PROJECT_MEMORY_TOPIC_SUBFOLDER)
- Cross-reference related memories using #tags and @file-references (ID: PROJECT_MEMORY_CROSS_REFERENCE)
- Maintain index in memories.md with links to topic files (ID: PROJECT_MEMORY_MAINTAIN_INDEX)

## Priority
Critical

## Error Handling
- Always provide fallback solutions
- Document lessons learned for future prevention
- Update confidence levels after errors
- If system commands fail, note the issue and continue with available information