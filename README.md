# PyreZ's Scoop Bucket

[![Tests](https://github.com/pyre-z/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/pyre-z/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/pyre-z/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/pyre-z/scoop-bucket/actions/workflows/excavator.yml)

Personal [Scoop](https://scoop.sh) bucket for apps I use and maintain myself.

## Install

```pwsh
scoop bucket add pyre https://github.com/pyre-z/scoop-bucket
scoop install pyre/<manifestname>
```

## Available manifests

<!-- Update this table when adding manifests. -->

| Manifest | Description |
| -------- | ----------- |
| —        | (none yet)  |

## Adding a manifest

1. Copy `bucket/app-name.json.template` to `bucket/<app-name>.json`
2. Fill in `version`, `url`, `hash`, `bin`, and a `checkver` + `autoupdate` block
3. Run `pwsh ./bin/checkver.ps1 <app-name> -Update` to verify auto-update works
4. Commit and push — CI will validate the manifest and Excavator will bump versions every 4 hours

See the [App Manifests](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests) wiki page for the full field reference.

## Notes

- This repo was generated from [ScoopInstaller/BucketTemplate](https://github.com/ScoopInstaller/BucketTemplate).
- Third-party manifests should respect their upstream licenses.
