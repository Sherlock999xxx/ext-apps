```markdown
# ext-apps Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `ext-apps` repository, a TypeScript React codebase. You'll learn how to structure files, write imports/exports, follow commit message conventions, and organize tests. This guide also provides suggested commands for common workflows.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `userProfile.tsx`, `appConfig.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { UserProfile } from './userProfile';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // userProfile.tsx
    export const UserProfile = () => { /* ... */ };
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `build` prefix for build-related changes.
- Keep commit messages concise (average ~46 characters).
  - Example:
    ```
    build: update dependencies to latest versions
    ```

## Workflows

_No explicit workflows detected in the repository._

## Testing Patterns

- **Test files** use the pattern `*.test.*`.
  - Example: `userProfile.test.tsx`
- **Testing framework** is not specified, but tests are colocated with source files or in the same directory.

  ```typescript
  // userProfile.test.tsx
  import { render } from '@testing-library/react';
  import { UserProfile } from './userProfile';

  test('renders user profile', () => {
    render(<UserProfile />);
    // assertions...
  });
  ```

## Commands

| Command | Purpose |
|---------|---------|
| /commit-build | Create a build-related commit using conventional commit format |
| /test | Run all test files matching `*.test.*` |
| /lint | Lint the codebase according to project standards |
```