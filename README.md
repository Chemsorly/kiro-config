# Kiro Config Power

A comprehensive .NET development power for Kiro IDE that provides quality gates, cross-platform testing, project memory management, and structured workflows.

## Features

- **Quality Gates**: Strict acceptance criteria with cross-platform testing
- **Project Memory**: Automatic tracking of decisions, lessons learned, and development history
- **Structured Workflows**: Research → Implementation → Debugging workflows with Plan/Agent modes
- **MCP Integration**: Web search, Context7 documentation, and sequential thinking tools
- **.NET Expertise**: Blazor, C#, NuGet package evaluation, and testing best practices
- **Cross-Platform**: Windows and Linux testing with Docker containers
- **Tool Selection**: Smart tool routing to avoid decision conflicts

## Prerequisites

- **Docker daemon must be running** - The MCP servers (web-search, context7, sequential-thinking) run as local Docker containers and require Docker to be available

## Installation

### From Repository (Recommended)
```bash
# SSH
kiro powers install git+ssh://git@github.com/chemsorly/kiro-config.git

# HTTPS
kiro powers install git+https://github.com/chemsorly/kiro-config.git
```

### From Local Directory (Development)
```bash
kiro powers install ./path/to/kiro-config-power
```

## What Gets Installed

When you install this power, it automatically:

1. **Configures MCP Servers**:
   - Web search (DuckDuckGo)
   - Context7 documentation lookup
   - Sequential thinking for complex problems

2. **Copies Prompt Templates** to `.kiro/prompts/`:
   - Repository analysis prompts
   - Feature development workflows (research, plan, implement, debug)
   - Validation and cleanup prompts

3. **Creates Project Memory Files** (in `.kiro/steering/project/`):
   - `memories.md` - Development history and decisions
   - `lessons-learned.md` - Reusable solutions and patterns
   - `scratchpad.md` - Session tracking and progress (MUST be used for all multi-step tasks)

4. **Loads Comprehensive Steering Rules**:
   - Core rules (acceptance criteria, security, performance, tool selection, project system)
   - .NET specific guidance (Blazor, testing, packages, commands)
   - Structured workflows (research, implementation, debugging)

## Usage

### Workflow Modes

The power operates in two modes for structured task execution:

**Plan Mode** (trigger: "plan")
- Gathers requirements and clarifies unknowns
- Updates scratchpad.md with session details
- Generates clarifying questions until 95%+ confidence
- Tracks all decisions and reasoning

**Agent Mode** (trigger: "agent")
- Activates when confidence ≥ 95%
- Executes implementation with scratchpad tracking
- Updates progress with status markers: [X], [-], [ ], [!], [?]
- Documents decisions and changes continuously

### Automatic Activation
The power activates when you mention relevant keywords:

- `dotnet`, `blazor`, `csharp` - Loads .NET development expertise

### Example Interactions

```
"Let's add some Blazor components"
→ Activates with Blazor lifecycle management and accessibility guidelines

"I need to test this C# service"  
→ Loads cross-platform testing requirements and quality gates

"Help me choose a .NET package"
→ Provides package evaluation criteria and Context7 lookup
```

### Available Prompts

Structured prompts for common development tasks:

**Repository Analysis**
- `/analyze-repository` - Build context for current session

**Feature Development**
- `/research-feature` - Research and plan unknown features
- `/plan-feature` - Plan features with known approaches
- `/implement-feature` - Execute implementation workflow
- `/debug-feature` - Systematic debugging approach

**Validation & Cleanup**
- `/check-acceptance-criteria` - Validate implementation quality
- `/cleanup-after-feature` - Clean up after feature completion

### Tool Selection

Smart routing to avoid decision conflicts:
- **Context7**: Official documentation, NuGet packages, library code examples
- **Web-search**: Search engine tool for research tasks
- **Sequential thinking**: Complex problems, multi-step analysis, planning

### Quality Assurance
Every implementation includes:
- ✅ Compile verification without warnings
- ✅ Cross-platform test execution (Windows/Linux)
- ✅ Coverage analysis with 80-90% thresholds
- ✅ Security and performance considerations
- ✅ Automatic documentation updates

## License

None specified - **Private use only**. This power is not intended for public distribution or marketplace listing.