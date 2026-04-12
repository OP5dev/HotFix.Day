# HotFix.Day &middot; Fixes, Failures & the Future of DevOps

> [!TIP]
> Things break in production; we write about why. Incident analysis, infrastructure automation, CI/CD, observability, and open-source SRE tooling.

## File structure

```text
├── public/
├── src/
│   ├── assets/
│   │   └── fonts/
│   ├── components/
│   ├── content/
│   ├── layouts/
│   ├── pages/
│   └── styles/
├── astro.config.mjs
├── README.md
├── package.json
└── tsconfig.json
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

The `src/content/` directory contains "collections" of related Markdown and MDX documents. Use `getCollection()` to retrieve posts from `src/content/blog/`, and type-check your frontmatter using an optional schema. See [Astro's Content Collections docs](https://docs.astro.build/en/guides/content-collections/) to learn more.

Static assets like images and fonts are stored in `src/assets/` so Astro can optimize and bundle them at build time. Images are processed by [Sharp](https://sharp.pixelplumbing.com/) and converted to WebP. Fonts are managed via the [Astro Fonts API](https://docs.astro.build/en/guides/fonts/) with optimized fallbacks to minimize layout shift. Only favicons belong in `public/`.

## Commands

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `bun install`             | Installs dependencies                            |
| `bun run dev`             | Starts local dev server at `localhost:4321`      |
| `bun run build`           | Build your production site to `./dist/`          |
| `bun run preview`         | Preview your build locally, before deploying     |
| `bun run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `bun run astro -- --help` | Get help using the Astro CLI                     |

## Debugging

The project includes a `.vscode/launch.json` with pre-configured debug profiles. Open the **Run and Debug** panel (`Ctrl+Shift+D`) and select a configuration:

- **Dev:** starts `bun run dev` with the VS Code debugger attached. Set breakpoints in `.astro` and `.ts` files and hit `F5`.
- **Build:** runs `bun run build` under the debugger, useful for diagnosing build-time issues in content collections or image processing.

---

[HotFix.Day](https://www.hotfix.day) &copy; 2016&ndash;present by [Rishav Dhar](https://github.com/rdhar) &middot; Code: [Apache 2.0](https://github.com/OP5dev/HotFix.Day?tab=Apache-2.0-1-ov-file#readme) &middot; Content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0).
