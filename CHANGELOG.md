# 更新记录 / Changelog

**最新发布 / Latest publication: 2026-10-23** · [立即下载 / Download now](README.md#downloads)

## 目录 / Contents

1. [2026-10-23 · 最新发行 / Latest publication](#release-2026-10-23)
2. [2026-10-17 · 首次发布 / Initial publication](#release-2026-10-17)
3. [后续版本 / Future releases](#future-releases)

<a id="release-2026-10-23"></a>
## 2026-10-23 · 最新发行 / Latest publication

### Facet 0.1.1-alpha-20261023-i18n

- 基于 **be3f27d9**，叠加安装语言修复；2026-10-23 重新构建。Rebuilt on **2026-10-23** from **be3f27d9** plus the installation-language fix.
- 安装选英文后首次启动即为英文，后续手动语言设置仍保留。English selected during setup takes effect on the next launch; later manual preferences remain effective.
- 纳入晶胞边框局部深度、矢量/键状态、弹出控件、主题与侧栏修正。Includes local cell-frame depth, vector/bond state, popup, theme and sidebar fixes.
- 已完成构建与文件校验；其余测试按要求停止。Builds and file checks completed; remaining tests were stopped as requested.
- [中英版本说明 / Bilingual release notes](downloads/facet/0.1.1-alpha-20261023-i18n/README.md) · [下载 / Download](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.1-alpha-20261023-i18n/Facet-Setup-0.1.1-alpha-20261023-x64.exe)

### ftkit 0.1.3-preview-20261022-phononfix

- 修复 VASP 质量修正段复合标题识别，并将晶胞/POMASS 一致性检查延续到文件末尾。Fixes compound VASP mass-corrected headings and checks lattice/POMASS consistency through the end of the file.
- 原样发布 2026-10-22 归档，保留原文件名与 SHA-256；本次不重新编译。Publishes the October 22 archive unchanged, preserving its filename and SHA-256; no rebuild for this publication.
- [中英版本说明 / Bilingual release notes](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.md) · [下载 / Download](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)

### 文档与版本管理 / Documentation and version management

首页和下载页置顶最新包；补充中英安装说明、手册入口、来源信息和校验值。保留 10 月 16 日的历史文件与标签。公开仓库不加入应用源码。

The home and downloads pages put current packages first, with bilingual installation instructions, manuals, provenance and checksums. Previous files and tags are preserved. Application source code is excluded.

<a id="release-2026-10-17"></a>
## 2026-10-17 · 首次发布 / Initial publication

### Facet 0.1.1-alpha-20261016-i18n

- Windows x64 安装包，一套核心与简体中文、English 资源。Windows x64 installer with one application core and Simplified Chinese and English resources.
- 包含序列标量图、STM 结构叠加、多面体及保存的 2D 视图恢复功能；包含开发版本 06e80d6 的标量图改进、LOCPOT 支持移除及恢复失败状态提示。Includes sequence scalar plots, STM structure overlays, polyhedra, and saved 2D view restoration, together with the scalar-plot refinements, removal of LOCPOT support, and recovery-failure status from development revision 06e80d6.
- 构建日期为 2026-10-16；2026-10-17 核对后原样归档。Built on 2026-10-16 and archived unchanged after verification on 2026-10-17.
- [版本说明 / Release notes](downloads/facet/0.1.1-alpha-20261016-i18n/README.md) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/facet-v0.1.1-alpha-20261016-i18n)

### ftkit 0.1.3-preview-20261016-r2

- Linux x86_64 静态链接预览包，无需 Python 或 Facet。Statically linked Linux x86_64 preview; Python and Facet are not required.
- 任务 101 / 103 使用 Relative energy (eV)，每份输出以最低能量为零点，缺失能量保持缺失。Tasks 101 and 103 use **Relative energy (eV)**, measured from the minimum in each output; missing energies remain missing.
- 包含 ftkit 更名及此前的声子容量修正。Includes the ftkit rename and previous phonon-capacity fixes.
- 构建日期为 2026-10-16；本次保留原始归档。Built on 2026-10-16; the original archive is preserved.
- [版本说明 / Release notes](downloads/ftkit/0.1.3-preview-20261016-r2/README.md) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/ftkit-v0.1.3-preview-20261016-r2)

### 仓库 / Repository

建立独立的发行仓库，提供中英对照说明、各产品的版本目录、SHA-256 清单和 Git 标签。仓库从独立的初始提交开始，没有导入开发源码或其提交历史。

Created a standalone distribution repository with Chinese-English documentation, product/version directories, SHA-256 checksums, and Git tags. It starts from an independent initial commit and does not import application source code or development history.

<a id="future-releases"></a>
## 后续版本 / Future releases

新版本在本文件顶部新增记录，更新 README 与 versions.json，保留已有版本目录、文件和标签。重打包也使用新的版本或修订号。

Add each new release at the top of this log, update README and versions.json, and preserve existing version directories, files, and tags. Repackaged files also receive a new version or revision.
