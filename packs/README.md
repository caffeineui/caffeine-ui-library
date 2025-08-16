# Asset Packs

This directory contains template-specific asset packs, organized by industry category. Each pack includes assets for a specific template or template family.

## Directory Structure

Asset packs are organized in a two-level hierarchy:

```
/packs/
  /<category>/
    /<template-name>/
      - pack.json
      - CREDITS.md
      - other template-specific assets
```

Categories include:

- **music** - Assets for music industry templates
- **food** - Assets for food industry templates
- **photography** - Assets for photography templates
- **professional** - Assets for professional services templates

## Adding a New Template Pack

1. Determine which category your template belongs to
2. Create a directory under that category with your template name (in kebab-case)
3. Add a `pack.json` file with metadata and asset references
4. Add a `CREDITS.md` file for third-party assets used in this template

See the main README.md for more details on how to use and contribute to packs.
