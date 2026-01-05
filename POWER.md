---
name: kiro-config
displayName: Kiro Config Power
version: 0.0.1
author: Chemsorly
keywords: [dotnet, blazor, csharp]
description: Comprehensive .NET development with quality gates, cross-platform testing, and project memory management
---

# Kiro Config Power

A comprehensive .NET development power that provides quality gates, cross-platform testing, project memory management, and structured workflows for Blazor and C# projects.

## Steering Files

This power includes comprehensive steering files that guide development. These files are stored in the `steering/` directory and should be accessed using the `readSteering` action when needed.

**IMPORTANT**: During onboarding, DO NOT create these files - they already exist in the power's `steering/` directory. Use `action="readSteering"` with `powerName="kiro-config"` and the appropriate `steeringFile` name to load them.

Available steering files:
- `core-acceptance-criteria.md` - Quality gates and completion requirements
- `core-conversation.md` - Communication and response guidelines
- `core-documentation.md` - Documentation standards
- `core-error-handling.md` - Standardized error handling
- `core-misc.md` - Miscellaneous development guidelines
- `core-performance.md` - Optimization guidelines
- `core-project-system.md` - Workflow and mode system
- `core-rule-hierarchy.md` - Rule precedence and conflict resolution
- `core-security.md` - Security practices
- `core-tool-selection.md` - Tool selection criteria
- `languages-dotnet-blazor.md` - Blazor best practices
- `languages-dotnet-commands.md` - Standardized command formats
- `languages-dotnet-core.md` - .NET coding conventions
- `languages-dotnet-packages.md` - NuGet package evaluation
- `languages-dotnet-testing.md` - Cross-platform testing
- `project-lessons-learned.md` - Reusable solutions and patterns
- `project-memories.md` - Development history and decisions
- `project-scratchpad.md` - Current session tracking
- `workflows-debugging-workflow.md` - Systematic problem resolution
- `workflows-implementation-workflow.md` - Quality-first development
- `workflows-research-workflow.md` - Structured research approach

## Onboarding Checklist

**Complete ALL three tasks below.** Order doesn't matter, but nothing should be skipped.

⚠️ **Skipping any task will result in incomplete power activation and incorrect behavior.**

### Prerequisites Check
- **Docker daemon must be running** - Required for MCP servers (web-search, context7, sequential-thinking)
- **Action**: Verify Docker is available or ask user to confirm before proceeding

---

### Task 1: Load Steering Files (19 total) ☐

**Why this matters**: These files contain quality gates, workflows, and development rules. Skipping any file means missing critical guidance.

**CRITICAL**: 
- Steering files already exist in the power's `steering/` directory
- DO NOT create new steering files with fsWrite/fsAppend
- USE `action="readSteering"` with `powerName="kiro-config"` for each file

**Files to Load:**

**Core Rules (10 files):**
- core-acceptance-criteria.md
- core-conversation.md
- core-documentation.md
- core-error-handling.md
- core-misc.md
- core-performance.md
- core-project-system.md
- core-rule-hierarchy.md
- core-security.md
- core-tool-selection.md

**.NET Language Rules (5 files):**
- languages-dotnet-blazor.md
- languages-dotnet-commands.md
- languages-dotnet-core.md
- languages-dotnet-packages.md
- languages-dotnet-testing.md

**Workflow Rules (3 files):**
- workflows-debugging-workflow.md
- workflows-implementation-workflow.md
- workflows-research-workflow.md

**Tool Call Example:**
```javascript
kiroPowers(action="readSteering", powerName="kiro-config", steeringFile="core-acceptance-criteria.md")
// Repeat for all 19 files
```

**✓ Verify**: Loaded 10 core + 5 dotnet + 3 workflows = 19 total files

---

### Task 2: Create Project Memory Files (3 total) ☐

**Why this matters**: These files track project-specific decisions and lessons, enabling context continuity across sessions.

**IMPORTANT**: Create these in the USER'S workspace at `.kiro/steering/` (NOT in the power's directory)

**Files to Create:**
1. `project-memories.md` - Development history and architectural decisions
2. `project-lessons-learned.md` - Reusable solutions and patterns discovered
3. `project-scratchpad.md` - Current session goals and progress tracking

**Tool Call Example:**
```javascript
fsWrite(path=".kiro/steering/project-memories.md", text="# Project Memories\n\nThis file tracks important development decisions and context.\n\n## Project Overview\n- **Created**: [Date]\n- **Type**: [TBD]\n\n## Key Decisions\n[To be documented]\n")
// Repeat for other 2 files with appropriate headers
```

**✓ Verify**: Created all 3 files in user's `.kiro/steering/` directory

---

### Task 3: Install Prompt Templates (7 total) ☐

**Why this matters**: These templates provide structured workflows for common development tasks.

