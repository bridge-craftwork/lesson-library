# lesson-library

A freely licensed (CC0) library of one-page bridge topic introductions
("PD lessons") for the Bridge Classroom platform. Each lesson is a
markdown + DSL source file authored in
[`lesson-studio`](https://github.com/bridge-craftwork/lesson-studio) (or
directly by hand), tagged with taxonomy skill paths so the platform can surface
it for remediation, convention-card-driven discovery, and curriculum coverage
analysis.

**This repo is content only** — one directory per lesson, plus CI lint. No
application code. The editor, DSL grammar, print view, and the full system
design live in `lesson-studio`; see its
[architecture doc](https://github.com/bridge-craftwork/lesson-studio/blob/main/documentation/lesson-library-architecture.md).

## Publishing model

Merge to `main` = published. Contributions come in by pull request; maintainers
may push directly under a branch-protection bypass. CI lint is a required status
check for everyone — it validates that the DSL parses, hands are legal, deal
references resolve, embedded quiz JSON is valid, front-matter skill paths exist
in the canonical taxonomy, front matter is complete, and the page renders.

## Lesson front matter

Every lesson carries YAML front matter (Contract 4):

```yaml
title: New Minor Forcing
skill_paths:
  - bidding_conventions/new_minor_forcing
primary: bidding_conventions/new_minor_forcing
level: intermediate
author: Rick Wilson
status: published
reviewed-by: self
```

## License

[CC0 1.0 Universal](LICENSE) — every lesson is dedicated to the public domain.
See [CONTRIBUTING.md](CONTRIBUTING.md) before submitting.
