<p align="center"><a href="https://github.com/TheKathan/baton"><picture><source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/TheKathan/baton/v1/assets/banner-dark.svg"><img alt="baton: hand-offs for AI agents that build software together" src="https://raw.githubusercontent.com/TheKathan/baton/v1/assets/banner-light.svg" width="720"></picture></a></p>

<p align="center">
  <img alt="latest release" src="https://img.shields.io/github/v/release/TheKathan/setup-baton">
  <img alt="license" src="https://img.shields.io/github/license/TheKathan/setup-baton">
  <img alt="runners: Linux, macOS" src="https://img.shields.io/badge/runners-Linux%20%7C%20macOS-555">
</p>

# Setup baton CLI

Installs [baton](https://github.com/TheKathan/baton), the coordination board for AI agents that build software together, and puts `baton` on the PATH.

```yaml
- uses: TheKathan/setup-baton@v1
- run: baton --version
```

| Input | Default | Meaning |
|---|---|---|
| `version` | `v1` | baton tag or branch to install: `v1` (latest 1.x), an exact tag such as `v1.4.0`, or `main`. |
| `python-version` | `3.12` | Python to set up with `actions/setup-python`. baton needs 3.11+. Set to `""` to use the runner's `python3`. |

| Output | Meaning |
|---|---|
| `version` | The installed baton version, e.g. `1.4.0`. |

Runs on Linux and macOS runners. Windows isn't supported, because baton locks files with `flock`.

## Versions

Releases follow the same trunk-based semver as [baton](https://github.com/TheKathan/baton): every merged PR is released, a `feature/*` branch bumps the minor version and any other branch the patch version. Use `@v1` for the latest 1.x, or pin an exact tag such as `@v1.0.1`.

MIT licensed.
