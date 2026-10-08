# scoop-bucket

A [Scoop](https://scoop.sh) bucket for command-line tools by Joessst-Dev:

| App | What it is |
|-----|------------|
| [`fft`](https://github.com/Joessst-Dev/fft-cli) | A command-line client for the fulfillmenttools fulfillment API |
| [`faehigkeiten`](https://github.com/Joessst-Dev/faehigkeiten) | A terminal UI and CLI that installs and tracks agent skills (`SKILL.md`) for Claude Code, Codex, Copilot, Cursor and more |

Add the bucket once:

```powershell
scoop bucket add joessst https://github.com/Joessst-Dev/scoop-bucket
```

Open a new terminal after installing an app: Scoop's shim directory is added to `PATH`
when Scoop itself is set up rather than by these installs.

## fft

```powershell
scoop install fft
```

Then `fft version`. Upgrades are `scoop update fft`. fft tells you when a newer release
exists, and names that command itself.

### Verifying what you install

Every fft release archive is checksummed, and its `checksums.txt` is signed keylessly with
[cosign](https://docs.sigstore.dev/) — there is no private key, and the signature is
bound to the fft-cli repository and the exact workflow that produced it, in Sigstore's
public transparency log. The `hash` in the manifest is the same sha256 Scoop verifies
before it unpacks anything.

The [install guide](https://joessst-dev.github.io/fft-cli/guide/install) has the full
verification recipe.

## faehigkeiten

```powershell
scoop install faehigkeiten
```

Then run `faehigkeiten` (or the short alias `fgk`) to start the TUI, or `fgk --help` for
the CLI. Upgrades are `scoop update faehigkeiten`.

The `hash` in the manifest is the sha256 from the release's `checksums.txt`, which Scoop
verifies before it unpacks anything.

## This bucket is generated

Each manifest is written by [GoReleaser](https://goreleaser.com) on every tag of its
project — see the `scoops:` block in that repository's `.goreleaser.yaml`:

| Manifest | Written by |
|----------|------------|
| `bucket/fft.json` | [`Joessst-Dev/fft-cli`](https://github.com/Joessst-Dev/fft-cli) |
| `bucket/faehigkeiten.json` | [`Joessst-Dev/faehigkeiten`](https://github.com/Joessst-Dev/faehigkeiten) |

Do not edit them by hand: the next release silently reverts the edit. Issues and pull
requests belong on the app's repository, not here.

## Licence

MIT, the same as fft and faehigkeiten.
