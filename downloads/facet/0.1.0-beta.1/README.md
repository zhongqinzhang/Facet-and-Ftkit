**English** | [简体中文](README.zh-CN.md)

# Facet 0.1.0-beta.1 · Beta 1

**[Download Windows x64 installer · 12.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.0-beta.1/Facet-Setup-0.1.0-beta.1-x64.exe)**  
[English user manual](docs/en-US/user-guide.txt) · [Release notes](docs/en-US/release-notes.txt)

Built and published: 2026-11-08 · 12,828,535 bytes · [Repository download](Facet-Setup-0.1.0-beta.1-x64.exe?raw=true) · [SHA-256](SHA256SUMS.txt)

## Contents

1. [Installation and language](#installation)
2. [Changes](#changes)
3. [Existing projects](#compatibility)
4. [Verification scope](#verification)
5. [Licenses and provenance](#licenses)

<a id="installation"></a>
## Installation and language

1. Verify the installer SHA-256, save your work and close Facet.
2. Run the EXE and choose English or Simplified Chinese.
3. Choose a per-user or all-users installation, select the directory and finish setup. All-users installation requires administrator permission.
4. Open **Help → About Facet** to view the full version and check for updates. Later changes through the toolbar's display-language control take effect after restart.

One core includes both languages. Setup initializes the language on the next launch; subsequent manual preferences are saved. First launch after installation has not been rechecked with this final package. Uninstall retains preferences and recovery data by default; clearing those data requires an explicit selection. Saved project files are retained. The installer does not have a paid publisher-identity signature.

<a id="changes"></a>
## Changes

- Use `0.1.0-beta.1` throughout; fix the `0.0.0` version entry point for new projects and exported structure packages.
- Share one 96-entry Cordero covalent-radius table, H–Cm, between frontend and Rust. Twelve reference entries are added; ten numerical values change.
- Correct Lr to `[Rn] 5f14 7s2 7p1`; identify estimates, compilations, theoretical predictions and fallbacks with source descriptions.
- Retain van der Waals values while correcting provenance and legacy-palette descriptions. Include 320 notice entries and 215 unique texts.
- Keep the compact font subset, compact About view, manual update checking and full version display. Manuals align across 21 chapters and 86 numbered subsections.

<a id="compatibility"></a>
## Existing projects

Coordinates, lattice, manual bonds, deleted-auto-bond overrides, colors, radius multipliers, originating version metadata and project format are retained. New reference radii can change affected sphere sizes and covalent bonds, including related 2D/3D views and exports. Old covalent caches rebuild; absolute-distance caches are unchanged by this data revision.

Windows Installer uses numeric version `0.1.0`; the app displays the full beta label. Installer configuration permits downgrades, but replacing an older alpha still needs installation validation. The update index explicitly identifies the current release instead of inferring publication order from version magnitude.

<a id="verification"></a>
## Verification scope

Completed checks include `pnpm check`, production builds, the language transform, 13 packaged resources, hashes and actual Chrome/WebView2 observations. A sample was viewed in 2D/3D, saved and reopened; legacy caches, manual bonds, colors and multipliers were inspected. No automated tests were run. Installation first launch, upgrades/downgrades, uninstall, native file dialogs and actual exports were not rechecked for this final package. The new-project version entry point passed static/build checks; actual Save As remains unchecked.

The package was built from `3205a156` plus reviewed changes, subsequently recorded in private source commit `4d868d0a`. Commit identity does not replace the artifact hash. See the [release manifest](release-manifest.json).

<a id="licenses"></a>
## Licenses and provenance

[Third-party licenses](licenses/README.md) · [Scientific data provenance](licenses/DATA_SOURCES.md) · [Corresponding third-party source](third-party-sources/README.md)

Original acquisition records for legacy VESTA/Studio/CPK palettes remain incomplete; colors are retained for compatibility. Ownership of newVESTA is confirmed. Notices accompany the distribution; original research papers are excluded.

[Back to latest downloads](../../../README.md#downloads)
