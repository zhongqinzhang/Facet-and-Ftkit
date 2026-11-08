[English](REVIEW.md) | **简体中文**

# 许可来源核对

Facet Windows x64 · 核对日期 2026-11-08

## 目录

1. [已核实来源](#sources)
2. [解释边界](#interpretation)
3. [未决项与核对范围](#limits)

<a id="sources"></a>
## 已核实来源

- 前端按生产依赖闭包清点，排除可选开发 peer。is-mobile 采用版本 README 原文；Ant Design SVG 与 Tauri dialog 缺失原文按 npm gitHead 补齐。
- Rust 锁定、离线 Windows 普通依赖共 207 项，排除自有 workspace、构建专用和过程宏。ts-rs、moyo、alloc-stdlib、UNIC、webview2 缺失原文按记录的上游提交补齐，保留 UNIC 版权头。
- Noto Sans Regular/Bold 对应 Google Fonts `3043c22d2f091ead19f47fbcabdd696b8c9b7edd`，blob 分别为 `9dd10199bc8e8fcfcc5c3a1a394557ed00c567c5`、`6e00cdce1dac34e409a0111296c90e98c6f40701`。保留 2012 Google OFL，披露字体内部旧 Apache 元数据。
- WebView2 SDK 1.0.3650.58 与 x64 static loader 匹配记录的官方原包；SDK LICENSE/NOTICE 不用 Rust wrapper 的 MIT 替代，指纹见 sources.json。
- Rust 1.97.1，提交 `8bab26f4f68e0e26f0bb7960be334d5b520ea452`：保留完整标准库声明和 compiler-builtins 的 MIT AND Apache-2.0 WITH LLVM-exception。
- WiX 3.14.1 固定 `b40e9a32c24033e11b77baf2c91a704382f898ed`。内嵌 UI DLL 哈希为 `7f47d98ab25cfea9b3a2e898c3376cc9ba1cd893b4948b0c27caa530fd0e34cc`，六幅图像匹配源码归档。源码 13,859,146 字节，SHA-256 `3cc4bdaca8070042a182675b047882211d042f35139efcb0eeac35eeb81bf9d3`。本轮未重新编译 WiX 源码。
- NSIS 3.11 实际使用 zlib、System、LangDLL、nsDialogs，保留 COPYING，不将未用的 bzip2/LZMA 压缩模块写为已分发。
- 保留 Matplotlib、Pretty Lattice、ColorBrewer、Jmol 原数据声明；加入 NIST 非 SRD 条款、Smits CC BY 4.0 署名/改编及 BODR 汇编说明。见[科学数据来源](DATA_SOURCES.zh-CN.md)。

<a id="interpretation"></a>
## 解释边界

AND 表达式保留全部适用原文；旧斜杠表达式按实际许可判断，brotli-decompressor 按 BSD 原文记录。option-ext 保守列入，尽管 dirs-sys 调用在 Unix 分支，已核对 Windows rlib 的代码/数据段为空；保留 MPL 声明和原源码，不为 Facet 自有代码指定许可。

Rust 全文含其他平台条目，不是 Windows 链接图；工具生成内容与真实嵌入 WiX 代码分别对待。许可和第三方对应源码与 Facet 自有实现分开。

<a id="limits"></a>
## 未决项与核对范围

newVESTA 归属已确认。Beta 1 为 320 项、215 份去重原文，旧 alpha 记录作为历史保留。共价半径、Lr 和来源分类按当前数据记录修正；VESTA/Studio/CPK 最初取得记录仍不完整，技术清单不能自动完成所有历史权利判断。

候选已完成静态检查、构建、包内容/哈希及样例界面/保存重开核对。未跑自动化测试；最终包安装、原生对话框和实际导出仍待验收。公开文档随后按语言整理，不改安装器和许可原文。原始论文和本地浏览器数据不分发。

[版本核对范围](../README.zh-CN.md#verification) · [许可目录](README.zh-CN.md)
