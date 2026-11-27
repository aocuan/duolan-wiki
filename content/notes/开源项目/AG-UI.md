---
title: AG-UI
type: 项目卡
tags:
  - 开源项目
  - 协议
  - 前端
date: 2026-11-26
updated: 2026-11-26
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/ag-ui-protocol/ag-ui
  - https://docs.ag-ui.com
publish: true
repo: https://github.com/ag-ui-protocol/ag-ui
license: MIT
stars: 21877
verdict: agent 和前端界面之间的开放事件协议，已发 1.0 稳定规范；给 agent 平台做前端时优先参考
---

# AG-UI

[AG-UI](https://github.com/ag-ui-protocol/ag-ui)（Agent-User Interaction Protocol）是一套开放、轻量、基于事件的协议，规定 agent 怎么和面向用户的应用对接。agent 会流式输出、在回复中途调用工具、更新共享状态、停下来等人确认、再派生子 agent；AG-UI 用一条双向事件流把这些统一起来，任何客户端都能按事件类型渲染。许可证 MIT，星标 21,877，截至 2026-11-26（太平洋时间）。

## 现状

2026 年 11 月发布 1.0：规范冻结并有 JSON Schema，TypeScript、Python 和 .NET 的 SDK 由规范生成，并且和 0.x 双向兼容。脚手架默认搭配 CopilotKit 前端。

## 和相邻协议的差别

- MCP 管 agent 怎么调用工具和数据源；AG-UI 管 agent 怎么把过程和结果交给界面。
- [[ACP]] 管编辑器或客户端怎么驱动编码 agent；AG-UI 更通用，面向任何用户界面。

相关项目：[[OpenBot]]。入口：[[indexes/开源项目]]。
