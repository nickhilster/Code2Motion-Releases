# Code2Motion desktop beta v0.1.0-beta.2

This beta adds reviewed presentation-mode metadata and Ambient Mode support for
Pain-ter. Interactive Mode remains the default. Wallpaper Mode remains disabled
because no reviewed wallpaper implementation is included yet.

The Linux x86_64 `.deb` installer is updated to Code2Motion `0.1.0-beta.2`.

# Unreleased — presentation modes (not published)

Adds the presentation-mode contract to the launcher and catalog. This section
describes work in the source repository only; nothing here has been published
to Code2Motion-Releases, and the live v0.1.0-beta.1 catalog is unchanged until
a deliberate release republishes the packages and catalog together.

- Catalog entries, package manifests, and installed runtime manifests now
  declare `presentation` modes (`interactive` / `ambient` / `wallpaper`).
  Missing metadata defaults to Interactive Mode only, so the published
  v0.1.0-beta.1 packages remain valid as they are.
- **Pain-ter 1.0.0** additionally declares **Ambient Mode** (reviewed):
  a borderless fullscreen Code2Motion-managed window, closable from the
  launcher. It is not a screensaver and does not touch the GNOME lock
  screen. Its package was rebuilt in-repo with the new declaration
  (SHA-256 `e5cd0e645d57f4bd431e42509b8120ec139e906fd29e2323f6924b4716c1d76d`);
  the other four packages are byte-identical to the published ones and only
  gained the explicit interactive-only default in the in-repo catalog.
- **Wallpaper Mode** is implemented as contract, validation, and UI gating
  only, and stays disabled for every experience: no reviewed wallpaper
  implementation exists yet, launches are refused explicitly, and there is
  no fallback to Interactive or Ambient Mode. The remaining implementation
  is specified in `desktop/README.md`.

# Code2Motion desktop beta v0.1.0-beta.1 — 2026-11-02

The launcher beta introduces a five-item curated catalog: Pain-ter, AudiOrbits,
Nebula Core, Spiroling Aftereffect, and Living Fractal Atlas. Each c2merse is a
separately installable, hash-verified package with its own license and
provenance. AudiOrbits is available on Linux only; the other four support
Linux, Windows, and macOS.

The catalog is downloaded from the public
[Code2Motion-Releases repository](https://github.com/nickhilster/Code2Motion-Releases).
The launcher validates catalog package hashes and every file hash before
installing. Catalog updates are not signed yet, so this beta trusts GitHub's
HTTPS delivery and the configured release repository; hashes detect mismatch,
not a malicious catalog publisher.

## Experiences

- **Pain-ter 1.0.0** — MIT, original work by Nikhil Khedkar.
- **AudiOrbits 1.0.0** — GPL-3.0-only, retains its upstream notices and fork
  attribution. It uses Linux GTK/WebKit, GStreamer, and PipeWire components;
  audio capture starts only after the user selects Start.
- **Nebula Core 1.0.0** — MIT, founder-confirmed original homebrew.
- **Spiroling Aftereffect 1.0.0** — MIT, founder-confirmed original homebrew;
  static-export dependency patches are documented in its source provenance.
- **Living Fractal Atlas 1.0.0** — MIT, founder-confirmed original homebrew;
  its remote font import was removed for offline use.

Four launcher thumbnails are screenshots from rendered native WebKit experience
windows. AudiOrbits uses a thumbnail derived from its own packaged fractal art;
the audio-reactive renderer was left paused during capture. The files are in
`desktop/public/experience-thumbnails/`.

The beta installers are unsigned and may show operating-system security
prompts. Review `SHA256SUMS` and the platform notes before installation. This
is a beta. Linux packages are built on Ubuntu; the Windows NSIS installer is
cross-compiled from Ubuntu with `cargo-xwin`, a Tauri-documented but
experimental path; macOS disk images are built on GitHub-hosted macOS runners.
Only the Linux build has been launched on a Linux host. Windows and macOS
clean-machine installation and manual runtime checks remain future
qualification work. The launcher is not an OS sandbox. Its catalog metadata is
not cryptographically signed, and AudiOrbits currently runs with the user's
normal permissions.
