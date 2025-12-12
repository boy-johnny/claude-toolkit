---
allowed-tools: Bash(git checkout -b:*), Bash(git add:*), Bash(git status:*), Bash(git push:*), Bash(git commit:*), Bash(gh pr create:*)
description: Commit, push, and open a PR in one workflow
---

## Context

- Current git status: !`git status`
- Current git diff (staged and unstaged changes): !`git diff HEAD`
- Current branch: !`git branch --show-current`

## Your task

Based on the above changes:

1. **Create branch** (if on main/master): Create a new feature branch with a descriptive name
2. **Stage and commit**: Stage relevant files and create a commit with an appropriate message
3. **Push branch**: Push the branch to origin
4. **Create PR**: Use `gh pr create` to create a pull request with:
   - Title: Brief description of the changes
   - Body: 1-3 bullet points summarizing changes + test plan checklist

## PR Description Template

```
## Summary
- [Brief description of change 1]
- [Brief description of change 2]

## Test Plan
- [ ] Verified [test case 1]
- [ ] Verified [test case 2]

---
*Generated with Claude Code*
```

You have the capability to call multiple tools in a single response. You MUST do all of the above in a single message. Do not use any other tools or do anything else. Do not send any other text or messages besides these tool calls.

