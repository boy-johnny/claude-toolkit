# Design Studio Plugin

Create distinctive, production-grade frontend interfaces that avoid generic AI aesthetics.

## Overview

The Design Studio Plugin helps you create beautiful, memorable frontend interfaces. It provides both an explicit command (`/design`) and an auto-activating skill that guides Claude toward creative, distinctive designs instead of generic AI-generated output.

## Command

### `/design [description]`

Explicitly invoke the design workflow to create frontend interfaces.

**Usage:**
```bash
/design A dashboard for a music streaming app
/design Landing page for an AI security startup
/design Settings panel with dark mode toggle
/design E-commerce product card with hover effects
```

## Skill

The `frontend-design` skill automatically activates when you ask Claude to:
- Build web components
- Create pages or applications
- Design interfaces or UI elements

It guides Claude toward creative, polished output without needing explicit commands.

## Design Philosophy

### Avoid "AI Slop" Aesthetics

Generic AI output often includes:
- Overused fonts (Inter, Roboto, Arial)
- Purple gradients on white backgrounds
- Predictable layouts
- Cookie-cutter patterns

This plugin explicitly steers away from these clichés.

### Embrace Distinctive Design

Every design should have:
- **Clear aesthetic direction**: Brutalist, minimalist, maximalist, retro, etc.
- **Memorable typography**: Distinctive font choices that elevate the design
- **Bold color choices**: Dominant colors with sharp accents
- **Purposeful motion**: High-impact animations at key moments
- **Visual texture**: Gradients, patterns, shadows that create atmosphere

## Typography Guide

### Never Use
- Inter, Roboto, Arial, Open Sans
- System fonts
- Generic sans-serifs

### Recommended Choices

| Style | Fonts |
|-------|-------|
| Code aesthetic | JetBrains Mono, Fira Code, Space Grotesk |
| Editorial | Playfair Display, Crimson Pro, Fraunces |
| Startup | Clash Display, Satoshi, Cabinet Grotesk |
| Technical | IBM Plex family, Source Sans 3 |
| Distinctive | Bricolage Grotesque, Obviously, Newsreader |

## Color Guidelines

- Use CSS variables for consistency
- Commit to a cohesive theme
- Dominant + accent > evenly distributed
- Draw from IDE themes, art movements, cultural aesthetics

## Motion Best Practices

- CSS-only animations when possible
- Staggered page load reveals
- Surprising hover states
- Smooth, purposeful transitions
- One orchestrated moment > scattered micro-interactions

## Examples

### Minimalist Dashboard
```
/design Minimalist analytics dashboard with monochrome theme
```
→ Refined typography, generous whitespace, subtle data visualization

### Maximalist Landing
```
/design Bold landing page for a creative agency
```
→ Overlapping elements, dynamic animations, strong color contrasts

### Retro Interface
```
/design 90s-inspired settings panel
```
→ Pixel fonts, beveled edges, nostalgic color palette

## Learn More

See the [Frontend Aesthetics Cookbook](https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb) for detailed guidance on prompting for high-quality frontend design.

## Author

GOODA

## Version

1.0.0
