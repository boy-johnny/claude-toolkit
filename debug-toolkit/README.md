# Debug Toolkit Plugin

Systematic debugging toolkit with bug hunting agents, error analysis, and trace logging capabilities.

## Overview

The Debug Toolkit Plugin provides structured workflows for identifying and fixing bugs. Instead of ad-hoc debugging, follow a systematic approach that ensures thorough investigation and proper fixes.

## Commands

### `/debug [description]`

Full debugging workflow for investigating and fixing bugs.

**Usage:**
```bash
/debug User login fails with "invalid credentials" even with correct password
/debug API returns 500 error on POST /users endpoint
/debug React component doesn't re-render when state changes
```

**Phases:**
1. Problem Definition - Understand expected vs actual behavior
2. Reproduction - Reproduce and gather evidence
3. Root Cause Analysis - Identify the actual cause
4. Fix Planning - Design the proper fix
5. Implementation - Apply the fix
6. Verification - Ensure fix works without regressions
7. Summary - Document findings

### `/trace [target]`

Trace execution flow through code to understand how something works.

**Usage:**
```bash
/trace handleUserLogin function
/trace POST /api/orders endpoint
/trace authentication middleware chain
```

**Output:**
- Entry points and callers
- Step-by-step execution path
- Data transformations
- External calls and side effects

### `/diagnose [issue]`

Quick diagnostic for rapid triage before full debugging.

**Usage:**
```bash
/diagnose TypeError: Cannot read property 'id' of undefined
/diagnose Application crashes on startup
/diagnose Slow response times on dashboard
```

**Output:**
- Likely cause with confidence level
- Quick checks to verify
- Suggested immediate action
- Whether full `/debug` is needed

## Agents

| Agent | Model | Purpose |
|-------|-------|---------|
| `bug-hunter` | Sonnet | Hunts bugs by tracing code paths and identifying failure points |
| `error-analyzer` | Opus | Deep analysis of errors and root cause identification |

## Skill

The `debugging` skill automatically activates when encountering errors or bugs, providing systematic debugging guidance.

## Debugging Philosophy

### Core Principles

1. **Reproduce First** - Never fix what you can't reproduce
2. **Hypothesis-Driven** - Form theories and test them systematically
3. **Binary Search** - Narrow down by bisecting the problem space
4. **Root Cause** - Fix the cause, not the symptom
5. **Document** - Track what you've tried and learned

### Common Bug Patterns

| Pattern | Symptoms | Common Fix |
|---------|----------|------------|
| Null reference | TypeError, undefined access | Add null checks, optional chaining |
| Race condition | Intermittent failures | Proper async handling, locks |
| State bug | Incorrect values, stale data | State management review |
| Type mismatch | Unexpected behavior, silent fails | Type validation, guards |
| Off-by-one | Array bounds, loop issues | Boundary condition review |

## Best Practices

### Before Debugging
- Get clear reproduction steps
- Note environment and conditions
- Check recent changes (`git log`)

### During Debugging
- Add logging strategically
- Test one hypothesis at a time
- Don't change multiple things at once
- Take notes on what you've tried

### After Fixing
- Verify the fix works
- Check for regressions
- Add tests to prevent recurrence
- Document the root cause

## Requirements

- Git for change tracking
- Access to logs if applicable
- Ability to reproduce the issue

## Author

GOODA

## Version

1.0.0
