[English](README.md) | **简体中文**

# ftkit 0.1.3-preview-20261022-phononfix

**[下载压缩包 · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)**

构建：2026-10-22 · 首次发布：2026-10-23 · 最新 ftkit 预览包

[中文使用手册](用户手册.txt) · [SHA-256](SHA256SUMS.txt) · [备用下载](ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz?raw=true)

## 目录

1. [安装与首次使用](#installation)
2. [本版内容](#changes)
3. [文档与核对范围](#verification)

<a id="installation"></a>
## 安装与首次使用

ftkit 是 Linux x86_64 静态链接命令行程序，无需 Python、Facet 或动态 libc。安装和验证脚本需要 Bash 4+ 与常见命令行工具。将压缩包和 SHA256SUMS.txt 下载到同一目录：

```bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
```

verify.sh 核验后配置 Bash PATH。保留解压目录；移动后重新运行安装脚本。仅校验用 `bash verify.sh --no-install`；仅配置 PATH 用 `bash install.sh`。进入计算目录运行 `ftkit`，按编号菜单选择任务。

<a id="contents"></a>
<a id="changes"></a>
## 本版内容

- 修复任务 301 对 VASP 质量修正段复合标题的识别，支持只含对应质量修正段的格式。
- 晶胞/POMASS 一致性检查延续到文件末尾；矛盾输入报错并保留已有输出。
- 模式顺序、质量修正规则、命令参数和格式不变。
- 任务 101 / 103 使用 Relative energy (eV)，每份输出以最低能量为零点，缺失能量保持缺失。
- 应用版本为 0.1.3，发行编号以本页完整版本为准。

<a id="verification"></a>
## 文档与核对范围

原发行核对完整包、程序哈希和包内 177 项校验值。BUILDINFO.json 记录原构建的 49 项测试、VASP 6.5.1 OUTCAR 回读与 ELF 审计。 本次没有重新构建或运行自动化测试；Linux 实机运行及旧内核兼容性未重新验证。完整手册目前只有中文。

<a id="user-guide"></a>
[中文完整手册](用户手册.txt) · [BUILDINFO.json](BUILDINFO.json) · [中文更新说明](更新说明.txt)

```text
c338878c3531b64daff35f0ca27ce89ee75ba4a55979a26ae571224b91b5f666  ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
```

[最新下载](../../../README.zh-CN.md#downloads) · [版本记录](../../../CHANGELOG.zh-CN.md)
