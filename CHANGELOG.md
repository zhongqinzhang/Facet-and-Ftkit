**English** | [简体中文](CHANGELOG.zh-CN.md)

# Changelog

**Latest publication: 2026-11-08** · [Download](README.md#downloads)

## Contents

1. [2026-11-08 · Facet Beta 1](#release-2026-11-08)
2. [2026-11-06 · Documentation erratum](#docs-2026-11-06)
3. [2026-10-23 · Alpha and phonon fix](#release-2026-10-23)
4. [2026-10-17 · Initial publication](#release-2026-10-17)
5. [Version policy](#future-releases)

<a id="release-2026-11-08"></a>
## 2026-11-08 · Facet 0.1.0-beta.1

- Publish the first Beta installer, 12.83 MB, with the reviewed 96-entry covalent-radius table, corrected Lr configuration, source labels, About/update checking, font subset, licenses and aligned manuals.
- Separate English and Chinese navigation throughout the home, download index, release guides and current license introductions. English is the default; the language links switch to a complete translated page.
- Keep the existing ftkit 0.1.3-preview-20261022-phononfix archive, historical binaries, bundled manuals and checksums unchanged.
- Static checks, builds, package inspection and manual sample save/reopen were completed. No automated tests were run; final-package installation and native export validation remain outstanding.
- [Beta release details](downloads/facet/0.1.0-beta.1/README.md).

<a id="docs-2026-11-06"></a>
## 2026-11-06 · Documentation erratum

The October 23 bundled notes incorrectly name `aa74b4d5`. The build uses `be3f27d9` plus the installation-language fix. The [erratum](downloads/facet/0.1.1-alpha-20261023-i18n/README.md#documentation-erratum) changes no archived binaries, manuals, manifests or checksums.

<a id="release-2026-10-23"></a>
## 2026-10-23 · Alpha and phonon fix

- **Facet 0.1.1-alpha-20261023-i18n:** rebuilt from `be3f27d9` plus the installation-language fix; includes local cell-frame depth and vector/bond, popup, theme and sidebar corrections. Installation language applies once on next launch; subsequent manual preferences are retained. Original builds/file checks and partial tests completed; remaining tests were stopped as requested. [Details](downloads/facet/0.1.1-alpha-20261023-i18n/README.md).
- **ftkit 0.1.3-preview-20261022-phononfix:** publish the October 22 archive unchanged. Fix compound VASP mass-corrected headings and check lattice/POMASS consistency through the end of the file. [Details](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md).
- Put current downloads and manual links first; retain October 16 archives and tags.

<a id="release-2026-10-17"></a>
## 2026-10-17 · Initial publication

- **Facet 0.1.1-alpha-20261016-i18n:** one core, Chinese/English resources, sequence scalar plots, STM overlays, polyhedra and saved 2D views. Includes `06e80d6` scalar-plot refinements, LOCPOT removal and recovery-failure messages. Built October 16; archived unchanged October 17. [Details](downloads/facet/0.1.1-alpha-20261016-i18n/README.md).
- **ftkit 0.1.3-preview-20261016-r2:** statically linked Linux preview with relative-energy labels for tasks 101/103, the ftkit rename and earlier phonon-capacity fixes. Built October 16 and preserved unchanged. [Details](downloads/ftkit/0.1.3-preview-20261016-r2/README.md).
- Start a standalone distribution repository with product/version directories, checksums and tags, without application source or development history.

<a id="future-releases"></a>
## Version policy

New releases receive new directories and tags. Update the home and versions.json and preserve older packages, manuals and hashes. A repackaged binary needs a new version or revision; documentation corrections are identified separately.
