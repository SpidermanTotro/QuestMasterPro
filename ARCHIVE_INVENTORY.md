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
- Book Publish Forge React prototype stored in this unrelated repository
- a byte-for-byte identical archive already exists at
  `SpidermanTotro/book-publish-forge/files (2).zip`
- SHA-256 for both copies:
  `b64acb87fa90ee0bde09034f3ccf18c30ebda19e11c90af98a7266d895f80da1`
- only `README.md` from the archive shares a path with files currently
  extracted on the Book Publish Forge default branch
- the other 85 archived paths are not currently extracted on that branch
- includes AI, collaboration, publishing, ethics, export, dashboard, service
  worker, and UI prototype files

The historical prototype is therefore preserved in the correct repository, but
its contents remain unreviewed and unextracted. It must be evaluated in isolation
and must not be merged into Book Publish Forge as one untested batch.

## Cleanup rule

Do not delete, archive, rename, or rewrite this repository until:

1. unique experimental Azeroth files are reviewed and preserved or explicitly rejected;
2. the Book Publish Forge prototype is audited from its copy in the correct repository;
3. the maintained QuestMaster repository and public links have a confirmed final name;
4. Henric gives explicit approval for the cleanup action, including disposal of duplicate archives.