**Process**:
1. Use `fetch_content` tool (web-search MCP server) to download from GitHub
2. Use `fsWrite` to save in `.kiro/prompts/` (directories created automatically)

⚠️ **CRITICAL**: The `fetch_content` tool removes line breaks. Add proper paragraph separation when writing files.

**Files to Install:**

**GitHub Base**: `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/`

1. `01 intro/analyze-repository.md` → `.kiro/prompts/01 intro/analyze-repository.md`
2. `02 feature/research-feature.md` → `.kiro/prompts/02 feature/research-feature.md`
3. `02 feature/plan-feature.md` → `.kiro/prompts/02 feature/plan-feature.md`
4. `02 feature/implement-feature.md` → `.kiro/prompts/02 feature/implement-feature.md`
5. `02 feature/debug-feature.md` → `.kiro/prompts/02 feature/debug-feature.md`
6. `03 validation/check-acceptance-criteria.md` → `.kiro/prompts/03 validation/check-acceptance-criteria.md`
7. `04 cleanup/cleanup-after-feature.md` → `.kiro/prompts/04 cleanup/cleanup-after-feature.md`

**Tool Call Example:**
```javascript
kiroPowers(action="use", powerName="kiro-config", serverName="web-search", toolName="fetch_content", 
  arguments={"url": "https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/01%20intro/analyze-repository.md"})
// Then write with proper line breaks
fsWrite(path=".kiro/prompts/01 intro/analyze-repository.md", text="[content with line breaks added]")
```

**✓ Verify**: Installed all 7 files with proper formatting (not wall of text)

---

## Final Validation Checklist

⚠️ **CRITICAL CHECKPOINT**: Before declaring onboarding complete, verify ALL items:

- [ ] Loaded 19 steering files (10 core + 5 dotnet + 3 workflows)
- [ ] Created 3 project memory files in `.kiro/steering/`
- [ ] Installed 7 prompt template files in `.kiro/prompts/`
- [ ] Updated project-scratchpad.md with onboarding completion status

**If ANY checkbox is unchecked, onboarding is NOT complete. Return to incomplete tasks.**

---

### Report Completion to User

Once all checkboxes are verified, report:

```
✅ Kiro-Config Power: Onboarding Complete

Successfully completed:
- Loaded 19 steering files (core rules, .NET rules, workflows)
- Created 3 project memory files
- Installed 7 prompt templates

The kiro-config power is now fully operational with:
- Quality gates (no warnings, 80-90% coverage, cross-platform testing)
- Structured workflows (research → implementation → debugging)
- Project memory system (tracking decisions and lessons)
- Blazor & C# expertise with best practices
```

## Available Prompts

Structured prompts for common development tasks:

### Repository Analysis
- `/analyze-repository` - Build context for current session

### Feature Development
- `/research-feature` - Research and plan unknown features
- `/plan-feature` - Plan features with known approaches
- `/implement-feature` - Execute implementation workflow
- `/debug-feature` - Systematic debugging approach

### Validation & Cleanup
- `/check-acceptance-criteria` - Validate implementation quality
- `/cleanup-after-feature` - Clean up after feature completion

## MCP Tools Available

When activated, this power provides access to:
- **Web Search**: Current information lookup and documentation research
- **Context7**: NuGet package documentation and code examples
- **Sequential Thinking**: Complex problem analysis and planning

## Usage Examples

### Automatic Activation
The power activates when you mention relevant keywords:

```
"Let's add some Blazor components"
→ Activates with Blazor-specific guidance and testing requirements

"I need to test this C# service"  
→ Loads cross-platform testing workflows and quality gates

"Help me choose a .NET package"
→ Provides package evaluation criteria and Context7 lookup
```

### Memory Management
I automatically maintain project context:
- Track development decisions in project-memories.md
- Document lessons learned in project-lessons-learned.md for future reference
- Use project-scratchpad.md for session planning and progress

### Quality Assurance
Every implementation includes:
- Compile verification without warnings
- Cross-platform test execution (Windows/Linux)
- Coverage analysis and threshold validation
- Security and performance considerations
- Check core-acceptance-criteria.md for full list

## What Happens After Onboarding

Once onboarding is complete, this power provides:

**Quality Gates**: All development follows strict criteria:
- Code must compile without warnings
- Tests must pass on both Windows and Linux platforms
- Coverage thresholds: 80-90% depending on complexity
- Cross-platform compatibility validation

**Structured Workflows**:
- **Research**: Documentation lookup and package evaluation
- **Implementation**: Quality-first development with testing
- **Debugging**: Systematic problem resolution

**.NET Expertise**:
- **Blazor Server**: Component lifecycle, JavaScript interop, accessibility
- **C# Best Practices**: SOLID principles, async/await patterns, performance
- **Cross-Platform**: Windows/Linux testing with Docker containers
- **Package Management**: NuGet evaluation with confidence scoring

Ready to build high-quality .NET applications with comprehensive AI assistance!