---
title: AI Native 组织对照
type: 主题综述
tags:
  - 品类
  - 综述
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · AI Native 组织
sources:
  - https://github.com/block/buzz
  - https://github.com/omnigent-ai/omnigent
  - https://github.com/paperclipai/paperclip
  - https://github.com/humanlayer/humanlayer
publish: true
---

# AI Native 组织对照

这里盯的是组织里人和 agent 怎么一起工作，不是个人在自己电脑上养一个助手。个人网关、本机工作台仍看 [[Personal-Agent品类对照]]。

## 几件真正要对上的能力

1. **同一会话里多人进出**：工程师、产品或其他角色进入同一个 agent 会话交替下指令，会话本身成为工作对象。
2. **数字同事进现有工作流**：在团队聊天或任务工具里接活、拆会话、等人拍板。
3. **组织知识给 AI 用**：有统一入口和说明书，而不是每人私下喂一套材料。
4. **人在回路的编排**：并行跑多个 agent，关键步骤由人批准。

## 开源和闭源怎么放在一起看

开源侧，[[Buzz]] 是人和 agent 同处的团队房间，中继可自托管；[[Omnigent]] 强调会话分享和共驾；[[Lody]] 能打开同一个编码会话，但跨设备同步主要走官方云；[[Paperclip]]、[[HumanLayer]]、[[Multica]]、[[Agent-Orchestrator]]、[[OpenHands]] 的团队能力，各自落在管理、审批、派活或编码云上。

闭源的团队编码产品也可以对这几项能力，但往往只能托管使用，不能当作开源对照的替代实现。比较时只并列能力，不要把「能自托管的房间」和「只能租用的云编码电脑」写成同一个东西。

入口：[[indexes/品类]]。
