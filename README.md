# Facet & ftkit

<a id="downloads"></a>
## 最新下载 / Latest downloads · 2026-10-23

| 软件 / Product | 最新发行 / Current release | 平台 / Platform | 下载 / Download | 文档 / Docs |
| --- | --- | --- | --- | --- |
| **Facet** | **0.1.1-alpha-20261023-i18n** | Windows x64 · 中文 / English | **[下载 EXE / Installer · 10.57 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.1-alpha-20261023-i18n/Facet-Setup-0.1.1-alpha-20261023-x64.exe)** | [安装与更新 / Install & changes](downloads/facet/0.1.1-alpha-20261023-i18n/README.md) |
| **ftkit** | **0.1.3-preview-20261022-phononfix** | Linux x86_64 | **[下载 tar.gz / Archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)** | [安装与更新 / Install & changes](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md) |

**Facet 已包含安装语言修复：安装时选 English，安装后首次启动即使用英文。** 此后手动切换语言仍会保存。

**Facet includes the installation-language fix: choose English during setup to use English on the next launch.** Later manual preferences remain effective.

[全部版本 / All releases](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases) · [备用下载目录 / Repository downloads](downloads/README.md) · [更新记录 / Changelog](CHANGELOG.md) · [版本与校验清单 / Version manifest](versions.json)

Facet 用于晶体、原子结构和计算结果可视化；ftkit 将支持的 VASP、Quantum ESPRESSO 结果转换为 Facet 文件。此公开仓库仅提供发行包和使用文档。

Facet visualizes crystal and atomic structures and simulation results. ftkit converts supported VASP and Quantum ESPRESSO results into Facet files. This public repository distributes packages and user documentation only.

## 目录 / Contents

1. [最新下载 / Latest downloads](#downloads)
2. [首次安装 / Quick start](#quick-start)
3. [本次更新 / What's new](#changes)
4. [使用文档 / User guides](#guides)
5. [校验下载 / Verify downloads](#checksums)
6. [历史版本 / Version history](#versions)
7. [反馈 / Feedback](#feedback)

<a id="quick-start"></a>
## 首次安装 / Quick start

### Facet · Windows x64

1. 下载上表 EXE，核对 SHA-256，保存工作并关闭已有 Facet。Download the EXE above, verify its SHA-256, save your work and close Facet.
2. 运行安装包，选择 English 或简体中文，完成安装后打开 Facet。Run setup, choose English or Simplified Chinese, complete installation and open Facet.
3. 本次安装的语言选择在首次启动应用一次；随后可在顶栏“界面语言 / Display language”修改，下次启动生效。The installation choice is applied once on the next launch. Later changes in **Display language** take effect after restarting Facet.

一套程序核心内置两种语言资源。再次完成安装或修复会采用新的语言选择。详见[安装说明](downloads/facet/0.1.1-alpha-20261023-i18n/README.md)。

One application core includes both languages. Completing another installation or repair applies the new language choice. See the [installation notes](downloads/facet/0.1.1-alpha-20261023-i18n/README.md).

### ftkit · Linux x86_64

将压缩包和对应的 SHA256SUMS.txt 放在同一目录，再运行 / Place the archive and its SHA256SUMS.txt in the same directory, then run:

~~~bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
~~~

保留解压目录。只核验、不配置 PATH 时使用 `bash verify.sh --no-install`。之后进入计算目录运行 `ftkit`；不需要 Python 或 Facet。

Keep the extracted directory. Use `bash verify.sh --no-install` to verify without configuring PATH. Then run `ftkit` in your calculation directory; Python and Facet are not required.

<a id="changes"></a>
## 本次更新 / What's new

- **Facet**：安装语言首次启动修复；晶胞边框局部深度；矢量/键状态与弹出控件修正；此前的主题、侧栏与 STM 更新。Installation-language startup fix; local unit-cell-edge depth; vector/bond state and popup fixes; preceding theme, sidebar and STM updates.
- **ftkit**：VASP 质量修正声子段复合标题兼容修复，晶胞和 POMASS 一致性检查覆盖到文件末尾。Support for compound headings in VASP mass-corrected phonon sections; lattice and POMASS consistency checks through the end of the file.

Facet 于 **2026-10-23** 重新构建，基于 **be3f27d9** 加已确认的语言修复。ftkit 为 **2026-10-22** 构建的最新归档，本次原样发布。两者均为预发布版本。

Facet was rebuilt on **2026-10-23** from **be3f27d9** plus the approved language fix. ftkit is the latest archive, built on **2026-10-22** and published unchanged. Both are prereleases.

构建与文件校验已完成；其余测试按本轮要求停止，详见[验证记录](downloads/facet/0.1.1-alpha-20261023-i18n/verification/README.md)。真实 Windows 安装及 Linux 运行验收未在本轮完成。

Builds and file checks completed; remaining tests were stopped as requested. See the [validation record](downloads/facet/0.1.1-alpha-20261023-i18n/verification/README.md). End-to-end Windows installation and Linux execution were not completed in this publication.

<a id="guides"></a>
## 使用文档 / User guides

- Facet：[中文手册](downloads/facet/0.1.1-alpha-20261023-i18n/docs/zh-CN/user-guide.txt) · [English user guide](downloads/facet/0.1.1-alpha-20261023-i18n/docs/en-US/user-guide.txt) · [本版中英对应 / Bilingual changes](downloads/facet/0.1.1-alpha-20261023-i18n/Progress.zh-en.md)
- ftkit：[中文手册](downloads/ftkit/0.1.3-preview-20261022-phononfix/用户手册.txt) · [中英安装说明 / Bilingual setup guide](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md)

<a id="checksums"></a>
## 校验下载 / Verify downloads

[Facet SHA-256](downloads/facet/0.1.1-alpha-20261023-i18n/SHA256SUMS.txt) · [ftkit SHA-256](downloads/ftkit/0.1.3-preview-20261022-phononfix/SHA256SUMS.txt)

Windows PowerShell：将结果与 Facet 校验清单比较 / Compare the result with Facet's checksum file:

~~~powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.1-alpha-20261023-x64.exe
~~~

Linux：在 ftkit 压缩包和校验清单所在目录运行 / Run in the directory containing the ftkit archive and its checksum file:

~~~bash
sha256sum -c SHA256SUMS.txt
~~~

<a id="versions"></a>
## 历史版本 / Version history

- 两个产品各自编号，使用 `facet-v…` 和 `ftkit-v…` 标签。Products have independent versions and tag prefixes.
- 新版写入 `downloads/产品/版本/`，保留旧包、校验值和标签；不覆盖既有发行文件。New versions get separate directories; existing packages, checksums and tags are preserved.
- [versions.json](versions.json) 按最新在前排列并记录完整版本号、日期、大小、SHA-256 和下载链接。The manifest lists newest versions first with dates, sizes, SHA-256 and download links.
- 应用内版本可能不随发行修订号变化；请用完整包名和哈希识别版本。The in-app version may remain unchanged between distribution revisions; identify a package by its full filename and hash.

GitHub Release 自动附带的 “Source code” 归档只是本发行仓库的快照，包含安装包与文档。安装请使用本页明确标注的 EXE 或 tar.gz 文件。

GitHub's automatic “Source code” archives are snapshots of this distribution repository containing packages and documents. Install using the specific EXE or tar.gz linked above.

<a id="feedback"></a>
## 反馈 / Feedback

在 [Issues](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues) 中注明产品名、完整发行版本、操作系统和复现步骤。Please include the product, full distribution version, operating system and reproduction steps in [Issues](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues).
