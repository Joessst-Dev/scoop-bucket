# scoop-bucket

A [Scoop](https://scoop.sh) bucket for [`fft`](https://github.com/Joessst-Dev/fft-cli),
a command-line client for the fulfillmenttools fulfillment API.

```powershell
scoop bucket add joessst https://github.com/Joessst-Dev/scoop-bucket
scoop install fft
```

Then `fft version` — in a new terminal, since Scoop's shim directory is added to `PATH`
when Scoop itself is set up rather than by this install.

Upgrades are `scoop update fft`. fft tells you when a newer release exists, and names
that command itself.

## This bucket is generated

`bucket/fft.json` is written by [GoReleaser](https://goreleaser.com) on every tag of
[`Joessst-Dev/fft-cli`](https://github.com/Joessst-Dev/fft-cli) — see the `scoops:`
block in that repository's `.goreleaser.yaml`. Do not edit it by hand: the next release
silently reverts the edit.

Issues and pull requests belong on
[`Joessst-Dev/fft-cli`](https://github.com/Joessst-Dev/fft-cli/issues), not here.

## Verifying what you install

Every release archive is checksummed, and its `checksums.txt` is signed keylessly with
[cosign](https://docs.sigstore.dev/) — there is no private key, and the signature is
bound to the fft-cli repository and the exact workflow that produced it, in Sigstore's
public transparency log. The `hash` in the manifest is the same sha256 Scoop verifies
before it unpacks anything.

The [install guide](https://joessst-dev.github.io/fft-cli/guide/install) has the full
verification recipe.

## Licence

MIT, the same as fft.
