# Bug Fixing Workflow

## Overview

This workflow provides a structured approach for using LLMs to assist in identifying, diagnosing, and fixing bugs in code.

## Workflow Steps

### 1. Bug Identification

**Prompt Template:**
```
# Bug Report Analysis

## Bug Description
[Provide the error message or unexpected behavior]

## Expected Behavior
[Describe what should happen]

## Current Behavior
[Describe what actually happens]

## Environment
- Language/Framework version: [e.g., Node.js 16, Python 3.9]
- OS: [e.g., macOS, Windows]
- Browser (if applicable): [e.g., Chrome, Firefox]

## Analyze this bug report and suggest potential causes and areas to investigate.
```

### 2. Code Investigation

**Prompt Template:**
```
# Code Investigation

## Bug Summary
[Brief description of the bug]

## Relevant Code
```[language]
[Paste the code that might contain the bug]
```

## Error Messages or Logs
```
[Paste any error messages or logs]
```

## Analyze this code and identify potential issues that could cause the described bug. Explain your reasoning.
```

### 3. Root Cause Analysis

**Prompt Template:**
```
# Root Cause Analysis

## Bug Summary
[Brief description of the bug]

## Code Investigation Results
[Summary of findings from code investigation]

## Additional Context
[Any additional information discovered during investigation]

## Based on the information provided, what is the most likely root cause of this bug? Explain the underlying issue and why it causes the observed behavior.
```

### 4. Solution Development

**Prompt Template:**
```
# Solution Development

## Root Cause
[Description of the identified root cause]

## Current Code
```[language]
[Paste the relevant code that needs to be fixed]
```

## Requirements for Fix
- [Requirement 1]
- [Requirement 2]

## Develop a solution to fix this bug. Provide the corrected code and explain how your changes address the root cause.
```

### 5. Solution Testing

**Prompt Template:**
```
# Solution Testing

## Proposed Fix
```[language]
[Paste the proposed solution]
```

## Test Cases
- [Test case 1: Input and expected output]
- [Test case 2: Input and expected output]

## Edge Cases to Consider
- [Edge case 1]
- [Edge case 2]

## Analyze this solution and verify it addresses the root cause. Suggest test cases to confirm the fix works correctly and doesn't introduce new issues.
```

## Best Practices

1. Always include the original bug report and error messages in your prompts.
2. Provide sufficient context about the codebase and environment.
3. Ask the LLM to explain its reasoning at each step.
4. Test the proposed solution against multiple scenarios.
5. Have the LLM review the solution for potential side effects or edge cases.

## Example

See the `examples/bug_fixing_example.md` file for a complete example of this workflow in action.