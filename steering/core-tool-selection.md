# Tool Selection
## Purpose
Defines which tool to use for different tasks to avoid decision conflicts and redundancy.

## Instructions
- Context7: Official documentation, NuGet packages, popular frameworks, library code examples (ID: TOOL_CONTEXT7_SCOPE)
- Web-search: New concepts, troubleshooting, alternatives, version comparisons (ID: TOOL_WEB_SCOPE)
- File operations: Code changes, reading existing code, testing (ID: TOOL_FILE_SCOPE)
- Sequential thinking: Complex problems, multi-step analysis, planning (ID: TOOL_THINKING_SCOPE)

## Decision Matrix
1. **Package/Library Research**: Context7 → Web-search (if Context7 insufficient)
2. **Documentation Lookup**: Context7 → Web-search → Official docs
3. **Implementation**: File operations → Testing → Validation
4. **Troubleshooting**: Sequential thinking → Context7/Web-search → File operations

## External Tools and MCP
- If you need more tools, you can ask for more. Do research for appropiate options (ID: TOOL_REQUEST_MORE). 
- If asking for a new Tool, only consider `https://hub.docker.com/u/mcp` as a source. Use the `web-search` tool to scan the site (ID: TOOL_MCP_ALLOWED_SOURCE)
- Context7 is approved for library documentation and code examples lookup (ID: TOOL_CONTEXT7_APPROVED)

## Priority
High

## Error Handling
- If Context7 fails, fallback to web-search immediately
- If web-search fails, proceed with available information and note limitation
- If a tool request has been denied, provide a fallback solution or a different MCP implementation. Add the denied request to this file and do not ask for it again