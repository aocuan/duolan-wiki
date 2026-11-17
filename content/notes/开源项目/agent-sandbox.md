---
title: agent-sandbox
type: 项目卡
tags:
  - 开源项目
  - 沙箱
date: 2026-11-17
updated: 2026-11-17
status: evergreen
source_bot: 研究 · 开源 Agent 项目
sources:
  - https://github.com/kubernetes-sigs/agent-sandbox
  - https://agent-sandbox.sigs.k8s.io
repo: https://github.com/kubernetes-sigs/agent-sandbox
license: Apache-2.0
stars: 4633
verdict: 集群里的沙箱调度接口，不是给同事打开的产品。有集群、自己做平台时再用；不要把它当成工作台。
publish: true
---

# agent-sandbox

[kubernetes-sigs/agent-sandbox](https://github.com/kubernetes-sigs/agent-sandbox)（Apache-2.0，约 4633 星，截至 2026-11-17，太平洋时间；文档 [agent-sandbox.sigs.k8s.io](https://agent-sandbox.sigs.k8s.io)）给集群提供一种沙箱对象：单例、有身份、能停能醒，也可以准备热池。隔离交给集群里的隔离运行时，自己不带桌面、登录或对话界面。

## 怎么用、不要怎么用

它适合作为「给 agent 开电脑」的调度层。可以把带浏览器和桌面的镜像，例如 [[agent-infra-sandbox]]，放进这种对象里。同事打不开一个调度对象，所以公司若是要马上给人用，应先看带界面的控制面或开发工作区，例如 [[Rakazo]]、[[Memoh]]、[[Coder]]。

更上面的密度调度（把很多长时间闲着的环境挤进少量节点）是另一层，见 [[Substrate]]。当前接口仍在早期，不能按已经稳定的生产规范来预期。

品类见 [[Agent电脑与沙箱层]]。入口：[[indexes/开源项目]]。
