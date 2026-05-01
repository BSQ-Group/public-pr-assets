# public-pr-assets

Public asset host for pull request preview screenshots produced by the
`/pull-request-create` skill in [BSQ-Group/public-brand](https://github.com/BSQ-Group/public-brand).

## Naming

Flat layout. Each file is named `<lowercase-ticket-key>-<viewport>.png`:

```
core-3219-desktop-1280.png
core-3219-tablet-768.png
core-3219-mobile-390.png
```

Standard viewports: `desktop-1280`, `tablet-768`, `mobile-390`.

## Cleanup

A scheduled GitHub Actions workflow drops files older than 90 days each Sunday —
references in old PR descriptions will eventually break, by which time the PRs
are long-merged.
