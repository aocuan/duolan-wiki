---
title: Cumora
type: 项目卡
tags:
  - 开源项目
  - 品类
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · AI Native 组织
sources:
  - https://github.com/yetone/cumora
  - https://cumora.ai
repo: https://github.com/yetone/cumora
license: MIT
stars: 4195
verdict: 人和 agent 平级的团队即时通讯；前后端均可自托管。适合作为组织级对照，而不是个人助手。
publish: true
---

# Cumora

[yetone/cumora](https://github.com/yetone/cumora)（MIT，约 4195 星，截至 2026-11-17，太平洋时间；站点 [cumora.ai](https://cumora.ai)）是团队聊天软件：人和 AI agent 作为平级成员，共用私聊、群聊、看板和日历。agent 可以认领任务、互相协调以免撞车，也可以收发邮件。

## 开源范围

仓库按 MIT 开放，服务端、桌面端、移动端和自带 agent 的接入程序都在同一仓里。托管版能力基本上能在自托管里找到对应实现。默认会指向官方域名，但可以用环境变量改掉。公开讨论里已有人在跑自托管。截至核验时，未见单独的企业目录或授权校验；付费订阅和企业单点登录不在开源范围里。

agent 有两种跑法：一种是在集群里给每个 agent 一个容器；另一种是把已有的编码 agent 接到工作区，模型密钥不必经过服务端。

## 怎么放

主类是组织级的人机同室，其次才是会话控制面和看板。不要把它和个人网关或「每人一台电脑」放进同一张竞品表。更近的对照是 [[Buzz]]，而不是 [[OpenClaw]]。

品类见 [[AI-Native组织对照]]。入口：[[indexes/开源项目]]。
