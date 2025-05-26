---
applyTo: "**"
---

# GitHub Copilot Instructions for Agentic Coding Sandbox

## Project Context

This project is a sandbox for exploring and developing Agentic Coding techniques using Large Language Models (LLMs). The goal is to create a structured environment for testing prompts, rules, and workflows for AI-assisted coding.

## Coding Guidelines

When generating code for this project, please follow these guidelines:

### General Principles

- Prioritize readability and maintainability over clever or overly concise code
- Include clear, descriptive comments explaining the purpose and functionality
- Follow consistent naming conventions and code organization
- Consider edge cases and error handling in your implementations
- Aim for modular, reusable components when possible

### Language-Specific Guidelines

#### JavaScript/TypeScript
- Use modern ES6+ syntax and features
- Prefer functional programming patterns where appropriate
- Use TypeScript types/interfaces for better code documentation
- Follow standard linting rules (eslint:recommended)

#### Python
- Follow PEP 8 style guidelines
- Use type hints for function parameters and return values
- Prefer explicit over implicit code
- Use docstrings for functions and classes

#### Markdown
- Use consistent heading hierarchy
- Include examples where helpful
- Structure content with clear sections
- Use code blocks with language specification

## Project Structure

When suggesting new files or modifications, be aware of the project structure:

- `.clinerules`: Code style settings for the cline tool
- `.github/`: GitHub configuration files, including Copilot instructions and prompts
  - `/.github/prompts`: Contains effective prompts for various coding tasks
- `CLAUDE.md`: Guidelines and best practices for working with Claude

## Task-Specific Guidance

### Creating Prompts
- Follow the structure outlined in `.github/prompts/generate-prompt.prompt.md`
- Include clear purpose, target audience, and expected output format
- Provide specific examples and constraints
- Consider different skill levels and use cases

## Collaboration Focus

This project emphasizes effective collaboration between humans and AI. When generating suggestions:

- Explain your reasoning and approach
- Offer alternatives when appropriate
- Highlight potential trade-offs or considerations
- Suggest improvements to existing code or documentation
- Provide educational context that helps the user learn

By following these instructions, you'll help create a valuable resource for developing and refining Agentic Coding techniques.
