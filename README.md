# PureScript Assert Multiple

Chain assertions contained in a monad.

## Status

| Source     | Shields                                                                                                                                      |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Project    | ![release][release_shield] ![license][license_shield] ![lines][lines_shield] ![languages][languages_shield]                                  |
| Health     | ![readthedocs][readthedocs_shield] ![github_review][github_review_shield]![codacy][codacy_shield] ![codacy_coverage][codacy_coverage_shield] |
| Repository | ![issues][issues_shield] ![issues_closed][issues_closed_shield] ![pulls][pulls_shield] ![pulls_closed][pulls_closed_shield]                  |
| Activity   | ![contributors][contributors_shield] ![monthly_commits][monthly_commits_shield] ![last_commit][last_commit_shield]                           |

## Installing

```bash
spago install purescript-assert-multiple
```

## Motivation

An array of assertions will not be evaluated eagerly:

```purs
import Test.Assert (assert)

do
  x <- 1 .. 5
  pure $ assert (x <= 5)
```

The 'resolve' function invokes them over a fold.

```purs
import Test.Assert.Multiple (resolve)

resolve do
  x <- 1 .. 5
  pure $ assert (x <= 5)
```

## Tests

To run tests:

```bash
grunt test
```

## Documentation

This repository's documentation is hosted on [readthedocs][readthedocs].

## Tooling

To run linters:

```bash
grunt lint
```

To run formatters:

```bash
grunt format
```

## Continuous integration

This repository uses github actions to lint and test each commit. Formatting tasks and writing/generating documentation must be done before committing new code.

## Versioning

This repository adheres to semantic versioning standards.
For more information on semantic versioning visit [SemVer][semver].

Bump2version is used to version and tag changes.
For example:

```bash
bump2version patch
```

## Changelog

Please read this repository's [changelog](CHANGELOG.md) for details on changes that have been made.

## Contributing

Please read this repository's guidelines on [contributing](CONTRIBUTING.md) for details on the process for submitting pull requests. Moreover, our [code of conduct](CODE_OF_CONDUCT.md) declares our collaboration standards.

## Contributors

- **Joel Lefkowitz** - _Initial work_ - [Joel Lefkowitz][author]

[![Buy Me A Coffee][coffee_button]][author_coffee]

## Remarks

Lots of love to the open source community!

![Be kind][be_kind]

<!-- Project links -->

[readthedocs]: https://purescript-assert-multiple.readthedocs.io/en/latest/

<!-- External links -->

[semver]: http://semver.org/
[be_kind]: https://media.giphy.com/media/osAcIGTSyeovPq6Xph/giphy.gif

<!-- Contributor links -->

[author]: https://github.com/joellefkowitz
[author_coffee]: https://www.buymeacoffee.com/joellefkowitz
[coffee_button]: https://cdn.buymeacoffee.com/buttons/default-blue.png

<!-- Project shields -->

[release_shield]: https://img.shields.io/github/v/tag/joellefkowitz/purescript-assert-multiple
[license_shield]: https://img.shields.io/github/license/joellefkowitz/purescript-assert-multiple
[lines_shield]: https://img.shields.io/tokei/lines/github/joellefkowitz/purescript-assert-multiple
[languages_shield]: https://img.shields.io/github/languages/count/joellefkowitz/purescript-assert-multiple

<!-- Health shields -->

[readthedocs_shield]: https://img.shields.io/readthedocs/purescript-assert-multiple
[github_review_shield]: https://img.shields.io/github/workflow/status/JoelLefkowitz/purescript-assert-multiple/Review
[codacy_shield]: https://img.shields.io/codacy/grade/e554a1597f8b40d9b7e54d7923c2049f
[codacy_coverage_shield]: https://img.shields.io/codacy/coverage/e554a1597f8b40d9b7e54d7923c2049f

<!-- Repository shields -->

[issues_shield]: https://img.shields.io/github/issues/joellefkowitz/purescript-assert-multiple
[issues_closed_shield]: https://img.shields.io/github/issues-closed/joellefkowitz/purescript-assert-multiple
[pulls_shield]: https://img.shields.io/github/issues-pr/joellefkowitz/purescript-assert-multiple
[pulls_closed_shield]: https://img.shields.io/github/issues-pr-closed/joellefkowitz/purescript-assert-multiple

<!-- Activity shields -->

[contributors_shield]: https://img.shields.io/github/contributors/joellefkowitz/purescript-assert-multiple
[monthly_commits_shield]: https://img.shields.io/github/commit-activity/m/joellefkowitz/purescript-assert-multiple
[last_commit_shield]: https://img.shields.io/github/last-commit/joellefkowitz/purescript-assert-multiple
