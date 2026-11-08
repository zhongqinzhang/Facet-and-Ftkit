[English](README.md) | **简体中文**

# Facet 0.1.0-beta.1 · Beta 1

**[下载 Windows x64 安装包 · 12.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.0-beta.1/Facet-Setup-0.1.0-beta.1-x64.exe)**  
[中文使用手册](docs/zh-CN/user-guide.txt) · [中文更新说明](docs/zh-CN/release-notes.txt)

构建和发布：2026-11-08 · 12,828,535 字节 · [备用下载](Facet-Setup-0.1.0-beta.1-x64.exe?raw=true) · [SHA-256](SHA256SUMS.txt)

## 目录

1. [安装与语言](#installation)
2. [本版变化](#changes)
3. [旧项目兼容](#compatibility)
4. [核对范围](#verification)
5. [许可与来源](#licenses)

<a id="installation"></a>
## 安装与语言

1. 核对安装包 SHA-256，保存工作并关闭 Facet。
2. 运行 EXE，选择简体中文或 English。
3. 选择“仅为我安装”或“为所有用户安装”，再选择目录并完成安装；为所有用户安装需要管理员权限。
4. 软件内选择“帮助 → 关于 Facet”查看完整版本和检查更新。界面语言可在顶栏切换，下次启动生效。

一个核心内置两种语言资源。安装语言用于下次启动的初始化，此后保存手动偏好；此最终包尚未重做真实安装首启验收。卸载默认保留设置和恢复数据，主动选择才清理这些数据；已保存的项目文件保留。安装器未使用付费发布者身份签名。

<a id="changes"></a>
## 本版变化

- 版本统一为 `0.1.0-beta.1`；修正新建项目/导出结构包版本入口原先为 `0.0.0` 的遗漏。
- Cordero 共价半径补齐为 H–Cm 共 96 项，前端与 Rust 共用一份数据。12 个新增文献条目中 10 个数值改变。
- Lr 组态修正为 `[Rn] 5f14 7s2 7p1`；状态栏补充估算、汇编、理论预测、兜底标记和来源。
- 保留范德华半径原数值，纠正来源分类与旧配色说明；补齐 320 项第三方声明、215 份去重许可原文。
- 保留精简字体，提供紧凑 About、主动检查更新、完整版本；中英文手册对应 21 章、86 个编号小节。

<a id="compatibility"></a>
## 旧项目兼容

旧项目保留坐标、晶格、手动键、删除自动键的覆盖记录、配色、半径比例、原始应用版本及文件格式。更新的参考半径可能改变受影响元素的球体大小和共价自动键；相关 2D/3D 图像或导出也可能变化。旧共价缓存重算，绝对距离缓存不因本次数据修订失效。

Windows Installer 内部版本为 `0.1.0`，应用显示完整 Beta 标识。安装配置允许降级，仍应对旧 alpha 覆盖安装做验收。更新索引按明确的最新版本指针工作，不按版本号大小猜测发布日期。

<a id="verification"></a>
## 核对范围

已完成 `pnpm check`、生产构建、语言 transform、13 个安装资源匹配、哈希核对，以及实际 Chrome/WebView2 界面观察。样例已完成 2D/3D 显示、保存重开和旧缓存/手动键/配色/比例核对。未跑自动化测试；最终包的安装首启、升级/降级、卸载、原生文件选择框及实际导出尚未重新验收。新建项目版本入口完成静态与构建核对，未完成实际另存为验证。

安装包先由 `3205a156` 加已审查修改构建，这些源码随后记录在私有提交 `4d868d0a`；提交身份不替代包哈希。见 [发行清单](release-manifest.json)。

<a id="licenses"></a>
## 许可与来源

[第三方许可证](licenses/README.zh-CN.md) · [科学数据来源](licenses/DATA_SOURCES.zh-CN.md) · [对应第三方源码](third-party-sources/README.zh-CN.md)

旧 VESTA/Studio/CPK 配色的最初取得记录仍不完整，颜色按兼容约定保留。newVESTA 自有代码归属已确认。许可导读与原文随发行材料提供，原始论文不在分发内容中。

[返回最新下载](../../../README.zh-CN.md#downloads)
