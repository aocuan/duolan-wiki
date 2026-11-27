---
title: AgenticOS
type: 项目卡
tags:
  - 开源项目
  - 组织工作区
  - Agent平台
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/vstorm-co/agenticos
publish: true
repo: https://github.com/vstorm-co/agenticos
license: Apache-2.0
stars: 900
verdict: 面向公司的自托管多租户 agent 平台；值得当「harness 产品化、进组织」的样本跟踪，个人助手不必选它
---

# AgenticOS

[AgenticOS](https://github.com/vstorm-co/agenticos) 是面向公司的自托管 agent 平台，不是个人 CLI 助手。业务方在控制台里配置指令、模型、RAG、Skills、浏览器、沙箱和 MCP，再把 agent 发布到 Web、聊天工具、网页挂件或 API。管理侧负责预算、审批和审计。许可证 Apache-2.0，星标 900，截至 2026-11-26（太平洋时间）。

## 开源范围

自托管就是主要交付方式，用 docker compose 即可在本地起；调研时没有官方托管 SaaS，也没有开箱即用的 K8s 方案。底层基于 Pydantic AI，口号是「代码定义能力，配置负责组合」。它既能接外部 MCP，也能把自己暴露成 MCP 服务。

需要留意的地方：

- 贡献高度集中在少数维护者身上。
- 捆绑的部分组件（例如 PDF 处理）带 AGPL 义务，二次分发前要核对。
- 自托管不等于全本地：诊断和遥测之类的出站默认值，部署前按官方文档逐项确认。

## 和相邻项目的差别

- 对照 [[OpenClaw]]、[[nanobot]]：那些是个人助手网关；AgenticOS 的重点是组织级控制面，包括 RBAC、预算、OIDC 和多渠道发布。
- 对照编码 harness（Claude Code、Cursor 一类）：AgenticOS 不替代写代码的工具，而是把 agent 能力包成公司内可治理的服务。
- 品类上更接近 [[AI-Native组织对照]] 里的组织工作区，以及 [[Harness]] 产品化。

入口：[[indexes/开源项目]]。
