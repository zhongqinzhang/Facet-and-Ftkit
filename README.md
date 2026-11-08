**English** | [简体中文](README.zh-CN.md)

# Facet & ftkit

<a id="downloads"></a>
## Latest downloads

| Product | Current release | Platform | Download |
| --- | --- | --- | --- |
| **Facet** | **0.1.0-beta.1 · Beta 1** | Windows x64 · Chinese and English | **[Download installer · 12.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.0-beta.1/Facet-Setup-0.1.0-beta.1-x64.exe)** · [Repository copy](https://raw.githubusercontent.com/zhongqinzhang/Facet-and-Ftkit/main/downloads/facet/0.1.0-beta.1/Facet-Setup-0.1.0-beta.1-x64.exe) |
| **ftkit** | **0.1.3-preview-20261022-phononfix** | Linux x86_64 | **[Download archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)** |

**User manuals:** [Facet user manual](downloads/facet/0.1.0-beta.1/docs/en-US/user-guide.txt) · [ftkit full user guide (Chinese)](downloads/ftkit/0.1.3-preview-20261022-phononfix/用户手册.txt)  
**Installation guides:** [Facet](downloads/facet/0.1.0-beta.1/README.md) · [ftkit](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md)

[Previous versions](downloads/README.md) · [Changelog](CHANGELOG.md) · [Version manifest and checksums](versions.json)

Facet visualizes crystal and atomic structures and simulation results. ftkit converts supported VASP and Quantum ESPRESSO results into Facet files. This repository provides distributions and user documentation. Developed by **[Ji Group](https://g.ruc.edu.cn/) · Renmin University of China**.

## Contents

1. [Latest downloads](#downloads)
2. [Getting started](#quick-start)
3. [What's new](#changes)
4. [Checksums and versions](#versions)
5. [Feedback](#feedback)

<a id="quick-start"></a>
## Getting started

- **Facet:** Download the EXE, save your work and close Facet, then run setup and choose a language and installation scope. One application core includes both languages. Later in-app language changes take effect after restart. See the [installation guide](downloads/facet/0.1.0-beta.1/README.md) for steps and validation limits.
- **ftkit:** Follow the [installation guide](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md) to verify and extract the tar.gz archive, then run `bash verify.sh`. Keep the extracted directory. Run `ftkit` in your calculation directory; Python and Facet are not required. The complete ftkit manual is currently available in Chinese.

<a id="changes"></a>
## What's new

Facet Beta 1 expands the shared covalent-radius table to 96 entries, corrects Lr, identifies estimates/compilations/predictions/fallbacks, adds About and manual update checking, includes third-party notices, and updates both manuals. Old covalent-bond caches are rebuilt; coordinates, colors, manual bonds and saved radius multipliers retain their existing contracts.

Static checks, builds, package inspection and sample UI/save/reopen review were completed. No automated tests were run. English first launch after installation, replacement installation, uninstall and native exports were not rechecked for the final package. Some historical palette acquisition records remain incomplete. See the [release details](downloads/facet/0.1.0-beta.1/README.md#verification).

The current ftkit package remains the October 22 phonon-fix archive. It is preserved without rebuilding.

<a id="versions"></a>
## Checksums and versions

[Facet SHA-256](downloads/facet/0.1.0-beta.1/SHA256SUMS.txt) · [ftkit SHA-256](downloads/ftkit/0.1.3-preview-20261022-phononfix/SHA256SUMS.txt)

```powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.0-beta.1-x64.exe
```

Each release has its own directory and tag. Existing packages, manuals and checksums are retained. [versions.json](versions.json) explicitly selects the current release for each product; filename sorting does not determine release order. The chosen Beta version is `0.1.0-beta.1`.

Facet-owned and ftkit-owned source code is excluded. The accompanying [WiX/option-ext source archives](downloads/facet/0.1.0-beta.1/third-party-sources/README.md) are third-party compliance materials, do not need installation and are separate from the main installer. GitHub's automatic Source code archives are snapshots of this distribution repository; install using the specific EXE or tar.gz above.

<a id="feedback"></a>
## Feedback

Please include the product, full release version, operating system and reproduction steps in [Issues](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues).
