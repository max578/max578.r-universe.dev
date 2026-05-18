# max578 r-universe registry

This repository is the r-universe package registry for the GitHub
account [`max578`](https://github.com/max578). r-universe reads
`packages.json` and builds the listed R packages on every commit,
publishing binary builds for Windows, macOS, and Linux at
`https://max578.r-universe.dev/`.

## Currently registered

| Package | Source | Branch |
|---|---|---|
| [`picMort`](https://github.com/max578/picMort) | `max578/picMort` | `main` |
| [`masque`](https://github.com/max578/masque) | `max578/masque` | `main` |

## Installation (for end users)

```r
install.packages("picMort", repos = "https://max578.r-universe.dev")
```

…will work once r-universe has built the first binary for the listed
package (usually within an hour of the registry being pushed; status
is visible at <https://max578.r-universe.dev>).

## How to add a package

Append a new object to `packages.json` and push to `main`. r-universe
re-reads the registry on each push.

```json
[
  {
    "package": "picMort",
    "url": "https://github.com/max578/picMort",
    "branch": "main"
  },
  {
    "package": "another_package",
    "url": "https://github.com/max578/another_package",
    "branch": "main"
  }
]
```

## Reference

- r-universe documentation: <https://docs.r-universe.dev/>
- Registry format: <https://docs.r-universe.dev/publish/build-registry.html>
