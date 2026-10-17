# Facet 0.1.1-alpha-20261016-i18n

Windows x64 · 简体中文 / English · Alpha

## 目录 / Contents

1. [下载与安装 / Download and installation](#installation)
2. [本版内容 / Release contents](#contents)
3. [校验与验证范围 / Checksums and validation](#verification)

<a id="installation"></a>
## 下载与安装 / Download and installation

[下载安装包 / Download installer](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.1-alpha-20261016-i18n/Facet-Setup-0.1.1-alpha-20261016-x64.exe) · [目录中的文件 / Repository copy](Facet-Setup-0.1.1-alpha-20261016-x64.exe) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/facet-v0.1.1-alpha-20261016-i18n)

安装包大小为 **10,007,222 字节 / bytes（10.01 MB）**，包含一份程序核心与简体中文、English 资源。运行安装包后选择语言并完成安装。

The installer contains one application core with Simplified Chinese and English resources. Run the installer, select a language, and complete the installation.

应用顶栏的“界面语言 / Display language”在下次启动时生效，已有的应用语言偏好优先于安装器选择。旧的独立 Facet English 安装及其用户数据不会自动迁移。

Changes to **Display language** in the application take effect on the next launch. An existing application language preference takes precedence over the installer selection. A previous standalone Facet English installation and its user data are not migrated automatically.

<a id="contents"></a>
## 本版内容 / Release contents

- 中英文界面共用同一程序核心。Chinese and English interfaces share the same application core.
- 包含序列标量图、STM 结构叠加、多面体及保存的 2D 视图恢复功能。Includes sequence scalar plots, STM structure overlays, polyhedra, and saved 2D view restoration.
- 已对照开发版本 **06e80d6** 核对标量图改进、LOCPOT 支持移除和恢复失败状态提示。Includes the scalar-plot refinements, removal of LOCPOT support, and recovery-failure status checked against development revision **06e80d6**.
- 构建日期：**2026-10-16**；本仓库首次发布日期：**2026-10-17**。本次没有重新构建，保留原始文件名与校验值。Build date: **2026-10-16**. First publication in this repository: **2026-10-17**. The original filename and checksum are preserved; this publication does not rebuild the application.

<a id="verification"></a>
## 校验与验证范围 / Checksums and validation

[SHA256SUMS.txt](SHA256SUMS.txt)

~~~text
bcfbc9af4d427b29d7b85f5a604d0c164b3e77f428a8f582ed7a31645bbc9e4b  Facet-Setup-0.1.1-alpha-20261016-x64.exe
~~~

~~~powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.1-alpha-20261016-x64.exe
~~~

本次发布已核对包的 SHA-256 和原始构建记录。此前已完成静态检查、构建、Project 绑定检查、相关接口测试、双语言浏览器工作流及 MSI 内容检查。真实 Windows 安装、升级、卸载和文件关联仍待隔离环境验证。

This publication verifies the package's SHA-256 against the original build record. Previous validation covered static checks, builds, Project bindings, targeted interface tests, bilingual browser workflows, and MSI contents. Installation, upgrade, uninstall, and file associations still require testing in an isolated Windows environment.

[返回主页 / Home](../../../README.md) · [更新记录 / Changelog](../../../CHANGELOG.md)
