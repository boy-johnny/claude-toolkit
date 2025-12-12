---
description: Trace execution flow through code to understand behavior
argument-hint: Function, endpoint, or feature to trace
---

# Trace

Trace the execution flow through code to understand how a specific function, endpoint, or feature works.

## Context

Target to trace: $ARGUMENTS

## Your Task

Perform a comprehensive trace of the execution flow:

**1. Find Entry Point**
- Locate where the target function/endpoint/feature is invoked
- Identify all callers and entry points

**2. Trace Forward**
- Follow the execution path step by step
- Document each function call and its purpose
- Note parameters passed and values returned
- Identify conditionals and branches

**3. Trace Data Flow**
- Track how data transforms through the flow
- Identify state changes and side effects
- Document external calls (APIs, database, file system)

**4. Map Dependencies**
- List all modules and files involved
- Identify shared state or global dependencies
- Note any async operations or callbacks

## Output Format

Provide a structured trace:

```
ENTRY POINT: [file:line] function_name(params)
│
├── [file:line] called_function_1(params)
│   ├── [purpose]: Brief description
│   ├── [returns]: What it returns
│   └── [side effects]: Any side effects
│
├── [file:line] called_function_2(params)
│   ├── [purpose]: Brief description
│   ├── [conditional]: If X then Y else Z
│   └── [external]: Database query / API call
│
└── EXIT: [return value or final state]
```

Include:
- File paths and line numbers
- Key decision points
- Data transformations
- Error handling paths
- List of all files involved

