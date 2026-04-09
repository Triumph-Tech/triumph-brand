# Triumph Brand

This repository is the single source of truth for Triumph Tech's brand assets and guidelines. It is designed to be consumed by agents and automation tools to produce consistently branded work.

## Contents

| Path | Description |
|---|---|
| `brand-kit.json` | Machine-readable brand data — colors, typography, logos, voice, and more |
| `brand-guidelines.md` | Human and agent-readable guidelines — tone, logo usage, and writing rules |
| `fonts/` | Goldman Sans font files (self-hosted) |
| `logos/` | SVG logo files — combination mark, logo mark, wordmark, and Digital Revival |
| `mascot/magnus/` | Magnus mascot assets |
| `assets/embellishments/` | Decorative brand elements |
| `guidelines/` | Official brand guidelines PDF |

## brand-kit.json Structure

```json
{
  "brand": {
    // Company name, tagline, website, and brand initiatives (e.g. Digital Revival)
  },
  "colors": {
    "primary":    // Invictus Blue — main brand color with 3 tones, RGB, CMYK, and text_on values
    "secondary":  // Electric Blue — accents and highlights
    "accent":     // Twilight Blue — backgrounds and UI elements
    "grayscale":  // 8-step grayscale scale
    "semantic":   // Success, warning, error, info (to be defined)
  },
  "typography": {
    "primary":    // Goldman Sans — sole authorized typeface, all weights with file paths
  },
  "logos": {
    "combination_mark":  // Icon + wordmark — primary logo (light and dark)
    "logo_mark":         // Icon only (light and dark)
    "wordmark":          // Text only (light and dark)
    "digital_revival":   // Digital Revival initiative logo (light and dark)
    "clearspace":        // Clearspace rule
    "backgrounds":       // Approved background colors and restrictions
  },
  "mascot": {
    // Magnus — name, description, and asset paths
  },
  "voice": {
    // Summary, tone descriptors, words to avoid, example phrases
  },
  "usage": {
    // Dos and don'ts
  },
  "brand_elements": {
    "image_wash":  // Layer specs for the Invictus Blue image treatment
  }
}
```
