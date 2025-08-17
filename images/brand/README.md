# Caffeine UI Brand Assets

This directory contains the official branding assets for Caffeine UI templates.

## Directory Structure

- `/logo` - Official Caffeine UI logos in various formats and sizes
- `/favicon` - Favicon files for web applications and templates

## Usage Guidelines

### Logos

- Use the full color logo on light backgrounds
- Use the white logo on dark backgrounds
- Always maintain proportions when resizing
- Maintain adequate clear space around the logo
- Use SVG format when possible for best quality

### Favicons

#### Current Files
- `favicon.ico` - Standard favicon file
- `favicon.svg` - Vector version (preferred when supported)
- `favicon-96x96.png` - 96×96 PNG version
- `apple-touch-icon.png` - For iOS devices
- `android-chrome-192x192.png` - For Android devices
- `android-chrome-512x512.png` - For Android devices
- `site.webmanifest` - Web app manifest file

#### To Be Added
- `favicon-16x16.png` - 16×16 PNG version (create from favicon-96x96.png)
- `favicon-32x32.png` - 32×32 PNG version (create from favicon-96x96.png)

You can create these using any image editing tool by resizing the 96×96 version.

## Standard Integration

### HTML Header Integration

```html
<!-- Favicon -->
<link
  rel="apple-touch-icon"
  sizes="180x180"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/apple-touch-icon.png"
/>
<!-- Add these once you've created them:
<link
  rel="icon"
  type="image/png"
  sizes="32x32"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon-32x32.png"
/>
<link
  rel="icon"
  type="image/png"
  sizes="16x16"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon-16x16.png"
/>
-->
<link
  rel="icon"
  type="image/png"
  sizes="96x96"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon-96x96.png"
/>
<link
  rel="icon"
  type="image/svg+xml"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon.svg"
/>
<link
  rel="manifest"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/site.webmanifest"
/>
<link
  rel="shortcut icon"
  href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon.ico"
/>
```

### Logo Integration

```html
<!-- Logo -->
<img
  src="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/logo/caffeine-ui-logo-full.svg"
  alt="Caffeine UI"
/>
```

## Branding Requirements

All templates must include:

1. The Caffeine UI logo in the footer or credits section
2. The text "Powered by Caffeine UI" next to the logo
3. Favicons for proper browser/device integration

## File Formats

- SVG: Vector format for logos (preferred for web use)
- PNG: Raster format with transparency
- ICO: For favicons
- WEBP: For optimized web use
