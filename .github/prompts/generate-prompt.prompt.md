---
mode: 'agent'
description: 'Effective prompt generation and optimization with GitHub Copilot'
---
# Meta-Prompt for Prompt Generation

This prompt file serves as a template for creating effective prompts using GitHub Copilot. It allows you to quickly and efficiently create prompts tailored to various purposes.

## 📁 Prompt File Information

Prompt files allow you to craft complete prompts in Markdown files, which you can then reference in chat. Unlike custom instructions that supplement your existing prompts, prompt files are standalone prompts that you can store within your workspace and share with others. With prompt files, you can create reusable templates for common tasks, store domain expertise in your codebase, and standardize AI interactions across your team.

### File Naming and Location

- **File Extension**: `.prompt.md` (Markdown files with this extension are recognized as prompt files)
- **Storage Locations**:
  - **Workspace prompt files**: Stored in the `.github/prompts` folder of the workspace (like this file at `.github/prompts/generate-prompt.prompt.md`)
  - **User prompt files**: Available across multiple workspaces and stored in the current VS Code profile

### Prompt File Structure

A prompt file consists of two sections:
1. **(Optional) Header with metadata** (Front Matter syntax)
   - `mode`: Chat mode to use (ask, edit, or agent [default])
   - `tools`: List of tools available in agent mode
   - `description`: A short description of the prompt
2. **Body with the prompt content**

You can reference other prompt files or instruction files using Markdown links with relative paths. You can also use variables with the `${variableName}` syntax, including workspace variables, selection variables, file context variables, and input variables.

### Common Use Cases

- **Code generation**: Create reusable prompts for components, tests, or migrations
- **Domain expertise**: Share specialized knowledge through prompts, such as security practices or compliance checks
- **Team collaboration**: Document patterns and guidelines with references to specs and documentation
- **Onboarding**: Create step-by-step guides for complex processes or project-specific patterns

### Prompt file examples

Prompt for a reusable task to generate a React form:

```markdown
---
mode: 'agent'
tools: ['githubRepo', 'codebase']
description: 'Generate a new React form component'
---
Your goal is to generate a new React form component based on the templates in #githubRepo contoso/react-templates.

Ask for the form name and fields if not provided.

Requirements for the form:
* Use form design system components: [design-system/Form.md](./react.prompt.md)
* Use `react-hook-form` for form state management:
* Always define TypeScript types for your form data
* Prefer *uncontrolled* components using register
* Use `defaultValues` to prevent unnecessary rerenders
* Use `yup` for validation:
* Create reusable validation schemas in separate files
* Use TypeScript types to ensure type safety
* Customize UX-friendly validation rules
```


Prompt for performing a security review of a REST API:
```
---
mode: 'edit'
description: 'Perform a REST API security review'
---
Perform a REST API security review:

* Ensure all endpoints are protected by authentication and authorization
* Validate all user inputs and sanitize data
* Implement rate limiting and throttling
* Implement logging and monitoring for security events
```

## 🎯 Objectives

- Generate prompts optimized for specific tasks and purposes
- Design prompts that enable effective communication with GitHub Copilot
- Create reusable and structured prompt templates
- Apply prompt engineering best practices

## 🧩 Guidelines for Prompt Generation

Consider the following elements when creating effective prompts:

### 1. Clarify Purpose and Target Audience

```
# [Prompt Title]

## Purpose
Describe specifically the purpose of this prompt and the desired outcomes.

## Target Users
Describe the technical level and background knowledge of the users this prompt is intended for.
```

### 2. Basic Prompt Structure

```
## Instructions
List clear and specific instructions in bullet points. Eliminate ambiguity and include examples for effectiveness.

## Constraints
Specify constraints or considerations to be aware of (e.g., specific coding conventions, security requirements).

## Input Format
Show the format and examples of information that users should provide.

## Output Format
Specifically indicate the format and structure of the expected response.
```

### 3. Context Provision Template

```
## Project Context
- Project name: [Project name]
- Tech stack: [Languages/Frameworks/Tools]
- Architecture: [Architecture patterns used]
- Special notes: [Other important information]

## Related Resources
- [Resource name]: [Description]
- [Resource name]: [Description]
```

## 💡 Templates by Prompt Type

### Code Generation Prompt

