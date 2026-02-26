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
- Add each page to the `.nav.yml` file for the section you want it to appear in.
- If you skip the nav update, the page will build but it will not show in the sidebar.

## Create new documentation

Step-by-step guide for adding a new page:

1. Pick the location for the page under `docs/`.
2. Create the markdown file with a clear title and short summary.
3. Add the page to the nearest `.nav.yml` so it appears in the sidebar.
4. Check links between related pages.
5. Preview locally with `mkdocs serve --strict`.
6. Run a strict build with `mkdocs build --strict` before opening a PR.

## Branch structure for teams

Use team-scoped branch names so changes are easy to trace:

- `docs/rocketry/<short-name>` for Rocketry Team documentation.
- `docs/uas/<short-name>` for UAS Team documentation.
- `docs/site/<short-name>` for global docs and shared pages.

## Commit and push docs

Steps to commit and push documentation changes:

1. Important: create a new branch with `git checkout -b docs/<short-name>`.
2. (Optional) Check what changed with `git status -sb`.
3. (Optional) Review the edits with `git diff`.
4. Stage the doc updates, for example `git add docs/writing-docs.md`.
5. Commit with a short message, like `git commit -m "docs: add new documentation tutorial"`.
6. Push your branch with `git push -u origin docs/<short-name>`.

## Open a pull request

Steps to open a PR for documentation updates:

1. Make sure your branch is pushed to GitHub.
2. Open GitHub and click "Compare & pull request" for your branch.
3. Add a short title and summary of the documentation changes.
4. Set the base branch to `main`.
5. Submit the PR and wait for review.

## Hosting details

Deployment is managed by the GitHub Actions workflow and `mkdocs gh-deploy`.
See the workflow file for branch and Pages settings.
