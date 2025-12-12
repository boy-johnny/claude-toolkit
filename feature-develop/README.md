# Feature Development Plugin

Guided feature development with codebase understanding and architecture focus.

## Overview

The Feature Development Plugin provides a systematic 7-phase workflow for implementing new features with deep codebase understanding, collaborative architecture design, and quality review.

## Command

### `/feature [description]`

Initiates the guided feature development workflow.

**Usage:**
```bash
/feature Add user authentication with OAuth2
/feature Implement dark mode toggle in settings
/feature Create export functionality for reports
```

## Workflow Phases

### Phase 1: Discovery
- Understand what needs to be built
- Clarify requirements with user
- Create comprehensive todo list

### Phase 2: Codebase Exploration
- Launch parallel code-explorer agents
- Map existing patterns and architecture
- Identify integration points

### Phase 3: Clarifying Questions
- Identify all ambiguities and edge cases
- Ask specific, concrete questions
- Wait for user answers before proceeding

### Phase 4: Architecture Design
- Launch parallel code-architect agents
- Design multiple implementation approaches
- Present trade-offs and recommendation

### Phase 5: Implementation
- Build the feature with user approval
- Follow codebase conventions
- Track progress with todos

### Phase 6: Quality Review
- Launch parallel code-reviewer agents
- Identify bugs and quality issues
- Address issues based on user decision

### Phase 7: Summary
- Document what was accomplished
- Summarize key decisions and files modified
- Suggest next steps

## Agents

| Agent | Model | Purpose |
|-------|-------|---------|
| `code-explorer` | Sonnet | Traces execution paths, maps architecture, documents dependencies |
| `code-architect` | Opus | Designs architecture blueprints with implementation details |
| `code-reviewer` | Opus | Reviews for bugs, quality issues, and convention compliance |

## Core Principles

1. **Ask clarifying questions** - Don't assume; ask specific questions
2. **Understand before acting** - Read and comprehend existing patterns
3. **Simple and elegant** - Prioritize maintainable, readable code
4. **Track progress** - Use todos throughout all phases

## Best Practices

- Let the workflow guide you through each phase
- Provide clear feature descriptions upfront
- Answer clarifying questions thoroughly
- Review architecture options before implementation
- Address quality issues promptly

## Author

GOODA

## Version

1.0.0
