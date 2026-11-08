[English](README.md) | **简体中文**

# ftkit 0.1.3-preview-20261016-r2

**[下载压缩包 · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261016-r2/ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz)**

构建：2026-10-16 · 首次发布：2026-10-17 · 历史归档

[中文使用手册](用户手册.txt) · [SHA-256](SHA256SUMS.txt) · [备用下载](ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz?raw=true)

## 目录

1. [安装与首次使用](#installation)
2. [本版内容](#changes)
3. [文档与核对范围](#verification)

<a id="installation"></a>
## 安装与首次使用

ftkit 是 Linux x86_64 静态链接命令行程序，无需 Python、Facet 或动态 libc。安装和验证脚本需要 Bash 4+ 与常见命令行工具。将压缩包和 SHA256SUMS.txt 下载到同一目录：

```bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261016-r2-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
```

verify.sh 核验后配置 Bash PATH。保留解压目录；移动后重新运行安装脚本。仅校验用 `bash verify.sh --no-install`；仅配置 PATH 用 `bash install.sh`。进入计算目录运行 `ftkit`，按编号菜单选择任务。

<a id="contents"></a>
<a id="changes"></a>
## 本版内容

- 包含 ftkit 更名和此前声子容量修正。
- 压缩包包含安装/验证脚本、示例、手册、构建信息及第三方许可，不含应用源码。
- 任务 101 / 103 使用 Relative energy (eV)，每份输出以最低能量为零点，缺失能量保持缺失。
- 应用版本为 0.1.3，发行编号以本页完整版本为准。

<a id="verification"></a>
## 文档与核对范围

原发行核对归档内容、整包 SHA-256 和程序哈希，包内 BUILDINFO.json 记录原测试范围。任务 101 的 stride、任务 101/103 的统一中断仍有已知限制，见手册。 本次没有重新构建或运行自动化测试；Linux 实机运行及旧内核兼容性未重新验证。完整手册目前只有中文。

<a id="user-guide"></a>
[中文完整手册](用户手册.txt)

此处手册更新于 2026-10-20；压缩包 docs/zh-CN/ 保留原始随包文档。

```text
d66f3539c585b5030eca7ff68f3e16e15db4d20ccb734253d7ae41597bc9dadd  ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
```

[最新下载](../../../README.zh-CN.md#downloads) · [版本记录](../../../CHANGELOG.zh-CN.md)
