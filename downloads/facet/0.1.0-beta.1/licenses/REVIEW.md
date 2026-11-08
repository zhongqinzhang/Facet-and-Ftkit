**English** | [简体中文](REVIEW.zh-CN.md)

# License provenance review

Facet Windows x64 · Reviewed 2026-11-08

## Contents

1. [Verified sources](#sources)
2. [Interpretation](#interpretation)
3. [Remaining work and validation](#limits)

<a id="sources"></a>
## Verified sources

- Production web dependency closure excludes optional development peers. is-mobile uses its versioned README license; missing Ant Design SVG and Tauri-dialog notices were recovered from npm gitHead commits.
- The native inventory contains 207 ordinary external dependencies from the locked, offline Windows graph, excluding owned workspace code, build-only dependencies and procedural macros. Missing ts-rs, moyo, alloc-stdlib, UNIC and webview2 notices were tied to recorded upstream commits; UNIC copyright headers are retained.
- Noto Sans Regular/Bold match Google Fonts commit `3043c22d2f091ead19f47fbcabdd696b8c9b7edd` (blobs `9dd10199bc8e8fcfcc5c3a1a394557ed00c567c5` and `6e00cdce1dac34e409a0111296c90e98c6f40701`). The 2012 Google OFL notice is retained; older embedded Apache metadata is disclosed.
- WebView2 SDK 1.0.3650.58 and its x64 static loader match the recorded official package. SDK LICENSE/NOTICE remain separate from Rust-wrapper MIT notices. Fingerprints are in sources.json.
- Rust 1.97.1, commit `8bab26f4f68e0e26f0bb7960be334d5b520ea452`: complete standard-library notices and compiler-builtins MIT AND Apache-2.0 WITH LLVM-exception texts are retained.
- WiX 3.14.1 is pinned to `b40e9a32c24033e11b77baf2c91a704382f898ed`. The embedded UI DLL hash is `7f47d98ab25cfea9b3a2e898c3376cc9ba1cd893b4948b0c27caa530fd0e34cc`; six images match the source archive. The 13,859,146-byte source archive hash is `3cc4bdaca8070042a182675b047882211d042f35139efcb0eeac35eeb81bf9d3`. WiX source was not rebuilt in this round.
- NSIS 3.11 uses zlib, System, LangDLL and nsDialogs; original COPYING is retained. Unused bzip2/LZMA compressor code is not claimed as shipped.
- Matplotlib, Pretty Lattice, ColorBrewer and Jmol data notices remain. NIST non-SRD terms, Smits CC BY 4.0 attribution/adaptation and BODR compilation notices are included. See [scientific provenance](DATA_SOURCES.md).

<a id="interpretation"></a>
## Interpretation

AND expressions retain all applicable texts; legacy slash expressions are reviewed against actual licenses. brotli-decompressor is recorded from its BSD text. option-ext remains conservatively listed although its dirs-sys consumer is Unix-only and the reviewed Windows rlib code/data sections were empty. MPL notice and original source are provided without assigning a license to Facet-owned code.

The complete Rust notice includes other targets and is not a Windows link map. Generated output is distinguished from actual embedded WiX code. License materials and corresponding third-party source remain separate from Facet-owned implementation.

<a id="limits"></a>
## Remaining work and validation

newVESTA ownership is confirmed. Beta 1 has 320 entries and 215 unique texts; prior alpha records remain historical. Covalent radii, Lr and reference classifications are corrected as described in the current data review. Legacy VESTA/Studio/CPK acquisition records remain incomplete; a technical inventory does not settle every rights question.

The candidate passed static checks, builds, package/hash inspection and manual sample UI/save/reopen review. No automated tests were run; final-package installation, native dialogs and actual exports remain unchecked. Public documentation was subsequently reorganized by language without changing the installer or original notices. Raw papers and local browser data are excluded.

[Release verification scope](../README.md#verification) · [License index](README.md)
