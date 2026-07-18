# Experimental Azeroth snapshot audit

This records the isolated review of `azeroth-pilot-reloaded-feature-complete-rewrite-experimental.zip`. It does not import the snapshot.

## Artifact integrity and composition

- SHA-256: `91e537171b28e1c18e246e072e1ad54d446a38fbfc5eee31f150e723314ab073`
- 212 files; archive integrity test passed
- no path traversal entries, symbolic links, embedded credentials, or private keys found
- 153 Lua files, 25 XML files, 10 workflows, plus media and vendored libraries

Comparison with the maintained `dev` branch of `SpidermanTotro/azeroth-pilot-reloaded`:

| Classification | Files |
|---|---:|
| Same path and identical content | 162 |
| Same path but modified | 22 |
| Present only in the snapshot | 28 |

The snapshot is therefore predominantly a copy of the upstream APR distribution, not a clean QuestMaster feature set.

## Unique candidates

The 28 snapshot-only files include:

- nine feature modules: Advanced Features, Consumable Advisor, Death Recovery, Gathering Tracker, Gear Advisor, Market, Professions, Quest Item Auto Use, and Talent Advisor
- a professions UI panel and two profession data files
- fifteen route/data files for later zones
- an extra CI workflow, Copilot instructions, and a VS Code recovery shell script

These files require individual functional and provenance review. “Unique by path” does not establish original authorship or compatibility.

## Safety and maintenance findings

- The Discord release workflow sends release content to an external webhook and is outside the local-first baseline.
- The VS Code recovery script kills server processes and moves user directories under `$HOME`; it is operational tooling, not addon source, and must not be imported.
- The CI workflow uses network package installation on each run and references a route checker that is absent, so that step silently skips.
- The snapshot includes upstream release automation, funding metadata, media, and vendored libraries; duplicating them would increase provenance and maintenance risk.
- Quest Item Auto Use and Advanced Features can invoke `C_Container.UseContainerItem`; these behaviors require explicit opt-in controls and in-game validation.
- High-frequency tickers and event registrations in advisory modules need performance testing in the WoW client.
- No evidence was found that this full snapshot belongs in the separate maintained `azeroth-pilot-reloaded-Pro-` architecture.

## Recovery decision

Do not merge or unpack the archive wholesale.

1. Keep the ZIP as historical evidence with its checksum.
2. Exclude workflows, funding/configuration metadata, the VS Code recovery script, upstream libraries/media, and unchanged upstream files.
3. Review each feature module and route independently for license/provenance, current WoW API compatibility, TOC/XML wiring, performance, and opt-in behavior.
4. Recover only a verified module or route per small pull request with targeted tests and attribution.
5. Prefer contributing generally useful APR fixes to the maintained upstream-derived repository rather than copying its full source into QuestMasterPro.
