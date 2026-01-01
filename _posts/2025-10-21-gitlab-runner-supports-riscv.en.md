---
layout: single
title:  "A Big Step for RISC-V: GitLab officially merged RISC-V Runner support"
date:   2025-10-21 18:18:18 +0800
categories: blog
tags: ecosystem news english
permalink: blog/gitlab-runner-supports-riscv

excerpt: "This means that hundreds of thousands of open source software projects
  hosted by GitLab will be able to more easily incorporate RISC-V into their
  CI/CD processes. The RISC-V software ecosystem will usher in another major growth."

---

# A Big Step: After 11 months of review, GitLab officially merged RISC-V Runner support!

TL;DR: GitLab Runners now have official RISC-V binary versions! This means that hundreds of thousands of open source software projects hosted by GitLab will be able to more easily incorporate RISC-V into their CI/CD processes. The RISC-V software ecosystem will usher in another major growth.

GitLab, a popular open source end-to-end software development platform, hosts well-known projects such as Wireshark, KiCAD, QEMU, and wget. Its community open source version supports well-known open source projects such as GNOME, KDE, Debian, Arch, and Kali Linux. Today, RISC-V runner support was added to its official repository. The native RISC-V runner means faster running speed and more realistic test environment, which is a breakthrough in common code hosting platforms[1].

For projects hosted by GitLab, there will be no need to compile the RISC-V runner yourself in the future. CI/CD can directly use the official RISC-V runner binary for building without special configuration, which further facilitates project management and reduces the mental burden of developers in developing/configuring pipelines (workflows).

The corresponding commit address [2], this Merge Request was provided by Meng Zhuo, an engineer at the Institute of Software, Chinese Academy of Sciences, and was finally merged after 11 months of careful review by GitLab upstream developers.

GitLab is expected to provide an official RISC-V runtime environment in the future, narrowing the gap with the mainstream x86 and Arm architectures.

Currently, the largest code hosting platform, such as GitHub, is limited by the fact that dotnet does not support RISC-V and the Azure platform does not have a corresponding RISC-V virtual machine. RISC-V runner is still not officially supported. There are only actions provided by enthusiasts, such as setup-riscv-gnu-toolchain [3] based on QEMU, run-on-architecture-riscv64-alpine [4], and RISC-V builders based on real development boards [5].

Contributor profile: Meng Zhuo is a PLCT Lab [7] development engineer, Go language RISC-V architecture maintainer [8], focusing on the development of RISC-V cloud native related applications. Welcome to follow his Github [6].

References:

- [1] https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities)
- [2] https://gitlab.com/gitlab-org/gitlab-runner/-/merge_requests/5131
- [3] https://github.com/marketplace/actions/setup-riscv-gnu-toolchain
- [4] https://github.com/marketplace/actions/run-on-architecture-riscv64-alpine
- [5] https://riscv.builders/
- [6] https://github.com/mengzhuo
- [7] PLCT Lab is affiliated with the Intelligent Software Research Center (ISRC) of the Institute of Software, Chinese Academy of Sciences (ISCAS).
- [8] [zh_cn] [Meng Zhuo: the way Go to RISC-V](https://mp.weixin.qq.com/s/cJ8AJjPEh-DqQBCKqPNsfg)
