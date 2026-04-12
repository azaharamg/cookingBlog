# Cooking Blog

Blog de recetas de cocina built with **Astro 5** + **React** + **Tailwind CSS v4**.

## Stack

- **Astro 5** - Static site generator
- **React** - Interactive components
- **Tailwind CSS v4** - Styling (via `@tailwindcss/vite`)
- **Content Collections** - Recipe data management

## Project Structure

```
src/
├── recipes/           # Recetas en markdown (Content Collection)
├── pages/             # Astro pages/routes
│   ├── index.astro    # Homepage
│   ├── menu-semanal.astro
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

- Recetas en `src/recipes/*.md` con frontmatter: `title`, `pubDate`, `description`, `category`, `image`
- Schema definido en `src/content.config.ts`

## Custom Theme Colors

Colors defined in `src/styles/global.css`:
- `--color-cream` (#faf6f1) - Background
- `--color-terracotta` (#c4654a) - Primary accent
- `--color-sage` (#7d9471) - Secondary accent
- `--color-olive` (#5c5c3d) - Hover states
- `--color-charcoal` (#2d2926) - Text