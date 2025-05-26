# CLAUDE.md - Guidelines for Agentic Coding

## Git Workflow
- Commit in appropriate work units with descriptive messages
- NEVER commit directly to the main branch - always use feature branches
- Follow conventional commit format
- Do not include "🤖 Generated with [Claude Code]" or "Co-Authored-By: Claude" in commits

## Code Style Guidelines
- **Formatting**: 2 spaces indentation, 80-100 char line length
- **Naming**: camelCase for variables/functions, PascalCase for classes
- **Imports**: Group by type (standard library → third-party → local)
- **Types**: Use TypeScript types/interfaces in JS/TS, type hints in Python
- **Error Handling**: Use explicit try/catch blocks, handle errors properly
- **Comments**: Document complex logic only, prefer self-documenting code
- **Functions**: Small, focused on single responsibility
- **Principles**: Readability over cleverness, modularity, explicit over implicit

## Language-Specific Guidelines
- **JavaScript/TypeScript**: Modern ES6+, functional patterns where appropriate
- **Python**: Follow PEP 8, use type hints, explicit docstrings
- **Markdown**: Consistent heading hierarchy, code blocks with language specs

## Project Organization
- Group files by feature/module rather than by file type
- Place tests alongside implementation files or in parallel test directory
- Key files: .clinerules, .github/copilot-instructions.md, .github/prompts/

## Development Commands
- Build: TBD (add command when build system is set up)
- Dev server: TBD
- Lint: TBD
- Typecheck: TBD
- Test: TBD
- Single test: TBD (specify pattern for running a specific test)

