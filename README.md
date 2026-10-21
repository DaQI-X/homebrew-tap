# DaQI-X/homebrew-tap

Homebrew tap for [Vv Transcribe](https://github.com/DaQI-X/Vv-Transcribe) — a local
subtitle transcription and proofreading tool for media professionals.

## Install

```sh
brew tap DaQI-X/tap
brew install --cask vv-transcribe
```

Apple Silicon and Intel Macs each get the matching DMG automatically.

## Getting a new version

The cask points at the `latest` GitHub Release and skips checksum verification
(`sha256 :no_check`), so no tap change is needed per release. The downside is that
`brew upgrade --cask vv-transcribe` sees the version as `latest` and usually reports
"already installed" even when a new build is out. To pull the newest build:

```sh
brew reinstall --cask vv-transcribe
```

The app also has a built-in **Check for updates** entry (设置 → 关于与更新) that
links to the release page.

## Unsigned build

Vv Transcribe is an open-source personal project and is **not code-signed or
notarized**, so Gatekeeper may block the first launch. Right-click the app and
choose **Open**, or run:

```sh
xattr -cr "/Applications/Vv Transcribe.app"
```

## Uninstall

```sh
# keeps transcripts and settings
brew uninstall --cask vv-transcribe

# also removes app data, model cache and preferences
brew uninstall --cask --zap vv-transcribe
brew untap DaQI-X/tap
```

## Windows

Windows installers are published on the
[releases page](https://github.com/DaQI-X/Vv-Transcribe/releases) as a `.exe`;
Homebrew is not used there.
