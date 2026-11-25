# Contributing to Austral

Thank you for your interest! This guide applies to all the repositories of the `austral-project` organization.

## Before you start

- **Bug**: open an issue with the "Bug" template on the repository of the bundle concerned, with the Austral, Symfony and PHP versions.
- **New feature**: first open a "Feature request" issue to discuss it before writing code.
- **Security vulnerability**: never a public issue, see [SECURITY.md](SECURITY.md).

## Branches

| Branch | Role | What goes there |
|--------|------|-----------------|
| `4.x` | Development (default branch) | New features, BC breaks announced in `UPGRADE-4.x.md` |
| `3.1` | Maintenance | Bug and security fixes only |

Open your pull request against the **oldest maintained branch** that contains the bug; the maintainer then merges the fix up to `4.x`.

The repositories that are not packages ([.github](https://github.com/austral-project/.github), [dev](https://github.com/austral-project/dev), [recipes](https://github.com/austral-project/recipes)) only have a `master` branch.

## Preparing a pull request

```bash
git clone git@github.com:austral-project/<bundle>.git && cd <bundle>
git switch -c fix/short-description 4.x
composer install
composer check   # cs-fixer (dry-run) + phpstan + phpunit
```

- One pull request = one topic.
- Add a test that fails without your fix.
- Add a line to the `## [Unreleased]` section of `CHANGELOG.md`.
- If the change affects what a project copies (configuration, routes, entities of the application), update the recipe of the bundle in [austral-project/recipes](https://github.com/austral-project/recipes) too.
- Commit messages follow [Conventional Commits](https://www.conventionalcommits.org/): `fix(form): ...`, `feat(admin): ...`, `docs: ...`, `perf: ...`, `refactor: ...`, `test: ...`, `chore: ...`. A BC break is marked with `!` (`feat(entity)!: ...`).
- Code, comments, documentation and commit messages are written in English.

## Coding style

- PHP ≥ 8.4, `declare(strict_types=1);` in every file.
- PHP-CS-Fixer `@Symfony` + `@Symfony:risky` rules (`composer cs-fix` fixes them automatically).
- PHPStan at the level set in the bundle's `phpstan.dist.neon`, with no new error.
- A bundle only depends on lower layers (see the organization home page). No reference to `App\`.

## Versions and releases

Austral follows [Semantic Versioning](https://semver.org/). **All bundles share the same major and minor version**: `4.1.0` is released for all bundles at the same time. Fixes (`4.1.x`) can be released for a single bundle. Releases are published by the maintainer.

## License

By contributing, you agree that your code is released under the MIT license.
