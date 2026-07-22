# lesson-library — working notes

**Content only.** A CC0 library of one-page bridge topic introductions ("PD
lessons"). One directory per lesson: `lessons/<slug>/<slug>.md`, plus any
lesson-local assets. **No application code lives here.**

The editor, the DSL grammar, the print pipeline, and the lint tool all live in
**[lesson-studio](https://github.com/bridge-craftwork/lesson-studio)** — start
with its `CLAUDE.md` and `documentation/contracts/`.

## Publishing model

Merge to `main` = published. Contributions come by PR; maintainers may push
directly under a branch-protection bypass. CI lint is the required check.

## CI

`.github/workflows/lint.yml` checks out lesson-studio and runs its validator
(`npm run lint:lessons`) against `lessons/` on every PR. It validates that the
DSL parses, hands are legal, front matter is complete, and skill paths exist in
the taxonomy.

To lint locally from a lesson-studio checkout:

```bash
cd ../lesson-studio && npm run lint:lessons -- ../lesson-library/lessons
```

To see a lesson rendered / check it fits one page:

```bash
cd ../lesson-studio && npm run dev          # then Open… the .md in the editor
npm run print:pdf -- --lesson ../lesson-library/lessons/<slug>/<slug>.md --out out.pdf
```

## Authoring conventions

- **No body `# H1`** — the front-matter `title` is the page heading; a body H1
  duplicates it. Start with content or the first `##`.
- **Auction annotations use PBN `=1=`** (`2D =1=`), with numbered notes after a
  `---` separator. Legacy `^1` still parses but isn't canonical.
- **`skill_paths` must exist in the taxonomy** or CI fails. Currently validated
  against a stopgap list in lesson-studio (`src/dsl/taxonomy.json`).
- **Print columns are per-lesson**: front-matter `columns:` (default 2). More
  columns ≠ fewer pages — narrow columns wrap tables *taller*. Trim content
  instead.
- Lessons target **one page**; it's a goal, not a guarantee.

Full block reference: lesson-studio `documentation/contracts/dsl-grammar.md`
(`hand`, `hands`, `auction`, `response-box`, `quiz`, `pagebreak`, `row`; `deal`
is reserved but not resolved until Phase 2).

## Status

**PR #1** seeds the first two lessons (New Minor Forcing; Lessons 1–6 summary).
Both are `status: draft` — the bridge content needs a maintainer review before
flipping to `published`.
