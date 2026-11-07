# vmr Homebrew tap

Homebrew tap for [`vmr`](https://github.com/gvcgo/version-manager) - a cross-platform SDK version manager.

## Install

```bash
brew install gvcgo/tap/vmr
```

## Layout

- `Formula/vmr.rb` is generated and pushed by [cargo-dist](https://axodotdev.github.io/cargo-dist/) from the vmr release workflow. Do not edit it by hand.
- The formula installs the prebuilt release archives from `gvcgo/version-manager`.

Status: bootstrap - the formula appears after the first tagged vmr release.
