**English** | [简体中文](README.zh-CN.md)

# ftkit 0.1.3-preview-20261016-r2

**[Download archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261016-r2/ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz)**

Built: 2026-10-16 · First published: 2026-10-17 · Archived release

[Full user guide (Chinese)](用户手册.txt) · [SHA-256](SHA256SUMS.txt) · [Repository copy](ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz?raw=true)

## Contents

1. [Installation and first use](#installation)
2. [Release contents](#changes)
3. [Documentation and verification](#verification)

<a id="installation"></a>
## Installation and first use

ftkit is a statically linked Linux x86_64 command-line tool. Python, Facet and a dynamic libc are not required. Setup and verification scripts require Bash 4+ and standard command-line tools. Download the archive and SHA256SUMS.txt into one directory:

```bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261016-r2-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
```

verify.sh configures your Bash PATH after verification. Keep the extracted directory; rerun setup after moving it. Use `bash verify.sh --no-install` for verification only or `bash install.sh` to configure PATH. Run `ftkit` in your calculation directory and choose a numbered task.

<a id="contents"></a>
<a id="changes"></a>
## Release contents

- Includes the ftkit rename and earlier phonon-capacity fixes.
- The archive includes setup/verification scripts, examples, manuals, build information and third-party notices, without application source.
- Tasks 101 and 103 use Relative energy (eV), relative to the minimum in each output; missing energies remain missing.
- The application version is 0.1.3; the full distribution revision is shown in this page title.

<a id="verification"></a>
## Documentation and verification

Original checks covered archive contents, the archive SHA-256 and executable hash. The included BUILDINFO.json records earlier tests. Task 101 stride and unified interruption for tasks 101/103 have documented limitations. No rebuild or automated tests were run for this update. Linux execution and older-kernel compatibility were not revalidated. The complete manual is currently available in Chinese.

<a id="user-guide"></a>
[Full user guide (Chinese)](用户手册.txt)

This standalone guide was revised on 2026-10-20; the archive retains its original bundled docs/zh-CN/ files.

```text
d66f3539c585b5030eca7ff68f3e16e15db4d20ccb734253d7ae41597bc9dadd  ftkit-0.1.3-preview-20261016-r2-linux-x86_64.tar.gz
```

[Latest downloads](../../../README.md#downloads) · [Changelog](../../../CHANGELOG.md)
