# ASTRAL Loader GitHub Actions build

## Required GitHub Secrets for signed releases

Add these repository secrets under **Settings → Secrets and variables → Actions**:

- `KEYSTORE_BASE64` — base64 of the release `.jks` file
- `KEYSTORE_PASSWORD` — keystore password
- `KEY_ALIAS` — key alias
- `KEY_PASSWORD` — key password

The keystore must **not** be committed to the repository.

## Build

Push to `main`/`master`, open a pull request, or run **Build ASTRAL Loader** manually from Actions.

The workflow uploads the APK as an artifact.

## Release

Create and push a tag such as:

```text
v1.0.1
```

The workflow builds the release APK and attaches it to the GitHub Release.
