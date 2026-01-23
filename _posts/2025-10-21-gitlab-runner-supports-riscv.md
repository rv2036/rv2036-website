---
layout: single
title: "里程碑！GitLab 合入 RISC-V Runner 支持"
date: 2025-10-21 18:18:18 +0800
categories: blog
tags: ecosystem news chinese
permalink: /blog/gitlab-runner-supports-riscv
lang: zh

excerpt: "原生的 RISC-V runner 意味着更快的运行速度，更真实的测试环境，这在常见代码托管平台中[1]属于突破性进展。"
---

历经11个月审核，GitLab官方今日合入RISC-V Runner支持。

GitLab，一个受欢迎的开源端到端的软件开发平台，自身托管着 Wireshark，KiCAD，QEMU，wget 等知名项目，其社区开源版本支撑着 GNOME，KDE，Debian，Arch，Kali Linux 等著名开源项目。今天在其官方仓库添加了RISC-V runner 支持，原生的 RISC-V runner 意味着更快的运行速度，更真实的测试环境，这在常见代码托管平台中[1]属于突破性进展。

对于 GitLab 托管的项目，在未来无需自行编译 RISC-V runner ，CI/CD 中不需要特殊配置便可直接使用官方提供的 RISC-V runner 二进制进行构建，进一步方便了项目管理，降低了开发人员的研发/配置流水线（workflow）的心智负担。

此次对应的提交地址[2]，此 Merge Request（合并请求） 由 PLCT 开发工程师 Meng Zhuo 提供，在 GitLab 上游开发者在仔细审核11个月后最终合入。

GitLab未来有望提供官方的 RISC-V 运行环境，缩短追平x86和Arm主流架构的差距。

目前最大的代码托管平台如 GitHub ，受限于 dotnet 不支持 RISC-V 和 Azure 平台没有对应 RISC-V 虚拟机， 仍未官方支持 RISC-V runner，仅有爱好者提供的Action如基于QEMU的 setup-riscv-gnu-toolchain [3]， run-on-architecture-riscv64-alpine[4] ，以及基于真实开发板的 RISC-V builders[5].

### 关于提交者 Meng Zhuo

PLCT Lab [7] 开发工程师，Go语言 RISC-V 架构 maintainer，关注 RISC-V 云原生相关应用发展。欢迎 follow 他的 Github[6]。
profile](./profile.png)

### 参考链接

- [1] https://en.wikipedia.org/wiki/Comparison_of_source-code-hosting_facilities)
- [2] https://gitlab.com/gitlab-org/gitlab-runner/-/merge_requests/5131
- [3] https://github.com/marketplace/actions/setup-riscv-gnu-toolchain
- [4] https://github.com/marketplace/actions/run-on-architecture-riscv64-alpine
- [5] https://riscv.builders/
- [6] https://github.com/mengzhuo
- [7] PLCT Lab is affiliated with the Intelligent Software Research Center (ISRC) of the Institute of Software, Chinese Academy of Sciences (ISCAS).
- [8] [zh_cn] [Meng Zhuo: the way Go to RISC-V](https://mp.weixin.qq.com/s/cJ8AJjPEh-DqQBCKqPNsfg)
