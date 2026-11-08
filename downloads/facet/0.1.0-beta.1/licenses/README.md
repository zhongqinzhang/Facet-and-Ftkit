**English** | [简体中文](README.zh-CN.md)

# Third-party licenses

Facet 0.1.0-beta.1 · **320 entries · 215 unique notice texts**

## Contents

1. [Reading the notices](#reading)
2. [Coverage](#coverage)
3. [Files](#files)
4. [Distribution and remaining provenance](#distribution)

<a id="reading"></a>
## Reading the notices

Choose **Help → About Facet → Third-party licenses**, then expand a category and component. The same notices are installed at `licenses/THIRD_PARTY_NOTICES.txt` and work offline.

These are the original copyright and license terms for dependencies, fonts and data. They are not a publisher-signing certificate and do not assign an open-source license to Facet-owned code. Beta distributions remain subject to the applicable third-party terms.

<a id="coverage"></a>
## Coverage

The inventory covers 99 web, 207 native, 9 asset, 3 system-runtime and 2 installer entries for Windows x64. It conservatively includes dependencies that a linker may remove; entry counts do not measure executing libraries. Build-only dependencies and procedural macros are excluded. Rust's full upstream standard-library notice contains other-platform entries and is not a Windows link map. System DLLs and the separately installed WebView2 runtime are not represented as bundled files. ftkit has a separate inventory.

<a id="files"></a>
## Files

| File | Purpose |
| --- | --- |
| [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) | Offline component index and complete original notices. |
| [third-party-notices.json](third-party-notices.json) | Structured inventory used by About and packaging. |
| [supplemental/](supplemental/) | Original upstream texts, attribution and adaptation statements. |
| [REVIEW.md](REVIEW.md) | Review evidence and unresolved acquisition history. |
| [DATA_SOURCES.md](DATA_SOURCES.md) | Scientific references and compatibility implications. |
| [beta1-data-review.json](beta1-data-review.json) | Current item-by-item data findings. |
| [historical-data-audit.json](historical-data-audit.json) | Pre-correction audit; old pending items are not the current state. |
| [sources.json](sources.json) | Reviewed provenance, resource fingerprints and license choices. |

Original notice texts remain in their original language. The English/Chinese switch changes the explanatory pages, not the legal texts.

<a id="distribution"></a>
## Distribution and remaining provenance

[Corresponding third-party sources](../third-party-sources/README.md) accompany this release: pinned WiX source and the conservatively retained option-ext package. They contain no Facet-owned source and are separate from the installer. Retain notices, attribution and the applicable source materials when redistributing.

newVESTA ownership has been confirmed by its author. Original acquisition records for the legacy VESTA/Studio/CPK palettes remain incomplete. Their colors are preserved for compatibility; numerical agreement does not establish a copying route or resolve every rights question. See the review above.

[Back to release](../README.md)
