# Facet 0.1.1-alpha-20261023-i18n

**[下载 Windows x64 安装包 / Download Windows x64 installer · 10.57 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.1-alpha-20261023-i18n/Facet-Setup-0.1.1-alpha-20261023-x64.exe)**

2026-10-23 · Alpha · 简体中文 / English · 一套程序核心 / One application core

[备用下载 / Repository download](Facet-Setup-0.1.1-alpha-20261023-x64.exe?raw=true) · [SHA-256](SHA256SUMS.txt) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/facet-v0.1.1-alpha-20261023-i18n)

## 目录 / Contents

1. [安装与语言 / Installation and language](#installation)
2. [更新内容 / What's new](#changes)
3. [用户文档 / Documentation](#docs)
4. [版本来源与验证 / Provenance and validation](#verification)

<a id="installation"></a>
## 安装与语言 / Installation and language

1. 保存工作并关闭 Facet，下载并校验本页 EXE。Save your work, close Facet, then download and verify the EXE above.
2. 运行安装包，选择 **English** 或 **简体中文** 并完成安装。Run setup, choose **English** or **Simplified Chinese**, and complete installation.
3. 安装后首次打开即采用这次选择，即使之前保存了中文或跟随系统。The next launch uses this installation choice, even if an earlier preference selected Chinese or System default.
4. 此后在顶栏“界面语言 / Display language”手动修改，保存后下次启动生效；再次完成安装或修复会应用新的安装选择。Later changes to **Display language** take effect on the next launch. Completing another installation or repair applies its new choice.

升级前保存项目。安装包沿用 Facet 的产品升级标识；旧的独立 Facet English 安装及其数据不自动迁移。

Save your projects before upgrading. The installer retains Facet's upgrade identity. A previous standalone Facet English installation and its data are not migrated automatically.

~~~powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.1-alpha-20261023-x64.exe
~~~

与 [SHA256SUMS.txt](SHA256SUMS.txt) 对照 / Compare with the checksum file:

~~~text
5c580fc700864d17fb341301d26b880673d0db0fa087ac992b3927f4a513051f
~~~

<a id="changes"></a>
## 更新内容 / What's new

- 修复安装选择英文后首次打开仍为中文的问题；保留之后的手动语言设置。Fixes the first launch ignoring English selected during setup, while preserving later manual preferences.
- 晶胞边框遵循局部前后关系，涵盖 2D、3D 和图片导出。Unit-cell edges respect local depth in 2D, 3D and image exports.
- 矢量编辑保留有效的键计算状态，修正弹出控件可见性。Vector editing preserves valid bond-computation state; popup visibility is corrected.
- 包含主题默认值、侧栏控件、STM 性能与可靠性更新，以及 3769 条成对中英文资源。Includes theme-default, sidebar-control and STM performance and reliability updates, with 3,769 paired Chinese and English messages.

<a id="docs"></a>
## 用户文档 / Documentation

- [中文用户手册](docs/zh-CN/user-guide.txt) · [English user guide](docs/en-US/user-guide.txt)
- [中文更新说明](docs/zh-CN/release-notes.txt) · [English release notes](docs/en-US/release-notes.txt)
- [本版中英文进展对应 / Bilingual changes](Progress.zh-en.md)
- [完整中英文资源表 / Complete language catalog](Language-catalog.tsv)

<a id="verification"></a>
## 版本来源与验证 / Provenance and validation

发行版本 **0.1.1-alpha-20261023-i18n**，构建日期 **2026-10-23**。源码基线 **be3f27d9bbc6875d1b5b8e5965496f7f2dec979c**，叠加已确认的安装语言修复。应用内版本为 **0.1.1-alpha**；区分发行包时请使用本页完整编号和 SHA-256。

Release **0.1.1-alpha-20261023-i18n**, built on **2026-10-23** from revision **be3f27d9** plus the approved installation-language fix. The application reports **0.1.1-alpha**; use the full distribution revision and SHA-256 to identify this package.

科学文件格式沿用 Project 33、结构包 25、序列包 12、声子包 8；语言设置独立于项目数据和撤销历史。Scientific formats remain Project 33, Structure Package 25, Sequence Package 12 and Phonon Package 8. Language preferences are separate from project data and undo history.

本次已完成构建、文件校验及部分测试；按用户要求停止余下测试。**不声称本版已完成全套测试或真实 Windows 安装验收。** 详见[验证记录](verification/README.md)和[发行清单](release-manifest.json)。

Builds, file checks and part of the test suite completed; remaining tests were stopped as requested. **This release does not claim a complete test run or an end-to-end Windows installation check.** See the [validation record](verification/README.md) and [release manifest](release-manifest.json).

[返回最新下载 / Latest downloads](../../../README.md) · [所有版本 / All versions](../../../CHANGELOG.md)
