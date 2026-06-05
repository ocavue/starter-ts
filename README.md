# pkg-name

[![NPM version](https://img.shields.io/npm/v/pkg-name?color=a1b858&label=)](https://www.npmjs.com/package/pkg-name)

A minimal [TypeScript] library starter — bundling, testing, linting, formatting, and automated npm releases, all preconfigured.

> **Using this template?** Click [**Use this template**](https://github.com/ocavue/starter-ts/generate), then rename `name`, `description`, `author`, `repository`, `homepage`, and `bugs` in `package.json` and write your code in `src/index.ts`.

## Project structure

- `src/` — source code, with co-located [Vitest] tests (`*.test.ts`)
- `dist/` — bundled output (ESM + type declarations), built by [tsdown]

## Scripts

Local development needs [Node.js] v22+ and [pnpm].

| Command          | Description                             |
| ---------------- | --------------------------------------- |
| `pnpm dev`       | Rebuild on change (`tsdown --watch`)    |
| `pnpm build`     | Bundle the library to `dist/`           |
| `pnpm test`      | Run tests with [Vitest]                 |
| `pnpm lint`      | Lint with [ESLint], [oxfmt], and [knip] |
| `pnpm fix`       | Auto-fix formatting and lint issues     |
| `pnpm typecheck` | Type-check with `tsc`                   |

## Publishing

Releases are automated with [release-please] and npm [trusted publishing] (OIDC) — no tokens to manage.

1. **First release (manual).** OIDC can't create a brand-new package, so publish the first version by hand:

   ```bash
   pnpm login && pnpm build && pnpm publish
   ```

   An unscoped name is public by default; add `--access public` for a scoped name.

2. **Enable OIDC.** On [npmjs.com], open the package → **Settings → Trusted Publisher → GitHub Actions**, and set the workflow filename to `release.yml`.

3. **Future releases (automatic).** Push [Conventional Commits] (`fix:`, `feat:`, …) to `master`; [release-please] opens a release PR that bumps the version, updates the changelog, and publishes on merge.

## Sponsors

<p align="center">
  <a href="https://github.com/sponsors/ocavue">
    <img src="https://cdn.jsdelivr.net/gh/ocavue/sponsors/sponsorkit/sponsors.svg" alt="My Sponsors">
  </a>
</p>

## License

MIT

[TypeScript]: https://www.typescriptlang.org/
[tsdown]: https://tsdown.dev/
[Vitest]: https://vitest.dev/
[ESLint]: https://eslint.org/
[oxfmt]: https://oxc.rs/docs/guide/usage/formatter
[knip]: https://knip.dev/
[Node.js]: https://nodejs.org/
[pnpm]: https://pnpm.io/
[release-please]: https://github.com/googleapis/release-please
[trusted publishing]: https://docs.npmjs.com/trusted-publishers/
[npmjs.com]: https://www.npmjs.com/
[Conventional Commits]: https://www.conventionalcommits.org/
