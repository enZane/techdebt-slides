# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Slidev presentation project for a technical debt presentation using the Neversink theme. Slidev is a slide presentation framework that uses Markdown to create slides with Vue.js components and modern web technologies. The project uses the Neversink theme which provides educational and academic presentation layouts with bright, flat, minimal design.

## Development Commands

**Install dependencies:**
```bash
pnpm install
```

**Start development server:**
```bash
pnpm dev
```
Opens the presentation at http://localhost:3030 with live reload and presenter mode.

**Build for production:**
```bash
pnpm run build
```
Outputs static files to `dist/` directory for deployment.

**Export presentation:**
```bash
pnpm run export
```
Exports slides to PDF or other formats.

## Working with Slides

- **Main content:** Edit `slides.md` to create your presentation content
- **Slide structure:** Each slide is separated by `---`
- **Frontmatter:** Configure presentation settings at the top of `slides.md`
- **Theme:** Currently using `neversink` theme with `color: pink` setting
- **Navigation:** Use arrow keys, space, or click navigation in presentation mode

## Architecture

- `slides.md` - Main presentation content and configuration
- `components/` - Custom Vue components for slides (Counter.vue example included)
- `snippets/` - TypeScript code examples that can be imported into slides
- Uses UnoCSS for utility-first styling
- Supports interactive elements, animations, code highlighting, and diagrams

## Neversink Theme Features

### Layouts Available
- `cover` - Title slide with optional note slot
- `intro` - Simple introduction layout
- `default` - Basic content layout
- `section` - Section divider slides
- `quote` - Quote slides with author attribution
- `full` - Full-screen layout for custom arrangements
- `two-cols-title` - Two-column layout with title
- `top-title` - Title at top with content below
- `top-title-two-cols` - Top title with two-column content
- `side-title` - Side title with main content area
- `image-left/right` - Image layouts
- `iframe-left/right` - Embedded website layouts
- `credits` - Movie-style scrolling credits

### Color Schemes
Extensive color options including: `black`, `white`, `dark`, `light`, `slate`, `gray`, `red`, `orange`, `amber`, `yellow`, `lime`, `green`, `emerald`, `teal`, `cyan`, `sky`, `blue`, `indigo`, `violet`, `purple`, `pink`, `rose`, `fuchsia`, `navy`

Each color has `-light` variants (e.g., `pink-light`, `sky-light`)

### Custom Components
- `<StickyNote>` - Draggable sticky notes with customizable colors
- `<SpeechBubble>` - Speech bubbles with different positions and animations
- `<Admonition>` - Call-out boxes with titles and color schemes
- `<AdmonitionType>` - Pre-styled admonitions (note, tip, warning, etc.)
- `<QRCode>` - QR code generation
- Kawaii icons: `<IceCream>`, `<BackPack>`, `<Cat>`, `<Browser>`, `<Mug>`, etc.

### Standard Slidev Features
- Code syntax highlighting with TypeScript support
- Animation and transition effects (`v-click`, `v-motion`)
- Mermaid and PlantUML diagram support
- LaTeX math rendering
- Built-in Monaco editor for live coding
- Drawing and annotation tools (`v-drag`)
- Presenter notes and presenter mode

## Neversink Layout Configuration

Most layouts support frontmatter options:
- `color` - Color scheme (e.g., `pink`, `sky-light`, `navy`)
- `align` - Alignment settings (e.g., `l-lt-lt` for left-left-top-left-top)
- `columns` - Column width settings (e.g., `is-6` for 6/12 column width)
- `titlewidth` - Title section width for side layouts
- `side` - Side positioning (`l` or `r` for left/right)

## Example Frontmatter

```yaml
---
layout: side-title
color: emerald-light
align: rm-lm
titlewidth: is-3
side: l
---
```

## Deployment

Configured for Netlify deployment with Node.js 20. Also supports Vercel deployment via `vercel.json`.