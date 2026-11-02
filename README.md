# Code2Motion c2merse packages

This public repository hosts versioned downloadable c2merse packages for the
Code2Motion desktop application. Download package files from the GitHub
Releases page; each release includes a catalog manifest and `SHA256SUMS`.

## Preview release

The initial preview contains Pain-ter 1.0.0 and AudiOrbits 1.0.0. Each package
is distributed with its own manifest, license, provenance, and applicable
third-party notices. Their licenses are separate: Pain-ter is MIT; AudiOrbits
is GPL-3.0-only.

These are experience archives, **not a desktop installer**. The Code2Motion
desktop app does not yet have its package install, launch, and uninstall flow
connected to these downloads. Do not treat this preview as a supported user
installation path or product release. AudiOrbits requires GTK 3, WebKitGTK
4.1, GStreamer, and PipeWire on Linux; its audio capture is user-started.

The release assets are versioned snapshots. Verify package archives against
the included `SHA256SUMS` before use. A signed online catalog and automated
in-app update mechanism are future work.
