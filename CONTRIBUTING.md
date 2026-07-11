# Contributing

Thank you for helping build a free, reusable library of bridge topic
introductions.

## Public domain dedication

**All submissions are dedicated to the public domain under
[CC0 1.0](LICENSE).** By opening a pull request or pushing to this repository,
you certify that your contribution is your own work (or already public domain)
and you waive all copyright and related rights to it worldwide. This keeps every
lesson's provenance unambiguous and freely reusable by anyone, for any purpose.

## How to contribute

1. Author your lesson in [`lesson-studio`](https://github.com/bridge-craftwork/lesson-studio),
   which produces a markdown + DSL file, or write the file directly by hand.
2. Add it as `lessons/<slug>/<slug>.md` with any lesson-local assets alongside.
3. Fill in the front matter completely (see the
   [README](README.md#lesson-front-matter)). Tag `skill_paths` against the
   canonical taxonomy — CI lint rejects tags that don't exist.
4. Open a pull request. CI lint runs on every PR and is a required check.
5. A maintainer reviews and merges. Merge to `main` = published.

Maintainers authoring directly may push under the branch-protection bypass;
direct pushes stamp `reviewed-by: self` so library metadata stays uniform.
