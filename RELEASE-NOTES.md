# Code2Motion c2merse catalog preview — 2026-11-02

This prerelease publishes two individually versioned experience packages for
evaluation: Pain-ter 1.0.0 and AudiOrbits 1.0.0. Each `.c2m` archive contains
its package manifest, source files, provenance, and applicable license and
third-party notices. Verify downloads with `SHA256SUMS` before use.

## Important status

These are experience package assets, not a Code2Motion desktop installer.
The launcher currently does not provide a working catalog install/update,
launch/close, or uninstall flow. Do not point product download buttons at
these assets as though that integration were released. A future launcher
catalog should verify a signed catalog or pinned package hashes before install.

AudiOrbits requires the Linux GTK 3, WebKitGTK 4.1, GStreamer, and PipeWire
runtime components documented in the package. Audio capture is user-started.
The first launch requires desktop access to those system components.

Pain-ter is distributed under MIT in Code2Motion as Nikhil Khedkar's original
work. AudiOrbits remains separately licensed under GPL-3.0-only; retain its
license and included third-party notices when redistributing it.
