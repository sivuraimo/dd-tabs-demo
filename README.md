# DD Astro Template

Blank starter for static sites on Astro + SCSS + GSAP. SEO, adaptive scaling and the folder
structure are already set up — create a project from it and start building sections.

## Start a new site

```sh
npm create astro@latest -- --template sivuraimo/DD-Astro-Template
```

The wizard asks for a folder name, installs dependencies and offers to run `git init`. The new
project gets its own clean history — nothing from this repo's commits comes along.

Then tell the agent:

> Read AGENTS.md and set up the template for project X.

It will walk through the setup checklist (domain, name, og-image, favicon, colors, font) and ask
for anything it doesn't know. After that, build the site section by section: one design block →
one section component.

## Commands

| Command                | Action                           |
| :--------------------- | :------------------------------- |
| `npm run dev`          | Dev server at `localhost:4321`   |
| `npm run build`        | Build to `dist/`                 |
| `npm run preview`      | Preview the build                |
| `npm run format`       | Format everything with Prettier  |
| `npm run format:check` | Check formatting without writing |

## Structure

```text
src/
├── assets/          fonts and images (processed by astro:assets)
├── components/
│   ├── atoms/       small reusable pieces, one folder per atom
│   └── sections/
│       ├── global/  header, footer, anything shared across pages
│       └── home/    sections of the home page (one folder per page)
├── data/            texts, lists and site settings — the future CMS layer
├── layouts/         Layout.astro: meta, SEO, global styles
├── pages/           routes, 404, robots.txt
├── scripts/         client scripts (gsap.ts registers plugins)
└── styles/          reset, global variables and typography, rem/em + breakpoint mixins
```

Conventions and rules for the agent live in [AGENTS.md](AGENTS.md).
