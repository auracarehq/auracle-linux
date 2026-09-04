# Auracle for Linux

This repository is the public distribution point for Auracle for Linux, the
native GNOME companion published by Auracare. It holds a README and releases —
nothing else. No source, no build workflow, and no CI live here; the source
of truth is the private `auratwin` repository, and every release published
here already passed that repository's own build, test, and checksum
verification before it arrived.

Auracle is a consumer wellness agent. It does not diagnose, treat, or dose.

## Install

Grab `auracle_*_amd64.deb` or `Auracle-*-x86_64.AppImage` from
[the latest release](https://github.com/auracarehq/auracle-linux/releases/latest).

- **.deb** (Debian, Ubuntu, and derivatives): `sudo apt install ./auracle_*_amd64.deb`
- **AppImage** (any modern Linux desktop): make it executable, then run it:
  `chmod +x Auracle-*-x86_64.AppImage && ./Auracle-*-x86_64.AppImage`

Neither artifact bundles a GTK runtime. Your desktop needs GTK 4.12 or newer
and Libadwaita 1.4 or newer already installed — true of a stock GNOME desktop
on a current Ubuntu or Fedora release.

## Verify

Every release publishes a `SHA256SUMS` file alongside its assets. Most people
download one artifact, not all of them, so check with `--ignore-missing`:

```sh
sha256sum --ignore-missing -c SHA256SUMS
```

## What this checksum proves

Nothing here is cryptographically signed. The checksum proves the bytes you downloaded are the bytes we published, not who published them.

## Update

Auracle for Linux does not update itself. There is no feed and no in-app check: compare the version in About against the latest release.

## Accessibility

A full manual pass with a screen reader, keyboard only, high contrast and large text has not been done on this build. If something does not work with assistive technology, please tell us — that is the gap most likely to have missed it.

## Report a problem

Issues are open on this repository:
<https://github.com/auracarehq/auracle-linux/issues>. No response-time
promise is made, but every report is read.

## License

Auracle for Linux is proprietary software. This repository carries no
`LICENSE` file and grants no rights of its own; it is a distribution point,
not a license grant. Every release ships its own `THIRD-PARTY-NOTICES.md`,
which discloses the open-source components this build depends on and their
own license terms.

## This README's source of truth

Edits made directly on this repository (through the GitHub web UI, for
instance) are transient: the next release overwrites this file from
`auratwin`'s own copy. Propose a change there instead.
