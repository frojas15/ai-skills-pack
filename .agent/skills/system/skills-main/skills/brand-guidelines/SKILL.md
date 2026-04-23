---
name: brand-guidelines
description: Applies brand colors and typography to any artifact that benefits from consistent visual identity. Use when brand colors, style guidelines, visual formatting, or company design standards apply. Customize the brand section below with your own colors and fonts.
license: Complete terms in LICENSE.txt
---

# Brand Styling Skill

## Overview

Apply consistent brand identity and style to documents, presentations, and interfaces.

**Keywords**: branding, corporate identity, visual identity, post-processing, styling, brand colors, typography, visual formatting, visual design

## How to Customize

Replace the colors and fonts below with your own brand values. The defaults below are a neutral starting point.

## Brand Guidelines

### Colors

**Main Colors:**

- Dark: `#1a1a1a` — Primary text and dark backgrounds
- Light: `#fafafa` — Light backgrounds and text on dark
- Mid Gray: `#a3a3a3` — Secondary elements
- Light Gray: `#e5e5e5` — Subtle backgrounds

**Accent Colors:**

- Primary Accent: `#e07850` — Primary accent (buttons, links, highlights)
- Secondary Accent: `#5a9abf` — Secondary accent (info, secondary actions)
- Tertiary Accent: `#6b8f50` — Tertiary accent (success, positive states)

> **Customization note:** Replace these hex values with your organization's brand colors. Keep the same structure (dark, light, mid, accents) for consistency.

### Typography

- **Headings**: Sans-serif display font (default: system sans-serif with Arial fallback)
- **Body Text**: Readable serif or sans-serif (default: system serif with Georgia fallback)
- **Monospace**: For code and data (default: system monospace)

> **Customization note:** Replace with your brand fonts. Common choices:
> - Headings: Poppins, Inter, Geist, Outfit, Cabinet Grotesk
> - Body: Lora, Source Serif, Merriweather, system defaults
> - Always include fallback fonts for cross-system compatibility

## Features

### Smart Font Application

- Applies heading font to titles (24pt and larger)
- Applies body font to paragraph text
- Automatically falls back to system fonts if custom fonts are unavailable
- Preserves readability across all systems

### Text Styling

- Headings (24pt+): Display/heading font
- Body text: Body font
- Smart color selection based on background contrast
- Preserves text hierarchy and formatting

### Shape and Accent Colors

- Non-text shapes use accent colors
- Cycles through primary, secondary, and tertiary accents
- Maintains visual interest while staying on-brand

## Technical Details

### Font Management

- Uses system-installed fonts when available
- Provides automatic fallback to system defaults
- No font installation required — works with existing system fonts
- For best results, pre-install your brand fonts in your environment

### Color Application

- Uses RGB/hex color values for precise brand matching
- Maintains color fidelity across different systems and platforms
- Works with any document generation library (python-pptx, docx, PDF generators, CSS)
