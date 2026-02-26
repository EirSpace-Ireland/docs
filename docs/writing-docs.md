# Writing documentation

This guide keeps documentation clear, consistent, and easy to maintain across
GitHub repos. Use it for new pages and updates.

## Principles

- Write for the next person to pick up the work.
- Lead with outcomes, then show steps.
- Keep pages short; split when they grow.

## Page structure

Use this order for most pages:

1. Title and 1-2 line summary.
2. Key facts or requirements.
3. Step-by-step process.
4. Links to related docs.

## Style guide

- Use short sentences and active voice.
- Prefer lists for repeatable steps.
- Put commands in code blocks.

## Markdown conventions

Inline code uses backticks: `command --flag`.

Code blocks use language hints:

```sh
mkdocs serve
```

## Math

Inline math: $E = mc^2$

Block math:

$$
E = mc^2
$$

## File placement

Where files should live in the repo:

- `mkdocs.yml` sits at the repo root.
- Markdown pages live under `docs/`.
- Shared assets (images, logos) go in `docs/static/`.
- Styles live in `docs/styles/`.
- Add each page to the `mkdocs.yml` nav.

## Hosting details

Deployment is managed by the GitHub Actions workflow and `mkdocs gh-deploy`.
See the workflow file for branch and Pages settings.
