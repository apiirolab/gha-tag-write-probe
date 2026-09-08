# gha-tag-write-probe

Throwaway security-research harness. Question: can a GitHub Actions job token with
`permissions: contents: write` force-move a release tag that consumers pin?

Replicates the shape of `actions/add-to-project`'s `post-dependabot.yml`: a push to a
`dependabot/npm_and_yarn/**` branch runs `actions/checkout` (which persists the job token into
`.git/config`) and then `npm ci`, which executes a dependency's `postinstall`. Here that
`postinstall` is the probe. Nothing is published to any registry and no token is ever printed.

Delete this repository when the measurement is done.
