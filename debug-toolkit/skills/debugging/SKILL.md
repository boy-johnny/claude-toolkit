---
name: debugging
description: Systematic debugging skill that activates when encountering errors, bugs, or unexpected behavior. Provides structured approach to identifying and fixing issues.
---

This skill activates when the user encounters errors, bugs, or unexpected code behavior. It provides a systematic debugging approach.

## When to Use

Activate this skill when:
- User reports an error or exception
- Code isn't behaving as expected
- Tests are failing
- Performance issues occur
- User explicitly asks to debug something

## Debugging Principles

**1. Reproduce Before Fixing**
Never attempt to fix a bug you can't reproduce. First confirm:
- Exact steps to trigger the issue
- Expected vs actual behavior
- Any error messages or logs

**2. Hypothesis-Driven Investigation**
- Form a hypothesis about the cause
- Design a test to verify or refute it
- Eliminate possibilities systematically
- Don't jump to conclusions

**3. Binary Search for Root Cause**
- If unsure where the bug is, bisect
- Add logging at midpoints
- Narrow down the problematic section

**4. Check Common Culprits First**
- Recent code changes (`git log`, `git diff`)
- Null/undefined values
- Off-by-one errors
- Async timing issues
- Type mismatches
- Missing error handling

**5. Read Error Messages Carefully**
- Parse stack traces completely
- Identify the actual error vs symptoms
- Note file names and line numbers
- Search for the error message in code

## Debugging Workflow

```
1. UNDERSTAND: What should happen vs what happens?
2. REPRODUCE: Can you trigger it reliably?
3. ISOLATE: Where does the behavior diverge?
4. IDENTIFY: What is the root cause?
5. FIX: Address the root cause, not symptoms
6. VERIFY: Does the fix work? Any side effects?
7. PREVENT: How to avoid similar bugs?
```

## Common Debug Commands

```bash
# Check recent changes
git log --oneline -20
git diff HEAD~5

# Search for error patterns
grep -r "error_message" --include="*.ts"
grep -r "throw" --include="*.ts"

# Find related code
grep -r "function_name" --include="*.ts"
```

## Output Expectations

When debugging:
- Be systematic, not random
- Document what you've tried
- State hypotheses clearly
- Provide evidence for conclusions
- Suggest preventive measures after fixing

