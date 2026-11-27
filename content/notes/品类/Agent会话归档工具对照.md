---
title: Agent 会话归档与经验复用工具对照
type: 主题综述
tags:
  - 品类
  - 记忆
  - 会话归档
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/kenn-io/agentsview
  - https://github.com/Asymptote-Labs/agent-beacon
  - https://github.com/vshulcz/deja-vu
  - https://github.com/thedotmack/claude-mem
  - https://github.com/nowledge-co/nowledge-mem
publish: true
---

# Agent 会话归档与经验复用工具对照

同时用好几种编码 agent 以后，会话散在各个工具里。相关工具可以按「想解决什么」分成三类。星标截至 2026-11-26（太平洋时间）；只看文档、更新记录和公开反馈，未逐个实测。

## 三类需求

1. **集中归档、能搜能看**：[[AgentsView]]（MIT，约 6,500 星）。读取 50 多种 agent 已有的会话，本地存储、全文搜索、统计花费，多台机器可以归到一处。对现有习惯打扰最小。
2. **让下一次 agent 用上以前的经验**：
   - [[Beacon]]（MIT，约 3,600 星）：跨 20 多种 harness 采集完整会话，提炼成可复用经验；有云版，安装时确认存储位置。
   - [[deja-vu]]（MIT，约 1,700 星）：单个二进制，读本机日志，不调用模型；个人维护。
   - [[claude-mem]]（Apache-2.0，约 12 万星）：用 hooks 记录工作轨迹并压缩注入，偏单一工具的跨会话上下文。
   - [[Nowledge-Mem]]：核心闭源，可以本地或 Docker 部署，能接网页版聊天工具，并把对话提炼成记忆。免费版有条数上限，付费前核对价格。
3. **多端接手同一个会话**：[[Lody]]、[[Omnigent]]。它们管「现在这场会话」，不负责导入历史。

## 建议

- 只想把编码对话归档好：先装 AgentsView。
- 想要自动记忆：免费、轻量的选 deja-vu；想跨工具沉淀经验、能接受云选项的看 Beacon；不要求开源、看重中文界面的再试 Nowledge Mem 免费版。
- 团队在手机和电脑之间接手同一场会话：看 Lody 或 Omnigent。
- 人和 agent 共用的聊天室（例如 [[Buzz]]）不导入历史，不属于这一类。

更底层的分层（原始记录检索、记忆层、个人上下文）见 [[Agent记忆与聊天记录工具]]。入口：[[indexes/品类]]。
