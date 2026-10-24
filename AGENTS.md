# AGENTS.md

## Keep this repo public and self-contained

This is a public fork of [voronp/type-graphql-dataloader](https://github.com/voronp/type-graphql-dataloader), maintained by ISoft Data. It is published to npm as `@isoftdata/type-graphql-dataloader`. There is also an inactive public downstream fork of this repo, so anything committed here should be assumed permanent and public.

Do not add internal ISoft tooling, dependencies, or secrets:

- No private `@isoftdata/*` packages (shared ESLint or Prettier configs, `add-changeset`, and so on). Outside contributors and forks can't install them, so `pnpm install` would fail.
- No calls to private ISoft repos, such as the shared `ISoft-Data-Systems/github-actions` reusable workflows. A public repo can't use them.
- No org-wide secrets (such as an org `NPM_TOKEN` used to read private packages) in CI, and no job-level token env that install scripts could read.
- No internal URLs, hostnames, ticket links, customer names, or credentials in code, comments, docs, or commit messages.

Keep ESLint and Prettier configured locally in this repo ([eslint.config.js](eslint.config.js), [.prettierrc.json](.prettierrc.json)) using public packages only.

The standard ISoft TypeScript project tooling (for example the `typescript-project` skill) does not apply to this repo where it conflicts with the rules above.
