# Official Themes Guidelines

## Overview
`OfficialThemes/` packages the OpenVCS theme set as an installable theme-only plugin. Keep the package lean and keep the shipped theme folders in sync with the metadata.

## Structure
- `themes/` — shipped theme bundles.
- `package.json` — plugin identity, OpenVCS metadata, and npm packaging rules.
- `dist/` — generated output; do not hand-edit.
- `README.md` — release-channel and usage notes.

## Where to look
| Task | Location | Notes |
|---|---|---|
| Plugin identity / metadata | `package.json` | `openvcs` block defines package identity and defaults. |
| Theme content | `themes/*/` | Individual shipped theme folders. |
| Packaging / release flow | `README.md`, `.github/workflows/publish.yml` | How the package is validated and published. |
| Generated artifacts | `dist/` | Build output only. |

## Conventions
- Keep the package theme-only; do not add app/runtime logic here.
- Keep `package.json`, README, and shipped theme folders aligned.
- Treat `dist/` as generated output.

## Anti-patterns
- Editing files under `dist/` by hand.
- Changing theme names or metadata without updating the README/package manifest.
- Introducing client/backend code into this package.

## Commands
```bash
npm test
npm pack
```

## Notes
- This package is consumed both as a normal npm dependency and through `Client/openvcs.plugins.json` during client builds.
