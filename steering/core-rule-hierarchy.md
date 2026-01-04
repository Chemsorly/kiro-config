# Rule Hierarchy
## Purpose
This rule defines how to resolve conflicts when multiple rules apply simultaneously.

## Instructions
- When rules conflict, follow this priority order: Critical > High > Medium > Low (ID: HIERARCHY_PRIORITY_ORDER)
- If same priority rules conflict, follow this hierarchy: conversation.rule.md > acceptance-criteria.rule.md > security.rule.md > performance.rule.md > others (ID: HIERARCHY_SAME_PRIORITY_ORDER)
- Document conflicts in scratchpad.md with resolution reasoning (ID: HIERARCHY_DOCUMENT_CONFLICTS)

## Rule Integration Matrix
- **Security + Performance**: Security takes precedence for credential handling, performance for resource optimization (ID: HIERARCHY_SECURITY_PERFORMANCE)
- **Accessibility + Performance**: Balance accessibility requirements with performance, document trade-offs (ID: HIERARCHY_ACCESSIBILITY_PERFORMANCE)
- **CI/CD + Testing**: CI/CD rules enhance testing rules for cross-platform scenarios (ID: HIERARCHY_CICD_TESTING)
- **Workflow + Project System**: Project system mode requirements override workflow flexibility (ID: HIERARCHY_PROJECT_WORKFLOW)
- **Documentation + All Rules**: Documentation requirements apply to all major changes and complex features (ID: HIERARCHY_DOCUMENTATION_UNIVERSAL)

## Priority
Critical

## Error Handling
- If hierarchy cannot resolve conflict, ask user for clarification
- Continue with most restrictive interpretation when in doubt