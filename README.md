# Official Themes

Official OpenVCS themes shipped as a theme-only plugin.

This package is resolved through `Client/openvcs.plugins.json` during client
builds and can also be referenced as a normal plugin source.

## Validate

```bash
npm test
```

## Pack For Config Use

```bash
npm pack
```

## Release Channels

The npm package can be consumed from prerelease channels published by CI:

- `latest`: stable releases
- `beta`: builds from the `Beta` branch
- `nightly`: scheduled builds from `Dev` when there are changes since the last nightly

Examples:

```bash
npm install @openvcs/official-themes@beta
npm install @openvcs/official-themes@nightly
```
