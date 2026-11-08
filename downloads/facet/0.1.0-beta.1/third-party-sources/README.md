**English** | [简体中文](README.zh-CN.md)

# Corresponding third-party source

## Contents

1. [Archives](#archives)
2. [Verification and redistribution](#verification)

<a id="archives"></a>
## Archives

These archives are third-party compliance materials. They contain no Facet-owned source and do not need to be installed.

| Archive | Component |
| --- | --- |
| [WiX 3.14.1 source](wix3-b40e9a32c24033e11b77baf2c91a704382f898ed.zip) | Complete unmodified source pinned to b40e9a32, including embedded MSI UI actions, helper libraries, images and build files. LICENSE.TXT contains MS-RL. |
| [option-ext 0.2.0](option-ext-0.2.0.crate) | Original MPL-2.0 crate retained for the conservative inventory; its consumer does not use the code on Windows. A .crate file is a tar.gz archive. |

<a id="verification"></a>
## Verification and redistribution

[SOURCE-MANIFEST.json](SOURCE-MANIFEST.json) records original URLs, exact sizes and hashes. [SHA256SUMS.txt](SHA256SUMS.txt) lists archive checksums. The archives came from pinned upstream versions; their code was not executed. WiX images and the previously reviewed official UI DLL were compared with the final MSI; WiX source was not rebuilt.

Keep this directory accessible alongside the installer and notices when distributing the release. These files are separate from the 12.83 MB installer and are not extra installation programs.

[Release](../README.md) · [Notices](../licenses/README.md)
