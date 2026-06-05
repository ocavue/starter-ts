# TypeScript Library Starter

[![NPM version](https://img.shields.io/npm/v/@ocavue/starter-ts?color=a1b858&label=)](https://www.npmjs.com/package/@ocavue/starter-ts)

A minimal [TypeScript](https://www.typescriptlang.org/) library starter with bundling, testing, linting, formatting, and automated npm releases, all preconfigured.

> **Using this template?** Click [Use this template](https://github.com/ocavue/starter-ts/generate), rename the package in `package.json`, and write your code in `src/index.ts`.

## Project structure

- `src/`: source code, with co-located [Vitest](https://vitest.dev/) tests (`*.test.ts`)
- `dist/`: bundled output (ESM + type declarations), built by [tsdown](https://tsdown.dev/)

## Scripts

Local development needs [Node.js](https://nodejs.org/) v22+ and [pnpm](https://pnpm.io/).

| Command          | Description                                                                                                                |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `pnpm dev`       | Rebuild on change (`tsdown --watch`)                                                                                       |
| `pnpm build`     | Bundle the library to `dist/`                                                                                              |
| `pnpm test`      | Run tests with [Vitest](https://vitest.dev/)                                                                               |
| `pnpm lint`      | Lint with [ESLint](https://eslint.org/), [oxfmt](https://oxc.rs/docs/guide/usage/formatter), and [knip](https://knip.dev/) |
| `pnpm fix`       | Auto-fix formatting and lint issues                                                                                        |
| `pnpm typecheck` | Type-check with `tsc`                                                                                                      |

## Publishing

Releases are automated with [release-please](https://github.com/googleapis/release-please) and npm [trusted publishing](https://docs.npmjs.com/trusted-publishers/) (OIDC). No tokens to manage.

1. **First release (manual).** OIDC can't create a brand-new package, so publish the first version by hand:

   ```bash
   pnpm login
   pnpm build
   pnpm publish
   ```

2. **Enable OIDC.** On [npmjs.com](https://www.npmjs.com/), open the package → **Settings → Trusted Publisher → GitHub Actions**, and set the workflow filename to `release.yml`.

3. **Future releases (automatic).** Push [Conventional Commits](https://www.conventionalcommits.org/) (`fix:`, `feat:`, …) to your default branch (usually `master` or `main`); [release-please](https://github.com/googleapis/release-please) opens a release PR that bumps the version, updates the changelog, and publishes on merge.

## Sponsors

<p align="center">
  <a href="https://github.com/sponsors/ocavue">
    <img src="https://cdn.jsdelivr.net/gh/ocavue/sponsors/sponsorkit/sponsors.svg" alt="My Sponsors">
  </a>
</p>

## License

[MIT](./LICENSE) © [ocavue](https://github.com/ocavue)
