| Q                 | A
|-------------------|--------
| Branch            | 4.x <!-- or 3.1 for a bug fix -->
| Bug fix?          | yes/no
| New feature?      | yes/no
| BC break?         | yes/no <!-- if yes: describe the migration in UPGRADE-4.x.md -->
| Related issues    | Fix #...

## Description

<!-- What this PR changes, and why. -->

## Checklist

- [ ] `composer check` passes locally (cs-fixer, phpstan, phpunit)
- [ ] A test covers the change
- [ ] A line is added to `CHANGELOG.md` (`[Unreleased]` section)
- [ ] The documentation is up to date if the behavior changes
