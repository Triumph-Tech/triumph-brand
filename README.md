# Triumph Brand

This repository is the single source of truth for Triumph Tech's brand assets and guidelines. It is designed to be consumed by agents and automation tools to produce consistently branded work.

## Repository Structure

| Path | Description |
|---|---|
| `brand-kit.json` | Machine-readable brand data — colors, typography, logos, personas, locations, and more |
| `brand-guidelines.md` | Human and agent-readable guidelines — tone, logo usage, and writing rules |
| `brand-review.html` | Visual reference page for all brand assets |
| `fonts/` | Goldman Sans font files (self-hosted) |
| `logos/` | Triumph Tech logo lockups — combination mark, logo mark, wordmark, and avatar |
| `sub-brands/` | Sub-brand logo assets — Digital Revival and Rock Cloud |
| `assets/embellishments/` | Blueprint-style decorative brand elements |
| `assets/personas/` | Persona assets — Magnus mascot and leader avatars |
| `samples/` | Sample files and usage examples |
| `guidelines/` | Official brand guidelines PDF |

## brand-kit.json Structure

```json
{
  "version": "2026.04",
  "base_url": "https://branding.triumph.tech",

  "brand": {
    // Company name, tagline, website
  },

  "locations": [
    // Mailing address (Peoria, AZ) and office address (Surprise, AZ)
    // Each entry: type, street, city, state, zip, country, lat, lng
  ],

  "sub_brands": [
    // Array of sub-brand entries, each with: id, type, name, description, tagline, website, logos.assets[]
    // digital_revival — campaign brand
    // rock_cloud      — Triumph's fully hosted Rock RMS platform
  ],

  "color_system": {
    "palette": {
      "primary":   // Invictus Blue (#0A2540) — main brand color, 3 tones, RGB, CMYK, text_on
      "secondary": // Electric Blue (#4BA9DF) — accents and highlights, 3 tones
      "accent":    // Twilight Blue (#5D758B) — backgrounds and UI elements, 3 tones
    },
    "interface": {
      // 7-step neutral scale: softest → strongest
      // Inverts symmetrically in dark mode
    },
    "semantic": {
      // success, warning, danger, info
      // Each has forecolor and background with light/dark values
    }
  },

  "typography": {
    "primary": // Goldman Sans — sole authorized typeface, all weights with file paths
  },

  "radius": {
    // none (0px), sm (4px), md (8px), lg (12px), xl (16px)
    // Each has a value and usage description
  },

  "logos": {
    "lockups": [
      // Array of logo lockup entries, each identified by type:
      // combination_mark — icon + wordmark (primary logo)
      // logo_mark        — icon only (avatars, favicons, small spaces)
      // wordmark         — text only
      // avatar           — square/round org avatar for directories and profiles
      // Each lockup contains an assets[] array with SVG and PNG variants at 256/512/1024
    ],
    "rules": [
      // Logo usage rules for agents and designers
    ]
  },

  "voice": {
    // summary, tone descriptors, words to avoid, example phrases
  },

  "brand_elements": {
    "embellishments": {
      // Blueprint-style decorative elements: web, arc, registration, gear
      // SVG + PNG at 256/512/1024 for each
    },
    "image_wash": {
      // Layer spec for the branded Invictus Blue photo treatment
      // Desaturate to 0%, then 15% opacity Invictus Blue overlay (Luminosity blend)
    }
  },

  "personas": [
    // Array of persona entries, each with: id, type, name, assets[]
    //
    // Mascot:
    //   magnus        — robot mascot, SVG variants (full_body, head, icon)
    //
    // Leaders (type: "leader") — partner headshots, PNG avatars at 256/512/1024:
    //   emily_forman  — Partner
    //   jon_edmiston  — Partner
    //   nick_airdo    — Partner
  ],

  "rules": [
    // Top-level agent directives for using this brand kit
  ]
}
```

## Asset Conventions

**Variants:** Every asset entry includes a `variant` field — `light`, `dark`, `transparent`, or a descriptive label (e.g., `full_body`, `avatar`).

**Sizes:** PNG assets are provided at 256, 512, and 1024 px.

**File paths:** All paths are relative to the repository root and match the physical directory structure.

**Logo usage:** Light variants are for use on dark backgrounds; dark variants are for use on light backgrounds. Prefer SVG for all vector and programmatic use.
