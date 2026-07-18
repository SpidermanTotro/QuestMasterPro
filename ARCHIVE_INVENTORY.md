# Archive inventory

Checked on 18 July 2026 against the current default branches of the related
repositories.

## `azeroth-pilot-reloaded-Pro--main (1).zip`

- 61 ZIP entries
- historical snapshot of the maintained QuestMaster Pro repository
- every archived file path is present in the current
  `SpidermanTotro/azeroth-pilot-reloaded-Pro-` repository
- the maintained repository contains newer code, patch support, CI, exercises,
  scripts, templates, and additional files

This archive appears superseded, but it should remain untouched until the broader
recovery and cleanup decision is approved.

## `azeroth-pilot-reloaded-feature-complete-rewrite-experimental.zip`

- 270 ZIP entries
- experimental Azeroth Pilot Reloaded rewrite
- contains unverified files not present in the current upstream-tracking
  `SpidermanTotro/azeroth-pilot-reloaded` default branch
- unique areas include additional APR core helpers, profession data, UI code,
  CI configuration, scripts, and route files for several expansions

This snapshot is **not safe to discard yet**. Unique code needs a security,
licensing, runtime, and provenance review before it is recovered or rejected.

## `files (2).zip`

- 86 ZIP entries
- unrelated Book Publish Forge React prototype stored in the wrong repository
- only `README.md` shares the same path as the current
  `SpidermanTotro/book-publish-forge` default branch
- 85 archived paths are not present in that current branch
- includes AI, collaboration, publishing, ethics, export, dashboard, service
  worker, and UI prototype files

This snapshot must be evaluated as an isolated historical prototype. It must not
be merged into Book Publish Forge as one untested batch.

## Cleanup rule

Do not delete, archive, rename, or rewrite this repository until:

1. unique experimental Azeroth files are reviewed and preserved or explicitly rejected;
2. the misfiled Book Publish Forge prototype is recovered to a clearly labelled review branch or explicitly rejected;
3. the maintained QuestMaster repository and public links have a confirmed final name;
4. Henric gives explicit approval for the cleanup action.
