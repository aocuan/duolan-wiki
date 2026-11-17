---
title: Lody
type: 项目卡
tags:
  - 开源项目
  - 会话控制面
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/LodyAI/Lody
  - https://lody.ai
publish: true
repo: https://github.com/LodyAI/Lody
license: Apache-2.0
stars: 1788
verdict: 本地调度已有编码 agent 可用；团队和跨设备同步不要按完整自托管来预期
---

# Lody

[Lody](https://github.com/LodyAI/Lody) 是给团队用的编码 agent 共享工作台。它不自己卖模型，而是用 ACP 把已经在跑的 Claude Code、Codex 等接到统一的会话上，再从桌面、手机、Web 或命令行去调度。可以共享对话、差异和权限审批。官网是 [lody.ai](https://lody.ai)。

许可证是 Apache-2.0。星标 1,788，统计截至 2026-11-17（太平洋时间），仓库当天仍有推送。

## 开源范围

开源的是本地这一截：命令行守护进程、桌面客户端、各家 ACP 适配，以及本地的协同客户端栈。跨设备同步、工作区账号、计费和推送等控制面，主要在官方云上。手机和 Web 的完整体验，以及同步服务的实现，不在主仓库里按「可自托管全栈」来提供。

因此：已经在用编码 CLI、想在本机把多个 agent 会话收拢来的人，可以试用。若需求是团队共用会话并且完全自托管，不要按 README 里的跨设备能力来预期。

## 和相邻项目的差别

- 对照 [[Memoh]]：Memoh 开的是 agent 自己的电脑；Lody 开的是调度你已有 CLI 的控制面。
- 对照 [[OpenClaw]]：OpenClaw 是通用的本地优先助手网关，不以共享编码会话和差异为核心。
- 对照 [[Buzz]]：Buzz 的房间是团队聊天加 agent 入室；Lody 更接近「打开同一个编码会话接着下指令」。

品类背景见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
