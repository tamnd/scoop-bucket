# tamnd Scoop bucket

[Scoop](https://scoop.sh) manifests for the tamnd command-line tools on Windows.
Each manifest installs a prebuilt, checksum-verified binary from the tool's
GitHub release and shims it onto your `PATH`.

On macOS use the [Homebrew tap](https://github.com/tamnd/homebrew-tap); on Linux
use the `.deb`/`.rpm`/`.apk` packages or `go install` from each tool's README.

## Use

```powershell
scoop bucket add tamnd https://github.com/tamnd/scoop-bucket
scoop install yomi
scoop install kage
scoop install tori
```

`scoop update <tool>` upgrades to the latest release; the manifests carry
`checkver`/`autoupdate` metadata so the version and hashes resolve from the
GitHub release automatically.

## Tools

| Manifest | What it does |
| --- | --- |
| [yomi](https://github.com/tamnd/yomi) | Read any web page, or a whole website, into clean Markdown |
| [kage](https://github.com/tamnd/kage) | Clone any website for offline viewing, with the JavaScript stripped out |
| [tori](https://github.com/tamnd/tori) | Build offline, browsable archives of X (Twitter) content |

## How it stays current

Each tool's release pipeline (GoReleaser) writes its manifest here on every
tagged release. Every manifest is validated as well-formed JSON with the
required keys in CI on each change.

## License

The bucket scaffolding is MIT. Each installed tool carries its own license,
bundled in its release archive.
