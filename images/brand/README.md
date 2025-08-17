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

- Use `favicon.ico` for standard favicon
- Use appropriate sizes for different platforms:
  - `favicon-16x16.png` - For standard use
  - `favicon-32x32.png` - For standard use
  - `apple-touch-icon.png` (180×180) - For iOS devices
  - `android-chrome-192x192.png` - For Android devices
  - `android-chrome-512x512.png` - For Android devices

## Standard Integration

### HTML Header Integration

```html
<!-- Favicon -->
<link rel="apple-touch-icon" sizes="180x180" href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon-16x16.png">
<link rel="manifest" href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/site.webmanifest">
<link rel="shortcut icon" href="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/favicon/favicon.ico">
```

### Logo Integration

```html
<!-- Logo -->
<img src="https://raw.githubusercontent.com/caffeineui/caffeine-ui-library/main/images/brand/logo/caffeine-ui-logo-full.svg" alt="Caffeine UI">
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