```
---
mode: 'agent'
description: '[Briefly describe the code generation purpose]'
---
# [Name of the Code Generation Task]

Please generate [language/framework] code based on the following requirements:

## Functional Requirements
- [Description of feature 1]
- [Description of feature 2]
- [Description of feature 3]

## Technical Requirements
- [Technical requirement 1] (e.g., Include TypeScript type definitions)
- [Technical requirement 2] (e.g., Use React hooks)
- [Technical requirement 3] (e.g., Design for testability)

## Code Style
- [Style guide reference or specific style requirements]
- [Naming conventions]
- [Comment requirements]

## Example
Here is an image of the expected implementation:

```[language]
// Sample code of what is expected
```

## Expected Output
- Fully executable code
- Explanatory comments for each section
- Concise explanation of usage
```

### Review/Analysis Prompt

```
---
mode: 'agent'
description: '[Briefly describe the review/analysis purpose]'
---
# [Name of the Review/Analysis Task]

Please review/analyze the following code from the perspective of [purpose]:

```[language]
// Code to be reviewed
```

## Review Aspects
Please evaluate from the following perspectives:
- [Aspect 1] (e.g., Performance)
- [Aspect 2] (e.g., Security)
- [Aspect 3] (e.g., Maintainability)
- [Aspect 4] (e.g., Testability)

## Expected Output
1. Overall assessment (strengths, weaknesses)
2. Improvement suggestions (including code examples)
3. Refactoring approaches
```

### Educational/Explanatory Prompt

```
---
mode: 'agent'
description: '[Briefly describe the educational/explanatory purpose]'
---
# [Name of the Educational/Explanatory Topic]

## Background
[Explain the background and importance of the topic in 2-3 sentences]

## Content to Explain
Please explain [topic] from the following aspects:
- [Aspect 1] (e.g., Basic concepts)
- [Aspect 2] (e.g., Implementation methods)
- [Aspect 3] (e.g., Common problems and solutions)
- [Aspect 4] (e.g., Best practices)

## Format
- Step-by-step explanation (from beginner to advanced)
- Specific code examples
- Real-world use cases and applications
- Visual explanations using diagrams and analogies

## Target Audience
[Technical level and background knowledge of the target audience]
```

## ⚙️ Prompt Optimization Techniques

### 1. Specificity and Clarity

- **Avoid ambiguous expressions**: Instead of "good code," use specific descriptions like "maintainable code (with clear function responsibilities and appropriate modularization)"
- **Include quantitative elements**: Instead of "short functions," specify "functions within 20 lines"
- **Provide examples**: Concrete examples are better than abstract instructions

### 2. Structure and Organization

- **Hierarchical structure**: Use headings and bullet points to organize information
- **Prioritization**: Describe the most important elements first
- **Section divisions**: Group related instructions together

### 3. Providing Context

- **Background information**: Explain why the generation is necessary
- **Constraints**: Clearly specify constraints to consider
- **Goal clarification**: Clearly state the desired end result

### 4. Incorporating Feedback Mechanisms

- **Iterative improvement**: Include instructions to further improve initial generation results
- **Evaluation criteria**: Specify criteria for evaluating the generated content
- **Offering choices**: Design to allow selection from multiple approaches

## 🔧 Prompt Generation Request Examples

```
Please generate a prompt for the following purpose:

Purpose: [Purpose of the prompt]
Target: [Target audience of the prompt]
Key elements:
- [Element 1]
- [Element 2]
- [Element 3]

Output format: Complete prompt file (including front matter)
Special requirements: [Any special requirements]
```

## 📝 Practical Examples of Prompt Generation

### Example 1: Code Review Prompt Generation

```
Please generate a prompt for the following purpose:

Purpose: Security review of PHP code
Target: Intermediate to advanced PHP developers
Key elements:
- Security checks based on OWASP Top 10
- Detection of vulnerabilities such as SQL injection, XSS, CSRF
- Best practices for secure data handling and validation
- Include code modification suggestions

Output format: Complete prompt file (including front matter)
Special requirements: Assume PHP version 8.2 or higher
```

### Example 2: Component Design Prompt Generation

```
Please generate a prompt for the following purpose:

Purpose: Designing reusable form components in React
Target: Developers familiar with TypeScript and React
Key elements:
- Type-safe design with TypeScript
- Accessibility compliance
- Customizable styling
- Integration of validation features
- Unit testing approach

Output format: Complete prompt file (including front matter)
Special requirements: Use React 18 and React Hook Form
```

---

## 🔍 Prompt Evaluation Criteria

You can evaluate generated prompts based on the following criteria:

- **Clarity**: Are the instructions specific and unambiguous?
- **Completeness**: Does it include all necessary information and constraints?
- **Structure**: Is the information logically organized?
- **Specificity**: Are concrete examples provided instead of abstract expressions?
- **Reusability**: Can it be adapted for similar tasks?

---

Use this meta-prompt to generate effective prompts suited to your purposes. By clearly defining specific use cases and required information, you can create higher quality prompts.