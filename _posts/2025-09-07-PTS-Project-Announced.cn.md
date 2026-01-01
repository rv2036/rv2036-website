---
layout: single
title:  "甲辰计划启动RISC-V开源软件性能跟踪平台（PTS）建设"
date:   2025-09-07 18:18:18 +0800
categories: blog projects infra news chinese

excerpt: "关注全球重要开源软件RISC-V性能演化趋势并发布路线图；诚邀RISC-V厂商捐赠机器参与共建"
---
是时候了：甲辰计划启动RISC-V开源软件性能跟踪平台（PTS）建设，关注全球重要开源软件RISC-V性能演化趋势并发布路线图；诚邀RISC-V厂商捐赠机器参与共建

## PTS的背景、使命、历史重要性
RISC-V开源软件性能跟踪平台（Performance Tracking System, PTS）的想法最早诞生于2020年[1]，当时甲辰计划主理人吴伟先生作为RISC-V国际基金会的 Code Speed SIG 的联席主席，希望能够建设一个类似 Mozilla 的 `AreWeFastYet.com` 平台一样的可视化的愿系统，来跟踪包括 JavaScript Engines 在内的各种重要的开源软件在 RISC-V 芯片和系统上的性能。当时 RISC-V IP 和芯片的发展还聚焦在嵌入式领域，能够运行 Linux 桌面环境的开发板只有 SiFive Unmatched 等少量型号。

在当时PTS项目还是比较超前的，最大的顾虑也包括了如果过早的公开RISC-V芯片和Arm/X86的性能差距，有可能会对RISC-V的全球生态发展势头起到计划外的负面作用。

Code Speed SIG 在成立一年之后因为各种原因解散并重组，PTS项目也就一直雪藏到了现在。期间PLCT实验室曾在2021、2023年数次尝试启动PTS的建设，但是由于各种资源限制和裁员分流等原因未能冲线。

2024年除夕，甲辰计划启动了，带来了转机。经过一年多的发展，已经有超过50家企业加入甲辰计划，**逐步形成了「RISC-V开发板随缘漂流计划」、「开源实习生联合招聘培养项目」等相互支撑的项目，使得PTS的建设可能性重新被提出。**甲辰计划目前已经积累了足够的场地赞助和运营支持（苦芽科技、英麒智能、PLCT实验室、合肥工业大学、大连理工大学等），并积累了最够多的RISC-V开发板设备（其中阿里巴巴达摩院玄铁团队捐赠了200套TH1520开发板LicheePi 4A），建设PTS所需要的启动阶段的硬件和资金支持已经就绪。
PTS的建设和运营对于RISC-V全球生态系统的发展至关重要。目前RISC-V已经完成了在嵌入式等领域的覆盖，并正在朝着高性能计算和数据中心场景进行冲刺。全球开源软件生态对于RISC-V已经有了相当不错的功能性支持，往后的重点会是寻找各种提升速度的优化机会。有一个自动化性能测评系统以及由其产生的方便查询和对比的性能数据库，对于开发人员定位性能回退、寻找优化机会都会事半功倍。

PTS将会作为一个开源项目托管在甲辰计划GitHub组织账号下。如果一切顺利，2025年10月1日起可以通过 `pts.rv2036.org` 进行访问。PTS收集到的所有的性能数据也将开源，并托管于 `https://github.com/rv2036` 组织账号下。

## 跟踪的开源软件和benchmark范围

以下是初始阶段规划纳入观测范围的软件。后续会逐步添加RISC-V社区关注的软件。性能测评套件常见的包括 SPEC CPU 20xx 系列、CoreMark 系列等。不同的语言和执行环境有不同的测试集合，PTS默认将会搜集尽可能多的开源免费测试集纳入跟踪范围。

**编译工具链**
- GNU Toolchain：包含C/C++、Fortran等语言的编译器的性能。
- Clang/LLVM：包含Clang、Flang等语言的编译器的性能。
- Rust Toolchain

**虚拟机**
- V8
- Spidermonkey
- OpenJDK
- Jeandle
- Go Runtime
- LuaJIT
- .NET

