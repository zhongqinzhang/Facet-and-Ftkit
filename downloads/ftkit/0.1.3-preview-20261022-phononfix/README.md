# ftkit 0.1.3-preview-20261022-phononfix

**[下载 Linux x86_64 发行包 / Download Linux x86_64 archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)**

构建 / Built: 2026-10-22 · 发布 / Published: 2026-10-23 · Preview

[备用下载 / Repository download](ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz?raw=true) · [SHA-256](SHA256SUMS.txt) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/ftkit-v0.1.3-preview-20261022-phononfix)

## 目录 / Contents

1. [安装与首次使用 / Installation and first use](#installation)
2. [更新内容 / What's new](#changes)
3. [文档与验证 / Documentation and validation](#verification)

<a id="installation"></a>
## 安装与首次使用 / Installation and first use

ftkit 是独立的 **Linux x86_64 命令行工具**，不需要安装 Python 或 Facet。静态链接程序不依赖动态 libc；安装与验证脚本需要 Bash 4+ 和常用命令行工具。

ftkit is a standalone **Linux x86_64 command-line tool**. Python and Facet are not required. Its statically linked executable does not require a dynamic libc; the setup and verification scripts require Bash 4+ and standard command-line utilities.

下载压缩包与本页 SHA256SUMS.txt，在同一目录执行 / Download the archive and SHA256SUMS.txt into the same directory, then run:

~~~bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
~~~

verify.sh 校验成功后会配置 Bash PATH。保留解压目录；移动后重新运行安装脚本。仅校验、不配置 PATH 时使用 `bash verify.sh --no-install`。

After successful verification, verify.sh configures your Bash PATH. Keep the extracted directory in place; rerun setup after moving it. Use `bash verify.sh --no-install` to verify without changing PATH.

进入计算结果目录后运行 `ftkit`，按菜单选择任务。首次使用可按[中文手册](用户手册.txt)中的示例操作。

Run `ftkit` in your calculation-output directory and choose a task from the menu. The [Chinese user guide](用户手册.txt) includes a first-conversion example.

<a id="changes"></a>
## 更新内容 / What's new

- 修复任务 301 将 VASP 质量修正段的双行复合标题误判为重复段的问题，并支持只含质量修正段的对应格式。Task 301 accepts compound headings in VASP mass-corrected sections, including files containing only the corrected section.
- 晶胞和有效 POMASS 一致性检查延续到文件末尾；矛盾输入会报错并保留已有输出。Lattice and effective POMASS checks continue through the end of the file; inconsistent input is rejected without replacing existing output.
- 保留模式顺序、质量修正规则、命令参数及文件格式；任务 101 / 103 继续使用 **Relative energy (eV)**。Mode ordering, mass-correction rules, command options and file formats are retained. Tasks 101 and 103 continue to use **Relative energy (eV)**.

<a id="verification"></a>
## 文档与验证 / Documentation and validation

[中文用户手册](用户手册.txt) · [中文更新说明](更新说明.txt) · [BUILDINFO.json](BUILDINFO.json)

本次原样发布 2026-10-22 的归档，没有重新构建。已核对完整包、可执行文件和包内 177 项校验值。BUILDINFO.json 记录原构建的 49 项测试、真实 VASP 6.5.1 OUTCAR 回读和 ELF 审计。**本次未执行 Linux 实机验证；旧内核兼容性未确认。**

The October 22 archive is published unchanged. Its archive hash, executable hash and 177 internal checksums were verified. BUILDINFO.json records 49 tests, a real VASP 6.5.1 OUTCAR roundtrip and an ELF audit from the original build. **Linux execution was not performed for this publication; compatibility with older kernels is unverified.**

~~~text
c338878c3531b64daff35f0ca27ce89ee75ba4a55979a26ae571224b91b5f666  ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
~~~

应用版本为 **0.1.3**；发行编号为 **0.1.3-preview-20261022-phononfix**。Application version: **0.1.3**; distribution revision: **0.1.3-preview-20261022-phononfix**.

[返回最新下载 / Latest downloads](../../../README.md) · [所有版本 / All versions](../../../CHANGELOG.md)
