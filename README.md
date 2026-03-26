# Schemas

The collection of schemas used in custom projets, including the `theme-config.json` schemas.

JSON schemas are used by code editors to offer tooltips, autocomplete, and validation.

## JSON schema usage

Many editors recognize the `$schema` property in JSON files.

Update your `theme-config.json` to include:

```json
{
 "$schema": "https://raw.githubusercontent.com/noveni/wp-rusty-cat-schemas/refs/heads/3.3.0/schemas/theme-config.json"
}
```

## How to update the schema

The schema is versioned by branch, matching the `wp-rusty-spotted-cat` version.

**When adding or modifying schema properties:**

```bash
# 1. Make sure you're on the right version branch
git checkout 3.3.0

# 2. Edit schemas/theme-config.json

# 3. Commit and push
git add schemas/theme-config.json
git commit -m "feat: describe what you added"
git push origin 3.3.0
```

**When a new version of `wp-rusty-spotted-cat` is released (e.g. 3.4.0):**

```bash
# 1. Create a new branch from the current one
git checkout 3.3.0
git checkout -b 3.4.0

# 2. Make your schema changes, then push the new branch
git push origin 3.4.0

# 3. Update the $schema URL in this README and in your projects' theme-config.json
```

> The `$schema` URL uses the branch name, so existing projects pinned to an older branch are unaffected when a new version branch is created.
