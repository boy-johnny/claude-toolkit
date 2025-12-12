# Claude Toolkit

A personal Claude Code plugin marketplace for streamlined development workflows.

## 🚀 Quick Start

### Installation

```bash
# In Claude Code, add this marketplace
/plugin marketplace add /Users/captrong/Project/App/Extensions/claude-code

# Install all plugins
/plugin install feature-develop@Dev-toolkit
/plugin install commit-workflow@Dev-toolkit
/plugin install debug-toolkit@Dev-toolkit
/plugin install design-studio@Dev-toolkit

# Verify installation
/help
```

## 📦 Plugins

### 1. Feature Develop

Guided feature development with systematic codebase exploration, architecture design, and quality review.

**Commands:**
- `/feature [description]` - Start guided feature development

**Agents:**
- `code-explorer` - Traces execution paths and maps architecture
- `code-architect` - Designs implementation blueprints
- `code-reviewer` - Reviews for bugs and quality issues

### 2. Commit Workflow

Streamline git operations with auto-commits, PR creation, and branch cleanup.

**Commands:**
- `/commit` - Create a commit with auto-generated message
- `/commit-push-pr` - Commit, push, and create PR in one workflow
- `/clean-gone` - Clean up deleted remote branches locally

### 3. Debug Toolkit

Systematic debugging with bug hunting, error analysis, and trace logging.

**Commands:**
- `/debug [description]` - Full debugging workflow
- `/trace [target]` - Trace execution flow through code
- `/diagnose [issue]` - Quick diagnostic for rapid triage

**Agents:**
- `bug-hunter` - Hunts bugs by tracing code paths
- `error-analyzer` - Deep analysis for root cause identification

**Skills:**
- `debugging` - Auto-activates for errors and bugs

### 4. Design Studio

Create distinctive, production-grade frontend interfaces.

**Commands:**
- `/design [description]` - Create beautiful frontend interfaces

**Skills:**
- `frontend-design` - Auto-activates for frontend work

## 📁 Structure

```
claude-code/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace manifest
├── README.md                      # This file
│
├── feature-develop/               # Feature development plugin
│   ├── .claude-plugin/plugin.json
│   ├── commands/feature.md
│   ├── agents/
│   │   ├── code-explorer.md
│   │   ├── code-architect.md
│   │   └── code-reviewer.md
│   └── README.md
│
├── commit-workflow/               # Git workflow plugin
│   ├── .claude-plugin/plugin.json
│   ├── commands/
│   │   ├── commit.md
│   │   ├── commit-push-pr.md
│   │   └── clean-gone.md
│   └── README.md
│
├── debug-toolkit/                 # Debugging plugin
│   ├── .claude-plugin/plugin.json
│   ├── commands/
│   │   ├── debug.md
│   │   ├── trace.md
│   │   └── diagnose.md
│   ├── agents/
│   │   ├── bug-hunter.md
│   │   └── error-analyzer.md
│   ├── skills/debugging/SKILL.md
│   └── README.md
│
└── design-studio/                 # Frontend design plugin
    ├── .claude-plugin/plugin.json
    ├── commands/design.md
    ├── skills/frontend-design/SKILL.md
    └── README.md
```

## 🔧 Usage Examples

### Feature Development
```bash
/feature Add user authentication with OAuth2
/feature Implement search functionality for products
/feature Create export to PDF feature
```

### Git Workflow
```bash
# Quick commit during development
/commit

# Ready to create PR
/commit-push-pr

# Cleanup after merging PRs
/clean-gone
```

### Debugging
```bash
# Full investigation
/debug Login fails with "invalid credentials" error

# Quick diagnosis
/diagnose TypeError: Cannot read property 'id' of undefined

# Understand code flow
/trace handleUserAuthentication function
```

### Frontend Design
```bash
/design Dashboard for a project management tool
/design Landing page for a SaaS product
/design Settings panel with dark mode
```

## 📋 Requirements

- **Claude Code** installed
- **Git** for commit-workflow commands
- **GitHub CLI** (`gh`) for `/commit-push-pr` command

## 🔄 Updating

To update plugins after making changes:

```bash
# Uninstall current version
/plugin uninstall feature-develop@Dev-toolkit

# Reinstall
/plugin install feature-develop@Dev-toolkit
```

## 📚 Resources

- [Claude Code Plugins Documentation](https://code.claude.com/docs/en/plugins)
- [Claude Code Skills Documentation](https://code.claude.com/docs/en/skills)
- [Claude Code Subagents Documentation](https://code.claude.com/docs/en/sub-agents)

## 👤 Author

GOODA

## 📄 License

MIT

## 🗓️ Version

1.0.0
