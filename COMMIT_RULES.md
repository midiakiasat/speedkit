# Commit Rules

## Allowed Verbs

Commits must use declarative verbs only:

- `add` - Add new system or file
- `freeze` - Lock version or state
- `append` - Append-only additions
- `retire` - Remove system or file

## Prohibited Verbs

Do not use:

- `improve`
- `update`
- `refactor`
- `fix`
- `enhance`
- `optimize`

## Format

Commits must be declarative, not descriptive.

**Correct:**
- `freeze: speedkit execution index v1.0`
- `add: system-name to index`
- `append: new-system documentation`

**Incorrect:**
- `update README with new information`
- `improve system documentation`
- `refactor index structure`

## Merge Policy

No squash merges. History must remain linear and visible.