**模拟器**
- QEMU
- Box64
- Wine-CE

**系统库和计算库、计算栈**
- glibc
- musl-c
- llvm libc
- OpenBLAS
- llama.cpp
- Eigen
- Highway
- 等等

## 跟踪的RISC-V芯片/系统范围

**主力测试机型（设备充足）**
- TH1520: SipeedLicheePi 4A
- SG2042: Milk-V PioneerBox

**标准测试机型（有至少1台设备可以长期稳定使用）**
- EIC7700: Milk-V Megrez
- K1: Sipeed LicheePi 3A

**期待测试机型（还没有稳定机器，但是 call for donation）**
- Sophgo SG2044
- A210
- SpacemiT K3
- DP1000: Milk-V Titan

### 基准操作系统
- RevyOS：玄铁IP系列默认使用的Debian发行版
- KarsierOS：苦芽科技基于openEuler社区版开发维护的商业维护版本
- Ubuntu：Canonical 对部分 RISC-V 开发板原生支持
- deepin：甲辰计划成员社区，在图形化界面方面很有本土化优势
- openKylin：甲辰计划成员社区，在图形化界面方面很有本土化优势

## 对比基线的选择
PTS将会陆续引入以下硬件系统作为非RISC-V架构的参考对比：
- RaspberryPi 4B - 2025Q3
- RaspberryPi 5 - 2025Q4 - call for donation
- Mac mini w/ M1 - 2025Q4 - call for donation
- AMD9950x - 2026Q1 - call for donation
- Mac mini w/ M4 - 2026Q2 - call for donation


## 路线图及成果发布

自2025Q4开始，PTS将会在每个季度结束之后15日内发布「RISC-V性能提升报告」。

**2025Q3**
- PTS开始筹建。
- 首批RISC-V设备上线（TH1520、SG2042、香山南湖单核）。
- V8进入PTS观测范围。
- 基线RaspberryPi 4B 上线

**2025Q4**
- 「RISC-V性能提升报告」创刊号发布。
- Spidermonkey进入观测范围。
- GNU Toolchain进入观测范围。
- Clang/LLVM进入观测范围。
- SPEC CPU 2006/2017 进入观测范围。
- 香山南湖四核上线
- 超睿DP100（Milk-V Titan）上线
- ESWIN EIC7700 SBC 上线
- Mac mini M1 上线
- RaspberryPi 5 上线

**2026Q1*8
- A210设备上线
- 香山昆明湖系列芯片上线
- 蓝芯CPU上线（TBD）

**2026Q2**
- 测试测评设备增加至100台、超过20种。
- 常用开源数据库进入测评范围。
- 增加稳定性测试。

**2026Q3**
- 测试设备增加至200台、完成对所有流行
- 所有HPC相关的常见开源测试集纳入测评范围。

**2026Q4**
- 所有数据中心关注的测评指标进入观测范围。

**2027Q1**
- 进入稳定维护状态。
- 测评硬件设备超过500台（套），跟踪软件项目超过100个，性能指标超过1000个。
- 添加至少2款128核RISC-V处理器。

## 与开源社区和开源团队的联动
即使筹备了5年，这依然是一个非常宏大的工程，有太多的工作需要完成和探索。甲辰计划主理人欢迎所有对该项目感兴趣的开发人和RISC-V相关团队加入进来。
## RISC-V开发板征集
欢迎RISC-V芯片和开发板厂商进行设备捐赠或借用。参与甲辰计划PTS的厂商将能够更快的观测到开源软件社区对自家芯片和硬件系统的支持情况，及时对性能回退进行修复，保持竞争优势地位。

## 总结和展望
RISC-V是一个充满活力的世界，欢迎加入！让我们用一纪的时间，在所有基础关键行业领域完成面向RISC-V的适配与优化，并形成超过万人的顶尖人才网络。

## 参考文献：
- [1] https://lists.riscv.org/g/sig-code-speed/topic/slides_proposal_of_code/79032157
- [2] https://arewefastyet.com/win11/benchmarks/overview?numDays=90
- [3] https://github.com/rv2036
