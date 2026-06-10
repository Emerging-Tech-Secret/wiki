# Content Cruncher Wiki (seed)

This directory is the **seed for the private `Emerging-Tech-Secret/wiki` repo** — the GitHub Pages
origin. Push its contents to that repo to bootstrap the wiki.

Layout (this dir = the wiki-repo root):

- `AGENTS.md` — the operating manual / schema the agent follows (not published).
- `wiki/` — agent-owned Markdown pages (the MkDocs `docs_dir`): `index.md`, `log.md`,
  `source_registry.yaml`, and `*.md` pages.
- `mkdocs.yml` — MkDocs Material config.
- `.github/workflows/` — `build` (PR gate), `deploy-pages` (push→Pages), `automerge`.
- `raw/`, `artifacts/`, `state/` — gitignored; live in S3 at runtime.

GitHub setup (one-time): **Settings → Pages → Source: GitHub Actions**, enable **Allow auto-merge**,
and protect `main` requiring the **build** check (so `automerge` only merges on green).
