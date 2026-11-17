---
title: Buzz
type: 项目卡
tags:
  - 开源项目
  - 团队房间
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 监控 · AI Native 组织
sources:
  - https://github.com/block/buzz
  - https://github.com/block/buzz-app
publish: true
repo: https://github.com/block/buzz
license: Apache-2.0
stars: 37545
verdict: 人和 agent 同房间、中继可自托管；它不是编码云电脑，也不是个人网关
---

# Buzz

[Buzz](https://github.com/block/buzz) 是人和 agent 待在同一套团队房间里的通信与协作平台。编码 agent 跑在参与者自己的电脑上，在频道里一起工作。主仓库是中继和平台，星标 37,545；桌面和 Web 客户端在 [block/buzz-app](https://github.com/block/buzz-app)（约 278 星）。两个仓库都是 Apache-2.0。数字截至 2026-11-17（太平洋时间），当天都还有推送。

2026 年 11 月，`buzz-app` 发出 1.0 稳定版，覆盖 macOS、Windows 和 Linux。自托管时需要单独部署中继服务。

## 开源范围

中继可以自托管。客户端和中继都在 Apache-2.0 下公开。使用时仍要核对组织权限、插件校验等默认值：例如插件签名校验是否强制，会直接影响团队安装插件时的安全假设，需要按官方文档核对本机配置。

## 和相邻项目的差别

- 对照 [[Lody]]：Lody 更像打开同一个编码会话；Buzz 更像把人和 agent 放进同一个团队频道。
- 对照 [[OpenClaw]]：OpenClaw 是个人或小范围的助手网关，可以被接进房间，但不是房间本身。
- 对照 [[Memoh]]：Memoh 是给 agent 的电脑和机房；Buzz 是人机同室的沟通层。

品类背景见 [[Personal-Agent品类对照]]。入口：[[indexes/开源项目]]。
