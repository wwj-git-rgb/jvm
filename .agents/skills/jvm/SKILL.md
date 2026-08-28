```markdown
# jvm Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `jvm` TypeScript codebase. You'll learn about file naming, import/export styles, commit message conventions, and how to structure and run tests. This guide is ideal for contributors looking to maintain consistency and quality in the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myModule.ts`, `helperFunctions.ts`

### Import Style
- Use **relative imports** for referencing other modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports** rather than default exports.
  - Example:
    ```typescript
    // utils.ts
    export function myFunction() { /* ... */ }

    // usage
    import { myFunction } from './utils';
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `chore` prefix for general maintenance.
  - Example: `chore: update dependencies`

## Workflows

### Commit Changes
**Trigger:** When making any code changes that need to be committed.
**Command:** `/commit-changes`

1. Stage your changes:
   ```bash
   git add .
   ```
2. Write a conventional commit message, using the `chore` prefix for maintenance:
   ```bash
   git commit -m "chore: update helperFunctions"
   ```
3. Push your changes:
   ```bash
   git push
   ```

### Add a New Module
**Trigger:** When creating a new feature or utility.
**Command:** `/add-module`

1. Create a new file using camelCase naming, e.g., `newFeature.ts`.
2. Use named exports for all functions or constants:
   ```typescript
   export function newFeature() { /* ... */ }
   ```
3. Import the module using a relative path where needed:
   ```typescript
   import { newFeature } from './newFeature';
   ```

### Write and Run Tests
**Trigger:** When adding or updating functionality.
**Command:** `/run-tests`

1. Create a test file with the `.test.` pattern, e.g., `myModule.test.ts`.
2. Write your tests using the project's preferred (unknown) testing framework.
3. Run the tests using the appropriate command for the framework (consult project documentation if unsure).

## Testing Patterns

- Test files should follow the `*.test.*` naming pattern.
  - Example: `utils.test.ts`
- The specific testing framework is not detected; follow any existing patterns in the codebase.
- Place tests alongside or near the modules they test.

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /commit-changes | Guide for committing code changes             |
| /add-module     | Steps to add a new module with conventions    |
| /run-tests      | Instructions for writing and running tests    |
```
