---
title: OpenBot
type: 项目卡
tags:
  - 开源项目
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 扫榜 · GitHub 趋势
sources:
  - https://github.com/CopilotKit/OpenBot
  - https://open.bot
repo: https://github.com/CopilotKit/OpenBot
license: MIT
stars: 12665
verdict: 可自托管的「每 bot 一台带浏览器的电脑」。多用户时要确认是否真的按人隔离容器，不要共用一个浏览器。
publish: true
---

# OpenBot

[CopilotKit/OpenBot](https://github.com/CopilotKit/OpenBot)（MIT，约 1.3 万星，截至 2026-11-17，太平洋时间；站点 [open.bot](https://open.bot)）是可自托管的 agent 工作台：每个 bot 可以有自己的电脑环境，并带上浏览器。它和「个人网关接到聊天渠道」不是同一层，更接近 agent 电脑。

多用户同时使用时，内存主要耗在浏览器上，而不是处理器。官方默认会限制同时活跃的浏览器数量，并在空闲一段时间后回收。若没有按人打开隔离环境，登录态和文件可能被共用，不适合当作多用户边界。

同形态还可以对照 [[Rakazo]]、[[OpenMausBot]]、[[Memoh]]。不要把它和必须依赖闭源对话层的模板项目当成同一个东西。

品类见 [[Agent电脑与沙箱层]]、[[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
