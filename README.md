# Code2Motion releases

This public repository hosts versioned Code2Motion desktop installers, the
curated c2merse catalog, and package archives. Download the beta from the
[Code2Motion Apps page](https://code2motion.app/apps) or the
[GitHub Releases page](https://github.com/nickhilster/Code2Motion-Releases/releases).
Each desktop release includes the catalog, individual `.c2m` packages, source
and license information, release notes, and `SHA256SUMS`.

## v0.1.0-beta.2 platforms

- Linux x86_64: updated `.deb` installer with Ambient Mode support for Pain-ter.
  The AppImage is not included in this release because the local AppImage
  bundler did not complete successfully. Wallpaper Mode remains disabled.

## v0.1.0-beta.1 platforms

- Linux x86_64: `.deb` and AppImage. AudiOrbits is Linux-only and requires GTK
  3, WebKitGTK 4.1, GStreamer, and PipeWire; audio capture is user-started.
- Windows x64: NSIS setup installer. This beta installer is unsigned. Its
  archive passed integrity checks, but Windows launch and clean-machine
  installation checks remain outstanding. It was cross-compiled on Ubuntu
  using the experimental `cargo-xwin` path.
- macOS: Apple silicon and Intel disk images built on GitHub-hosted runners.
  The images are unsigned; macOS launch and clean-machine installation checks
  remain outstanding.

The launcher catalog is curated and works independently of accounts, KinOS,
and AI services. Users can install and remove experiences individually;
removing one does not remove it from the catalog. AudiOrbits is the only
Linux-only work in this beta.

## Licensing and verification

The launcher source is MIT licensed. Each c2merse retains its own license and
provenance; AudiOrbits remains GPL-3.0-only. Review the release notes and
included per-experience notices before redistribution.

Beta installers and catalog assets are unsigned. `SHA256SUMS` detects damaged
or altered files but does not establish who published them. The launcher is
not an operating-system sandbox, and AudiOrbits runs with the user's normal
permissions.
