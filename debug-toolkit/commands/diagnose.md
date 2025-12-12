---
description: Quick diagnostic for common issues - errors, crashes, performance
argument-hint: Error message, symptom, or issue type
---

# Diagnose

Quick diagnostic tool for common issues. Use for rapid triage before diving into full debugging.

## Context

Issue to diagnose: $ARGUMENTS

## Diagnostic Checklist

### 1. Error Analysis (if error message provided)
- Parse the error message and stack trace
- Identify the error type and origin
- Find the file and line where it occurs
- Look for similar errors in the codebase

### 2. Recent Changes Check
- Check `git log --oneline -20` for recent commits
- Check `git diff HEAD~5` for recent changes
- Identify if issue correlates with recent modifications

### 3. Common Issue Patterns

**Null/Undefined Errors:**
- Missing null checks
- Async timing issues
- Uninitialized variables

**Type Errors:**
- Incorrect parameter types
- Missing type conversions
- API response shape changes

**Import/Module Errors:**
- Missing dependencies
- Circular imports
- Incorrect paths

**State Issues:**
- Race conditions
- Stale state
- Missing updates

**Configuration Issues:**
- Environment variables
- Missing config files
- Wrong environment

### 4. Quick Fixes to Try

Based on issue type, suggest:
- Common fixes that often resolve the issue
- Quick validation steps
- Relevant documentation or references

## Output

Provide:
1. **Likely cause**: Most probable root cause based on evidence
2. **Confidence**: How confident (low/medium/high) based on available information
3. **Quick checks**: 2-3 things to verify immediately
4. **Suggested action**: Next step to take
5. **If not resolved**: Recommend `/debug` for full investigation

