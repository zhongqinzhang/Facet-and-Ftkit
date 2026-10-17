# Facet & ftkit — 下载与版本 / Downloads and releases

Facet 用于晶体与原子结构及计算结果的可视化；ftkit 将支持的 VASP、Quantum ESPRESSO 结果转换为 Facet 文件。此公开仓库仅发布安装包、发行压缩包和使用说明，不包含应用源码或开发仓库的提交历史。

Facet visualizes crystal and atomic structures and simulation results. ftkit converts supported VASP and Quantum ESPRESSO outputs into Facet files. This public repository contains binary distributions and user documentation only. Application source code and development history are not included.

## 目录 / Contents

1. [最新下载 / Latest downloads](#downloads)
2. [快速开始 / Quick start](#quick-start)
3. [校验文件 / Verify your download](#checksums)
4. [版本管理 / Version history](#versions)
5. [反馈 / Feedback](#feedback)

<a id="downloads"></a>
## 最新下载 / Latest downloads

| 软件 / Product | 发行版本 / Release | 平台 / Platform | 下载 / Download | 说明 / Notes |
| --- | --- | --- | --- | --- |
| Facet | 0.1.1-alpha-20261016-i18n | Windows x64 | [安装包 · Installer · 10.01 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.1-alpha-20261016-i18n/Facet-Setup-0.1.1-alpha-20261016-x64.exe) | [中文 / English](downloads/facet/0.1.1-alpha-20261016-i18n/README.md) |
| ftkit | 0.1.3-preview-20261016-r2 | Linux x86_64 | [压缩包 · Archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261016-r2/ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz) | [中文 / English](downloads/ftkit/0.1.3-preview-20261016-r2/README.md) |

Facet 安装时可选择简体中文或 English，一份程序核心包含两种语言资源。ftkit 是独立的 Linux 命令行工具，无需安装 Facet 或 Python。

Choose Simplified Chinese or English when installing Facet; both languages share one application core. ftkit is a standalone Linux command-line tool and does not require Facet or Python.

当前两个版本均为预发布版。包的构建日期为 **2026-10-16**，本仓库首次发布日期为 **2026-10-17**；本次发布保留原始文件及校验值，没有重新构建。

Both packages are prereleases, built on **2026-10-16** and first published in this repository on **2026-10-17**. The original files and checksums are preserved; the packages have not been rebuilt for this publication.

[全部发行 / All releases](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases) · [目录下载 / Browse downloads](downloads/README.md) · [更新记录 / Changelog](CHANGELOG.md)

<a id="quick-start"></a>
## 快速开始 / Quick start

### Facet · Windows

1. 下载上表中的安装包，并按下节核对 SHA-256。Download the installer above and verify its SHA-256.
2. 运行安装包，选择安装语言并完成安装。Run the installer, select a language, and complete the installation.
3. 在应用顶栏更改“界面语言 / Display language”后，重新启动应用使设置生效。Restart Facet after changing **Display language** in the top bar.

已有的应用语言偏好优先于安装器选择。旧的独立 Facet English 安装及其用户数据不会自动迁移，详见[版本说明](downloads/facet/0.1.1-alpha-20261016-i18n/README.md)。

An existing application language preference takes precedence over the installer selection. A previous standalone Facet English installation and its user data are not migrated automatically. See the [release notes](downloads/facet/0.1.1-alpha-20261016-i18n/README.md).

### ftkit · Linux

下载并校验压缩包，然后在 Linux 终端执行：

Download and verify the archive, then run these commands in a Linux terminal:

~~~bash
tar -xzf ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261016-r2-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
~~~

验证成功后，verify.sh 会将解压目录配置到 Bash PATH。请保留该目录；仅验证而不配置 PATH 时使用 bash verify.sh --no-install。中文手册位于包内 docs/zh-CN/。

After successful verification, verify.sh adds the extracted directory to your Bash PATH. Keep that directory in place. Use bash verify.sh --no-install to verify without configuring PATH. The Chinese user guide is included under docs/zh-CN/.

<a id="checksums"></a>
## 校验文件 / Verify your download

每个版本都附带 **SHA256SUMS.txt**，可从对应 Release 或版本目录下载：

Each release includes **SHA256SUMS.txt**, available from its Release page and version directory:

- [Facet SHA-256](downloads/facet/0.1.1-alpha-20261016-i18n/SHA256SUMS.txt)
- [ftkit SHA-256](downloads/ftkit/0.1.3-preview-20261016-r2/SHA256SUMS.txt)

Windows PowerShell：

~~~powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.1-alpha-20261016-x64.exe
~~~

将结果与 Facet 的 SHA256SUMS.txt 比较。Compare the result with Facet's SHA256SUMS.txt.

Linux：将 ftkit 压缩包与其 SHA256SUMS.txt 放在同一目录，再运行：

Linux: place the ftkit archive and its SHA256SUMS.txt in the same directory, then run:

~~~bash
sha256sum -c SHA256SUMS.txt
~~~

<a id="versions"></a>
## 版本管理 / Version history

- **分别编号 / Separate versions**：Facet 与 ftkit 分别维护版本；Git 标签使用 facet-v… 和 ftkit-v… 前缀。Facet and ftkit have independent versions, with facet-v… and ftkit-v… Git tag prefixes.
- **保留历史 / Keep previous releases**：发行文件位于 downloads/产品/版本/；新版本使用新目录和新标签，保留旧文件与校验值。Each version has its own product/version directory and tag. Keep previous packages and checksums.
- **不覆盖已发布包 / Do not replace published files**：重打包或修正包内容时增加版本或修订号，不复用同一个标签。A changed or rebuilt package gets a new version or revision and a new tag.
- **最新入口 / Current versions**：本页提供下载入口；[versions.json](versions.json) 记录每个产品的最新版本、文件大小、SHA-256 和历史版本。[CHANGELOG.md](CHANGELOG.md) 提供中英文更新记录。This page provides download links; versions.json records current versions and package metadata, while CHANGELOG.md records release changes.
- **发布流程 / Publishing**：新建版本目录，核对包与校验值，更新版本清单和说明，提交后创建对应标签与 Release。Add the version directory, verify the package and checksum, update the manifest and notes, commit, and create the matching tag and Release.

GitHub 的 Release 页面会自动显示 Source code (zip/tar.gz)。这些是本发布仓库的自动归档，只包含发行文件与说明；安装软件请下载上表指定的文件。

GitHub automatically lists Source code (zip/tar.gz) archives on Release pages. They are snapshots of this distribution repository and contain only its release files and documentation. Download the specific installer or archive listed above to use the software.

<a id="feedback"></a>
## 反馈 / Feedback

请在 [Issues](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues) 中提供软件名称、完整发行版本、操作系统、复现步骤和相关错误信息。

Please include the product name, full release version, operating system, steps to reproduce, and relevant error messages when opening an [issue](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues).
