---
description: Systematic debugging workflow for identifying and fixing bugs
argument-hint: Description of the bug or unexpected behavior
---

# Debug

You are helping a developer debug an issue. Follow a systematic approach: understand the symptoms, trace the code path, identify root cause, then fix.

## Core Principles

- **Reproduce first**: Always try to reproduce the issue before diving into code
- **Hypothesis-driven**: Form hypotheses and test them systematically
- **Trace execution**: Follow data flow and control flow meticulously
- **Document findings**: Keep track of what you've tried and learned
- **Use TodoWrite**: Track all progress throughout

---

## Phase 1: Problem Definition

**Goal**: Understand exactly what's happening vs what should happen

Initial bug report: $ARGUMENTS

**Actions**:
1. Create todo list with all phases
2. Clarify with user:
   - What is the expected behavior?
   - What is the actual behavior?
   - When did it start happening?
   - Can they reproduce it consistently?
   - Any error messages or stack traces?
3. Summarize understanding of the problem

---

## Phase 2: Reproduction & Evidence Gathering

**Goal**: Reproduce the bug and gather evidence

**Actions**:
1. Launch bug-hunter agent to:
   - Find related code paths
   - Identify potential failure points
   - Locate relevant error logs or handling
2. Attempt to reproduce the issue
3. Document:
   - Exact steps to reproduce
   - Environment details if relevant
   - Any patterns (happens always, sometimes, under specific conditions)

If unable to reproduce, ask user for more details or environment information.

---

## Phase 3: Root Cause Analysis

**Goal**: Identify the root cause, not just symptoms

**Actions**:
1. Launch error-analyzer agent to:
   - Trace execution path from entry point
   - Identify where state changes unexpectedly
   - Find the exact line where behavior diverges from expected
2. Form hypotheses about root cause based on evidence
3. Test each hypothesis:
   - Add logging or debugging statements if needed
   - Check related code for similar patterns
   - Verify assumptions about data and state
4. Confirm root cause with concrete evidence

**DO NOT PROCEED TO FIX WITHOUT CONFIRMING ROOT CAUSE**

---

## Phase 4: Fix Planning

**Goal**: Design the proper fix

**Actions**:
1. Present root cause analysis to user:
   - What went wrong and why
   - Where exactly in the code
   - Why it wasn't caught before
2. Propose fix options:
   - Minimal fix (patch the symptom)
   - Proper fix (address root cause)
   - Comprehensive fix (add safeguards to prevent similar issues)
3. **Ask user which approach they prefer**
4. Identify potential side effects of the fix

---

## Phase 5: Fix Implementation

**Goal**: Implement the fix correctly

**DO NOT START WITHOUT USER APPROVAL**

**Actions**:
1. Wait for explicit user approval
2. Implement the chosen fix
3. Follow codebase conventions
4. Add appropriate error handling
5. Update todos as you progress

---

## Phase 6: Verification

**Goal**: Ensure the fix works and doesn't break anything

**Actions**:
1. Verify the fix solves the original issue
2. Check for regressions:
   - Related functionality still works
   - Edge cases are handled
   - No new errors introduced
3. Launch code-reviewer agent to check fix quality
4. Suggest preventive measures:
   - Tests to add
   - Validation to implement
   - Documentation to update

---

## Phase 7: Summary

**Goal**: Document what was learned

**Actions**:
1. Mark all todos complete
2. Summarize:
   - What the bug was (root cause)
   - Why it happened
   - How it was fixed
   - Files modified
   - Preventive measures recommended
3. Note any patterns to watch for in the future

