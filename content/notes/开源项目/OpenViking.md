---
title: OpenViking
type: 项目卡
tags:
  - 开源项目
  - 记忆
  - 上下文
date: 2026-11-26
updated: 2026-11-26
status: evergreen
sources:
  - https://github.com/volcengine/OpenViking
publish: true
repo: https://github.com/volcengine/OpenViking
license: AGPL-3.0
stars: 42898
verdict: 把知识、记忆和 Skills 放进同一个可浏览的虚拟文件系统；思路好，但 AGPL 许可要先评估
---

# OpenViking

[OpenViking](https://github.com/volcengine/OpenViking) 是火山引擎开源的 agent 上下文数据库。它把文档与代码（资源）、用户偏好与经验（记忆）、做事方法（Skills）放进同一个虚拟文件系统，每条内容都有 `viking://` 地址。agent 像操作文件一样用 `ls`、`tree`、`read`、`grep` 浏览，每个目录带自动生成的摘要，先看摘要再决定读什么。许可证 AGPL-3.0，星标 42,898，截至 2026-11-26（太平洋时间）。

## 开源范围

服务端和 Web Studio 都可以自托管，另有在线试用。AGPL-3.0 意味着改了代码再对外提供网络服务时，要按许可证开放修改，商用前要先评估。

## 判断

它把「记忆是黑盒」变成「记忆是可以打开检查的目录」，和 [[LLM知识库]]、[[Agentic搜索]] 的思路一致：先让 agent 能像人一样翻目录，再在子树里做语义搜索。2026 年 9 月热过一波，之后仍在增长。

## 和相邻项目的差别

- 对照 [[Basic-Memory]]：Basic Memory 直接用普通 Markdown 文件；OpenViking 是带服务端的虚拟文件系统。
- 对照 [[Hindsight]]、[[Mem0]]：那些专注记忆层；OpenViking 同时管知识、记忆和 Skills。

地图见 [[Agent知识库项目地图]]。入口：[[indexes/开源项目]]。
