# Caffeine UI Library

Official asset library for Caffeine UI templates (images, icons, fonts, 3D, audio/video). No application code in this repo.

## What's inside

- **/images/** - Brand logos, photography, and textures
- **/icons/** - Monochrome, duotone, and color icons
- **/fonts/** - Typography assets and font files
- **/models/** - 3D models in various formats (GLB, GLTF, OBJ, FBX)
- **/audio/** - Sound effects and audio loops
- **/video/** - Video clips and overlay elements
- **/meta/** - Sample thumbnails and templates for documentation

## How to use

- You may use assets under CC BY 4.0 unless otherwise marked in the asset's `CREDITS.md` and in `NOTICE.md`.
- You must preserve attribution required by each asset.
- See [LICENSE.md](LICENSE.md) for full license details.
- If an asset has stricter terms, those terms control for that asset.

## Attribution

- All third-party assets and their attributions are listed in [NOTICE.md](NOTICE.md).
- Each asset folder MUST include a `CREDITS.md` describing source, license, author, changes, and required attribution text.

## Contributing assets

1. Create a new folder under the correct category (see structure).
2. Add the files (optimize if possible).
3. Create `CREDITS.md` using the template below.
4. Update `NOTICE.md` with the same entry.
5. If the license requires including a license file, add it inside the asset's folder as `LICENSE-THIRD-PARTY.txt`.
6. Open a PR.

**CREDITS.md** template:

```
# CREDITS

* Asset Name: <name>
* Source: <URL>
* Author: <name/org>
* License: <e.g., CC BY 4.0> (link to license)
* Changes: <what you changed>
* Required attribution: "<exact text user must include>"
```

## Large files / Git LFS

This repo uses Git LFS for large binaries (images, models, audio/video). Install LFS before cloning/pushing.

## Trademark

Logos and marks may be subject to trademark rights. Use responsibly.

## Contact

For takedowns or license questions: <add contact email when ready>

## Asset Packs System

As the library scales to many templates, we use a "packs" system to keep assets organized and attributions clear.

### Packs vs Shared

- **/packs/\<slug\>/...** = Per-template assets + `pack.json` manifest
- Root folders (**/images**, **/icons**, etc.) = Shared assets usable across packs

### 1) Namespacing by "asset pack"

Add one more top-level layer that groups assets by the template (or family) they belong to:

```
/packs/
  /minimal-studio/                 # template (pack) slug
    pack.json                      # manifest (see below)
    /images/…                      # only the assets this template needs
    /icons/…
    /fonts/…
    /models/…
    /audio/…
    /video/…
    CREDITS.md                     # roll-up credits for this pack
    LICENSE-THIRD-PARTY.txt        # optional, if required by sources
  /astrolux-landing/
    pack.json
    /images/…
    …
```

### 2) One manifest per pack

Each pack includes a JSON manifest that templates can read to know where to load assets:

**`pack.json` Schema:**

```json
{
  "name": "Minimal Studio",
  "slug": "minimal-studio",
  "version": "1.0.0",
  "updated": "2025-08-15",
  "assets": [
    {
      "id": "hero-bg-blur",
      "type": "image",
      "path": "images/hero/hero-blur-1600w.webp",
      "hash": "sha256-...optional...",
      "license": "CC BY 4.0",
      "source": "https://example.com/…",
      "author": "Author Name",
      "attribution": "© Author Name, used under CC BY 4.0",
      "notes": "Blurred and color-graded"
    },
    {
      "id": "logo-mark",
      "type": "svg",
      "path": "../../images/brand/caffeine-mark.svg",
      "license": "Caffeine UI trademark — restricted use",
      "source": "internal",
      "author": "Caffeine UI"
    }
  ]
}
```

- `path` is relative to the pack folder. You can reference shared root assets with `../..`.
- Add `hash` if you want integrity checks or cache-busting.

### 3) Naming Conventions

- **Templates/packs:** `kebab-case` (e.g., `minimal-studio`, `astrolux-landing`)
- **Files:** `descriptor-width.ext` for raster (e.g., `hero-blur-1600w.webp`)
- **Vectors:** `descriptor.svg` (`logo-mark.svg`, `icon-close-24.svg`)
- **3D:** `objectName-scale.glb` (`capsule-high.glb`)
- **Audio:** `sfx-whoosh-fast-120bpm.wav`
- **Preview thumbs:** put tiny `*.webp` in `meta/samples/` and reference from `pack.json`

### 4) Credits Structure

- Each **pack** has a `CREDITS.md` (roll-up)
- Each **third-party asset**: add an entry to the pack's `CREDITS.md` _and_ to root `NOTICE.md`
- If a license requires including the full text, add `LICENSE-THIRD-PARTY.txt` next to the asset

### 5) Asset Storage Options

- **Pack-local assets:** place them inside `/packs/<slug>/…` and list in that pack's manifest
- **Shared assets:** store once in root category folders, then reference from `pack.json`

### 6) Versioning Policy

- Bump `pack.json` `version` when changing or swapping assets
- If replacing a file while avoiding breaking older templates, add a new file with a versioned name (e.g., `hero-blur-1920w-v2.webp`) and mark the old one as `"deprecated": true` in the manifest

### 7) VS Code Workflow

To create a new template pack, run this in your AI assistant from repo root:

```
Create a new template asset pack with slug "<your-slug>" under /packs.
Folders: images, icons, fonts, models, audio, video (only create the ones I need; include .keep files for empty).
Create packs/<your-slug>/pack.json using the schema from README with empty "assets": [] and default version 1.0.0.
Create packs/<your-slug>/CREDITS.md using the repo template. Do not add any third-party entries yet.
```

### 8) Adding Assets to a Pack

To add an asset to a pack:

```
I've placed a file at packs/minimal-studio/images/hero/hero-blur-1600w.webp.
Add this entry to packs/minimal-studio/pack.json "assets":
- id: hero-bg-blur
- type: image
- path: images/hero/hero-blur-1600w.webp
- license: CC BY 4.0
- source: https://sketchfab.com/… (example)
- author: Jane Doe
- attribution: "© Jane Doe, used under CC BY 4.0"
- notes: Converted to WebP, color graded.
Also append the same info to packs/minimal-studio/CREDITS.md and to root NOTICE.md.
```

### 9) Automations

- You can add validation scripts to ensure each `pack.json` entry has a matching file and a corresponding entry in `NOTICE.md`

## Template Creation Guide

For developers creating templates that use Caffeine UI assets, please refer to:

- [Template Creation Guide](/docs/TEMPLATE_GUIDE.md) - Step-by-step guide for creating new templates
- [Template Index](/docs/TEMPLATE_INDEX.md) - Catalog of all existing templates
