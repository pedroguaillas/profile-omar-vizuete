# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development

Dev server runs at `localhost:4321`. Always start in background mode:

```sh
astro dev --background
```

Manage with: `astro dev stop`, `astro dev status`, `astro dev logs`.

Build and preview:

```sh
npm run build
npm run preview
```

Type-check:

```sh
npm run astro check
```

## Architecture

Astro 7 project — file-based routing, zero JS by default, component islands when interactivity needed.

- `src/pages/` — each `.astro` file is a route. `index.astro` is `/`.
- `src/layouts/` — shell wrappers using `<slot />` for content injection. `Layout.astro` is the base HTML shell.
- `src/components/` — reusable `.astro` components (or framework components if added).
- `src/assets/` — images/SVGs processed by Astro's asset pipeline (import directly in `.astro` files).
- `public/` — static files served as-is (favicons, fonts, etc.).

No UI framework (React/Vue/Svelte) installed yet. Add via `astro add <framework>` if needed.

Tailwind v4 installed via `@tailwindcss/vite`. Global styles in `src/styles/global.css`, imported in `Layout.astro`.

## Documentation

Full docs: https://docs.astro.build

Key guides:
- [Routing](https://docs.astro.build/en/guides/routing/)
- [Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Framework components](https://docs.astro.build/en/guides/framework-components/)
- [Content collections](https://docs.astro.build/en/guides/content-collections/)
- [Styling / Tailwind](https://docs.astro.build/en/guides/styling/)
- [i18n](https://docs.astro.build/en/guides/internationalization/)
