---
allowed-tools: Bash(git add:*), Bash(git status:*), Bash(git commit:*)
description: Create a git commit with auto-generated message
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10`

## Your task

Based on the above changes, create a single git commit.

## Guidelines

1. **Analyze the changes**: Review the diff to understand what was modified
2. **Match commit style**: Look at recent commits to match the repository's commit message style
3. **Draft message**: Create a clear, concise commit message following conventional commits if the repo uses them
4. **Stage files**: Stage the appropriate files (avoid staging .env, credentials, or sensitive files)
5. **Commit**: Create the commit with the drafted message

You have the capability to call multiple tools in a single response. Stage and create the commit using a single message. Do not use any other tools or do anything else. Do not send any other text or messages besides these tool calls.

