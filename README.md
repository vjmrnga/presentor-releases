# Presentor releases

Installers for **Presentor**, the desktop app for showing song and response slides during
church services.

## Installing

Download `Presentor-Setup-<version>.exe` from the
[latest release](https://github.com/vjmrnga/presentor-releases/releases/latest) and run it.

## Updates

Once installed, Presentor keeps itself up to date. It checks this page for a new version a
few seconds after it starts and every few hours while it is open, downloads it in the
background, and installs it the next time Presentor is closed. An update never interrupts a
service. You can also check now, or restart to update right away, under
**Settings → Updates**.

## For maintainers

This repository only holds the release files; there is no source code here. Releases are
published by `npm run release` in the app's source repository.

Every release needs these files, which `npm run release` uploads:

- `Presentor-Setup-<version>.exe`: the installer
- `Presentor-Setup-<version>.exe.blockmap`: lets installed copies download only what changed
- `latest.yml`: tells installed copies which version is newest

Do not delete or rename `latest.yml` on the newest release, and do not mark releases as
drafts or pre-releases. Installed copies ignore both, so they would stop updating.
