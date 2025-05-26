# Code Style Rules

## Purpose

These rules ensure that LLM-generated code follows consistent style and formatting conventions.

## General Rules

1. **Indentation**: Use 2 spaces for indentation, not tabs.
2. **Line Length**: Keep lines under 100 characters when possible.
3. **Naming Conventions**:
   - Use `camelCase` for variables and functions
   - Use `PascalCase` for classes and interfaces
   - Use `UPPER_SNAKE_CASE` for constants
4. **File Organization**:
   - Group related functions and classes together
   - Order methods logically (e.g., lifecycle methods first in React components)
   - Keep files focused on a single responsibility
5. **Comments**:
   - Add comments for complex logic only
   - Use JSDoc for function documentation
   - Keep comments updated when code changes
6. **Imports**:
   - Group imports by type (built-in, external, internal)
   - Sort imports alphabetically within groups
   - Use destructuring for multiple imports from the same module

## Language-Specific Rules

### JavaScript/TypeScript

1. Use strict equality (`===`) instead of loose equality (`==`).
2. Use template literals instead of string concatenation.
3. Use destructuring for object and array assignments when practical.
4. Prefer `const` over `let`, and avoid `var`.
5. Use async/await instead of raw promises when possible.
6. Always specify return types in TypeScript functions.

### Python

1. Follow PEP 8 guidelines.
2. Use type hints in function signatures.
3. Use f-strings for string formatting.
4. Use list/dict comprehensions for simple transformations.
5. Use meaningful variable names instead of single-letter variables (except in simple loops).

## Enforcement

When generating code, LLMs should prioritize these style rules and explicitly mention if they are deviating from them for a specific reason.