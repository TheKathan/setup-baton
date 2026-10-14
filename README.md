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

MIT licensed.
