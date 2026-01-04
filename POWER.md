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

## Onboarding

When this power activates, I'll help you set up a structured development environment with:

### Prerequisites
- **Docker daemon must be running** - The MCP servers (web-search, context7, sequential-thinking) run as local Docker containers and require Docker to be available

### 1. Project Memory System
I'll create and maintain project memory files in `.kiro/steering/project/`:
- `memories.md` - Development history and decisions
- `lessons-learned.md` - Reusable solutions and patterns  
- `scratchpad.md` - Current session tracking

### 2. Prompt Templates
I'll copy the existing prompt templates from this power's `prompts/` directory to your workspace's `.kiro/prompts/` directory:
- Copy all files from `prompts/01 intro/` (analyze-repository.md)
- Copy all files from `prompts/02 feature/` (research-feature.md, plan-feature.md, implement-feature.md, debug-feature.md)
- Copy all files from `prompts/03 validation/` (check-acceptance-criteria.md)
- Copy all files from `prompts/04 cleanup/` (cleanup-after-feature.md)
- Preserve the directory structure exactly as it exists in the power

### 3. Quality Gates
All development follows strict quality criteria:
- Code must compile without warnings
- Tests must pass on both Windows and Linux platforms
- Coverage thresholds: 80-90% depending on complexity
- Cross-platform compatibility validation

### 4. Structured Workflows
I follow established workflows for:
- **Research**: Documentation lookup and package evaluation
- **Implementation**: Quality-first development with testing
- **Debugging**: Systematic problem resolution

### 5. .NET Expertise
Specialized knowledge for:
- **Blazor Server**: Component lifecycle, JavaScript interop, accessibility
- **C# Best Practices**: SOLID principles, async/await patterns, performance
- **Cross-Platform**: Windows/Linux testing with Docker containers
- **Package Management**: NuGet evaluation with confidence scoring

## Available Steering Files

### Core Rules
- `acceptance-criteria.md` - Quality gates and completion requirements
- `project-system.md` - Workflow and mode system for task execution
- `security.md` - Security practices and validation requirements
- `performance.md` - Optimization guidelines and resource management
- `error-handling.md` - Standardized error handling across operations

### .NET Specific
- `core.md` - .NET coding conventions and principles
- `blazor.md` - Blazor component lifecycle and best practices
- `testing.md` - Cross-platform testing requirements
- `packages.md` - NuGet package evaluation criteria
- `commands.md` - Standardized command formats

### Workflows
- `research-workflow.md` - Structured approach to investigating solutions
- `implementation-workflow.md` - Quality-first development process
- `debugging-workflow.md` - Systematic problem resolution

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
- Track development decisions in memories.md
- Document lessons learned in lessons-leanred.md for future reference
- Use scratchpad.md for session planning and progress

### Quality Assurance
Every implementation includes:
- Compile verification without warnings
- Cross-platform test execution (Windows/Linux)
- Coverage analysis and threshold validation
- Security and performance considerations
- Check acceptance-criteria.md for full list

## Installation

This power will automatically:
1. Configure MCP servers for web search, documentation, and thinking tools
2. Copy all prompt template files from the power's `prompts/` directory to `.kiro/prompts/` in your workspace (preserving directory structure)
3. Create project memory files in `.kiro/steering/project/`
4. Load comprehensive steering rules for .NET development
5. Enable structured workflows and quality gates

Ready to build high-quality .NET applications with comprehensive AI assistance!