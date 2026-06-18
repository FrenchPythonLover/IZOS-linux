# Contributing to IZOS

Thank you for your interest in contributing to IZOS. 

## Before contributing

* Read the README.
* Verify the said contribution isn't already in review / already present
* Open an issue before making large changes.
* Keep pull requests focused on a single feature or bugfix.
* Please, no useless commiting like 'fixing xxx in README', it just blows up the git history for no useful contribution.

## Coding guidelines

### Shell scripts

* Use POSIX shell when possible.
* Keep scripts readable and documented.
* Avoid hardcoded paths.  
*For reference, take a look at the fs/init (init file) script. It's not perfect but a great example.*
  
### C code

* Compile with warnings enabled.
* Comment non-obvious code.
* Keep dependencies minimal.  
*For reference, look at some files in linux/src/. It's the best example out there*
  
## Commit messages
Format: `USERNAME -> part: content`  
Examples:

* `Tilto66 -> kernel: enable ext4 support`
* `FrenchPythonLover -> init: fix extmount detection`
* `apprenti2012 -> kmscon: add French keyboard layout`
* `Kelbazz -> busybox: update configuration`  
*The format above is the most preferred one for consistency.*  

## Testing

Before opening a pull request:

* Verify initramfs generation works.
* Verify the system boots in QEMU.
* Ensure that the generated initramfs has a reasonable file size.

## Submitting a pull request 
Pull requests (PRs for short) are subject to strict formatting:  

### Code pull requests
Code pull requests are PRs that are either:
  - modifying the kernel code
  - editing the target fs (extmount / initramfs)
  - changing the programs source files
  - bugfixes
  - Multiple (or all) of the above
Here is the formatting:
```
Author: <Author of the code / PR>
Type: code
Subtype: <Explain with a few words the category of the change>
AI: <yes/no (only if AI was used to generate or significantly assist the code)>
New size: <insert new size of initramfs and/or extfs>
Description: <Provide a detailed description of the changes>
```
### Docs pull requests
Docs pull requests are simply PRs that change the wiki, MD files (like this exact one right now), and other documentation-related content on this project.  
Formatting for such PRs is:
```
Author: <Author of the code / PR>
Type: docs
Subtype: <Explain with a few words the documentation category of the change>
AI: <yes/no (only if AI was used to generate or significantly assist the code)>
Description: <Provide a detailed description of the changes>
```

## Reporting bugs using issues

Include:

* Host operating system.
* QEMU version.
* Steps to reproduce.
* Relevant logs.
In a format close to this:
```
Author: <Author of the issue>
OS: <include OS version, including kernel version if on macOS, linux or bsd>
Architecture: <x86, x64, arm, aarch64, mips, loongarch...>
QEMU Version: <Insert version extracted from qemu-system-x86-64 --version>
Steps to reproduce: <Provide with very detailed instructions to reproduce the encountered bug>
Logs: <Put some relevant logs (like qemu output) here>
```

## Code of conduct
Be respectful and constructive.

Everyone is welcome to contribute regardless of age or experience level.
