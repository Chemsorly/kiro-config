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

## Onboarding

When this power activates, I'll help you set up a structured development environment with:

### Prerequisites
- **Docker daemon must be running** - The MCP servers (web-search, context7, sequential-thinking) run as local Docker containers and require Docker to be available

### 1. Load Steering Files
**CRITICAL**: The steering files already exist in this power's `steering/` directory. During onboarding:
- DO NOT create new steering files
- DO NOT use fsWrite or fsAppend to create steering files
- USE `action="readSteering"` with `powerName="kiro-config"` to load existing files
- Example: `kiroPowers(action="readSteering", powerName="kiro-config", steeringFile="core-acceptance-criteria.md")`

The steering files provide all development guidelines, workflows, and quality gates needed for .NET development.

### 2. Project Memory System (User Workspace)
I'll create and maintain project memory files in the USER'S workspace `.kiro/steering/` directory (NOT in the power's directory):
- `project-memories.md` - Development history and decisions
- `project-lessons-learned.md` - Reusable solutions and patterns  
- `project-scratchpad.md` - Current session tracking

These files are specific to the user's project and should be created fresh for each project.

### 3. Prompt Templates
I'll fetch and copy prompt templates from the GitHub repository to your workspace's `.kiro/prompts/` directory:
- Use the `fetch_content` tool from the web-search MCP server to download each file
- Fetch all prompt files using raw GitHub URLs:
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/01%20intro/analyze-repository.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/02%20feature/research-feature.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/02%20feature/plan-feature.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/02%20feature/implement-feature.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/02%20feature/debug-feature.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/03%20validation/check-acceptance-criteria.md`
  - `https://raw.githubusercontent.com/chemsorly/kiro-config/main/prompts/04%20cleanup/cleanup-after-feature.md`
- Create the directory structure (`.kiro/prompts/01 intro/`, `.kiro/prompts/02 feature/`, etc.)
- IMPORTANT: The `fetch_content` tool omits line breaks from the content
- When writing files, add appropriate line breaks between paragraphs and sections to restore proper formatting
- Ensure the files are readable with proper paragraph separation

### 4. Quality Gates
All development follows strict quality criteria:
- Code must compile without warnings
- Tests must pass on both Windows and Linux platforms
- Coverage thresholds: 80-90% depending on complexity
- Cross-platform compatibility validation

### 5. Structured Workflows
I follow established workflows for:
- **Research**: Documentation lookup and package evaluation
- **Implementation**: Quality-first development with testing
- **Debugging**: Systematic problem resolution

### 6. .NET Expertise
Specialized knowledge for:
- **Blazor Server**: Component lifecycle, JavaScript interop, accessibility
- **C# Best Practices**: SOLID principles, async/await patterns, performance
- **Cross-Platform**: Windows/Linux testing with Docker containers
- **Package Management**: NuGet evaluation with confidence scoring

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

## Installation

This power will automatically:
1. Configure MCP servers for web search, documentation, and thinking tools
2. Fetch all prompt template files from GitHub using the `fetch_content` tool and copy them to `.kiro/prompts/` in your workspace
3. Create project memory files in `steering/`
4. Load comprehensive steering rules for .NET development
5. Enable structured workflows and quality gates

Ready to build high-quality .NET applications with comprehensive AI assistance!