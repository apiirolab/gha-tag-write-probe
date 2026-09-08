# gha-tag-write-probe

**Throwaway measurement fixture. Not a real project. Delete when done.**

It carries a deliberately unsafe pair of workflows that reproduce the structure of
`actions/attest`'s `rebuild-dist.yml` + `commit-dist.yml`: an unprivileged `pull_request`
builder that uploads an artifact, and a privileged `workflow_run` consumer that takes the ref
it checks out and pushes to **out of that artifact**.

Everything it can write to is inside this repository.

    gh repo delete apiirolab/gha-tag-write-probe --yes
