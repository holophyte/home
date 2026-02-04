# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the landing page for holophyte.ai, built with Astro and Tailwind CSS v4. The project uses Bun as the package manager and runtime.

## Development Commands

```bash
# Install dependencies
bun install

# Start development server
bun run dev

# Build for production
bun run build

# Preview production build
bun run preview
```

## Architecture

This is a single-page Astro application with a component-based architecture:

- **Entry point**: `src/pages/index.astro` - assembles all components in order
- **Layout**: `src/layouts/Layout.astro` - base HTML structure, includes global styles and fonts
- **Components**: `src/components/` - modular sections (Nav, Hero, Features, About, GardenTeaser, Footer)
- **Styling**: `src/styles/global.css` - global Tailwind styles; Tailwind v4 configured via Vite plugin in `astro.config.mjs`

The application uses:
- Astro 5.x for static site generation
- Tailwind CSS v4 (via `@tailwindcss/vite` plugin)
- lucide-astro for icons
- TypeScript with strict null checks enabled

## Deployment

The site is configured for Netlify deployment:
- Build command: `bun run build`
- Publish directory: `dist`
- SPA fallback configured for client-side routing
