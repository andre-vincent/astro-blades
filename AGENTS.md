# AGENTS.md

This file provides guidance to coding agents when working with code in this repository.

## Commands

```shell
npm run dev        # start dev server
npm run build      # type-check (astro check) then build
npm run check      # type-check only
npm run preview    # preview production build
npm run format     # format with Prettier
```

Any Node package manager works. The project includes `mise.toml` for Node version management (requires Node ^22, ^24, or ^26).

## Architecture

This is an Astro 7 static site template (single-author blog + personal site). No client-side JavaScript or cookies; everything renders to static HTML.

**Styling:** Pico CSS v2 via SCSS. `src/styles/main.scss` controls which Pico modules are included. The theme uses minimal custom CSS and avoids CSS classes in favour of semantic HTML elements.

**Path aliases** (defined in `tsconfig.json`):
- `@components/*` → `src/components/`
- `@layouts/*` → `src/layouts/`
- `@styles/*` → `src/styles/`
- `@utils/*` → `src/utils/`
- `~/*` → `src/`

**Content:** Blog posts live in `src/content/blog/` as Markdown files. Required frontmatter: `title`, `description`, `pubDate`. Optional: `tags`. The file path becomes the post URL. Content schema is defined in `src/content.config.ts` using Astro's glob loader.

**Tags:** Tags are slugified via `tagToSlug()` in `src/utils/tags.ts` (non-alphanumeric chars → hyphens). Tag pages are generated dynamically from `src/pages/tags/[id].astro`.

**Layouts:**
- `Base.astro` — wraps all pages; accepts optional `title`, `description`, `ogType` props
- `BlogPost.astro` — wraps blog post content; receives typed `CollectionEntry<"blog">["data"]` props

**Site config:** `src/settings.ts` exports `siteConfig` with title, description, lang, favicon path, and Open Graph image settings. Edit this to customise the site identity.

**Navigation:** Managed directly in `src/components/PageHeader.astro`.

**Templates:** `src/templates/` contains starter files for new pages (`page.astro`) and posts (`post.md`).

**RSS:** Auto-generated at `/rss.xml` via `src/pages/rss.xml.js`.
