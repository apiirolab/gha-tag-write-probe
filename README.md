# gha-tag-write-probe (finished, inert)

Throwaway security-research harness, run 2026-09-08. All workflows, branches and tags have been
removed; nothing here executes. Kept only because organization members cannot delete repositories
in this org - **an org owner should delete it.**

It measured whether a GitHub Actions job token with `permissions: contents: write` can force-move a
release tag that consumers pin. It can, unless a tag ruleset exists. Full harness and results are
recorded in the research repo under `src/actions_tag_write_probe/`.
