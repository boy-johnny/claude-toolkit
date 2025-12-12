# Commit Workflow Plugin

Streamline your git workflow with simple commands for committing, pushing, and creating pull requests.

## Overview

The Commit Workflow Plugin automates common git operations, reducing context switching and manual command execution. Instead of running multiple git commands, use a single slash command to handle your entire workflow.

## Commands

### `/commit`

Creates a git commit with an automatically generated commit message based on staged and unstaged changes.

**What it does:**
1. Analyzes current git status
2. Reviews both staged and unstaged changes
3. Examines recent commit messages to match your repository's style
4. Drafts an appropriate commit message
5. Stages relevant files
6. Creates the commit

**Usage:**
```bash
/commit
```

**Features:**
- Automatically drafts commit messages that match your repo's style
- Follows conventional commit practices
- Avoids committing files with secrets (.env, credentials.json)

### `/commit-push-pr`

Complete workflow command that commits, pushes, and creates a pull request in one step.

**What it does:**
1. Creates a new branch (if currently on main)
2. Stages and commits changes with an appropriate message
3. Pushes the branch to origin
4. Creates a pull request using `gh pr create`
5. Provides the PR URL

**Usage:**
```bash
/commit-push-pr
```

**Features:**
- Analyzes all commits in the branch (not just the latest)
- Creates comprehensive PR descriptions with:
  - Summary of changes (1-3 bullet points)
  - Test plan checklist
- Handles branch creation automatically
- Uses GitHub CLI (`gh`) for PR creation

**Requirements:**
- GitHub CLI (`gh`) must be installed and authenticated
- Repository must have a remote named `origin`

### `/clean-gone`

Cleans up local branches that have been deleted from the remote repository.

**What it does:**
1. Lists all local branches to identify [gone] status
2. Identifies and removes worktrees associated with [gone] branches
3. Deletes all branches marked as [gone]
4. Provides feedback on removed branches

**Usage:**
```bash
/clean-gone
```

**Features:**
- Handles both regular branches and worktree branches
- Safely removes worktrees before deleting branches
- Shows clear feedback about what was removed
- Reports if no cleanup was needed

## Workflow Examples

### Quick commit workflow:
```bash
# Write code
/commit
# Continue development
```

### Feature branch workflow:
```bash
# Develop feature across multiple commits
/commit  # First commit
# More changes
/commit  # Second commit
# Ready to create PR
/commit-push-pr
```

### Maintenance workflow:
```bash
# After several PRs are merged
/clean-gone
# Clean workspace ready for next feature
```

## Requirements

- Git must be installed and configured
- For `/commit-push-pr`: GitHub CLI (`gh`) must be installed and authenticated
- Repository must be a git repository with a remote

## Troubleshooting

### `/commit` creates empty commit
- Ensure you have unstaged or staged changes
- Run `git status` to verify changes exist

### `/commit-push-pr` fails to create PR
- Install GitHub CLI: `brew install gh` (macOS)
- Authenticate: `gh auth login`
- Ensure repository has a GitHub remote

### `/clean-gone` doesn't find branches
- Run `git fetch --prune` to update remote tracking
- Branches must be deleted from the remote to show as [gone]

## Author

GOODA

## Version

1.0.0
