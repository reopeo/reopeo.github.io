# Repository Guidelines

## Project Structure & Module Organization

This repository is a HugoBlox academic portfolio built with Hugo.

- `content/` contains Markdown pages grouped by type, including `blog/`, `projects/`, `publications/`, `courses/`, and `events/`. Keep page-specific images, PDFs, and data beside the page's `index.md`.
- `data/authors/me.yaml` stores profile metadata.
- `config/_default/` contains Hugo menus, languages, site parameters, and module configuration.
- `assets/media/` holds files processed by Hugo; `static/uploads/` contains files copied directly to the generated site.
- `layouts/` contains local template overrides.
- `.github/workflows/` defines build, deployment, publication-import, and dependency-upgrade automation.
- `public/` is generated output and should not be edited manually.

## Build, Test, and Development Commands

Use Node.js 22, pnpm 10, and Hugo Extended at the version specified in `hugoblox.yaml`.

```bash
pnpm install          # Install frontend and search dependencies
pnpm dev              # Start the local Hugo server
pnpm build            # Build the minified site and Pagefind index
pnpm run pagefind     # Rebuild search data from an existing public/ directory
```

Before opening a pull request, run `pnpm build`. CI performs the same Hugo build and uploads the resulting `public/` artifact.

## Coding Style & Naming Conventions

Use two-space indentation in YAML and JSON. Preserve existing front matter structure and HugoBlox block conventions. Prefer lowercase, hyphen-separated directory names such as `content/blog/data-visualization/`. Leaf pages should normally use a page bundle: `topic-name/index.md` with related media in the same directory. Use descriptive image names; reserve `featured.jpg` or `featured.png` for listing thumbnails.

Keep Markdown concise, use sentence-case headings, and avoid editing generated files, `node_modules/`, or lockfiles unless dependencies change.

## Testing Guidelines

There is no separate unit-test framework. A successful `pnpm build` is the primary automated check. For content or layout changes, also inspect the affected pages through `pnpm dev`, verify links and media, and check responsive rendering. Publication changes should confirm citation files and downloadable PDFs remain accessible.

## Commit & Pull Request Guidelines

History is currently minimal, but automation uses Conventional Commit-style messages such as `feat(publications): ...` and `chore(deps): ...`; follow that pattern with an imperative summary. Keep commits focused.

Pull requests should explain the change, list validation performed, link relevant issues, and include screenshots for visual updates. Do not commit secrets or production credentials; use repository secrets for deployment values.
