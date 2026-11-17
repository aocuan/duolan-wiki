---
title: OpenHands
type: 项目卡
tags:
  - 开源项目
  - agent电脑
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · Personal Agent
sources:
  - https://github.com/OpenHands/OpenHands
  - https://openhands.dev
publish: true
repo: https://github.com/OpenHands/OpenHands
license: MIT
stars: 93631
verdict: 开源编码 agent 里体量最大的之一；多租户托管层另有仓库和许可，不要把单租户 Helm 当成可卖的云
---

# OpenHands

[OpenHands](https://github.com/OpenHands/OpenHands) 是开源的 AI 驱动开发环境。官网是 [openhands.dev](https://openhands.dev)。许可证是 MIT。星标 93,631，统计截至 2026-11-17（太平洋时间），仓库当天仍有推送。

## 开源范围

主仓可以自部署。多租户托管是另一层：存在单独的 Cloud 仓库，许可不是开源许可；开源的 Helm 更接近单租户、需要自己处理鉴权的部署。文档也写过，多用户要走企业或托管产品。把 OpenHands 当「编码 agent 云」来选时，必须把这一层算进去。

## 和相邻项目的差别

- 对照 [[Maka]]、[[Goose]]：同属编码 agent，OpenHands 更完整地面对「云上干活」，但也因此把多租户单独切开。
- 对照 [[Memoh]]、[[Rakazo]]：那些是通用 agent 电脑或控制面；OpenHands 的重心是软件工程任务。

品类见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
