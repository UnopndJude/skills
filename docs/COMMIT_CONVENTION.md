# Git Commit Message Convention

This repository follows the **Conventional Commits** specification with customizations for Claude Skills.

## Format

```
<type>(<skill-name>): <subject>

[optional body]

[optional footer(s)]
```

## Type

The type must be one of the following:

- **feat**: A new skill or feature addition
- **fix**: A bug fix in an existing skill
- **docs**: Documentation only changes
- **refactor**: Code refactoring that neither fixes a bug nor adds a feature
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **chore**: Changes to build process, dependencies, or configuration files

## Scope

The scope must be the **skill name** (e.g., `calculator`, `weather`, `translator`). This helps identify which skill the commit affects.

## Subject

- Use imperative, present tense: "add" not "added" nor "adds"
- Don't capitalize the first letter
- No period (.) at the end
- Maximum 72 characters

## Examples

### Adding a new skill
```
feat(calculator): add basic arithmetic operations
```

### Fixing a bug
```
fix(weather): resolve API timeout issue
```

### Updating documentation
```
docs(translator): update usage examples
```

### Refactoring
```
refactor(calculator): improve error handling logic
```

### Performance improvement
```
perf(weather): optimize API response caching
```

### Adding tests
```
test(calculator): add unit tests for division
```

### Maintenance
```
chore: update dependencies
```

## Multi-line Format

For more detailed commits, use the following format:

```
feat(calculator): add scientific calculator functions

Add support for trigonometric functions (sin, cos, tan)
and logarithmic operations. This extends the basic
calculator with advanced mathematical capabilities.

Closes #123
```

## Rules

1. **Type is required** and must be one of the specified types
2. **Scope is required** and must be a valid skill name
3. **Subject is required** and must be in imperative mood
4. **Body is optional** but recommended for complex changes
5. **Footer is optional** for breaking changes or issue references

## Breaking Changes

If a commit introduces a breaking change, add `BREAKING CHANGE:` in the footer:

```
feat(calculator): change API interface

BREAKING CHANGE: The calculate() method now requires
a configuration object instead of individual parameters.
```

