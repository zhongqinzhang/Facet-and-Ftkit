[English](README.md) | **简体中文**

# 第三方对应源码

## 目录

1. [归档内容](#archives)
2. [核对与分发](#verification)

<a id="archives"></a>
## 归档内容

这些归档用于提供第三方许可材料，不含 Facet 自有源码，也不需要安装。

| 归档 | 对应组件 |
| --- | --- |
| [WiX 3.14.1 源码](wix3-b40e9a32c24033e11b77baf2c91a704382f898ed.zip) | 固定 b40e9a32 完整未修改源码，含 MSI 内嵌 UI 动作、辅助库、图像、构建文件。LICENSE.TXT 为 MS-RL。 |
| [option-ext 0.2.0](option-ext-0.2.0.crate) | 保守依赖清单保留的 MPL-2.0 原始 crate；Windows 消费路径未使用该代码。.crate 是 tar.gz 归档。 |

<a id="verification"></a>
## 核对与分发

[SOURCE-MANIFEST.json](SOURCE-MANIFEST.json) 记录原始 URL、准确大小和哈希；[SHA256SUMS.txt](SHA256SUMS.txt) 列出归档校验值。文件来自固定上游版本，未执行其中代码。最终 MSI 的图像和既有官方 UI DLL 已核对，本轮未重新编译 WiX。

再次分发时将此目录与安装包、声明一同放在可访问位置。它们与 12.83 MB 主安装包分开，不是额外需要运行的安装程序。

[版本说明](../README.zh-CN.md) · [许可目录](../licenses/README.zh-CN.md)
