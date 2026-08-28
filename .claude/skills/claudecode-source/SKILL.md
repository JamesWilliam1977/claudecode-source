```markdown
# claudecode-source Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides a comprehensive guide to contributing to the `claudecode-source` repository, which is a TypeScript codebase with no detected framework. It covers coding conventions, commit patterns, common workflows, and testing practices. The repository emphasizes multilingual documentation updates and a flexible approach to API specification brainstorming.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `apiProvider.ts`, `userSettings.test.ts`

### Import Style
- Mixed import styles are used. Both named and default imports may appear.
  - Example:
    ```typescript
    import { fetchData } from './apiUtils';
    import config from './config';
    ```

### Export Style
- Prefer **named exports**.
  - Example:
    ```typescript
    // Good
    export function getUser() { ... }
    export const API_VERSION = 'v2';

    // Avoid
    export default function() { ... }
    ```

### Commit Patterns
- Commit types: `ignore`, `refactor`, `docs`, `feat`, `fix`
- Prefix commit messages with the type.
  - Example: `fix: correct provider locale mapping`
- Keep commit messages concise (~40 characters).

## Workflows

### Update Provider Docs Across Multiple Locales
**Trigger:** When you need to add or update provider documentation for all supported languages/locales.  
**Command:** `/update-provider-docs`

1. Edit or add the provider section in the main `providers.mdx` file:
    ```
    packages/web/src/content/docs/providers.mdx
    ```
2. Replicate the change across all locale-specific `providers.mdx` files:
    ```
    packages/web/src/content/docs/ar/providers.mdx
    packages/web/src/content/docs/bs/providers.mdx
    packages/web/src/content/docs/da/providers.mdx
    packages/web/src/content/docs/de/providers.mdx
    packages/web/src/content/docs/es/providers.mdx
    packages/web/src/content/docs/fr/providers.mdx
    packages/web/src/content/docs/it/providers.mdx
    packages/web/src/content/docs/ja/providers.mdx
    packages/web/src/content/docs/ko/providers.mdx
    packages/web/src/content/docs/nb/providers.mdx
    packages/web/src/content/docs/pl/providers.mdx
    packages/web/src/content/docs/pt-br/providers.mdx
    packages/web/src/content/docs/ru/providers.mdx
    packages/web/src/content/docs/th/providers.mdx
    packages/web/src/content/docs/tr/providers.mdx
    packages/web/src/content/docs/zh-cn/providers.mdx
    packages/web/src/content/docs/zh-tw/providers.mdx
    ```
3. Ensure consistency and accuracy across all locales.
4. Commit your changes with a descriptive message, e.g.:
    ```
    docs: update provider docs for all locales
    ```

### Ignore or Update API Specs for Brainstorming
**Trigger:** When you want to save or ignore changes/ideas in the API specification without functional impact.  
**Command:** `/ignore-api-ideas`

1. Edit `packages/opencode/specs/v2/api.ts` with new ideas, notes, or non-functional changes.
    ```typescript
    // brainstorming: consider adding batch endpoints
    // TODO: evaluate impact on existing clients
    ```
2. Commit your changes with an `ignore` prefix in the message:
    ```
    ignore: add brainstorming notes to api spec
    ```
3. These commits are typically non-functional and used for ideation or documentation.

## Testing Patterns

- Test files follow the pattern: `*.test.*`
  - Example: `apiProvider.test.ts`
- Testing framework is **unknown**; check existing test files for conventions.
- Place tests alongside the code they cover or in dedicated test directories.
- Example test file structure:
    ```typescript
    // apiProvider.test.ts
    import { getUser } from './apiProvider';

    describe('getUser', () => {
      it('returns user data', () => {
        // test implementation
      });
    });
    ```

## Commands

| Command                | Purpose                                                        |
|------------------------|----------------------------------------------------------------|
| /update-provider-docs  | Update provider documentation across all supported locales      |
| /ignore-api-ideas      | Save or ignore brainstorming changes in the API specification  |
```
