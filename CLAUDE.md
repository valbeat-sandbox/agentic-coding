# CLAUDE.md

## Git Workflow

- Commit in appropriate work units with descriptive messages
- NEVER commit directly to the main branch - always use feature branches
- Follow conventional commit format
- Do not include "🤖 Generated with [Claude Code](https://claude.ai/code)" in PR comments and Commit messages
- Co-Authored-By: Claude <noreply@anthropic.com>"

## Documentation Maintenance

- Update CLAUDE.md continuously without being asked
- Add new rules and procedures when clarified
- Accumulate project-specific knowledge and best practices
- Record frequently used commands and shortcuts
- Update when code conventions change or new tools are introduced

## Build & Development Commands
- Build: TBD (add command when build system is set up)
- Dev server: TBD
- Lint: TBD
- Typecheck: TBD
- Test: TBD
- Single test: TBD (specify pattern for running a specific test)

## Code Style Guidelines
- **Formatting**: Use consistent indentation (2 spaces recommended)
- **Naming**: Use descriptive names in camelCase for variables/functions, PascalCase for classes
- **Imports**: Group imports by type (standard library first, then third-party, then local)
- **Types**: Use strong typing where applicable
- **Error Handling**: Use try/catch blocks and handle errors explicitly
- **Comments**: Write clear comments for complex logic, avoid unnecessary comments
- **Functions**: Keep functions small and focused on a single task
- **Line Length**: Aim for 80-100 characters per line

## Project Organization
- Group files by feature/module rather than by file type
- Place tests alongside implementation files or in parallel test directory


