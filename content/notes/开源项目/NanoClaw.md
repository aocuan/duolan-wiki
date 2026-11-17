---
title: NanoClaw
type: 项目卡
tags:
  - 开源项目
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/nanocoai/nanoclaw
  - https://nanoclaw.dev
repo: https://github.com/nanocoai/nanoclaw
license: MIT
stars: 31116
verdict: OpenClaw 的容器隔离减配版个人网关，不是带桌面的 agent 电脑。适合要隔离的个人助手，不适合当公司工作台。
publish: true
---

# NanoClaw

[nanocoai/nanoclaw](https://github.com/nanocoai/nanoclaw)（MIT，约 3.1 万星，截至 2026-11-17，太平洋时间；站点 [nanoclaw.dev](https://nanoclaw.dev)）是个人助手 / 网关。它针对的是把聊天渠道凭证和命令执行放在同一进程里的风险：默认在容器里跑 bash、文件和浏览器，凭据可以走宿主侧注入，而不把原始密钥塞进容器。

## 不要和这些东西搞混

它和 [[OpenClaw]] 是同一品类，主干更瘦，功能常常要在自己的分支里加。即时通讯渠道不是 clone 完就能用，而是按需装上。

它不是 [[Memoh]]、[[Rakazo]]、[[OpenMausBot]] 那种带可看桌面的工作台。隔离层是普通容器，不要按微虚机或远程桌面来预期。沙箱运行时要看 [[agent-sandbox]] 或 [[agent-infra-sandbox]]。

仓库迭代快，issue 也多，适合当可审计的轻量网关来跟踪，不适合当成已经稳定的企业基线。

品类见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
