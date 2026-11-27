---
title: Personal Agent 品类对照
type: 主题综述
tags:
  - 开源项目
  - 综述
date: 2026-11-17
updated: 2026-11-26
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/openclaw/openclaw
  - https://github.com/felinics/Memoh
  - https://github.com/LodyAI/Lody
  - https://github.com/block/buzz
publish: true
---

# Personal Agent 品类对照

开源「个人 agent」看起来都像聊天助手，其实经常不是一类产品。先把品类钉死，再谈能不能自托管、开了哪一层，比较才有意义。

## 结论

至少要分成五层。一个仓库通常只把其中一层做深，README 却可能把相邻能力写得很满。

| 品类 | 它真正做的事 | 例子 |
|---|---|---|
| 个人助手 / 网关 | 自己跑一个入口，把助手接到聊天渠道、文件和工具上 | [[OpenClaw]]、[[Hermes-Agent]]、[[nanobot]]、[[NanoClaw]]、[[Octop]] |
| Agent 电脑 / 工作台 | 给每个 agent 一台带桌面、浏览器和文件的隔离环境 | [[Memoh]]、[[Rakazo]]、[[OpenMausBot]]、[[OpenBot]]、[[Maka]]、[[Goose]]、[[OpenHands]] |
| 会话控制面 | 调度已经在跑的编码 CLI，共享会话、差异和权限 | [[Lody]]、[[Paseo]]、[[Herdr]]、[[t3code]]、[[Omnigent]] |
| 团队房间 | 人和 agent 作为成员待在同一套频道或房间里 | [[Buzz]] |
| 看板 / 派活 | 建任务、分给某个 agent、看进度、等人来评审；自己通常不写代码 | [[Multica]]、[[Agent-Orchestrator]]、[[Paperclip]] |

还有一层常常被混进来：**沙箱或云开发环境**。它解决的是「给人和 agent 一台可回收的运行环境」，不是聊天产品，也不是个人助手。不要和上面五类放进同一张竞品表。

## 怎么判断开源范围

口诀就一条：宣传里把团队、手机、同步写得很满时，去看仓库里有没有对应的服务端。没有，云就是产品；服务端都在、只缺托管运维，才是可自托管路线。

对照见各项目卡：[[Lody]] 属于前者，[[Memoh]]、[[OpenClaw]]、[[Buzz]]、[[Rakazo]] 更接近后者，但各自开的不是同一层。组织级的多人协作另见 [[AI-Native组织对照]]，电脑和沙箱另见 [[Agent电脑与沙箱层]]。

## 不要混用的几个词

- **个人 agent**：一直在线、能用工具把事办完的助手。和「你问我答」的聊天机器人不同。
- **Agent 电脑**：给 agent 用的隔离环境，关了笔记本电脑它仍可继续跑。不是人去远程桌面写代码的开发机。
- **共享会话**：多个人进入同一个 agent 对话交替下指令。这和「一个团队里每人各有一个助手」不是一回事。
- **自托管**：能在自己的机器上跑起来，不等于官方把可拿去当商品卖的多租户云也开了源。

相关项目卡见上表。
还有两类不要和上面的开源项目卡混着比。一是源码可见但不是 OSI 开源的产品，例如 Agor（BUSL-1.1），可以看形态，不能按开源内核来用。二是形态很像带桌面的个人 agent、但对话或云层仍依赖闭源服务的模板，开源对照时应把这一层写清楚，再去看 [[Rakazo]]、[[OpenMausBot]]、[[Memoh]] 这类能自托管的底座。

2026 年 11 月出现的 [[nod]] 也属于「个人助手 + 自带电脑」这一形态，可以和 [[OpenMausBot]] 对照看。

入口：[[indexes/开源项目]]。
