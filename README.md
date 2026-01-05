# Fancy Agents

A curated agent configuration for OpenCode and Claude Code with strict behavioral guidelines and powerful MCP integrations.

## What's Inside

### AGENTS.md
Comprehensive system prompt enforcing:
- **Documentation-first workflow** with mandatory verification
- **Plan → Approval → Execute** pattern for all operations
- **Grounding & citations** for external information
- **Safety & privacy** guardrails
- **Quality gates** for testing and code changes
- Provider-neutral patterns for OpenCode and Claude Code

### .mcp.json
Curated MCP server configuration:
- **sequential-thinking** - Enhanced reasoning capabilities
- **context7** - Multi-source documentation lookup

## Usage

1. **OpenCode/Claude Code**: Place `AGENTS.md` at your repository root to enforce agent behavior
2. **MCP Setup**: Configure `.mcp.json` with your environment variables:
   - `CONTEXT7_API_KEY` for Context7
   - `GITHUB_TOKEN` for GitHub integration

## Key Features

- Zero-tolerance enforcement for critical workflows
- Mandatory documentation verification before API/library use
- Explicit approval gates for all tool usage
- Privacy-first approach with PII/secrets protection
- Timeboxing and retry limits to prevent runaway operations
- Cross-provider compatibility (OpenCode + Claude Code)

## Structure

```
.
├── AGENTS.md       # Agent behavior enforcement
├── .mcp.json       # MCP server configuration
└── README.md       # This file
```

---

Built for reliable, auditable, and safe agent operations.
