# Schemas

The collection of schemas used in custom projets, including the `theme-config.json` schemas.

JSON schemas are used by code editors to offer tooltips, autocomplete, and validation.

## JSON schema usage

Many editors recognize the `$schema` property in JSON files.

Update your `theme-config.json` to include:

```json
{
 "$schema": "https://raw.githubusercontent.com/noveni/wp-rusty-cat-schemas/refs/heads/3.2.0/schemas/theme-config.json"
}
```
