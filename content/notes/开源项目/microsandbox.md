---
title: microsandbox
type: 项目卡
tags:
  - 开源项目
  - 沙箱
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/superradcompany/microsandbox
repo: https://github.com/superradcompany/microsandbox
license: Apache-2.0
stars: 9103
verdict: 本机或内网里做隔离执行的微虚机运行时。只要跑代码、不要桌面时可以看；它不是工作台产品。
publish: true
---

# microsandbox

[superradcompany/microsandbox](https://github.com/superradcompany/microsandbox)（Apache-2.0，约 9103 星，截至 2026-11-17，太平洋时间）是可编程的微虚机运行时，可以嵌进进程里跑，也兼容常用的容器镜像格式。它解决的是「把不可信代码隔离开」，不是给每个人开一台能看的电脑。

若目标是带浏览器和桌面的一体环境，先看 [[agent-infra-sandbox]]；若要在集群里管生命周期，再看 [[agent-sandbox]]。需要远程桌面和控制面时，不要从这一层起步。

品类见 [[Agent电脑与沙箱层]]。入口：[[indexes/开源项目]]。
