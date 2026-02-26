# EirSpace Docs

This repository hosts the EirSpace documentation site built with MkDocs
Material. It includes a local development setup, GitHub Actions deployment, and
documentation structure for teams and subgroups.

## Quick start (Nix + direnv)

1. Install Nix and direnv.
2. Run `direnv allow` in the repo root.
3. Start the dev server:

```sh
mkdocs serve
```

Open `http://127.0.0.1:8000` in your browser.

## Quick start (Python virtualenv)

Use this if you do not use Nix.

1. Create and activate a virtualenv:

```sh
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```sh
pip install mkdocs mkdocs-material pymdown-extensions
```

3. Run the site locally:

```sh
mkdocs serve
```

## Building the site

To generate a static build:

```sh
mkdocs build --strict
```

Output is written to the `site/` directory.

## Hosting and deployment

This repo deploys to GitHub Pages using the workflow in
`.github/workflows/mkdocs.yml`.

- Pull requests to `main` run a build check.
- Pushes to `main` build and publish to the `gh-pages` branch.

If you need to deploy manually, run:

```sh
mkdocs gh-deploy --force
```

Then ensure GitHub Pages is configured to serve from the `gh-pages` branch,
root folder.

## Project structure

- `mkdocs.yml`: Site configuration and navigation.
- `docs/`: All markdown content.
- `docs/static/`: Images and static assets (logo, favicon).
- `docs/styles/`: Custom CSS and MathJax config.
- `.github/workflows/`: CI build + deploy workflow.

## Writing documentation

See `docs/writing-docs.md` for page structure, style guidance, and conventions.

## Contribution guidelines

Please do not push directly to `main`. Use a branch and open a pull request.

Recommended flow:

1. Create a branch: `git checkout -b docs/your-change`
2. Make edits and commit.
3. Push the branch: `git push -u origin docs/your-change`
4. Open a PR targeting `main`.
5. Merge after review and CI passes.

## Math support

LaTeX math is enabled with MathJax and `pymdownx.arithmatex`.

Inline math:

```
$E = mc^2$
```

Block math:

```
$$
E = mc^2
$$
```

## Updating the theme

Theme settings live in `mkdocs.yml`. Custom styling is in
`docs/styles/extra.css`, with the color palette in `docs/styles/palette.css`.

The logo and favicon are in:

- `docs/static/logo.png`
- `docs/static/favicon.ico`
