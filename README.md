# vmr Homebrew tap

Homebrew tap for [`vmr`](https://github.com/gvcgo/version-manager) - a cross-platform SDK version manager.

## Install

```bash
brew install gvcgo/tap/vmr
```

The formula ships the prebuilt binary for macOS (Intel / Apple silicon) and Linux (x86_64 / ARM64),
so nothing is compiled locally.

Homebrew only provides the `vmr` executable; `vmr` installs the SDK versions themselves under
`~/.vmr`. To apply version switches to the current shell, add one line to your shell config:

```bash
eval "$(vmr init zsh)"     # bash / zsh
vmr init fish | source     # fish
```

## Layout

- `Formula/vmr.rb` is rendered from `vmr/packaging/homebrew/vmr.rb.in` in the
  [version-manager](https://github.com/gvcgo/version-manager) repository and pushed here by that
  repository's release workflow (`.github/workflows/release.yml`, job `homebrew`).
  Do not edit it by hand.

## Updating

Every published vmr release rewrites `Formula/vmr.rb` here. The push requires a `TAP_GITHUB_TOKEN`
secret with write access to this repository, configured in the version-manager repository.
