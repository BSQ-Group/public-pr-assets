# public-pr-assets

Public asset host for pull request preview screenshots produced by the
`/pull-request-create` skill in [BSQ-Group/public-brand](https://github.com/BSQ-Group/public-brand).

Layout: one folder per PR, named `<lowercase-ticket-key>` (e.g. `core-3219/`),
containing `desktop-1280.png`, `tablet-768.png`, `mobile-390.png`.

A scheduled GitHub Actions workflow drops folders older than 90 days each
Sunday — references in old PR descriptions will eventually break, by which
time the PRs are long-merged.
