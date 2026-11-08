[English](README.md) | **简体中文**

# 第三方许可证

Facet 0.1.0-beta.1 · **320 项声明 · 215 份去重许可原文**

## 目录

1. [阅读许可](#reading)
2. [覆盖范围](#coverage)
3. [文件说明](#files)
4. [分发与剩余来源问题](#distribution)

<a id="reading"></a>
## 阅读许可

选择“帮助 → 关于 Facet → 第三方许可证”，展开类别和组件。安装目录的 `licenses/THIRD_PARTY_NOTICES.txt` 提供同一份完整内容，支持离线阅读。

这些是依赖、字体和数据的原始版权与许可条件，不是发布者签名证书，也不是给 Facet 自有代码声明开源许可。Beta 包同样遵守适用第三方条件。

<a id="coverage"></a>
## 覆盖范围

Windows x64 清单包含前端 99 项、原生 207 项、字体/资源 9 项、系统运行组件 3 项、安装器 2 项。清单保守包含可能被链接器剔除的依赖，不能将条目数当作实际执行库数量。构建专用依赖和过程宏不计入；Rust 完整标准库声明含其他平台内容，不等于 Windows 链接清单。系统 DLL 和独立安装的 WebView2 Runtime 不冒称随包嵌入。ftkit 使用独立清单。

<a id="files"></a>
## 文件说明

| 文件 | 用途 |
| --- | --- |
| [THIRD_PARTY_NOTICES.txt](THIRD_PARTY_NOTICES.txt) | 离线组件目录和完整许可原文。 |
| [third-party-notices.json](third-party-notices.json) | About 与打包共用的结构化清单。 |
| [supplemental/](supplemental/) | 上游许可原文、署名及改编说明。 |
| [REVIEW.zh-CN.md](REVIEW.zh-CN.md) | 核查证据与未决取得记录。 |
| [DATA_SOURCES.zh-CN.md](DATA_SOURCES.zh-CN.md) | 科学数据参考与兼容影响。 |
| [beta1-data-review.json](beta1-data-review.json) | 当前逐项数据结论。 |
| [historical-data-audit.json](historical-data-audit.json) | 修正前审计，旧待办不代表当前状态。 |
| [sources.json](sources.json) | 已核对来源、资源指纹与许可选择。 |

许可原文保留原始语言。顶部切换作用于解释性页面，不翻改法律原文。

<a id="distribution"></a>
## 分发与剩余来源问题

本版随附 [第三方对应源码](../third-party-sources/README.zh-CN.md)：固定版本 WiX 源码及保守保留的 option-ext 原包。它们不含 Facet 自有源码，与安装器分开提供。再次分发时保留声明、署名和适用的源码材料。

newVESTA 归属已由作者确认。旧 VESTA/Studio/CPK 配色的最初取得记录仍不完整，颜色为兼容保留；数值相符不能证明复制路径或自动解决所有权利问题，详见来源核查页。

[返回版本说明](../README.zh-CN.md)
