---
title: Rakazo
type: 项目卡
tags:
  - 开源项目
  - agent电脑
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/elie222/rakazo
  - https://rakazo.com
publish: true
repo: https://github.com/elie222/rakazo
license: Apache-2.0
stars: 8928
verdict: 自托管控制面里最接近「每个 bot 一台可接管电脑」的选择之一；仍在快速迭代，不要按多年稳定的企业平台来预期
---

# Rakazo

[Rakazo](https://github.com/elie222/rakazo) 是一套可自托管的多端控制面：每个 bot 有自己的对话、记忆、例行任务，以及一台可查看、可接管的电脑。人用浏览器、桌面或手机去连自己拉起的服务，而不是把助手装在某一台笔记本里。官网是 [rakazo.com](https://rakazo.com)。

许可证是 Apache-2.0。星标 8,928，统计截至 2026-11-17（太平洋时间），仓库当天仍有推送。

## 开源范围

核心不依赖官方网站才能运行，Docker Compose 可以自部署。电脑默认是 Docker 容器，也可以换成其他沙箱后端。模型通常是自带密钥。后来补上了邀请别人进入同一 Space、共享 bot 和那台电脑的能力；早期版本更接近「多个互相隔离的个人账号」，看文档时要以当前版本为准。

它仍在快速发版，适合试用和二次开发，不宜当成已经稳定多年的生产多租户平台。

## 和相邻项目的差别

- 对照 [[Memoh]]：两者都给 agent 电脑。Rakazo 更像自托管的 Web 控制面；Memoh 更常通过即时通讯渠道进入常驻机房，许可证是 AGPL。
- 对照 [[OpenMausBot]]：OpenMausBot 把电脑放在使用者自己的机器上；Rakazo 的 bot 和电脑跑在你托管的服务上。
- 对照 [[Coder]]：Coder 给人开开发工作区，不是让 bot 自己点浏览器干活。

品类见 [[Agent电脑与沙箱层]]。入口：[[indexes/开源项目]]。
