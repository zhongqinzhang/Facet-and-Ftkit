# ftkit 0.1.3-preview-20261016-r2

Linux x86_64 · Preview

## 目录 / Contents

1. [下载与安装 / Download and installation](#installation)
2. [本版内容 / Release contents](#contents)
3. [校验与验证范围 / Checksums and validation](#verification)

<a id="installation"></a>
## 下载与安装 / Download and installation

[下载发行包 / Download archive](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261016-r2/ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz) · [目录中的文件 / Repository copy](ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz) · [Release](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/tag/ftkit-v0.1.3-preview-20261016-r2)

发行包大小为 **3,830,658 字节 / bytes（3.83 MB）**。程序为 Linux x86_64 静态链接可执行文件，无需安装 Python 或 Facet。验证和安装脚本需要 Bash 4+ 及常见命令行工具；包内 BUILDINFO.json 记录详细要求。

The archive contains a statically linked Linux x86_64 executable. Python and Facet are not required. The verification and installation scripts require Bash 4+ and standard command-line utilities; see the included BUILDINFO.json for details.

下载并校验后执行 / After downloading and verifying:

~~~bash
tar -xzf ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261016-r2-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
~~~

verify.sh 验证成功后会将解压目录配置到 Bash PATH。请保留该目录；移动后重新运行安装脚本。只验证时使用 bash verify.sh --no-install；只配置 PATH 时使用 bash install.sh。

After successful verification, verify.sh adds the extracted directory to Bash PATH. Keep that directory in place and rerun the installer if you move it. Use bash verify.sh --no-install for verification only, or bash install.sh to configure PATH.

进入计算目录后运行 ftkit，按编号菜单选择任务。完整中文手册及更新说明位于包内 docs/zh-CN/。

Run ftkit in your calculation directory and choose a task from the numbered menu. The complete Chinese user guide and change log are included under docs/zh-CN/.

<a id="contents"></a>
## 本版内容 / Release contents

- 应用版本为 **0.1.3**，本发行包编号为 **0.1.3-preview-20261016-r2**。Application version: **0.1.3**; distribution revision: **0.1.3-preview-20261016-r2**.
- 任务 101 / 103 的能量名称为 **Relative energy (eV)**；每份输出以最低能量为零点，缺失能量保持缺失。Tasks 101 and 103 label energies as **Relative energy (eV)**, relative to the minimum in each output; missing energies remain missing.
- 包含 ftkit 更名和此前的声子容量修正。Includes the ftkit rename and previous phonon-capacity fixes.
- 包内保留安装与验证脚本、示例、使用手册、构建记录及第三方许可，没有应用源码。Includes installation and verification scripts, examples, documentation, build records, and third-party licenses; application source code is not included.
- 构建日期：**2026-10-16**；本仓库首次发布日期：**2026-10-17**。本次原样发布，没有重新构建。Build date: **2026-10-16**. First publication in this repository: **2026-10-17**. The original archive is published unchanged.

<a id="verification"></a>
## 校验与验证范围 / Checksums and validation

[SHA256SUMS.txt](SHA256SUMS.txt)

~~~text
d66f3539c585b5030eca7ff68f3e16e15db4d20ccb734253d7ae41597bc9dadd  ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
~~~

在下载目录执行 / In the download directory:

~~~bash
sha256sum -c SHA256SUMS.txt
~~~

本次已核对归档目录、完整包 SHA-256 和包内程序哈希。BUILDINFO.json 记录原有测试范围；Linux 实机运行与旧版内核兼容性仍未验证。任务 101 的 stride 和任务 101 / 103 的统一中断流程仍待完善，详见包内手册。

This publication verifies archive contents, the archive SHA-256, and the executable hash. BUILDINFO.json records prior tests. Linux execution and compatibility with older kernels remain unverified. Task 101 stride handling and unified interruption handling for tasks 101 and 103 remain incomplete; see the included user guide.

[返回主页 / Home](../../../README.md) · [更新记录 / Changelog](../../../CHANGELOG.md)
