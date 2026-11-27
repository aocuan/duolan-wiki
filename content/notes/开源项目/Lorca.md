---
title: Lorca
type: 项目卡
tags:
  - 开源项目
  - 个人网关
date: 2026-11-17
updated: 2026-11-26
status: evergreen
source_bot: 监控 · Personal Agent
sources:
  - https://github.com/egoist/lorca
  - https://lorca.app
publish: true
repo: https://github.com/egoist/lorca
license: GPL-3.0
stars: 376
verdict: 强调端到端加密和本机身份的个人多 agent 应用；体量小，许可证是 GPL-3.0，二次分发时要仔细看
---

# Lorca

[Lorca](https://github.com/egoist/lorca) 想做单人使用、带 agent、并且端到端加密的通讯应用。官网是 [lorca.app](https://lorca.app)。许可证是 GPL-3.0。星标 376，统计截至 2026-11-17（太平洋时间）。

## 开源范围

跨设备中转的服务端也在开源范围内。身份在本地生成密钥，中转服务器按设计只能看到密文。它的体量仍然很小，更适合作为「加密遥控」路线的样本，而不是已经验证过的大规模底座。内核思路接近把 [[Pi]] 的循环用另一种语言重写，而不是直接依赖 Pi 的包。

Windows 和 Linux 客户端用作者自己的 Go 桌面框架 [[MyGo]] 写成，macOS 客户端是 Swift 原生。

品类见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
