# Recipe Blog

A recipe blog built with **Astro 5** + **React** + **Tailwind CSS v4**.

## Stack

- **Astro 5** - Static site generator
- **React** - Interactive components
- **Tailwind CSS v4** - Styling (via `@tailwindcss/vite`)
- **Content Collections** - Recipe data management

## Project Structure

```
src/
├── recipes/           # Markdown recipes (Content Collection)
├── pages/             # Astro pages/routes
│   ├── index.astro    # Homepage
│   ├── recetas/[category].astro
│   └── recipes/[...slug].astro
├── components/        # Astro & React components
├── layouts/           # Page layouts
└── styles/            # Global CSS
```

## Commands

| Command           | Action                                      |
| :---------------- | :------------------------------------------ |
| `npm install`     | Installs dependencies                       |
| `npm run dev`     | Starts dev server at `localhost:4321`      |
| `npm run build`   | Build production site to `./dist/`          |
| `npm run preview` | Preview build locally                      |

## Content Collections

Recipes in `src/recipes/*.md` with the following required frontmatter:

```yaml
---
title: "Recipe Title"
pubDate: 2026-01-01
category: kids | traditional | desserts
---
```

Recipe content goes in markdown below the frontmatter.

## Contributing

To add a recipe:

1. Fork the repository
2. Create a file in `src/recipes/your-recipe.md`
3. Add the required frontmatter and markdown content
4. Submit a Pull Request

### Guidelines

- File name should be descriptive (e.g. `pure-de-merluza.md`)
- Images go in `public/images/`
- Categories: `kids` (children recipes), `traditional`, `desserts`

## Custom Theme Colors

Colors defined in `src/styles/global.css`:
- `--color-cream` (#faf6f1) - Background
- `--color-terracotta` (#c4654a) - Primary accent
- `--color-sage` (#7d9471) - Secondary accent
- `--color-olive` (#5c5c3d) - Hover states
- `--color-charcoal` (#2d2926) - Text

## Deploy

Deploy to [Render](https://render.com) as Static Site:

- **Build Command**: `npm install && npm run build`
- **Publish Directory**: `dist`