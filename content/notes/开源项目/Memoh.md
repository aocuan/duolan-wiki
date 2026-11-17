---
title: Memoh
type: 项目卡
tags:
  - 开源项目
  - agent电脑
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/felinics/Memoh
  - https://memoh.ai
publish: true
repo: https://github.com/felinics/Memoh
license: AGPL-3.0
stars: 2816
verdict: 适合自托管试用；托管云是另一层，不等于缺核心代码
---

# Memoh

[Memoh](https://github.com/felinics/Memoh) 是开源的多 agent 平台：每个 agent 有自己的隔离电脑，包括文件、桌面、浏览器、网络和长期记忆。也可以把已有的编码 agent 接到这台电脑上。官网是 [memoh.ai](https://memoh.ai)。

许可证是 AGPL-3.0。星标 2,816，统计截至 2026-11-17（太平洋时间），仓库当天仍有推送。

## 开源范围

自托管栈是开源的，可以自行拉起。没有放进开源仓库的，主要是「替你运维」那一层：多租户、计费和托管编排。官方另有托管云，那是便利，不是核心代码缺一块。AGPL 会约束把修改后的服务当作闭源云再卖出去，但不影响只使用、不提供网络服务的场景。

没有看到独立的官方手机应用。移动侧通常通过即时通讯渠道或浏览器访问，桌面和 Web 是主要界面。

## 和相邻项目的差别

- 对照 [[OpenClaw]]：OpenClaw 是本地优先的个人网关，把助手接到已有聊天渠道和工具上，不是「给每个 agent 配一台电脑」。
- 对照 [[Lody]]：Lody 开的是调度已有编码 CLI 的控制面，跨设备和团队同步主要走官方云。
- 对照 [[Buzz]]：Buzz 是人和 agent 待在同一个团队房间里，不是 agent 机房。

品类背景见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
