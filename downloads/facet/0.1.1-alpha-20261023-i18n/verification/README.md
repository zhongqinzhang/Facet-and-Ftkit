# 构建与验证记录 / Build and validation record

## 目录 / Contents

1. [完成项 / Completed](#completed)
2. [未完成项 / Incomplete](#incomplete)

<a id="completed"></a>
## 完成项 / Completed

- 架构、TypeScript 与 3769 条双语资源检查；59 项前端定向测试；13 项晶胞深度浏览器测试。Architecture, TypeScript and catalog checks; 59 targeted frontend tests; 13 cell-depth browser tests.
- 前端、原生 release、MSI 与双语言 EXE 构建。Frontend, native release, MSI and bilingual EXE builds.
- 单一程序核心、内嵌英语安装界面、语言属性、升级标识及 4 份随包手册一致性核对。Single-core payload, embedded English installer UI, language properties, upgrade identity and four bundled manuals checked.
- 2132 份构建输入、16 项前端资源身份及发行文件 SHA-256 核对。2,132 build inputs, 16 frontend assets and distribution SHA-256 checks.
- ftkit 原始归档及包内 177 项校验值核对。Original ftkit archive and 177 internal checksums verified.

<a id="incomplete"></a>
## 未完成项 / Incomplete

按用户要求，停止原生语言测试编译、矢量/键浏览器测试和双语工作流浏览器测试；未继续运行安装器派发、MSI 转换测试集或安装语言浏览器测试。已通过的旧包测试不能代替本版完整验收。

At the user's request, native language test compilation, vector/bond browser tests and bilingual workflow browser tests were stopped. Installer dispatch, MSI-transform test suites and installer-language browser tests were not run. Earlier package results do not constitute complete validation of this release.

未进行真实 Windows 安装、升级、卸载或重启；本次也未在 Linux 上运行 ftkit。

Actual Windows installation, upgrade, uninstall and reboot, and ftkit execution on Linux, were not performed.

[详细记录 / Machine-readable record](check-results.json)
