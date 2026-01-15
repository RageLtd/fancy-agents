# Fancy Agents

A curated agent configuration for Claude Code with strict behavioral guidelines and powerful plugin integrations.

## Quick Start

### Option 1: Use as GitHub Template

1. Click **"Use this template"** on GitHub to create a new repository
2. Clone your new repository
3. Run the setup script:
   ```bash
   # macOS/Linux
   ./scripts/setup.sh

   # Windows (PowerShell)
   .\scripts\setup.ps1
   ```
4. Restart Claude Code to pick up the new marketplace and plugins

### Option 2: Download and Extract

1. Download the repository as a ZIP file
2. Extract the contents to your project root
3. Run the setup script (see above)
4. Restart Claude Code

## What's Inside

### Agent Configuration

**AGENTS.md** - Comprehensive system prompt enforcing:
- **Documentation-first workflow** with mandatory verification
- **Plan → Approval → Execute** pattern for all operations
- **Grounding & citations** for external information
- **Safety & privacy** guardrails
- **Quality gates** for testing and code changes

### Claude Code Plugins

**`.claude/settings.json`** - Pre-configured plugins from the official marketplace:
- **context7** - Multi-source documentation lookup
- **feature-dev** - Guided feature development workflow
- **code-review** - Multi-aspect code review
- **pr-review-toolkit** - Comprehensive PR review agents
- **typescript-lsp** - TypeScript language server integration
- **rust-analyzer-lsp** - Rust language server integration
- **code-simplifier** - Code clarity and maintainability
- **security-guidance** - Security best practices
- **plugin-dev** - Plugin development tools
- **atlassian** - Jira/Confluence integration
- **Notion** - Notion workspace integration

### Setup Scripts

**`scripts/setup.sh`** (macOS/Linux) and **`scripts/setup.ps1`** (Windows):
- Install TypeScript language server
- Install Rust Analyzer
- Add the [RageLtd/claude-mem](https://github.com/RageLtd/claude-mem) plugin marketplace

## Structure

```
.
├── .claude/
│   └── settings.json    # Plugin configuration
├── scripts/
│   ├── setup.sh         # macOS/Linux setup
│   └── setup.ps1        # Windows setup
├── AGENTS.md            # Agent behavior enforcement
└── README.md            # This file
```

## Requirements

- [Claude Code](https://claude.ai/code) CLI installed
- Node.js (for TypeScript LSP)
- Rust toolchain (optional, for Rust Analyzer)
- Git (for marketplace installation)

## Post-Setup

After running the setup script:

1. **Restart Claude Code** to load the new marketplace
2. **Run `/plugins`** to see available plugins from RageLtd/claude-mem
3. **Enable additional plugins** as needed via Claude Code settings

Some plugins require additional configuration:
- **atlassian** - Requires Atlassian account authentication
- **Notion** - Requires Notion workspace authorization

---

Built for reliable, auditable, and safe agent operations.
