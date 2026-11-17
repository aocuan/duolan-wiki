---
title: Agent 电脑与沙箱层
type: 主题综述
tags:
  - 品类
  - 综述
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/agent-infra/sandbox
  - https://github.com/elie222/rakazo
  - https://github.com/felinics/Memoh
  - https://github.com/coder/coder
publish: true
---

# Agent 电脑与沙箱层

「给 agent 一台电脑」其实叠了好几层。开源项目往往只把其中一层做深，宣传却容易写满。比较时先分清要的是哪一层。

## 四层

1. **镜像**：一台能用的电脑长什么样。[[agent-infra-sandbox]] 把浏览器、终端、文件和桌面放进同一个容器。它不管登录和多人编排。
2. **调度**：很多大部分时间闲着的环境，如何启动、休眠和超售。集群里的沙箱接口属于这一层，不是给最终使用者打开的产品。
3. **控制面 / 产品壳**：账号、对话、审批、接管屏幕。[[Rakazo]] 是自托管的 Web 控制面，电脑默认在服务器上的容器里；[[Memoh]] 更像常驻机房，人从即时通讯渠道进入；[[OpenMausBot]] 把电脑放在使用者自己的设备上。
4. **人用的开发工作区**：[[Coder]] 给人（和在里面写代码的 agent）开隔离开发机。人连进去工作，这和 bot 自己点网页干活不是一回事。

## 怎么选

- 先要验证 computer-use：可以从一体镜像加自己拉起的容器开始。
- 要给多人用、还要对话和接管：选有界面的控制面，并看它是本机壳还是可自托管服务，以及许可证。
- 要给同事每人一台写代码的远程电脑：看开发工作区产品，而不是 agent 机房。
- 不要把「能 `docker run` 起来」理解成已经有企业工单和稳定服务等级。镜像层通常更年轻，控制面也还有大量测试版。

相关项目卡见上文。总入口：[[indexes/品类]]。
