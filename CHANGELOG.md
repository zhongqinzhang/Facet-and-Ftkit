# 更新记录 / Changelog

此处记录公开发行包的版本与变化，分别标明构建日期与发布日期。已发布的包保留原始文件名与 SHA-256。

This log records public distributions and their changes, with separate build and publication dates. Published packages retain their original filenames and SHA-256 checksums.

## 目录 / Contents

1. [2026-10-17 · 首次发布 / Initial publication](#release-2026-10-17)
2. [后续版本 / Future releases](#future-releases)

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
