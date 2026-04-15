# Development Guidelines

## Process
- **Plan First**: Discuss approach before writing code; surface all implementation decisions that need alignment
- **Confirm Before Coding**: Agree on the plan, then follow it precisely
- **Stop and Discuss**: If an unforeseen issue arises during implementation, raise it before continuing
- **Disagreements**: Raise genuine technical concerns once with reasoning; defer to my judgment if I still prefer the original approach

## Code Standards
- **Simplicity & Maintainability**: Write simple, straightforward code that's easy to update
- **Early Returns**: Use to avoid nested conditions
- **Reusability**: Introduce abstractions when architecturally motivated or when the same logic appears 3+ times
- **Minimal Changes**: Only modify code related to the task; when refactoring IS the task, prioritize clean structure over minimal diff
- **Refactoring**: Proactively flag opportunities even when out of scope; don't act on them unless asked
- **Adjacent Bugs**: Flag with a TODO comment; don't fix unless asked
- **Clean Logic**: Keep core logic clean and push implementation details to the edges

## Comments
- Self-documenting code is the goal — comments explain *why*, not *what*
- Public APIs and interfaces get doc comments regardless

## Naming Conventions
- Prefer long, intention-revealing names over short, ambiguous ones
- Booleans use `is`/`has` prefixes (e.g. `isValid`, `hasChildren`)
- Classes are noun phrases; methods are verb phrases
- Never abbreviate unless universally understood (e.g. `id`, `url`)

## Error Handling
- Fail fast — surface errors immediately and loudly rather than recovering silently
- Use exceptions for error signaling; not result types or error codes
- Validate defensively at multiple layers, not just at the boundary

## Design Patterns
- Think in terms of established GoF and architectural patterns — creational, structural, and behavioral
- Suggest patterns by name when they fit naturally; don't force them
- Prefer architectural layering patterns (e.g. service-repository, unit of work) over flat structure
- Name patterns explicitly when introducing them so we share vocabulary

## Testing
- Always write tests after implementation, never before — no TDD
- Cover logic-layer code with unit tests; integration tests where behavior warrants it
- Prefer host-compilable unit tests where possible
- GUI and environment-specific components are verified manually

## When Planning
- Present multiple options with pros/cons when they exist
- Call out edge cases and how we should handle them
- Share opinions on best practices; distinguish opinion from fact
- When reviewing code, flag everything — correctness, style, naming, structure, missed patterns

## Git Workflow
- **Never commit on my behalf** — I review all changes and commit myself
- Do not run `git commit` under any circumstances unless explicitly asked in that moment
- Creating new branches is fine when the work warrants isolation

## Response Style & Context
- Thorough, complete explanations over brevity; full context over follow-up questions
- Headers and bullets for multi-part answers; prose for single-topic responses
- Skip preamble and trailing summaries — get to the substance
- Senior software engineer — no need to over-explain fundamentals; use pattern vocabulary; genuine dialogue, not validation
