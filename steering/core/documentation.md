# Documentation
## Purpose
Defines documentation standards, visual aids, and knowledge capture requirements.

## Instructions
- Use Mermaid diagrams for architecture, data flow, and sequence diagrams (ID: DOCUMENTATION_USE_MERMAID)
- Include diagrams for complex features: architecture overview, data flow, state transitions (ID: DOCUMENTATION_COMPLEX_FEATURES_DIAGRAMS)
- Document design decisions with rationale in implementation docs (ID: DOCUMENTATION_DESIGN_DECISIONS)
- Create standalone design documents for major features before implementation (ID: DOCUMENTATION_DESIGN_FIRST)
- Include code examples in documentation for clarity (ID: DOCUMENTATION_CODE_EXAMPLES)
- Use tables for component responsibilities, comparisons, and specifications (ID: DOCUMENTATION_USE_TABLES)

## Mermaid Diagram Types
- **Architecture**: `graph TB` for component relationships and dependencies (ID: DOCUMENTATION_MERMAID_ARCHITECTURE)
- **Data Flow**: `sequenceDiagram` for interaction between components (ID: DOCUMENTATION_MERMAID_SEQUENCE)
- **State Machines**: `stateDiagram-v2` for status transitions (ID: DOCUMENTATION_MERMAID_STATE)
- **Entity Relationships**: `erDiagram` for data models (ID: DOCUMENTATION_MERMAID_ER)

## Documentation Structure
Major feature documentation should include:
1. Overview (current state, target state, requirements)
2. Architecture diagram with component responsibilities
3. Component details with code structure
4. Data flow diagrams (sequence diagrams)
5. Implementation steps (phased approach)
6. Testing strategy
7. Migration path (if breaking changes)
8. Performance and security considerations
9. Q&A section for design decisions

## When to Create Documentation
- **Major Features**: Create design doc before implementation (ID: DOCUMENTATION_MAJOR_FEATURES)
- **Architecture Changes**: Document before and after state (ID: DOCUMENTATION_ARCHITECTURE_CHANGES)
- **Complex Algorithms**: Include flowcharts or pseudocode (ID: DOCUMENTATION_COMPLEX_ALGORITHMS)
- **API Changes**: Document interface changes with examples (ID: DOCUMENTATION_API_CHANGES)

## Priority
Medium

## Error Handling
- If diagrams become too complex, split into multiple focused diagrams
- If Mermaid syntax errors occur, validate at mermaid.live before committing
- Document any diagram rendering issues in the file itself