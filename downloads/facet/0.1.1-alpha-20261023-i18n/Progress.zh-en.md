# 本版进展中英文对应 / Bilingual release progress

## 目录 / Contents

1. [变化对应 / Changes](#changes)
2. [版本来源 / Provenance](#provenance)
3. [验证范围 / Validation scope](#validation)

<a id="changes"></a>
## 变化对应 / Changes

| 中文 | English |
| --- | --- |
| 安装时选择 English，安装后首次启动即使用英文，包括此前保存了中文或跟随系统的情况。 | Selecting English during setup makes the next launch use English, including when an earlier preference was Chinese or System default. |
| 每次安装的语言选择只应用一次；此后手动修改仍会保存，下次启动生效。 | Each installation choice is applied once. Later manual changes are saved and take effect on the next launch. |
| 再次完成安装或修复时，采用新的语言选择。 | Completing another installation or repair applies the new language choice. |
| 保留同一程序核心和 3769 条中英对应资源。 | One application core contains 3,769 paired Chinese and English messages. |
| 晶胞边框按照局部前后关系与结构混合显示，涵盖 2D、3D 及图片导出。 | Unit-cell edges respect local depth relative to the structure in 2D, 3D and image exports. |
| 编辑矢量后保留有效的键计算状态，修正弹出控件的可见性。 | Vector edits preserve valid bond-computation state; popup controls remain visible. |
| 包含此前的主题默认值、侧栏控件和 STM 性能与可靠性更新。 | Includes the preceding theme-default, sidebar-control and STM performance and reliability updates. |
| ftkit 301 支持 VASP 质量修正段的复合标题，并检查到文件末尾的晶胞和有效 POMASS 一致性。 | ftkit task 301 accepts compound headings in VASP mass-corrected sections and checks lattice and effective POMASS consistency through the end of the file. |
| ftkit 保留已有相对能量输出及命令接口，本次原样发布 10 月 22 日归档。 | ftkit retains its relative-energy output and command interface. The October 22 archive is published unchanged. |

<a id="provenance"></a>
## 版本来源 / Provenance

Facet：**0.1.1-alpha-20261023-i18n**，基于 **be3f27d9bbc6875d1b5b8e5965496f7f2dec979c**，叠加已确认的安装语言修复。构建日期：2026-10-23。

Facet: **0.1.1-alpha-20261023-i18n**, built on **2026-10-23** from the revision above plus the approved installation-language fix.

ftkit：**0.1.3-preview-20261022-phononfix**，构建日期：2026-10-22；本次发布日期：2026-10-23。两个软件各自编号，Facet 的源码提交号不代表 ftkit 的构建来源。

ftkit: **0.1.3-preview-20261022-phononfix**, built on **2026-10-22** and published here on **2026-10-23**. The products are versioned independently; Facet's source revision does not identify the ftkit build.

<a id="validation"></a>
## 验证范围 / Validation scope

静态检查、59 项前端定向测试及 13 项晶胞深度浏览器测试已完成。按本轮要求停止其余测试，继续完成构建、载荷身份、随包手册与 SHA-256 核对。没有执行真实 Windows 安装、升级、卸载或 Linux 运行验收。

Static checks, 59 targeted frontend tests and 13 cell-depth browser tests completed. Remaining tests were stopped as requested; packaging continued with payload, bundled-manual and SHA-256 checks. End-to-end Windows installation, upgrade, uninstall and Linux execution were not performed.
