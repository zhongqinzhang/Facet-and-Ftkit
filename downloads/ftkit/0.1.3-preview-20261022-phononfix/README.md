**English** | [简体中文](README.zh-CN.md)

# ftkit 0.1.3-preview-20261022-phononfix

**[Download archive · 3.83 MB](https://github.com/zhongqinzhang/Facet-and-Ftkit/releases/download/ftkit-v0.1.3-preview-20261022-phononfix/ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz)**

Built: 2026-10-22 · First published: 2026-10-23 · Current ftkit preview

[Full user guide (Chinese)](用户手册.txt) · [SHA-256](SHA256SUMS.txt) · [Repository copy](ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz?raw=true)

## Contents

1. [Installation and first use](#installation)
2. [Release contents](#changes)
3. [Documentation and verification](#verification)

<a id="installation"></a>
## Installation and first use

ftkit is a statically linked Linux x86_64 command-line tool. Python, Facet and a dynamic libc are not required. Setup and verification scripts require Bash 4+ and standard command-line tools. Download the archive and SHA256SUMS.txt into one directory:

```bash
sha256sum -c SHA256SUMS.txt
tar -xzf ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
cd ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64
bash verify.sh
source "$HOME/.config/ftkit/env.sh"
ftkit --version
```

verify.sh configures your Bash PATH after verification. Keep the extracted directory; rerun setup after moving it. Use `bash verify.sh --no-install` for verification only or `bash install.sh` to configure PATH. Run `ftkit` in your calculation directory and choose a numbered task.

<a id="contents"></a>
<a id="changes"></a>
## Release contents

- Task 301 accepts compound headings in VASP mass-corrected sections, including the corresponding corrected-section-only format.
- Lattice/POMASS consistency checks continue through the end of the file; contradictory input is rejected without replacing existing output.
- Mode order, mass-correction rules, command options and formats are unchanged.
- Tasks 101 and 103 use Relative energy (eV), relative to the minimum in each output; missing energies remain missing.
- The application version is 0.1.3; the full distribution revision is shown in this page title.

<a id="verification"></a>
## Documentation and verification

The original publication checked the archive, executable and 177 internal checksums. BUILDINFO.json records 49 tests, a VASP 6.5.1 OUTCAR roundtrip and an ELF audit from the original build. No rebuild or automated tests were run for this update. Linux execution and older-kernel compatibility were not revalidated. The complete manual is currently available in Chinese.

<a id="user-guide"></a>
[Full user guide (Chinese)](用户手册.txt) · [BUILDINFO.json](BUILDINFO.json) · [Release notes (Chinese)](更新说明.txt)

```text
c338878c3531b64daff35f0ca27ce89ee75ba4a55979a26ae571224b91b5f666  ftkit-0.1.3-preview-20261022-phononfix-linux-x86_64.tar.gz
```

[Latest downloads](../../../README.md#downloads) · [Changelog](../../../CHANGELOG.md)
