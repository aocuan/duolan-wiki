---
title: OpenClaw
type: 项目卡
tags:
  - 开源项目
  - 个人网关
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · OpenClaw 生态
sources:
  - https://github.com/openclaw/openclaw
  - https://openclaw.ai
publish: true
repo: https://github.com/openclaw/openclaw
license: MIT
stars: 394619
verdict: 本地自托管个人助手网关的标杆；不要把它当成团队云或 agent 电脑来选
---

# OpenClaw

[OpenClaw](https://github.com/openclaw/openclaw) 是本地优先的开源个人 AI 助手。自己运行 Gateway，把它接到已经在用的聊天渠道，并连接浏览器、文件和工具；模型可以换成不同的云模型或本地模型。官网是 [openclaw.ai](https://openclaw.ai)。

许可证是 MIT。星标 394,619，统计截至 2026-11-17（太平洋时间），仓库当天仍有推送。这个星标量说明它是当前开源个人助手里的事实底座之一，但不等于「什么场景都该用它」。

## 开源范围

主仓库按自托管网关来开源，官方路线强调自己运行、而不是再提供一套多租户托管云。一个 Gateway 上可以建多个 agent，各自指定工作区，用来隔离不同任务。需要注意：技能目录、配对名单等仍可能是全局的，工作区默认也不是硬沙箱，绝对路径仍可能摸到别的目录，除非打开更严的隔离。

## 和相邻项目的差别

- 对照 [[Memoh]]：OpenClaw 是网关和渠道，不是给每个 agent 一台带桌面的电脑。
- 对照 [[Lody]]：Lody 聚焦共享编码会话；OpenClaw 聚焦个人或小团队把助手接到日常聊天里。
- 对照 [[Buzz]]：Buzz 是人和 agent 同处的团队房间；OpenClaw 可以被接进这类房间，但本身不是房间产品。

实践和版本追踪适合另外写成趋势稿，不必全部堆在项目卡里。品类背景见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
