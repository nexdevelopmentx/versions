# NEX Development | Versions

Public version manifests for NEX Development FiveM scripts.

Each `nex_<script>.json` file is fetched at runtime by the script's
server-side `version_check.lua` to detect available updates. When the
remote `version` is higher than the script's local `fxmanifest.lua`
`version`, the server console prints a boxed update notice.

## JSON shape

```json
{
    "version": "1.0.2",
    "release_date": { "day": 28, "month": 5, "year": 2026 },
    "notes": "Short summary of what changed in this release."
}
```

## Release process

1. Cut the release in the script's private repo (bump `fxmanifest` `version`).
2. Update the matching `nex_<script>.json` here on `main`.
3. Servers running an older build will see the update box on next restart.
