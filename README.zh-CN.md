[English](README.md) | **简体中文**

# Facet & ftkit

<a id="downloads"></a>
## 最新下载

| 软件 | 最新版本 | 平台 | 下载 |
| --- | --- | --- | --- |
| **Facet** | **0.1.0-beta.1 · Beta 1** | Windows x64 · 中英双语 | **[下载安装包 · 12.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/facet-v0.1.0-beta.1/Facet-Setup-0.1.0-beta.1-x64.exe)** |
| **ftkit** | **0.1.3-preview-20261022-phononfix** | Linux x86_64 | **[下载压缩包 · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)** |

**使用手册：** [Facet 中文手册](downloads/facet/0.1.0-beta.1/docs/zh-CN/user-guide.txt) · [ftkit 中文手册](downloads/ftkit/0.1.3-preview-20261022-phononfix/用户手册.txt)  
**安装说明：** [Facet](downloads/facet/0.1.0-beta.1/README.zh-CN.md) · [ftkit](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.zh-CN.md)

[历史版本](downloads/README.zh-CN.md) · [更新记录](CHANGELOG.zh-CN.md) · [版本与校验清单](versions.json)

Facet 用于晶体、原子结构和计算结果可视化；ftkit 将支持的 VASP、Quantum ESPRESSO 结果转换为 Facet 文件。这里提供发行包与使用文档。开发团队：**[Ji Group](https://g.ruc.edu.cn/) · 中国人民大学**。

## 目录

1. [最新下载](#downloads)
2. [开始使用](#quick-start)
3. [本版变化](#changes)
4. [校验与版本管理](#versions)
5. [反馈](#feedback)

<a id="quick-start"></a>
## 开始使用

- **Facet：** 下载 EXE，保存工作并关闭正在运行的 Facet，运行安装器后选择语言和安装范围。软件使用一套程序核心及两种语言资源。应用内语言切换在重启后生效。完整步骤及本轮验收边界见 [Facet 安装说明](downloads/facet/0.1.0-beta.1/README.zh-CN.md)。
- **ftkit：** 下载 tar.gz，按 [安装说明](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.zh-CN.md)校验、解压并运行 `bash verify.sh`；保留解压目录。进入计算目录运行 `ftkit`。不需要 Python 或 Facet。

<a id="changes"></a>
## 本版变化

Facet Beta 1 补齐共价半径至 96 项、修正 Lr 组态、标明估算/汇编/理论预测/兜底来源，加入关于与检查更新、第三方许可清单，并更新两种语言的手册。旧共价自动键缓存会重算；坐标、配色、手动键和保存的半径比例保持原有契约。

本版完成静态检查、构建、包内容及样例界面/保存重开核对；按要求未跑自动化测试。最终包的英文安装首启、覆盖安装、卸载和原生导出尚未重新验收。旧配色的部分历史取得记录仍待补齐。详情见 [版本说明](downloads/facet/0.1.0-beta.1/README.zh-CN.md#verification)。

ftkit 最新包仍为 2026-10-22 声子修正版，本次原样保留；没有重新构建。

<a id="versions"></a>
## 校验与版本管理

[Facet SHA-256](downloads/facet/0.1.0-beta.1/SHA256SUMS.txt) · [ftkit SHA-256](downloads/ftkit/0.1.3-preview-20261022-phononfix/SHA256SUMS.txt)

```powershell
Get-FileHash -Algorithm SHA256 .\Facet-Setup-0.1.0-beta.1-x64.exe
```

每次发行使用独立版本目录和标签，旧包、手册及校验值保留。[versions.json](versions.json) 明确指定各产品的最新版本，不能只按文件名数值排序。Beta 版本号为本次选定的 `0.1.0-beta.1`。

公开材料不包含 Facet 或 ftkit 自有源码。随附的 [WiX/option-ext 对应源码](downloads/facet/0.1.0-beta.1/third-party-sources/README.zh-CN.md)是第三方许可材料，不需要安装，也不计入主安装包体积。GitHub 自动生成的 Source code 归档仅是本发行仓库快照；安装请使用上方明确标出的 EXE 或 tar.gz。

<a id="feedback"></a>
## 反馈

请在 [Issues](https://github.com/zhongqinzhang/Facet-and-Ftkit/issues) 中注明产品名、完整版本、操作系统和复现步骤。
