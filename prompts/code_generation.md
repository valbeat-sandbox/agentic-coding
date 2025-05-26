# Code Generation Prompts

Effective prompts for generating new code using LLMs.

## Basic Structure

```
# Task: [Brief description of what needs to be created]

## Requirements
- [Functional requirement 1]
- [Functional requirement 2]
- [Non-functional requirement 1]

## Context
- [Relevant project information]
- [Existing architecture or patterns to follow]
- [Dependencies or constraints]

## Expected Output
- [Description of the code to be generated]
- [Specific file format or structure]
- [Naming conventions to follow]

## Examples
[Similar code examples if available]
```

## Example: Creating a Utility Function

```
# Task: Create a date formatting utility function

## Requirements
- Function should convert ISO date strings to user-friendly formats
- Support multiple output formats (short, medium, long)
- Handle invalid dates gracefully with error messages
- Include JSDoc documentation

## Context
- This will be used in a React application
- We use TypeScript for type safety
- Should follow functional programming principles

## Expected Output
- A TypeScript function with proper typing
- Named "formatDate" in camelCase
- Export as a named export

## Examples
Input: "2023-04-15T14:32:17Z", format: "short"
Output: "4/15/2023"

Input: "2023-04-15T14:32:17Z", format: "medium"
Output: "Apr 15, 2023"
```