[English](CHANGELOG.md) | **简体中文**

# 更新记录

**最新发布：2026-11-08** · [下载](README.zh-CN.md#downloads)

## 目录

1. [2026-11-08 · Facet Beta 1](#release-2026-11-08)
2. [2026-11-06 · 文档勘误](#docs-2026-11-06)
3. [2026-10-23 · Alpha 与声子修正](#release-2026-10-23)
4. [2026-10-17 · 首次发布](#release-2026-10-17)
5. [版本规则](#future-releases)

<a id="release-2026-11-08"></a>
## 2026-11-08 · Facet 0.1.0-beta.1

- 发布首个 Beta 安装包，12.83 MB，包含已核对的 96 项共价半径、Lr 组态修正、来源标记、About/更新检查、精简字体、许可清单和对应手册。
- 首页、下载索引、各版本说明与当前许可导读拆为独立中英文页面；默认英文，顶部可切换完整中文页面。
- ftkit 0.1.3-preview-20261022-phononfix、旧安装包、随包手册与校验值保持不变。
- 完成静态检查、构建、包内容及样例保存重开核对；未跑自动化测试，最终包安装和原生导出仍待验收。
- [Beta 版本说明](downloads/facet/0.1.0-beta.1/README.zh-CN.md)。

<a id="docs-2026-11-06"></a>
## 2026-11-06 · 文档勘误

10 月 23 日随包更新说明中的 `aa74b4d5` 应为 `be3f27d9` 加安装语言修复。见[勘误](downloads/facet/0.1.1-alpha-20261023-i18n/README.zh-CN.md#documentation-erratum)；不改变归档包、手册、清单和校验值。

<a id="release-2026-10-23"></a>
## 2026-10-23 · Alpha 与声子修正

- **Facet 0.1.1-alpha-20261023-i18n：**基于 `be3f27d9` 加安装语言修复重建；纳入晶胞边框局部深度、矢量/键、弹出控件、主题与侧栏修正。安装选择在下次启动应用一次，随后保留手动偏好。原构建/文件检查及部分测试完成，其余测试按要求停止。[说明](downloads/facet/0.1.1-alpha-20261023-i18n/README.zh-CN.md)。
- **ftkit 0.1.3-preview-20261022-phononfix：**原样发布 10 月 22 日归档，修正 VASP 质量修正段复合标题识别，晶胞/POMASS 检查延续到文件末尾。[说明](downloads/ftkit/0.1.3-preview-20261022-phononfix/README.zh-CN.md)。
- 最新下载与手册置顶，保留 10 月 16 日归档和标签。

<a id="release-2026-10-17"></a>
## 2026-10-17 · 首次发布

- **Facet 0.1.1-alpha-20261016-i18n：**一套核心与两种语言资源，包含序列标量图、STM 叠加、多面体及 2D 视图恢复；纳入 `06e80d6` 的标量图、LOCPOT 移除和恢复失败提示。10 月 16 日构建，17 日原样归档。[说明](downloads/facet/0.1.1-alpha-20261016-i18n/README.zh-CN.md)。
- **ftkit 0.1.3-preview-20261016-r2：**Linux 静态链接预览，任务 101/103 使用相对能量，包含 ftkit 更名和此前声子容量修正。10 月 16 日构建，保留原包。[说明](downloads/ftkit/0.1.3-preview-20261016-r2/README.zh-CN.md)。
- 建立独立发行仓库，提供产品/版本目录、校验值和标签，不导入应用源码或开发历史。

<a id="future-releases"></a>
## 版本规则

新版使用新目录和标签，更新首页和 versions.json，保留旧包、手册和校验值。二进制重新打包使用新版本或修订号；文档勘误单独标注。
