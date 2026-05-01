# public-pr-assets

Public asset host for pull request preview screenshots produced by the
`/pull-request-create` skill in [BSQ-Group/public-brand](https://github.com/BSQ-Group/public-brand).

## Layout

**One branch per PR**, named with the lowercase ticket key (e.g. `core-3219`).
Each branch contains three viewport PNGs at the root:

```
core-3219/
  desktop-1280.png
  tablet-768.png
  mobile-390.png
```

Public URL form:
```
https://raw.githubusercontent.com/BSQ-Group/public-pr-assets/<branch>/<viewport>.png
```

`main` carries only this README and the sweep workflow — never any PR
screenshots.

## Cleanup

`.github/workflows/sweep.yml` runs each Sunday on `main` and deletes
any `core-*` branch whose latest commit is older than 90 days. Old PR
descriptions eventually break, by which time the PRs are long-merged.
